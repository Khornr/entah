# entah
flowchart TD
    A[Start] --> B[Main Screen]
    B --> |Sign In| C[Sign In Screen]
    B --> |Sign Up| D[Sign Up Screen]
    B --> |Exit| Z[End]

    C --> |Login Successful| E[Menu Screen]
    C --> |Login Failed| C
    C --> |Back| B

    D --> |Create Account| B
    D --> |Back| B

    E --> |Book Ticket| F[Film Selection Screen]
    E --> |Cancel Ticket| G[Ticket Cancellation Screen]
    E --> |View Order History| K[Order History Screen]
    E --> |Admin Mode| L[Admin Screen]
    E --> |Back| B

    F --> |Select Film| H[Seat Selection Screen]
    F --> |Back| E

    H --> |Select Seats| I[Booking Confirmation Screen]
    H --> |Reset Seats| H
    H --> |Back| F

    I --> |Confirm Booking| J[Ticket Printed Screen]
    I --> |Cancel Booking| F
    I --> |Back| H

    G --> |Cancel Booking| E
    G --> |Back| E

    J --> |Book Again| E
    J --> |Exit| Z

    K --> |View Details| K
    K --> |Back| E

    L --> |Reset Seats| M[Reset Seats Screen]
    L --> |View Order History| K
    L --> |Back| B

    M --> |Reset Single Film| M
    M --> |Reset All Seats| M
    M --> |Back| L

    Z
