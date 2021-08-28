---
description: La funzione SetBoolInBlob imposta un valore booleano in una determinata posizione all'interno di un BLOB.
ms.assetid: 354d22be-b8c4-4068-8356-19b30ac188d0
title: Funzione SetBoolInBlob (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetBoolInBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 95785714919ad99026c8e179c11f992a79efc4d99d0de4caab20fd00f63cbffc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120128821"
---
# <a name="setboolinblob-function"></a>Funzione SetBoolInBlob

La **funzione SetBoolInBlob** imposta un valore booleano in una determinata posizione all'interno di un BLOB.

## <a name="syntax"></a>Sintassi


```C++
DWORD SetBoolInBlob(
  _In_       HBLOB hBlob,
  _In_ const char  *pOwnerName,
  _In_ const char  *pCategoryName,
  _In_ const char  *pTagName,
  _In_       BOOL  Bool
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hBlob* \[ Pollici\]
</dt> <dd>

Handle a un BLOB.

</dd> <dt>

*pOwnerName* \[ Pollici\]
</dt> <dd>

Puntatore al nome **del proprietario** DEL BLOB.

</dd> <dt>

*pCategoryName* \[ Pollici\]
</dt> <dd>

Puntatore al nome della **categoria** BLOB.

</dd> <dt>

*pTagName* \[ Pollici\]
</dt> <dd>

Puntatore al nome del **tag** BLOB.

</dd> <dt>

*Bool* \[ Pollici\]
</dt> <dd>

Valore booleano impostato nella posizione specificata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è NMERR \_ SUCCESS.

Se la funzione ha esito negativo, il valore restituito è un valore NMERR che indica l'errore.

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

[GetBoolFromBlob](getboolfromblob.md)
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
</dt> <dt>

[SetStringInBlob](setstringinblob.md)
</dt> </dl>

 

 




