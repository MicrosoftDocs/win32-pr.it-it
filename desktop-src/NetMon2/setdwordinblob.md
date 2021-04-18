---
description: La funzione SetDwordInBlob imposta il valore DWORD denominato di un BLOB.
ms.assetid: 9174cd5c-4442-4fbe-8dc7-f8a74e1cc85d
title: Funzione SetDwordInBlob (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetDwordInBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 9bca0efe61824c6fb8dd41b0b241791b6303799d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310489"
---
# <a name="setdwordinblob-function"></a>SetDwordInBlob (funzione)

La funzione **SetDwordInBlob** imposta il valore **DWORD** denominato di un BLOB.

## <a name="syntax"></a>Sintassi


```C++
DWORD SetDwordInBlob(
  _In_       HBLOB hBlob,
  _In_ const char  *pOwnerName,
  _In_ const char  *pCategoryName,
  _In_ const char  *pTagName,
  _In_       DWORD Dword
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hBlob* \[ in\]
</dt> <dd>

Handle per un BLOB da impostare.

</dd> <dt>

*pOwnerName* \[ in\]
</dt> <dd>

Puntatore al nome del **proprietario** del BLOB da impostare.

</dd> <dt>

*pCategoryName* \[ in\]
</dt> <dd>

Puntatore al nome della **categoria** BLOB da impostare.

</dd> <dt>

*pTagName* \[ in\]
</dt> <dd>

Puntatore al nome del **tag** BLOB da impostare.

</dd> <dt>

*DWORD* \[ in\]
</dt> <dd>

Valore **DWORD** del BLOB da impostare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è NMERR \_ Success.

Se la funzione ha esito negativo, il valore restituito è un valore NMERR che indica l'errore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                              |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl>     |
| Libreria<br/>                  | <dl> <dt>Npptools. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Npptools.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[GetDwordFromBlob](getdwordfromblob.md)
</dt> <dt>

[SetBoolInBlob](setboolinblob.md)
</dt> <dt>

[SetClassIDInBlob](setclassidinblob.md)
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

 

 




