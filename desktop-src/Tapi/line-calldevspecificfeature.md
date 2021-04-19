---
description: Il messaggio TSPI LINE \_ CALLDEVSPECIFICFEATURE viene inviato alla funzione di callback LineEvent per notificare a TAPI gli eventi specifici del dispositivo che si verificano su una riga o un indirizzo.
ms.assetid: bf470f5b-f7e5-4f98-9b60-12da599ebf26
title: Messaggio LINE_CALLDEVSPECIFICFEATURE (TSPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2891f019035f53be4dbc0a40de429e5c0d9dc567
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332255"
---
# <a name="line_calldevspecificfeature-message"></a>\_Messaggio linea CALLDEVSPECIFICFEATURE

Il messaggio TSPI **line \_ CALLDEVSPECIFICFEATURE** viene inviato alla funzione di callback [**LineEvent**](/windows/win32/api/tspi/nc-tspi-lineevent) per notificare a TAPI gli eventi specifici del dispositivo che si verificano su una riga o un indirizzo. Il significato del messaggio e l'interpretazione del *dwParam1* tramite i parametri di *dwParam3* sono specifici del dispositivo.


```C++
            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*htLine* 
</dt> <dd>

Handle di oggetto opaco TAPI al dispositivo della linea.

</dd> <dt>

*htCall* 
</dt> <dd>

Handle di oggetto opaco TAPI al dispositivo di chiamata.

</dd> <dt>

*dwMsg* 
</dt> <dd>

RIGA del valore \_ CALLDEVSPECIFICFEATURE.

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

Il messaggio di **riga \_ CALLDEVSPECIFICFEATURE** viene utilizzato da un provider di servizi insieme alla funzione [**TSPI \_ lineDevSpecificFeature**](/windows/win32/api/tspi/nf-tspi-tspi_linedevspecificfeature) . Il suo significato è specifico del dispositivo.

TAPI invia il messaggio di [**riga \_ DEVSPECIFICFEATURE**](/previous-versions/windows/desktop/legacy/ms725227(v=vs.85)) alle applicazioni in risposta alla ricezione di questo messaggio da un provider di servizi. I parametri *htLine* e *htCall* vengono convertiti nel *hCall* appropriato come parametro *hDevice* a livello di TAPI. I parametri *dwParam1*, *dwParam2* e *dwParam3* vengono passati senza modifiche.

Non esiste alcun messaggio direttamente corrispondente a livello di TAPI, sebbene questo messaggio sia molto simile alla riga \_ DEVSPECIFICFEATURE. A livello di TSPI, i messaggi relativi alle funzionalità specifiche del dispositivo vengono suddivisi tra gli eventi di Reporting sulle righe e sugli indirizzi e gli eventi di Reporting sulle chiamate.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2,0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>TSPI. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**LINEA \_ DEVSPECIFICFEATURE**](/previous-versions/windows/desktop/legacy/ms725227(v=vs.85))
</dt> <dt>

[**\_LINEDEVSPECIFICFEATURE TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linedevspecificfeature)
</dt> </dl>

 

