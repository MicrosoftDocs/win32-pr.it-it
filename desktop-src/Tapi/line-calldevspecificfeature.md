---
description: Il messaggio TSPI LINE CALLDEVSPECIFICFEATURE viene inviato alla funzione di callback LINEEVENT per notificare a TAPI gli eventi specifici del dispositivo che si verificano in una riga \_ o in un indirizzo.
ms.assetid: bf470f5b-f7e5-4f98-9b60-12da599ebf26
title: LINE_CALLDEVSPECIFICFEATURE messaggio (Tspi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb8dde8377f952f02f021209b01f846ba323cc7dbf8795743422e2c83e457b5b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119873631"
---
# <a name="line_calldevspecificfeature-message"></a>MESSAGGIO \_ LINE CALLDEVSPECIFICFEATURE

Il messaggio TSPI **LINE \_ CALLDEVSPECIFICFEATURE** viene inviato alla funzione di callback [**LINEEVENT**](/windows/win32/api/tspi/nc-tspi-lineevent) per notificare a TAPI gli eventi specifici del dispositivo che si verificano in una riga o in un indirizzo. Il significato del messaggio e l'interpretazione dei *parametri da dwParam1* a *dwParam3* sono specifici del dispositivo.


```C++
            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*htLine* 
</dt> <dd>

Handle di oggetto opaco TAPI per il dispositivo linea.

</dd> <dt>

*htCall* 
</dt> <dd>

Handle di oggetto opaco TAPI per il dispositivo di chiamata.

</dd> <dt>

*dwMsg* 
</dt> <dd>

Valore LINE \_ CALLDEVSPECIFICFEATURE.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Specifico del dispositivo.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Specifico del dispositivo.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Specifico del dispositivo.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il **messaggio LINE \_ CALLDEVSPECIFICFEATURE** viene usato da un provider di servizi insieme alla funzione [**\_ lineDevSpecificFeature TSPI.**](/windows/win32/api/tspi/nf-tspi-tspi_linedevspecificfeature) Il significato è specifico del dispositivo.

TAPI invia il [**messaggio LINE \_ DEVSPECIFICFEATURE**](/previous-versions/windows/desktop/legacy/ms725227(v=vs.85)) alle applicazioni in risposta alla ricezione di questo messaggio da un provider di servizi. I *parametri htLine* e *htCall* vengono convertiti nell'oggetto *hCall* appropriato come *parametro hDevice* a livello TAPI. I *parametri dwParam1*, *dwParam2* e *dwParam3* vengono passati senza modifiche.

Non esiste alcun messaggio direttamente corrispondente a livello TAPI, anche se questo messaggio è molto simile a LINE \_ DEVSPECIFICFEATURE. A livello TSPI, i messaggi di funzionalità specifici del dispositivo vengono suddivisi tra gli eventi di segnalazione su righe e indirizzi e quelli che segnalano eventi sulle chiamate.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2.0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>Tspi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**LINE \_ DEVSPECIFICFEATURE**](/previous-versions/windows/desktop/legacy/ms725227(v=vs.85))
</dt> <dt>

[**TSPI \_ lineDevSpecificFeature**](/windows/win32/api/tspi/nf-tspi-tspi_linedevspecificfeature)
</dt> </dl>

 

