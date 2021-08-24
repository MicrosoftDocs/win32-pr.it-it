---
description: La funzione PdhVbUpdateLog aggiorna la query corrente e scrive nuovi dati nel file di log. Questa funzione chiama PdhUpdateLog.
ms.assetid: a7a3ad18-2d61-448e-9764-ba363398e804
title: Funzione PdhVbUpdateLog
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbUpdateLog
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: c7bf8af71d3a0f5cd20a84ef0f1532806e3d3e8d268bd2d322d617534b533cc2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033611"
---
# <a name="pdhvbupdatelog-function"></a>Funzione PdhVbUpdateLog

La **funzione PdhVbUpdateLog** aggiorna la query corrente e scrive nuovi dati nel file di log. Questa funzione chiama [**PdhUpdateLog**](/windows/desktop/api/Pdh/nf-pdh-pdhupdateloga).

> [!IMPORTANT]
> La funzione descritta in questo argomento potrebbe essere modificata o non disponibile in futuro. È invece consigliabile usare le funzioni descritte in [Funzioni dei contatori delle prestazioni.](performance-counters-functions.md)

Function PdhVbUpdateLog( \_ ByVal hLog As PDH \_ HLOG, \_ ByVal szUserString As LPCTSTR \_ )

## <a name="parameters"></a>Parametri

<dl> <dt>

*hLog* \[ Pollici\]
</dt> <dd>

Handle per il file di log da aggiornare. Questo handle viene restituito dalla [**funzione PdhVbOpenLog.**](pdhvbopenlog.md)

</dd> <dt>

*szUserString* \[ Pollici\]
</dt> <dd>

Puntatore a una stringa che specifica i dati da aggiungere al file di log. Viene in genere usato per i commenti all'interno del file di log.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, restituisce 0.

Se la funzione ha esito negativo, il valore restituito è un codice [di errore di sistema](/windows/desktop/Debug/system-error-codes) o un codice di errore [PDH](pdh-error-codes.md). Di seguito sono riportati i valori possibili.



| Codice restituito                                                                                                | Descrizione                                                                                            |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <dt>**BUFFER PDH \_ \_ INSUFFICIENTE**</dt> </dl>   | I dati richiesti sono più grandi del buffer fornito. Impossibile restituire i dati richiesti.<br/> |
| <dl> <dt>**ARGOMENTO PDH \_ NON \_ VALIDO**</dt> </dl>      | Uno o più buffer di stringa non hanno le dimensioni corrette.<br/>                                  |
| <dl> <dt>**HANDLE PDH \_ NON \_ VALIDO**</dt> </dl>        | L'handle non è un oggetto PDH valido.<br/>                                                       |
| <dl> <dt>**ERRORE DI APERTURA \_ \_ DEL FILE DI LOG \_ PDH \_**</dt> </dl> | Impossibile aprire il file di log specificato.<br/>                                                      |
| <dl> <dt>**FILE PDH \_ \_ NON \_ TROVATO**</dt> </dl>       | Impossibile trovare il file specificato.<br/>                                                          |



 

## <a name="remarks"></a>Commenti

Deve essere presente una query attualmente aperta e i contatori desiderati devono essere aggiunti alla query prima che venga chiamata questa funzione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                               |
| Libreria<br/>                  | <dl> <dt>Pdh.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Pdh.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**PdhUpdateLog**](/windows/desktop/api/Pdh/nf-pdh-pdhupdateloga)
</dt> <dt>

[**PdhVbGetLogFileSize**](pdhvbgetlogfilesize.md)
</dt> <dt>

[**PdhVbOpenLog**](pdhvbopenlog.md)
</dt> </dl>

 

