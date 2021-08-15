---
description: Imposta il filtro di corrispondenza del modello BLOB.
ms.assetid: 44e7c67a-f430-4d68-bc7f-f6bbd5b9e5a9
title: Funzione SetNPPPatternFilterInBlob (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetNPPPatternFilterInBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: a920d6ffc135855826719e31613119a27671e334d5a75ce7dba29c2b140816fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118363752"
---
# <a name="setnpppatternfilterinblob-function"></a>Funzione SetNPPPatternFilterInBlob

La **funzione SetNPPPatternFilterInBlob** imposta il filtro di corrispondenza del modello BLOB.

## <a name="syntax"></a>Sintassi


```C++
DWORD SetNPPPatternFilterInBlob(
  _In_  HBLOB        hBlob,
  _In_  LPEXPRESSION pExpression,
  _Out_ HBLOB        hErrorBlob
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hBlob* \[ Pollici\]
</dt> <dd>

Handle per il BLOB.

</dd> <dt>

*pExpression* \[ Pollici\]
</dt> <dd>

Puntatore a una [struttura EXPRESSION](expression.md) che definisce l'espressione di filtro impostata.

</dd> <dt>

*hErrorBlob* \[ Cambio\]
</dt> <dd>

Handle a un BLOB di errore che specifica dove nel BLOB originale si è verificato l'errore (se presente).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la **funzione SetNPPPatternFilterInBlob** ha esito positivo, il valore restituito è NMERR \_ SUCCESS.

Se la funzione ha esito negativo, il valore restituito è un valore NMERR che indica l'errore.

## <a name="remarks"></a>Commenti

I dati del filtro di corrispondenza dei criteri archiviati nella **categoria Config** del BLOB.

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

[GetNPPAddressFilterFromBlob](getnppaddressfilterfromblob.md)
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

[SetNPPTriggerInBlob](setnpptriggerinblob.md)
</dt> <dt>

[SetStringInBlob](setstringinblob.md)
</dt> </dl>

 

 




