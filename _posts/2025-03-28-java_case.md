---
layout: single
title: 자바 Switch문 대체
---
```
package com.XXXXXXXXXXX.demo;
 
import java.math.BigDecimal;
import java.math.BigInteger;
 
class CheckUtil {
     
    String      refValString =      null;
    Integer     refValInteger =     null;
    Long        refValLong =        null;
    Double      refValDouble =      null;
    BigDecimal  refValBigDecimal =  null;
    BigInteger  refValBigInteger =  null;
     
    CheckUtil(String refValParam){
        this.refValString = refValParam;
    }
     
    CheckUtil(Integer refValParam){
        this.refValInteger = refValParam;
    }
     
    CheckUtil(Long refValParam){
        this.refValLong = refValParam;
    }
     
    CheckUtil(Double refValParam){
        this.refValDouble = refValParam;
    }
     
    CheckUtil(BigDecimal refValParam){
        this.refValBigDecimal = refValParam;
    }
     
    CheckUtil(BigInteger refValParam){
        this.refValBigInteger = refValParam;
    }
     
    public boolean check(String caseValParam) {
        if(this.refValString != null && this.refValString.equals(caseValParam)) {
            return true;
        } else {
            return false;
        }
    }
     
    public boolean check(Integer caseValParam) {
        if(this.refValInteger != null && this.refValInteger.equals(caseValParam)) {
            return true;
        } else {
            return false;
        }
    }
     
    public boolean check(Long caseValParam) {
        if(this.refValLong != null && this.refValLong.equals(caseValParam)) {
            return true;
        } else {
            return false;
        }
    }
     
    public boolean check(BigDecimal caseValParam) {
        if(this.refValBigDecimal != null && this.refValBigDecimal.equals(caseValParam)) {
            return true;
        } else {
            return false;
        }
    }
     
    public boolean check(BigInteger caseValParam) {
        if(this.refValBigInteger != null && this.refValBigInteger.equals(caseValParam)) {
            return true;
        } else {
            return false;
        }
    }
     
}
 
public class SwitchTest {
     
    public static void main(String[] args) {
         
        String inputString =            "03";
        int inputInteger =              2;
        //BigDecimal inputBigDecimal =  new BigDecimal("1000000000");
         
        ////////////////////////////////////////////////////////////////////////////////
         
        //요건1: inputString 값에 따라 아래를 수행
        //☞ inputString 값이 "01"이면 "안녕하세요." 출력
        //☞ inputString 값이 "02"이면 "Hola." 출력
        //☞ inputString 값이 "03"이면 "Guten Tag." 출력
        CheckUtil c = new CheckUtil(inputString);
        //case "01":
        if(c.check("01")) {
            System.out.println("요건1.CheckUtil   ▶ 안녕하세요.");
        }
        //case "02":
        else if(c.check("02")) {
            System.out.println("요건1.CheckUtil   ▶ Hola.");
        }
        //case "03":
        else if(c.check("03")) {
            System.out.println("요건1.CheckUtil   ▶ Guten Tag.");
        }
         
        ////////////////////////////////////////////////////////////////////////////////
         
        //요건1 switch/case 문으로 작성 시 
        switch(inputString){
        case "01":
            System.out.println("요건1.switch  ▶ 안녕하세요.");
            break;
        case "02":
            System.out.println("요건1.switch  ▶ Hola.");
            break;
        case "03":
            System.out.println("요건1.switch  ▶ Guten Tag.");
            break;
        }
         
        ////////////////////////////////////////////////////////////////////////////////
         
        //요건2: inputInteger 값에 따라 아래를 수행
        //☞ inputInteger 값이 1이면 "100,000원 입금" 출력
        //☞ inputInteger 값이 2이면 "200,000원 입금" 출력
        //☞ inputInteger 값이 3이면 "300,000원 입금" 출력
        //☞ 그외에는 "400,000원 입금" 출력
        c = new CheckUtil(inputInteger);
        //case 1:
        if(c.check(1)) {
            System.out.println("요건2.CheckUtil   ▶ 100,000원 입금");
        }
        //case 2:
        else if(c.check(2)) {
            System.out.println("요건2.CheckUtil   ▶ 200,000원 입금");
        }
        //case 3:
        else if(c.check(3)) {
            System.out.println("요건2.CheckUtil   ▶ 300,000원 입금");
        }
        //default:
        else {
            System.out.println("요건2.CheckUtil   ▶ 400,000원 입금");
        }
         
        ////////////////////////////////////////////////////////////////////////////////
    }
}
```
