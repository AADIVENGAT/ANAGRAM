# ANAGRAM
Algorithm based problem
//Anagram

Sample input:Eat
             Ate

Sample output: Anagram

#include<stdio.h>
#include<string.h>
int main()
{
    char word1[99] ;
    char word2[99] ;
    gets(word1);
    gets(word2);
    // printf("%s , %s",word1,word2);
    int len1 = strlen(word1);
    int len2 = strlen(word2);
    int count1[26] = {0};
    int count2[26] = {0};
    for(int i=0;i<len1;i++)
    {
        char ch = word1[i];
        if(ch>='a' && ch<='z')
        {
            ch = ch - 32;
        }
        count1[ch-'A']++;
    }
    for(int i=0;i<len2;i++)
    {
        char ch = word2[i];
        if(ch>='a' && ch<='z')
        {
            ch = ch - 32;
            }
        count2[ch-'A']++;
    }
    for(int i=0;i<26;i++)
    {
        printf("%d ",count1[i]);
    }   
    printf("\n");
    for(int i=0;i<26;i++)
    {
        printf("%d ",count2[i]);
    }   
    printf("\n");

    /*
        'A' : 65
        'a' : 97 
        '0' : 48
        ' ' : 32
    */    
}
