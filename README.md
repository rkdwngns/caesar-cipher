# caesar-cipher

이 프로그램은 카이사르 암호를 생성 및 푸는 프로그램 입니다.
카이사르의 원리 부터 보자면 원 형태 그대로의 영어 문장을 치고
key라는 값이 있는데 이 key값만큼 옆으로 밀어냅니다.
이 원리를 이용해 만들었습니다.
```c
int main(void)
{
	char value[100] ={0,};
	int key, chek, i;
	printf("암호문 입력: ");
	 fgets(value, 100, stdin);
		printf("Key 값 : ");
	  scanf("%d" ,&key);
```
fgets로 암호를 입력 받습니다. 그러고 글자를 얼마나 밀어줄지 정하는 key값을 받습니다.

```c
if( chek == 2 ) key =- key;
	for( i=0; i<strlen(value); i++ ) {
		if( value[i]>='A' && value[i]<='Z' ) {
			value[i] -= 'A';
	if( value[i] + key < 0 ) {
		value[i] += 26;
		}
		value[i] = (value[i] + key ) % 26;
		value[i] += 'A';
```
간략하게 설명하자면 i는 배열에 담긴 글자들을 차례대로 꺼내주는 역할을 합니다. 첫번째 if문은 대문자를 아스키 코드 변환입니다.
그런뒤  key값을 통해 글자들을 밀어줍니다. 복호화는 암호화는 반대로 진행 됩니다.
여기서 if문을 조건을 통해 출력하면 printf하나만으로 복호화 암호화 등을 동시에 출력이 가능합니다.
그리고 여기서 26이 있는데 26이 뜻하는 건 영어 알파벳의 개수를 뜻합니다.



----------------------------------------------------------출력 화면-------------------------------------------------------

![image](https://user-images.githubusercontent.com/93520535/181007946-817364ff-adc6-474b-93bf-d96ec718052f.png)


![image](https://user-images.githubusercontent.com/93520535/181008089-327ba1e7-08ae-40e4-8c59-71da2d2a5048.png)


