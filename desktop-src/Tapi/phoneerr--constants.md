---
description: Questo è l'elenco dei codici di errore che l'implementazione può restituire quando si richiamano le operazioni sui dispositivi telefonici. Consultare le descrizioni delle singole funzioni per determinare quali di questi codici di errore possono essere restituiti da ogni funzione.
ms.assetid: 763a9dc2-3e70-4169-a66e-3aac78ef8d33
title: Costanti PHONEERR_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b41ba5d14f4aa12318dd4bc9f2b20e4e9e2e6b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333951"
---
# <a name="phoneerr_-constants"></a>\_Costanti PHONEERR

Questo è l'elenco dei codici di errore che l'implementazione può restituire quando si richiamano le operazioni sui dispositivi telefonici. Consultare le descrizioni delle singole funzioni per determinare quali di questi codici di errore possono essere restituiti da ogni funzione.

<dl> <dt>

<span id="PHONEERR_ALLOCATED"></span><span id="phoneerr_allocated"></span>**PHONEERR \_ allocato**
</dt> <dd> <dl> <dt>



La risorsa specificata è già allocata.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_BADDEVICEID"></span><span id="phoneerr_baddeviceid"></span>**\_BADDEVICEID PHONEERR**
</dt> <dd> <dl> <dt>



L'identificatore di dispositivo specificato non è valido o non è compreso nell'intervallo.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_DISCONNECTED"></span><span id="phoneerr_disconnected"></span>**PHONEERR \_ disconnesso**
</dt> <dd> <dl> <dt>



La chiamata è stata disconnessa.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_INCOMPATIBLEAPIVERSION"></span><span id="phoneerr_incompatibleapiversion"></span>**\_INCOMPATIBLEAPIVERSION PHONEERR**
</dt> <dd> <dl> <dt>



L'applicazione ha richiesto una versione o un intervallo di versioni dell'API che non può essere supportato dall'implementazione dell'API di telefonia o dal provider di servizi corrispondente.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_INCOMPATIBLEEXTVERSION"></span><span id="phoneerr_incompatibleextversion"></span>**\_INCOMPATIBLEEXTVERSION PHONEERR**
</dt> <dd> <dl> <dt>



L'applicazione ha richiesto una versione dell'estensione o un intervallo di versioni che non può essere supportato dal provider di servizi.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_INIFILECORRUPT"></span><span id="phoneerr_inifilecorrupt"></span>**\_INIFILECORRUPT PHONEERR**
</dt> <dd> <dl> <dt>



A causa di incoerenze interne o problemi di formattazione nel file di Telephon.ini, non può essere letto e compreso correttamente da TAPI.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_INUSE"></span><span id="phoneerr_inuse"></span>**\_InUse PHONEERR**
</dt> <dd> <dl> <dt>



Il dispositivo è attualmente in uso. Non è possibile configurare il dispositivo.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_INVALAPPHANDLE"></span><span id="phoneerr_invalapphandle"></span>**\_INVALAPPHANDLE PHONEERR**
</dt> <dd> <dl> <dt>



Il punto di controllo di utilizzo o l'handle di registrazione specificato dall'applicazione non è valido.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_INVALAPPNAME"></span><span id="phoneerr_invalappname"></span>**\_INVALAPPNAME PHONEERR**
</dt> <dd> <dl> <dt>



Il nome dell'applicazione specificato non è valido. Se l'applicazione specifica un nome di applicazione, si presuppone che la stringa non contenga caratteri non visualizzabili e con terminazione **null**.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_INVALBUTTONLAMPID"></span><span id="phoneerr_invalbuttonlampid"></span>**\_INVALBUTTONLAMPID PHONEERR**
</dt> <dd> <dl> <dt>



L'identificatore del pulsante o della lampada specificato non è compreso nell'intervallo o non è valido.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_INVALBUTTONMODE"></span><span id="phoneerr_invalbuttonmode"></span>**\_INVALBUTTONMODE PHONEERR**
</dt> <dd> <dl> <dt>



