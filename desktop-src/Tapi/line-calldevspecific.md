---
description: Il messaggio TSPI LINE CALLDEVSPECIFIC viene inviato alla funzione di callback LINEEVENT per notificare a TAPI gli eventi specifici del dispositivo che si \_ verificano in una chiamata.
ms.assetid: accd753a-3be0-4c7d-bbc7-d294d1381144
title: LINE_CALLDEVSPECIFIC messaggio (Tspi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9930da3c30d51781b10b28ed7a712cb681950eaea1a387212a5e0894658a9125
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012601"
---
# <a name="line_calldevspecific-message"></a>LINE \_ CALLDEVSPECIFIC message

Il messaggio TSPI **LINE \_ CALLDEVSPECIFIC** viene inviato alla funzione di callback [**LINEEVENT**](/windows/win32/api/tspi/nc-tspi-lineevent) per notificare a TAPI gli eventi specifici del dispositivo che si verificano in una chiamata. Il significato del messaggio e l'interpretazione dei *parametri da dwParam1* a *dwParam3* sono specifici del dispositivo.


```C++
            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*htLine* 
</dt> <dd>

Handle dell'oggetto opaco TAPI per il dispositivo linea.

</dd> <dt>

*htCall* 
</dt> <dd>

Handle di oggetto opaco TAPI per il dispositivo di chiamata.

</dd> <dt>

*dwMsg* 
</dt> <dd>

Valore LINE \_ CALLDEVSPECIFIC.

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

Il **messaggio LINE \_ CALLDEVSPECIFIC** viene usato da un provider di servizi insieme alla [**funzione \_ lineDevSpecific TSPI.**](/windows/win32/api/tspi/nf-tspi-tspi_linedevspecific) Il significato è specifico del dispositivo.

TAPI invia il [**messaggio \_ LINE DEVSPECIFIC alle**](/previous-versions/windows/desktop/legacy/ms725225(v=vs.85)) applicazioni in risposta alla ricezione di questo messaggio da un provider di servizi. I *parametri htLine* e *htCall* vengono convertiti nell'oggetto *hCall* appropriato come *parametro hDevice* a livello TAPI. I *parametri dwParam1*, *dwParam2* e *dwParam3* vengono passati senza modifiche.

Non esiste alcun messaggio direttamente corrispondente a livello TAPI, anche se questo messaggio è molto simile a [**LINE \_ DEVSPECIFIC**](/previous-versions/windows/desktop/legacy/ms725225(v=vs.85)). A livello TSPI, i messaggi specifici del dispositivo vengono suddivisi tra gli eventi di segnalazione su righe e indirizzi e quelli che segnalano eventi sulle chiamate.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2.0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>Tspi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**LINE \_ DEVSPECIFIC**](/previous-versions/windows/desktop/legacy/ms725225(v=vs.85))
</dt> <dt>

[**LINEEVENT**](/windows/win32/api/tspi/nc-tspi-lineevent)
</dt> <dt>

[**TSPI \_ lineDevSpecific**](/windows/win32/api/tspi/nf-tspi-tspi_linedevspecific)
</dt> </dl>

 

