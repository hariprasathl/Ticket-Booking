# Ticket-Booking
#include <stdio.h>

int main() {
    int seats[10] = {0};
    int seats2[10] = {0};
    char userGender;
    char userName[50];
    for(int i=0;i<100;i++){
    printf("\nEnter your name: ");
    scanf("%s", userName);
    printf("Enter your gender (M/F): ");
    scanf(" %c", &userGender);
    int movieChoice;
    printf("\nSelect a movie:\n");
    printf("1. Jigarthanda\n");
    printf("2. Parking\n");
    printf("Enter the number of the movie: ");
    scanf("%d", &movieChoice);

    switch (movieChoice) {
        case 1:
            printf("Enjoy watching Jigarthanda!\n");
             printf("Available Seats: ");
        for (int i = 1; i <= 10; i++) {
        if (seats[i] == 0) {
            printf("%d ",i);
        }
        else{
            printf(" ");
        }
    }
    
    //int seats[10];
    int seatChoice;
    printf("\nEnter the seat number you want to book (1-10): ");
    scanf("%d", &seatChoice);
    if (seatChoice < 1 || seatChoice > 10 || seats[seatChoice] == 1) {
        printf("Invalid seat choice or seat already booked. Exiting.\n");
      continue;   
    }
    seats[seatChoice] = 1;
printf("\n");
    printf("%s\n", userName);
    printf(" %c\n", userGender);
    printf("Seat %d booked successfully!\n", seatChoice);
            break;
            
            
        case 2:
            printf("Enjoy watching Parking!\n");
             printf("Available Seats: ");
    for (int i = 1; i <= 10; ++i) {
        if (seats2[i] == 0) {
            printf("%d ", i);
        }
        else{
            printf(" ");
        }
    }
    
    //int seats[10];
    int seatChoice2;
    printf("\nEnter the seat number you want to book (1-10): ");
    scanf("%d", &seatChoice2);
    if (seatChoice2 < 1 || seatChoice2 > 10 || seats2[seatChoice2] == 1) {
        printf("Invalid seat choice or seat already booked. Exiting.\n");
      continue;   
    }
    seats2[seatChoice2] = 1;
printf("\n");
    printf("%s\n", userName);
    printf(" %c\n", userGender);
    printf("Seat %d booked successfully!\n", seatChoice2);
            break;
        default:
            printf("Invalid movie choice.\n");
            continue;
    }
}

}
