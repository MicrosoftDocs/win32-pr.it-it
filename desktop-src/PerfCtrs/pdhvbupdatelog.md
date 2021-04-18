---
description: La funzione PdhVbUpdateLog Function aggiorna la query corrente e scrive nuovi dati nel file di log. Questa funzione chiama PdhUpdateLog.
ms.assetid: a7a3ad18-2d61-448e-9764-ba363398e804
title: PdhVbUpdateLog (funzione)
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
ms.openlocfilehash: c02e533f57481004b0a7de9f779399b20bddc0af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312142"
---
# <a name="pdhvbupdatelog-function"></a>PdhVbUpdateLog (funzione)

La funzione **PdhVbUpdateLog** Function aggiorna la query corrente e scrive nuovi dati nel file di log. Questa funzione chiama [**PdhUpdateLog**](/windows/desktop/api/Pdh/nf-pdh-pdhupdateloga).

> [!IMPORTANT]
> La funzione descritta in questo argomento può essere modificata o non disponibile in futuro. Microsoft consiglia invece di utilizzare le funzioni descritte in [funzioni dei contatori delle prestazioni](performance-counters-functions.md).

Funzione PdhVbUpdateLog ( \_ ByVal numero As PDH \_ numero, \_ ByVal szUserString As LPCTSTR \_ )

## <a name="parameters"></a>Parametri

<dl> <dt>

*numero* \[ in\]
</dt> <dd>

Handle per il file di log da aggiornare. Questo handle viene restituito dalla funzione [**PdhVbOpenLog**](pdhvbopenlog.md) .

</dd> <dt>

*szUserString* \[ in\]
</dt> <dd>

Puntatore a una stringa che specifica i dati da aggiungere al file di log. Questa operazione viene in genere utilizzata per i commenti nel file di log.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, restituisce 0.

Se la funzione ha esito negativo, il valore restituito è un [codice di errore di sistema](/windows/desktop/Debug/system-error-codes) o un codice di [errore PDH](pdh-error-codes.md). Di seguito sono riportati i valori possibili.



| Codice restituito                                                                                                | Descrizione                                                                                            |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_buffer insufficiente PDH \_**</dt> </dl>   | I dati richiesti sono maggiori del buffer fornito. Impossibile restituire i dati richiesti.<br/> |
| <dl> <dt>**\_argomento PDH non valido \_**</dt> </dl>      | La dimensione di uno o più buffer di stringa non è corretta.<br/>                                  |
| <dl> <dt>**\_handle PDH non valido \_**</dt> </dl>        | L'handle non è un oggetto PDH valido.<br/>                                                       |
| <dl> <dt>**\_errore di \_ apertura del file di registro PDH \_ \_**</dt> </dl> | Impossibile aprire il file di log specificato.<br/>                                                      |
| <dl> <dt>**il \_ file PDH non è stato \_ \_ trovato**</dt> </dl>       | Impossibile trovare il file specificato.<br/>                                                          |



 

## <a name="remarks"></a>Commenti

È necessario che sia presente una query attualmente aperta ed è necessario aggiungervi i contatori desiderati prima di chiamare questa funzione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                               |
| Libreria<br/>                  | <dl> <dt>PDH. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Pdh.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**PdhUpdateLog**](/windows/desktop/api/Pdh/nf-pdh-pdhupdateloga)
</dt> <dt>

[**PdhVbGetLogFileSize**](pdhvbgetlogfilesize.md)
</dt> <dt>

[**PdhVbOpenLog**](pdhvbopenlog.md)
</dt> </dl>

 

