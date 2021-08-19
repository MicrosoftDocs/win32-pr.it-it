---
title: Metodi della proprietà IADsLargeInteger (Iads.h)
description: I metodi di proprietà dell'interfaccia IADsLargeInteger ottengono e impostano le proprietà descritte nella tabella seguente. Per altre informazioni, vedere Metodi delle proprietà dell'interfaccia.
ms.assetid: 73e0c7fe-e468-4f92-9c9e-721bf00dd4bb
ms.tgt_platform: multiple
keywords:
- Metodi della proprietà IADsLargeInteger ADSI
topic_type:
- apiref
api_name:
- IADsLargeInteger Property Methods
- IADsLargeInteger.HighPart
- IADsLargeInteger.get_HighPart
- IADsLargeInteger.put_HighPart
- IADsLargeInteger.LowPart
- IADsLargeInteger.get_LowPart
- IADsLargeInteger.put_LowPart
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b46a992accea468b6f3c8a70c7fcfcbe63cf72667c4394c27df273767a387b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023479"
---
# <a name="iadslargeinteger-property-methods"></a>Metodi della proprietà IADsLargeInteger

I metodi di proprietà [**dell'interfaccia IADsLargeInteger**](/windows/desktop/api/Iads/nn-iads-iadslargeinteger) ottengono e impostano le proprietà descritte nella tabella seguente. Per altre informazioni, vedere [Metodi delle proprietà dell'interfaccia](interface-property-methods.md).

## <a name="properties"></a>Proprietà

<dl> <dt>

**HighPart**
</dt> <dd> <dl>

Parte alta dell'intero.

<dt>

Tipo di accesso: Lettura/Scrittura
</dt> <dt>

Tipo di dati scripting: **LONG**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_HighPart(
  [out] LONG* retval
);
HRESULT put_HighPart(
  [in] LONG lnHighPart
);
```


</dt> </dl> </dd> <dt>

**LowPart**
</dt> <dd> <dl>

Parte bassa dell'intero.

<dt>

Tipo di accesso: Lettura/Scrittura
</dt> <dt>

Tipo di dati scripting: **LONG**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_LowPart(
  [out] LONG* retval
);
HRESULT put_LowPart(
  [in] LONG lnLowPart
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a>Commenti

Se largeInt è di **tipo LargeInteger,** il relativo valore viene specificato da quelli di **HighPart** **e LowPart** in base alla formula seguente.


```VB
largeInt = HighPart * 2^32 + LowPart
```



## <a name="examples"></a>Esempio

Nell'esempio Visual Basic di codice seguente viene impostato un numero intero grande 43937327281.


```VB
Dim LI As New LargeInteger
LI.HighPart = 10
LI.LowPart = 987654321
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Iads.h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | \_IADsLargeInteger IID è definito come 9068270B-0939-11D1-8BE1-00C04FD8D503<br/>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IADsLargeInteger**](/windows/desktop/api/Iads/nn-iads-iadslargeinteger)
</dt> </dl>

 

 





