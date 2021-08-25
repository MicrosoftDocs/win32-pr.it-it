---
description: La funzione RegCreateBlobKey archivia un BLOB nella chiave del Registro di sistema specificata.
ms.assetid: 14f3763e-aa04-4d51-b388-81ebf0d3952c
title: Funzione RegCreateBlobKey (Netmon.h)
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
ms.openlocfilehash: 3267fd0ba5e6fe56b99b5d465f69718fe5509a7ead58acf1d8dafb642397af5e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119889651"
---
# <a name="regcreateblobkey-function"></a>Funzione RegCreateBlobKey

La **funzione RegCreateBlobKey** archivia un BLOB nella chiave del Registro di sistema specificata.

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

*hkey* \[ Cambio\]
</dt> <dd>

Handle per la chiave del Registro di sistema in cui verrà archiviato il BLOB.

</dd> <dt>

*szBlobName* \[ Pollici\]
</dt> <dd>

Nome (definito dall'applicazione) che rappresenta il BLOB nel Registro di sistema.

</dd> <dt>

*hBlob* \[ Pollici\]
</dt> <dd>

Handle per il BLOB salvato.

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

[RegOpenBlobKey](regopenblobkey.md)
</dt> </dl>

 

 




