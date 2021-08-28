---
description: Questo è l'elenco dei codici di errore che l'implementazione può restituire quando richiama operazioni sui dispositivi telefonici. Consultare le descrizioni delle singole funzioni per determinare quale di questi codici di errore può restituire ogni funzione.
ms.assetid: 763a9dc2-3e70-4169-a66e-3aac78ef8d33
title: PHONEERR_ costanti (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b66c4dd2078b7de1572137ee1d759e7b186328dc5604c9790e444db428eb774a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119060659"
---
# <a name="phoneerr_-constants"></a>Costanti \_ PHONEERR

Questo è l'elenco dei codici di errore che l'implementazione può restituire quando richiama operazioni sui dispositivi telefonici. Consultare le descrizioni delle singole funzioni per determinare quale di questi codici di errore può restituire ogni funzione.

<dl> <dt>

<span id="PHONEERR_ALLOCATED"></span><span id="phoneerr_allocated"></span>**PHONEERR \_ ALLOCATO**
</dt> <dd> <dl> <dt>



La risorsa specificata è già allocata.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_BADDEVICEID"></span><span id="phoneerr_baddeviceid"></span>**PHONEERR \_ BADDEVICEID**
</dt> <dd> <dl> <dt>



L'identificatore di dispositivo specificato non è valido o non è compreso nell'intervallo.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_DISCONNECTED"></span><span id="phoneerr_disconnected"></span>**PHONEERR \_ DISCONNESSO**
</dt> <dd> <dl> <dt>



La chiamata è stata disconnessa.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_INCOMPATIBLEAPIVERSION"></span><span id="phoneerr_incompatibleapiversion"></span>**PHONEERR \_ INCOMPATIBLEAPIVERSION**
</dt> <dd> <dl> <dt>



L'applicazione ha richiesto una versione dell'API o un intervallo di versioni che non può essere supportato dall'implementazione dell'API Di telefonia o dal provider di servizi corrispondente.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_INCOMPATIBLEEXTVERSION"></span><span id="phoneerr_incompatibleextversion"></span>**PHONEERR \_ INCOMPATIBLEEXTVERSION**
</dt> <dd> <dl> <dt>



L'applicazione ha richiesto una versione dell'estensione o un intervallo di versioni che non può essere supportato dal provider di servizi.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_INIFILECORRUPT"></span><span id="phoneerr_inifilecorrupt"></span>**PHONEERR \_ INIFILECORRUPT**
</dt> <dd> <dl> <dt>



A causa di incoerenze interne o problemi di formattazione nel file Telephon.ini, non può essere letto e compreso correttamente da TAPI.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_INUSE"></span><span id="phoneerr_inuse"></span>**PHONEERR \_ INUSE**
</dt> <dd> <dl> <dt>



Il dispositivo è attualmente in uso. Impossibile configurare il dispositivo.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_INVALAPPHANDLE"></span><span id="phoneerr_invalapphandle"></span>**PHONEERR \_ INVALAPPHANDLE**
</dt> <dd> <dl> <dt>



L'handle di utilizzo specificato dell'applicazione o l'handle di registrazione non è valido.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_INVALAPPNAME"></span><span id="phoneerr_invalappname"></span>**PHONEERR \_ INVALAPPNAME**
</dt> <dd> <dl> <dt>



Il nome dell'applicazione specificato non è valido. Se un nome di applicazione viene specificato dall'applicazione, si presuppone che la stringa non contenga caratteri non visualizzabili e che sia **NULL**-terminated.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_INVALBUTTONLAMPID"></span><span id="phoneerr_invalbuttonlampid"></span>**PHONEERR \_ INVALBUTTONLAMPID**
</dt> <dd> <dl> <dt>



L'identificatore di pulsante/lamp specificato non è compreso nell'intervallo o non è valido.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_INVALBUTTONMODE"></span><span id="phoneerr_invalbuttonmode"></span>**PHONEERR \_ INVALBUTTONMODE**
</dt> <dd> <dl> <dt>



Il parametro della modalità pulsante non è valido.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_INVALBUTTONSTATE"></span><span id="phoneerr_invalbuttonstate"></span>**PHONEERR \_ INVALBUTTONSTATE**
</dt> <dd> <dl> <dt>



Il parametro degli stati del pulsante non è valido.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_INVALDATAID"></span><span id="phoneerr_invaldataid"></span>**PHONEERR \_ INVALDATAID**
</dt> <dd> <dl> <dt>



L'identificatore dati specificato non è valido.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_INVALDEVICECLASS"></span><span id="phoneerr_invaldeviceclass"></span>**PHONEERR \_ INVALDEVICECLASS**
</dt> <dd> <dl> <dt>



Il telefono specificato non supporta la classe del dispositivo indicata.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_INVALEXTVERSION"></span><span id="phoneerr_invalextversion"></span>**PHONEERR \_ INVALEXTVERSION**
</dt> <dd> <dl> <dt>



Il numero di versione dell'estensione del provider di servizi non è valido.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_INVALHOOKSWITCHDEV"></span><span id="phoneerr_invalhookswitchdev"></span>**PHONEERR \_ INVALHOOKSWITCHDEV**
</dt> <dd> <dl> <dt>



Il parametro del dispositivo hookswitch non è valido.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_INVALHOOKSWITCHMODE"></span><span id="phoneerr_invalhookswitchmode"></span>**PHONEERR \_ INVALHOOKSWITCHMODE**
</dt> <dd> <dl> <dt>



Il parametro hookswitch mode non è valido.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_INVALLAMPMODE"></span><span id="phoneerr_invallampmode"></span>**PHONEERR \_ INVALLAMPMODE**
</dt> <dd> <dl> <dt>



Il parametro lamp mode specificato non è valido.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_INVALPARAM"></span><span id="phoneerr_invalparam"></span>**PHONEERR \_ INVALPARAM**
</dt> <dd> <dl> <dt>



Un parametro, ad esempio un valore di riga o di colonna o un handle di finestra, non è valido o non è compreso nell'intervallo.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_INVALPHONEHANDLE"></span><span id="phoneerr_invalphonehandle"></span>**PHONEERR \_ INVALPHONEHANDLE**
</dt> <dd> <dl> <dt>



L'handle di dispositivo specificato non è valido.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_INVALPHONESTATE"></span><span id="phoneerr_invalphonestate"></span>**PHONEERR \_ INVALPHONESTATE**
</dt> <dd> <dl> <dt>



Il dispositivo telefonico non è in uno stato valido per l'operazione richiesta.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_INVALPOINTER"></span><span id="phoneerr_invalpointer"></span>**PHONEERR \_ INVALPOINTER**
</dt> <dd> <dl> <dt>



Uno o più parametri puntatore specificati non sono validi.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_INVALPRIVILEGE"></span><span id="phoneerr_invalprivilege"></span>**PHONEERR \_ INVALPRIVILEGE**
</dt> <dd> <dl> <dt>



Il *parametro dwPrivilege* non è valido.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_INVALRINGMODE"></span><span id="phoneerr_invalringmode"></span>**PHONEERR \_ INVALRINGMODE**
</dt> <dd> <dl> <dt>



Il parametro della modalità anello non è valido.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_NODEVICE"></span><span id="phoneerr_nodevice"></span>**PHONEERR \_ NODEVICE**
</dt> <dd> <dl> <dt>



L'identificatore di dispositivo specificato, precedentemente valido, non è più accettato perché il dispositivo associato è stato rimosso dal sistema dopo l'ultima inizializzazione di TAPI o è danneggiato in un modo che non è stato rilevato durante l'inizializzazione.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_NODRIVER"></span><span id="phoneerr_nodriver"></span>**PHONEERR \_ NODRIVER**
</dt> <dd> <dl> <dt>



Il provider di servizi telefonici per il dispositivo specificato ha rilevato che uno dei relativi componenti è mancante o danneggiato in un modo che non è stato rilevato in fase di inizializzazione. Per risolvere il problema, è consigliabile Pannello di controllo'utente.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_NOMEM"></span><span id="phoneerr_nomem"></span>**PHONEERR \_ NOMEM**
</dt> <dd> <dl> <dt>



Memoria insufficiente per completare l'operazione richiesta o impossibile allocare o bloccare la memoria.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_NOTOWNER"></span><span id="phoneerr_notowner"></span>**PHONEERR \_ NOTOWNER**
</dt> <dd> <dl> <dt>



L'applicazione non dispone dei privilegi di proprietario per il dispositivo telefonico specificato.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_OPERATIONFAILED"></span><span id="phoneerr_operationfailed"></span>**OPERAZIONE PHONEERR \_ NON RIUSCITA**
</dt> <dd> <dl> <dt>



L'operazione non è riuscita per un motivo non specificato.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_OPERATIONUNAVAIL"></span><span id="phoneerr_operationunavail"></span>**OPERAZIONE \_ PHONEERRUNAVAIL**
</dt> <dd> <dl> <dt>



L'operazione non è disponibile.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_REINIT"></span><span id="phoneerr_reinit"></span>**PHONEERR \_ REINIT**
</dt> <dd> <dl> <dt>



Se è stata richiesta la reinizializzazione TAPI, ad esempio in seguito all'aggiunta o alla rimozione di un provider di servizi di telefonia, le richieste [**phoneInitialize**](/windows/desktop/api/Tapi/nf-tapi-phoneinitialize), [**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa) o [**phoneOpen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen) vengono rifiutate con questo errore fino a quando l'ultima applicazione non arresta l'utilizzo dell'API (usando [**phoneShutdown**](/windows/desktop/api/Tapi/nf-tapi-phoneshutdown)), in cui la nuova configurazione diventa effettiva e le applicazioni sono nuovamente autorizzate a chiamare **phoneInitialize** o **phoneInitializeEx**.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_REQUESTOVERRUN"></span><span id="phoneerr_requestoverrun"></span>**PHONEERR \_ REQUESTOVERRUN**
</dt> <dd> <dl> <dt>



È stato superato il numero massimo di richieste telefoniche in sospeso.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_RESOURCEUNAVAIL"></span><span id="phoneerr_resourceunavail"></span>**RISORSA \_ PHONEERRUNAVAIL**
</dt> <dd> <dl> <dt>



Impossibile completare l'operazione a causa dell'overcommit delle risorse.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_STRUCTURETOOSMALL"></span><span id="phoneerr_structuretoosmall"></span>**STRUTTURA \_ PHONEERRTOOSMALL**
</dt> <dd> <dl> <dt>



La struttura delle estremità del telefono specificata è troppo piccola.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_UNINITIALIZED"></span><span id="phoneerr_uninitialized"></span>**PHONEERR \_ NON INIZIALIZZATO**
</dt> <dd> <dl> <dt>



L'operazione è stata richiamata prima di qualsiasi applicazione denominata [**phoneInitialize**](/windows/desktop/api/Tapi/nf-tapi-phoneinitialize), [**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa).


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

I valori 0xC0000000 da 0xFFFFFFFF sono disponibili per le estensioni specifiche del dispositivo. i valori da 0x80000000 a 0xBFFFFFFF sono riservati; e 0x00000000 tramite 0x7FFFFFFF vengono usati come identificatori di richiesta.

Se un'applicazione riceve un errore che non gestisce in modo specifico (ad esempio un errore definito da un'estensione specifica del dispositivo), deve considerare l'errore come OPERAZIONE PHONEERRFAILED (per un motivo non \_ specificato).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2.0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**phoneInitialize**](/windows/desktop/api/Tapi/nf-tapi-phoneinitialize)
</dt> <dt>

[**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa)
</dt> <dt>

[**phoneOpen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen)
</dt> <dt>

[**phoneShutdown**](/windows/desktop/api/Tapi/nf-tapi-phoneshutdown)
</dt> </dl>

 

 




