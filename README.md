# Java String
나는 스트링이라네~~~

## String Api
스트링 함수
1. length - 문자열의 길이를 구한다.
```java
String a = "String/Test";
System.out.println(a.length());
```
2. indexOf - 문자열의 위치를 리턴한다
```java
System.out.println(a.indexOf("Te"));
```

## Algorithm
스트링을 활용한 알고리즘 풀이
1. Anagram
```java
public boolean checkAnagram(String a, String b){
	boolean result = false;
	// 대소문자 처리
	a = a.toLowerCase();
	b = b.toLowerCase();
	// option : 공백제거 후 문자열 쪼개기
	a = a.replace(" ","");
	b = b.replace(" ","");
	// 길이 비교
	if(a.length() != b.length()){
		return false;
	}
	// 정렬을 하기 위해서 char 배열로 변경
	char aTemp[] = a.toCharArray();
	char bTemp[] = b.toCharArray();
	
	// 캐릭터 배열 정렬
	Arrays.sort(aTemp);
	Arrays.sort(bTemp);

	// 문자열 비교후 리턴
	return Arrays.equals(aTemp, bTemp);
}

```
