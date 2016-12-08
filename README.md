#include <stdio.h>
#include <stdlib.h>

int ava_waste(int ava, int end_ava);
int ultimate_waste(int ultimates, int end_ultimates);
int bomb_waste(int bomb, int end_bomb);


typedef struct player {
    int ava
    ,ultimates
    ,bomb
    ,end_ava
    ,end_ultimates
    ,end_bomb;

};



int main() {

    struct player *ptr;


    int num, i, sum = 0;

    printf("Enter group size");
    scanf("%d",&num);
    ptr = (struct player*) malloc(num * sizeof(struct player));

    if(ptr == NULL)
    {
        printf("Error");
        exit(0);
    }


    for(i = 0; i < num; i ++)
    {
        printf("Enter starting ultimates, avalanches and energy bombs");
        scanf("%d%d%d", &(ptr+i)->ultimates, &(ptr+i)->ava, &(ptr+i)->bomb);
    }

    printf("Displaying Infromation:\n");
    for(i = 0; i < num; ++i)
        printf("%d\t%d\t%d\n", (ptr+i)->ultimates, (ptr+i)->ava, (ptr+i)->bomb);
    }




/**    printf("What's your starting avalance?");
    scanf("%d", &ava);

    printf("What's your starting ultimates");
    scanf("%d", &ultimates);

    printf("What's your starting energy bomb");
    scanf("%d", &bomb);

    printf("How many avalanches you have now?");
    scanf("%d", &end_ava);

    printf("How many ultimates you have now?");
    scanf("%d", &end_ultimates);

    printf("How many energy bombs you have now?");
    scanf("%d", &end_bomb);

    printf("Your total waste is %d gold", (ava_waste(ava, end_ava)
                                     + ultimate_waste(ultimates, end_ultimates)
                                     + bomb_waste(bomb, end_bomb)));

    return 0;
}

int ava_waste(int ava, int end_ava) {
    return ((ava - end_ava) * 45);
}

int ultimate_waste(int ultimates, int end_ultimates){
    return ((ultimates - end_ultimates)* 350);
}

int bomb_waste(int bomb, int end_bomb){
    return ((bomb - end_bomb)* 162);
}

 **/
