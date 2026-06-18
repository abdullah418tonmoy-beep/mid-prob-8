#include <stdio.h>

int main() {
    int num, patients, fever, tFPatients = 0;
    float temp;

    printf("Enter number of wards: ");
    scanf("%d", &num);

    for (int i = 1; i <= num; i++)
        {
        fever = 0;
        printf("Enter number of patients in Ward %d: ", i);
        scanf("%d", &patients);

        for (int j = 0; j < patients; j++)
        {
            printf(" Patient %d temperature: ", j + 1);
            scanf("%f", &temp);

            if (temp > 38.0)
            {
                fever++;
            }
        }

        tFPatients += fever;
        if (fever > 5)
        {
            printf(">> Ward %d has more than 5 fever patients.\n", i);
        }
    }

    printf("\nTotal patients with a fever: %d\n", tFPatients);
    return 0;
}
