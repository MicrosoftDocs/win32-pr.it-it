---
description: Le variabili di tipo VARIANT hanno un campo tag di tipo vt che indica il tipo di dati.
ms.assetid: 3436faf6-2e66-46a1-b1e8-84f513282c16
title: Impostazione del campo Type Tag
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2683980127b1b93de5cdfa0d19879d17699f2c3402d9404b32f094b78637c641
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117974485"
---
# <a name="setting-the-type-tag-field"></a>Impostazione del campo Type Tag

**Le** variabili di tipo VARIANT hanno un campo tag **di tipo vt** che indica il tipo di dati. **I** valori restituiti di tipo VARIANT vengono restituiti dai metodi con il campo tag type impostato sul tipo di dati del valore restituito. **I** parametri di input di tipo VARIANT in una chiamata al metodo devono avere il campo del tag di tipo impostato dall'applicazione su uno dei valori supportati. La corrispondenza tra i tipi di parametro e i tipi di dati è la seguente.



| Tipo di parametro              | Tipo di dati                                      |
|-----------------------------|------------------------------------------------|
| PROPTYPE \_ LONG<br/>   | VT \_ I2 o VT \_ I4<br/>                    |
| PROPTYPE \_ DATE<br/>   | DATA \_ VT<br/>                            |
| PROPTYPE \_ BINARY<br/> | VT \_ BSTR o (VT \_ BSTR \| VT \_ BYREF)<br/> |
| STRINGA \_ PROPTYPE<br/> | VT \_ BSTR o (VT \_ BSTR \| VT \_ BYREF)<br/> |



 

Nell'esempio seguente viene illustrato come inizializzare i tipi di dati variant elencati in precedenza.


```C++
HRESULT hr;
VARIANT vEMail;
VARIANT vNotBefore;
VARIANT vCount;
VARIANT vByRef;
BSTR bstr = NULL;
SYSTEMTIME st;

//Set the BSTR variant data type.
VariantInit(&vEMail);
vEMail.vt = VT_BSTR;   
vEMail.bstrVal = SysAllocString(L"someone@example.com");
if (NULL == vEMail.bstrVal)
{
    hr = E_OUTOFMEMORY;
    //Handle error.   
}
//Use the variant.
VariantClear(&vEMail);  //when done


//Set the BSTR|BYREF variant data type.
VariantInit(&vByRef);
vByRef.vt = VT_BSTR | VT_BYREF;   
vByRef.pbstrVal = &bstr;
//Use the variant.
VariantClear(&vByRef);  //when done
SysFreeString(bstr);


//Set the DATE variant data type.
memset(&st, 0, sizeof(SYSTEMTIME));
st.wYear = 2000;
st.wMonth = 1;
st.wDay = 1;
st.wHour = 12;

VariantInit(&vNotBefore);
vNotBefore.vt = VT_DATE;
if (!SystemTimeToVariantTime(&st, &vNotBefore.date))
{
    hr = E_FAIL;
    //Handle error.
}
//Use the variant.
VariantClear(&vNotBefore);  //when done


//Set the LONG variant data type.
VariantInit(&vCount);
vCount.vt = VT_I4;
vCount.long = 123456;
//Use the variant.
VariantClear(&vCount);  //when done
```



 

 




