---
description: La funzione GetCaptureCommentFromFilename estrae il commento di acquisizione da un file di acquisizione.
ms.assetid: d3665cb0-d54d-45f7-aef9-c2e603d6f773
title: Funzione GetCaptureCommentFromFilename (Netmon.h)
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
ms.openlocfilehash: 1b92b81fa00834c3a4038a6a6bb9f295246a7c0b217c99779a5d2c569dbbf982
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118366812"
---
# <a name="getcapturecommentfromfilename-function"></a>Funzione GetCaptureCommentFromFilename

La **funzione GetCaptureCommentFromFilename** estrae il commento di acquisizione da un [*file di acquisizione.*](c.md)

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

*lpFilename* \[ Pollici\]
</dt> <dd>

Puntatore al nome del file di acquisizione.

</dd> <dt>

*lpComment* \[ Pollici\]
</dt> <dd>

Puntatore a una stringa preallocato per il commento.

</dd> <dt>

*BufferSize* \[ Pollici\]
</dt> <dd>

Dimensione della stringa.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, ovvero se il commento viene trovato e copiato o non è presente alcun commento nel file di acquisizione, il valore restituito è NMERR \_ SUCCESS.

Se la funzione ha esito negativo, il valore restituito è un codice di errore.



| Codice restituito                                                                                                 | Descrizione                                                                  |
|-------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <dt>**ERRORE DI LETTURA \_ FILE NMERR \_ \_**</dt> </dl>     | Impossibile leggere il commento di acquisizione.<br/>                               |
| <dl> <dt>**FORMATO DI FILE NON VALIDO DI \_ \_ \_ NMERR**</dt> </dl> | Il frame comment non è un formato di file valido.<br/>                     |
| <dl> <dt>**FILE NMERR \_ \_ NON \_ TROVATO**</dt> </dl>      | Impossibile trovare il file specificato dal parametro *lpFilename.*<br/> |
| <dl> <dt>**PARAMETRO NON \_ VALIDO DI NMERR \_**</dt> </dl>    | Uno dei parametri è specificato in modo non corretto.<br/>                   |



 

## <a name="remarks"></a>Commenti

[*Esperti*](e.md) e [*parser*](p.md) possono chiamare la **funzione GetCaptureCommentFromFilename.**

Per recuperare il commento di un'acquisizione in tempo reale, chiamare la [funzione GetCaptureComment.](getcapturecomment.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Libreria<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[GetCaptureComment](getcapturecomment.md)
</dt> </dl>

 

 




