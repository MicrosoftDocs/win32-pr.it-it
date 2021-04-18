---
description: La funzione RegOpenBlobKey recupera un BLOB archiviato nella chiave del registro di sistema specificata.
ms.assetid: f6b16c07-c705-47f1-a21c-6155368551c7
title: Funzione RegOpenBlobKey (Netmon. h)
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
ms.openlocfilehash: 24d788c8c4b69525d6c0be374845b44f804982bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319404"
---
# <a name="regopenblobkey-function"></a>RegOpenBlobKey (funzione)

La funzione **RegOpenBlobKey** recupera un BLOB archiviato nella chiave del registro di sistema specificata.

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

*HKEY* \[ in\]
</dt> <dd>

Handle per la chiave del registro di sistema che contiene il BLOB.

</dd> <dt>

*szBlobName* \[ in\]
</dt> <dd>

Nome che identifica il BLOB specificato nel registro di sistema.

</dd> <dt>

*phBlob* \[ out\]
</dt> <dd>

Puntatore al BLOB recuperato.

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

[RegCreateBlobKey](regcreateblobkey.md)
</dt> </dl>

 

 