Il parametro della modalità pulsante non è valido.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_INVALBUTTONSTATE"></span><span id="phoneerr_invalbuttonstate"></span>**\_INVALBUTTONSTATE PHONEERR**
</dt> <dd> <dl> <dt>



Il parametro degli Stati dei pulsanti non è valido.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_INVALDATAID"></span><span id="phoneerr_invaldataid"></span>**\_INVALDATAID PHONEERR**
</dt> <dd> <dl> <dt>



L'identificatore di dati specificato non è valido.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_INVALDEVICECLASS"></span><span id="phoneerr_invaldeviceclass"></span>**\_INVALDEVICECLASS PHONEERR**
</dt> <dd> <dl> <dt>



Il telefono specificato non supporta la classe di dispositivi indicata.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_INVALEXTVERSION"></span><span id="phoneerr_invalextversion"></span>**\_INVALEXTVERSION PHONEERR**
</dt> <dd> <dl> <dt>



Il numero di versione dell'estensione del provider di servizi non è valido.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_INVALHOOKSWITCHDEV"></span><span id="phoneerr_invalhookswitchdev"></span>**\_INVALHOOKSWITCHDEV PHONEERR**
</dt> <dd> <dl> <dt>



Il parametro del dispositivo hookswitch non è valido.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_INVALHOOKSWITCHMODE"></span><span id="phoneerr_invalhookswitchmode"></span>**\_INVALHOOKSWITCHMODE PHONEERR**
</dt> <dd> <dl> <dt>



Il parametro della modalità hookswitch non è valido.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_INVALLAMPMODE"></span><span id="phoneerr_invallampmode"></span>**\_INVALLAMPMODE PHONEERR**
</dt> <dd> <dl> <dt>



Il parametro della modalità lampada specificato non è valido.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_INVALPARAM"></span><span id="phoneerr_invalparam"></span>**\_INVALPARAM PHONEERR**
</dt> <dd> <dl> <dt>



Un parametro, ad esempio un valore di riga o di colonna o un handle di finestra, non è valido o non è compreso nell'intervallo.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_INVALPHONEHANDLE"></span><span id="phoneerr_invalphonehandle"></span>**\_INVALPHONEHANDLE PHONEERR**
</dt> <dd> <dl> <dt>



L'handle di dispositivo specificato non è valido.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_INVALPHONESTATE"></span><span id="phoneerr_invalphonestate"></span>**\_INVALPHONESTATE PHONEERR**
</dt> <dd> <dl> <dt>



Il dispositivo telefonico non è in uno stato valido per l'operazione richiesta.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_INVALPOINTER"></span><span id="phoneerr_invalpointer"></span>**\_INVALPOINTER PHONEERR**
</dt> <dd> <dl> <dt>



Uno o più parametri del puntatore specificati non sono validi.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_INVALPRIVILEGE"></span><span id="phoneerr_invalprivilege"></span>**\_INVALPRIVILEGE PHONEERR**
</dt> <dd> <dl> <dt>



Il parametro *dwPrivilege* non è valido.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_INVALRINGMODE"></span><span id="phoneerr_invalringmode"></span>**\_INVALRINGMODE PHONEERR**
</dt> <dd> <dl> <dt>



Il parametro della modalità anello non è valido.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_NODEVICE"></span><span id="phoneerr_nodevice"></span>**PHONEERR \_ NOdevice**
</dt> <dd> <dl> <dt>



L'identificatore di dispositivo specificato, che in precedenza era valido, non viene più accettato perché il dispositivo associato è stato rimosso dal sistema perché TAPI è stato inizializzato per l'ultima volta o è danneggiato in modo non rilevato durante l'inizializzazione.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_NODRIVER"></span><span id="phoneerr_nodriver"></span>**PHONEERR \_ NOdriver**
</dt> <dd> <dl> <dt>



