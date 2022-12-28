

#include <stdio.h>
#include<string.h>
char *lexicographic_sort(const char* a, const char* b);
char *lexicographic_sort_reverse(const char* a, const char* b);
char *sort_by_number_of_distinct_characters(const char* a, const char* b);
char *sort_by_length(const char* a, const char* b);
int main()
{
    const char a[]={"wkue"},b[]={"qoi"},c[]={"sbv"},d[]={"fekls"};
    
    printf("/*increasing*/\n");
    char *s1=lexicographic_sort(a,b);
    char *s2=lexicographic_sort(c,s1);
    char *s3=lexicographic_sort(d,s2);
    
    printf("%s\n",s3);
    printf("%s\n",s2);
    printf("%s\n",s1);
   
    
    printf("/*decreasing*/\n");
    s1=lexicographic_sort_reverse(a,b);
    s2=lexicographic_sort_reverse(c,s1);
    s3=lexicographic_sort_reverse(d,s2);
    printf("%s\n",s3);
    printf("%s\n",s2);
    printf("%s\n",s1);
    
    printf("/*sort by dist char*/\n");
    s1=sort_by_number_of_distinct_characters(a,b);
    s2=sort_by_number_of_distinct_characters(c,s1);
    s3=sort_by_number_of_distinct_characters(d,s2);
    printf("%s\n",s3);
    printf("%s\n",s2);
    printf("%s\n",s1);
   
     printf("/*sort by length*/\n");
    s1=sort_by_length(a,b);
    s2=sort_by_length(c,s1);
    s3=sort_by_length(d,s2);
    printf("%s\n",s3);
    printf("%s\n",s2);
    printf("%s\n",s1);
   
    
    return 0;
}
char *lexicographic_sort(const char* a, const char* b) {
    return *a<*b?a:b;
    

}

char *lexicographic_sort_reverse(const char* a, const char* b) {
    return *a>*b?a:b;

}

char * sort_by_number_of_distinct_characters(const char* a, const char* b) {
    
    return strlen(a)<strlen(b)?a:b;
}

char *sort_by_length(const char* a, const char* b) {
    return strlen(a)<strlen(b)?a:b;
}

