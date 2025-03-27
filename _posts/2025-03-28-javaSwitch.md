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
```
