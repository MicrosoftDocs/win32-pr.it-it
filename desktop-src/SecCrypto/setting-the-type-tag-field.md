---
description: Le variabili di tipo VARIANT hanno un campo di tag del tipo VT che indica il tipo di dati dei dati.
ms.assetid: 3436faf6-2e66-46a1-b1e8-84f513282c16
title: Impostazione del campo tag del tipo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e443fae33b14bd4270e63188ff96a042a91c8e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225865"
---
# <a name="setting-the-type-tag-field"></a>Impostazione del campo tag del tipo

Le variabili di tipo **Variant** hanno un campo di tag del tipo **VT** che indica il tipo di dati dei dati. I valori restituiti del tipo **Variant** vengono restituiti dai metodi con il campo del tag type impostato sul tipo di dati del valore restituito. I parametri di input di tipo **Variant** in una chiamata al metodo devono avere il campo dei tag type impostato dall'applicazione su uno dei valori supportati. Di seguito è riportata la corrispondenza dei tipi di parametro con i tipi di dati.



| Tipo di parametro              | Tipo di dati                                      |
|-----------------------------|------------------------------------------------|
| PROPTYPE \_ Long<br/>   | VT \_ I2 o VT \_ I4<br/>                    |
| \_Data PROPTYPE<br/>   | \_Data VT<br/>                            |
| \_binario PROPTYPE<br/> | VT \_ BSTR o (VT \_ BSTR \| VT \_ ByRef)<br/> |
| \_stringa PROPTYPE<br/> | VT \_ BSTR o (VT \_ BSTR \| VT \_ ByRef)<br/> |



 

Nell'esempio seguente viene illustrato come inizializzare i tipi di dati Variant elencati in precedenza.


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



 

 




