---
description: La funzione RegCreateBlobKey archivia un BLOB nella chiave del registro di sistema specificata.
ms.assetid: 14f3763e-aa04-4d51-b388-81ebf0d3952c
title: Funzione RegCreateBlobKey (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RegCreateBlobKey
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: fc46b38919b37dc004c1065b0cc8d5f80e65984c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319405"
---
# <a name="regcreateblobkey-function"></a>RegCreateBlobKey (funzione)

La funzione **RegCreateBlobKey** archivia un BLOB nella chiave del registro di sistema specificata.

## <a name="syntax"></a>Sintassi


```C++
DWORD RegCreateBlobKey(
  _Out_       HKEY  hkey,
  _In_  const char  *szBlobName,
  _In_        HBLOB hBlob
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*HKEY* \[ out\]
</dt> <dd>

Handle per la chiave del registro di sistema in cui verrà archiviato il BLOB.

</dd> <dt>

*szBlobName* \[ in\]
</dt> <dd>

Nome (applicazione definita) che rappresenta il BLOB nel registro di sistema.

</dd> <dt>

*hBlob* \[ in\]
</dt> <dd>

Handle per il BLOB salvato.

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

[RegOpenBlobKey](regopenblobkey.md)
</dt> </dl>

 

 




