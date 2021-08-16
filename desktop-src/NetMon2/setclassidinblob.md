---
description: La funzione SetClassIDInBlob imposta il valore dell'identificatore di classe denominato di un BLOB.
ms.assetid: d17dd48b-2e35-4c57-ba33-688180910b63
title: Funzione SetClassIDInBlob (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetClassIDInBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 70e68d3a0d9d105b765ee6cd0ae1a6422f48e3dd6776cf144b302c9e1c5ff951
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118364160"
---
# <a name="setclassidinblob-function"></a>Funzione SetClassIDInBlob

La **funzione SetClassIDInBlob** imposta il valore dell'identificatore di classe denominato di un BLOB.

## <a name="syntax"></a>Sintassi


```C++
DWORD SetClassIDInBlob(
  _In_       HBLOB hBlob,
  _In_ const char  *pOwnerName,
  _In_ const char  *pCategoryName,
  _In_ const char  *pTagName,
  _In_ const CLSID *pClsID
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hBlob* \[ Pollici\]
</dt> <dd>

Handle per un BLOB.

</dd> <dt>

*pOwnerName* \[ Pollici\]
</dt> <dd>

Puntatore al nome **del proprietario** DEL BLOB impostato.

</dd> <dt>

*pCategoryName* \[ Pollici\]
</dt> <dd>

Puntatore al **nome della categoria** BLOB impostato.

</dd> <dt>

*pTagName* \[ Pollici\]
</dt> <dd>

Puntatore al nome **del tag** BLOB impostato.

</dd> <dt>

*pClsID* \[ Pollici\]
</dt> <dd>

Puntatore all'identificatore di classe del BLOB impostato.

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

[GetClassIDFromBlob](getclassidfromblob.md)
</dt> <dt>

[SetBoolInBlob](setboolinblob.md)
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

 

 




