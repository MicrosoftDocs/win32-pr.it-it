---
description: La funzione SetMacAddressInBlob imposta l'indirizzo MAC richiesto di un BLOB.
ms.assetid: f44d0cec-ced7-4d2a-a58e-aeb476bfe800
title: Funzione SetMacAddressInBlob (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetMacAddressInBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 2183f5635dcdb15362a86a77ae2b3c109c71dbd5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883342"
---
# <a name="setmacaddressinblob-function"></a>SetMacAddressInBlob (funzione)

La funzione **SetMacAddressInBlob** imposta l'indirizzo Mac richiesto di un BLOB.

## <a name="syntax"></a>Sintassi


```C++
DWORD SetMacAddressInBlob(
  _In_       HBLOB hBlob,
  _In_ const char  *pOwnerName,
  _In_ const char  *pCategoryName,
  _In_ const char  *pTagName,
  _In_ const BYTE  *pMacAddress
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hBlob* \[ in\]
</dt> <dd>

Handle per il BLOB da impostare.

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

*pMacAddress* \[ in\]
</dt> <dd>

Puntatore all'indirizzo MAC del BLOB da impostare.

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

[GetMacAddressFromBlob](getmacaddressfromblob.md)
</dt> <dt>

[SetBoolInBlob](setboolinblob.md)
</dt> <dt>

[SetClassIDInBlob](setclassidinblob.md)
</dt> <dt>

[SetDwordInBlob](setdwordinblob.md)
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

 

 




