---
description: La funzione PdhVbGetLogFileSize restituisce le dimensioni del file di log specificato. Questa funzione chiama PdhGetLogFileSize.
ms.assetid: 8f4fbb68-b0f5-4163-ae6e-5b7139a35adf
title: Funzione PdhVbGetLogFileSize
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbGetLogFileSize
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: cd3925eee621ac205615f17b26767096151d459628ca7d331a7aaee3336b27ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119674791"
---
# <a name="pdhvbgetlogfilesize-function"></a>Funzione PdhVbGetLogFileSize

La **funzione PdhVbGetLogFileSize** restituisce le dimensioni del file di log specificato. Questa funzione chiama [**PdhGetLogFileSize**](/windows/desktop/api/Pdh/nf-pdh-pdhgetlogfilesize).

> [!IMPORTANT]
> La funzione descritta in questo argomento potrebbe essere modificata o non disponibile in futuro. Microsoft consiglia invece di usare le funzioni descritte in [Funzioni dei contatori delle prestazioni](performance-counters-functions.md).

Funzione PdhVbGetLogFileSize( \_ ByVal hLog As PDH \_ HLOG, \_ ByRef llSize As LONG \_ ) As DWORD

## <a name="parameters"></a>Parametri

<dl> <dt>

*hLog* \[ Pollici\]
</dt> <dd>

Handle per il file di log. Questo handle viene restituito dalla [**funzione PdhOpenLog.**](/windows/desktop/api/Pdh/nf-pdh-pdhopenloga)

</dd> <dt>

*llSize* \[ Cambio\]
</dt> <dd>

Puntatore a una variabile che riceve le dimensioni del file di log, in byte.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, restituisce 0.

Se la funzione ha esito negativo, il valore restituito è un codice di errore [di sistema](/windows/desktop/Debug/system-error-codes) o un codice di [errore PDH](pdh-error-codes.md). Di seguito sono riportati i valori possibili.



| Codice restituito                                                                                                | Descrizione                                                                                            |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <dt>**BUFFER PDH \_ INSUFFICIENTE \_**</dt> </dl>   | I dati richiesti sono maggiori del buffer fornito. Impossibile restituire i dati richiesti.<br/> |
| <dl> <dt>**ARGOMENTO PDH \_ NON \_ VALIDO**</dt> </dl>      | Uno o più buffer di stringa non hanno le dimensioni corrette.<br/>                                  |
| <dl> <dt>**HANDLE PDH \_ NON \_ VALIDO**</dt> </dl>        | L'handle non è un oggetto PDH valido.<br/>                                                       |
| <dl> <dt>**ERRORE DI APERTURA \_ DEL FILE DI LOG \_ PDH \_ \_**</dt> </dl> | Impossibile aprire il file di log specificato.<br/>                                                      |
| <dl> <dt>**FILE PDH \_ \_ NON \_ TROVATO**</dt> </dl>       | Impossibile trovare il file specificato.<br/>                                                          |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                               |
| Libreria<br/>                  | <dl> <dt>Pdh.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Pdh.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**PdhGetLogFileSize**](/windows/desktop/api/Pdh/nf-pdh-pdhgetlogfilesize)
</dt> <dt>

[**PdhVbOpenLog**](pdhvbopenlog.md)
</dt> <dt>

[**PdhVbUpdateLog**](pdhvbupdatelog.md)
</dt> </dl>

 