Il provider del servizio telefonico per il dispositivo specificato ha rilevato che uno dei suoi componenti è mancante o danneggiato in modo che non sia stato rilevato al momento dell'inizializzazione. Per risolvere il problema, è consigliabile usare il pannello di controllo telefonia.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_NOMEM"></span><span id="phoneerr_nomem"></span>**nome del PHONEERR \_**
</dt> <dd> <dl> <dt>



Memoria insufficiente per completare l'operazione richiesta oppure non è possibile allocare o bloccare la memoria.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_NOTOWNER"></span><span id="phoneerr_notowner"></span>**\_NOtowner PHONEERR**
</dt> <dd> <dl> <dt>



L'applicazione non dispone del privilegio proprietario per il dispositivo telefonico specificato.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_OPERATIONFAILED"></span><span id="phoneerr_operationfailed"></span>**\_OPERATIONFAILED PHONEERR**
</dt> <dd> <dl> <dt>



L'operazione non è riuscita per un motivo non specificato.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_OPERATIONUNAVAIL"></span><span id="phoneerr_operationunavail"></span>**\_OPERATIONUNAVAIL PHONEERR**
</dt> <dd> <dl> <dt>



Operazione non disponibile.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_REINIT"></span><span id="phoneerr_reinit"></span>**PHONEERR \_ REinit**
</dt> <dd> <dl> <dt>



Se è stata richiesta la reinizializzazione di TAPI, ad esempio in seguito all'aggiunta o alla rimozione di un provider di servizi di telefonia, le richieste [**phoneInitialize**](/windows/desktop/api/Tapi/nf-tapi-phoneinitialize), [**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa) o [**phoneOpen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen) vengono rifiutate con questo errore fino a quando l'ultima applicazione non arresta l'utilizzo dell'API (usando [**phoneShutdown**](/windows/desktop/api/Tapi/nf-tapi-phoneshutdown)), a quel punto la nuova configurazione diventa effettiva e le applicazioni sono nuovamente autorizzate a chiamare **phoneInitialize** o **phoneInitializeEx**


</dt> </dl> </dd> <dt>

<span id="PHONEERR_REQUESTOVERRUN"></span><span id="phoneerr_requestoverrun"></span>**\_REQUESTOVERRUN PHONEERR**
</dt> <dd> <dl> <dt>



È stato superato il numero massimo di richieste telefoniche in attesa.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_RESOURCEUNAVAIL"></span><span id="phoneerr_resourceunavail"></span>**\_RESOURCEUNAVAIL PHONEERR**
</dt> <dd> <dl> <dt>



Non è possibile completare l'operazione a causa di un overcommit delle risorse.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_STRUCTURETOOSMALL"></span><span id="phoneerr_structuretoosmall"></span>**\_STRUCTURETOOSMALL PHONEERR**
</dt> <dd> <dl> <dt>



La struttura dei tappi telefonici specificata è troppo piccola.


</dt> </dl> </dd> <dt>

<span id="PHONEERR_UNINITIALIZED"></span><span id="phoneerr_uninitialized"></span>**PHONEERR non \_ inizializzato**
</dt> <dd> <dl> <dt>



L'operazione è stata richiamata prima di qualsiasi applicazione denominata [**phoneInitialize**](/windows/desktop/api/Tapi/nf-tapi-phoneinitialize), [**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa).


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

I valori da 0xC0000000 a 0xFFFFFFFF sono disponibili per le estensioni specifiche del dispositivo. i valori 0x80000000 tramite 0xBFFFFFFF sono riservati. e 0x00000000 tramite 0x7FFFFFFF vengono usati come identificatori di richiesta.

Se un'applicazione restituisce un errore che non gestisce in modo specifico (ad esempio un errore definito da un'estensione specifica del dispositivo), deve considerare l'errore come un \_ OPERATIONFAILED PHONEERR (per un motivo non specificato).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2,0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



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

 

 




