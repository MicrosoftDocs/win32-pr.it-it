---
description: La funzione GetCaptureCommentFromFilename estrae il commento di acquisizione da un file di acquisizione.
ms.assetid: d3665cb0-d54d-45f7-aef9-c2e603d6f773
title: Funzione GetCaptureCommentFromFilename (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCaptureCommentFromFilename
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 9dbfb086ccc27ad2f4c35018c3384a4b81ef0528
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305916"
---
# <a name="getcapturecommentfromfilename-function"></a>GetCaptureCommentFromFilename (funzione)

La funzione **GetCaptureCommentFromFilename** estrae il commento di acquisizione da un [*file di acquisizione*](c.md).

## <a name="syntax"></a>Sintassi


```C++
DWORD  WINAPI GetCaptureCommentFromFilename(
  _In_ LPSTR lpFilename,
  _In_ LPSTR lpComment,
  _In_ DWORD BufferSize
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lpFileName* \[ in\]
</dt> <dd>

Puntatore al nome del file di acquisizione.

</dd> <dt>

*lpComment* \[ in\]
</dt> <dd>

Puntatore a una stringa preallocata per il commento.

</dd> <dt>

*BufferSize* \[ in\]
</dt> <dd>

Dimensione della stringa.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, ovvero se il commento viene trovato e copiato o se non è presente alcun commento nel file di acquisizione, il valore restituito è NMERR \_ Success.

Se la funzione ha esito negativo, il valore restituito è un codice di errore.



| Codice restituito                                                                                                 | Descrizione                                                                  |
|-------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <dt>**\_errore di \_ lettura del file NMERR \_**</dt> </dl>     | Impossibile leggere il commento di acquisizione.<br/>                               |
| <dl> <dt>**\_formato di \_ file non valido NMERR \_**</dt> </dl> | Il frame di commento non è un formato di file valido.<br/>                     |
| <dl> <dt>**il \_ file NMERR non è stato \_ \_ trovato**</dt> </dl>      | Impossibile trovare il file specificato dal parametro *lpFileName* .<br/> |
| <dl> <dt>**\_parametro NMERR non valido \_**</dt> </dl>    | Uno dei parametri non è stato specificato correttamente.<br/>                   |



 

## <a name="remarks"></a>Commenti

Gli [*esperti*](e.md) e i [*parser*](p.md) possono chiamare la funzione **GetCaptureCommentFromFilename** .

Per recuperare il commento di un'acquisizione in tempo reale, chiamare la funzione [GetCaptureComment](getcapturecomment.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Libreria<br/>                  | <dl> <dt>Nmap. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[GetCaptureComment](getcapturecomment.md)
</dt> </dl>

 

 




