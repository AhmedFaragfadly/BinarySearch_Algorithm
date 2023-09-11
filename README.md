//BinarySearch_Algorithm


#include <stdio.h>
#include <stdlib.h>
#define DATA_MAX_SIZE      10
typedef unsigned int   uint32;
typedef   signed int   sint32;
uint32 MYDATA[] = {11,12,13,14,15,16,17,18,19,20};
int main()
{

sint32 ret =0 ;
ret = BINARY_search(MYDATA , 0 ,9,15);


printf("%i " , ret);


}
sint32 BINARY_search(sint32 DATA[] , uint32 Start ,uint32 end, sint32 VALUE)
{
uint32 INDEX =0 ;

while ( Start <= end)
{
INDEX = Start + ((end-Start)/2);
if(DATA [INDEX] == VALUE)

	{
	return INDEX;
	
	
	}
	else if( VALUE > DATA[INDEX])

	{
	Start = INDEX +1 ;
	
	}
	
	else
	{
	end = INDEX-1 ;
	}
}

}
