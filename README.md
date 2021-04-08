# 9-divisors
Finding the number of integers with exactly 9 divisors

#include stdio.in

int main()
{
  int n;
  printf(“\nEnter the number : “);
  scanf(“%d”, &n);
  printf(“\nThe number which has exactly 9 divisors : “);
  int count = 0;

  int c = 0;
  for (int i = 1; i <= n; i++)
  {
    for (int j = 1; j <= i; j++)
    {
      if (i % j == 0)
      {
        count = count + 1;
      }
      if (count == 9)
      {
        printf(“%d “, i);
        c = c + 1;
      }
    }
  }
  printf(“\n\nTotal = %d\n”, c);
  return 0;
}

