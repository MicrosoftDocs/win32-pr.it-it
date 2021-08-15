---
description: La funzione RegOpenBlobKey recupera un BLOB archiviato nella chiave del Registro di sistema specificata.
ms.assetid: f6b16c07-c705-47f1-a21c-6155368551c7
title: Funzione RegOpenBlobKey (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RegOpenBlobKey
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 5d372d6cc69c4e80691f96075aaa0d9030c90d06fc8256f85a7ed2dc894f3fc1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118364150"
---
# <a name="regopenblobkey-function"></a>Funzione RegOpenBlobKey

La **funzione RegOpenBlobKey** recupera un BLOB archiviato nella chiave del Registro di sistema specificata.

## <a name="syntax"></a>Sintassi


```C++
DWORD RegOpenBlobKey(
  _In_        HKEY  hkey,
  _In_  const char  *szBlobName,
  _Out_       HBLOB *phBlob
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hkey* \[ Pollici\]
</dt> <dd>

Handle per la chiave del Registro di sistema che contiene il BLOB.

</dd> <dt>

*szBlobName* \[ Pollici\]
</dt> <dd>

Nome che identifica il BLOB specificato nel Registro di sistema.

</dd> <dt>

*phBlob* \[ Cambio\]
</dt> <dd>

Puntatore al BLOB recuperato.

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

[RegCreateBlobKey](regcreateblobkey.md)
</dt> </dl>

 

 




