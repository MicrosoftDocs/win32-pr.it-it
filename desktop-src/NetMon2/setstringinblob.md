---
description: Imposta una stringa in una posizione specificata all'interno di un BLOB.
ms.assetid: 645e6b8b-aaaf-429f-ad2f-bf4364ef4e80
title: Funzione SetStringInBlob (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetStringInBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 293aabf86769a8cfa678df79a04b5158b9c1d19c80d660b144c4a33cbf32c56f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118363680"
---
# <a name="setstringinblob-function"></a>Funzione SetStringInBlob

La **funzione SetStringInBlob** imposta una stringa in una determinata posizione all'interno di un BLOB.

## <a name="syntax"></a>Sintassi


```C++
DWORD SetStringInBlob(
  _In_       HBLOB hBlob,
  _In_ const char  *pOwnerName,
  _In_ const char  *pCategoryName,
  _In_ const char  *pTagName,
  _In_ const char  *pString
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hBlob* \[ Pollici\]
</dt> <dd>

Handle per il BLOB.

</dd> <dt>

*pOwnerName* \[ Pollici\]
</dt> <dd>

Puntatore alla **sezione Owner** del BLOB, in cui è impostata la stringa.

</dd> <dt>

*pCategoryName* \[ Pollici\]
</dt> <dd>

Puntatore alla **sezione Category** del BLOB, in cui è impostata la stringa.

</dd> <dt>

*pTagName* \[ Pollici\]
</dt> <dd>

Puntatore al **tag** della stringa richiesta.

</dd> <dt>

*pString* \[ Pollici\]
</dt> <dd>

Puntatore alla variabile in cui verrà restituito un puntatore alla stringa.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è NMERR \_ SUCCESS.

Se la funzione ha esito negativo, il valore restituito è un valore NMERR che indica il problema.

Se le informazioni **specificate su Owner,** **Category** o **Tag** non esistono, il valore restituito è NMERR BLOB ENTRY DOES \_ NOT \_ \_ \_ \_ EXIST.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                              |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl>     |
| Libreria<br/>                  | <dl> <dt>Npptools.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Npptools.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[GetStringFromBlob](getstringfromblob.md)
</dt> <dt>

[SetBoolInBlob](setboolinblob.md)
</dt> <dt>

[SetClassIDInBlob](setclassidinblob.md)
</dt> <dt>

[SetDwordInBlob](setdwordinblob.md)
</dt> <dt>

[SetMacAddressInBlob](setmacaddressinblob.md)
</dt> <dt>

[SetNetworkInfoInBlob](setnetworkinfoinblob.md)
</dt> <dt>

[SetNPPAddressFilterInBlob](setnppaddressfilterinblob.md)
</dt> <dt>

[SetNPPPatternFilterInBlob](setnpppatternfilterinblob.md)
</dt> <dt>

[SetNPPTriggerInBlob](setnpptriggerinblob.md)
</dt> </dl>

 

 




