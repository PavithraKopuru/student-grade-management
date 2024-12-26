#include <stdio.h>

#define MAX_STUDENTS 100

typedef struct {
    char name[50];
    float grade;
} Student;

void addStudent(Student students[], int *count) {
    if (*count < MAX_STUDENTS) {
        printf("Enter student name: ");
        scanf("%s", students[*count].name);
        printf("Enter student grade: ");
        scanf("%f", &students[*count].grade);
        (*count)++;
    } else {
        printf("Maximum student limit reached.\n");
    }
}

void displayGrades(Student students[], int count) {
    float total = 0.0;
    printf("\nStudent Grades:\n");
    for (int i = 0; i < count; i++) {
        printf("%s: %.2f\n", students[i].name, students[i].grade);
        total += students[i].grade;
    }
    if (count > 0) {
        printf("Average grade: %.2f\n", total / count);
    }
}

int main() {
    Student students[MAX_STUDENTS];
    int count = 0;
    int choice;

    do {
        printf("\n1. Add Student\n2. Display Grades\n3. Exit\n");
        printf("Enter your choice: ");
        scanf("%d", &choice);

        switch (choice) {
            case 1:
                addStudent(students, &count);
                break;
            case 2:
                displayGrades(students, count);
                break;
            case 3:
                printf("Exiting...\n");
                break;
            default:
                printf("Invalid choice. Please try again.\n");
        }
    } while (choice != 3);

    return 0;
}
