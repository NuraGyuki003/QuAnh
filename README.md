
#include<stdio.h>
//#include<conio.h>
#include<bits/stdc++.h>

int main(){
    int tongsotinchi, sotinchidatichluy, sotinchiyeucau;
    float GPAhientai, GPAtieuchuan, diemtruchoi;
    
    printf("Nhập tổng số tín chỉ:");
        scanf("%d", &tongsotinchi);
        
    printf("Nhập số tín chỉ đã tích luỹ: ");
        scanf("%d", &sotinchidatichluy);
        if(sotinchidatichluy > tongsotinchi){
            printf("Xem lại số tín chỉ đã tích luỹ");
            getch();

        }
    
    printf("Nhập số tín chỉ yêu cầu:");
        scanf("%d", &sotinchiyeucau);
    
    printf("Nhập GPA hiện tại: ");
        scanf("%f", &GPAhientai);
    
    GPAtieuchuan = (3.5 * tongsotinchi - GPAhientai*sotinchidatichluy )/sotinchiyeucau;
    
    if(GPAtieuchuan > 4.0){
        printf("Không thể đạt được GPA trên 3.5 với số tín chỉ yêu cầu và GPA hiện tại. \n");
    }

    else{
        diemtruchoi = (GPAtieuchuan - GPAhientai*sotinchidatichluy)/(sotinchiyeucau - sotinchidatichluy);
        printf("Điểm trung bình cần thiết để đạt được GPA trên 3.5 là: %.2f\n", diemtruchoi);
    }
        return 0;
    }
