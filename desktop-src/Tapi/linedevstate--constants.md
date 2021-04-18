---
description: Le \_ costanti del flag di bit LINEDEVSTATE descrivono vari eventi dello stato della riga.
ms.assetid: 41e8a777-a57a-4d6c-850f-e21b58081b0d
title: Costanti LINEDEVSTATE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49717c1adb0f62a48a041f5920c0b82c7b817277
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333650"
---
# <a name="linedevstate_-constants"></a>\_Costanti LINEDEVSTATE

Le costanti del flag di bit **LINEDEVSTATE \_** descrivono vari eventi dello stato della riga.

<dl> <dt>

<span id="LINEDEVSTATE_BATTERY"></span><span id="linedevstate_battery"></span>**\_batteria LINEDEVSTATE**
</dt> <dd> <dl> <dt>



Il livello della batteria è stato modificato in modo significativo (cellulare).


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_CAPSCHANGE"></span><span id="linedevstate_capschange"></span>**\_CAPSCHANGE LINEDEVSTATE**
</dt> <dd> <dl> <dt>



Indica che, a causa delle modifiche di configurazione apportate dall'utente o altre circostanze, uno o più membri della struttura [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) per l'indirizzo sono stati modificati. Per leggere la struttura aggiornata, l'applicazione deve usare [**lineGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetdevcaps) . Se un provider di servizi invia un messaggio di [**riga \_ LINEDEVSTATE**](line-linedevstate.md) contenente questo valore a TAPI, TAPI lo passerà a applicazioni che hanno negoziato la versione di TAPI 1,4 o versioni successive. le applicazioni che trattano una versione precedente di TAPI riceveranno i messaggi di **riga \_ LINEDEVSTATE** specificando LINEDEVSTATE \_ reinit, richiedendo di arrestare e reinizializzare la connessione a TAPI per ottenere le informazioni aggiornate.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_CLOSE"></span><span id="linedevstate_close"></span>**chiusura di LINEDEVSTATE \_**
</dt> <dd> <dl> <dt>



La riga è stata chiusa da un'altra applicazione.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_CONFIGCHANGE"></span><span id="linedevstate_configchange"></span>**\_CONFIGCHANGE LINEDEVSTATE**
</dt> <dd> <dl> <dt>



Indica che sono state apportate modifiche alla configurazione a uno o più dispositivi multimediali associati al dispositivo della linea. L'applicazione, se desidera, può utilizzare [**lineGetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig) per leggere le informazioni aggiornate. Se un provider di servizi invia un messaggio di [**riga \_ LINEDEVSTATE**](line-linedevstate.md) contenente questo valore a TAPI, TAPI lo passerà a applicazioni con la versione 1,4 di TAPI negoziata o successiva. le applicazioni che negoziano una versione precedente dell'API non riceveranno alcuna notifica.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_COMPLCANCEL"></span><span id="linedevstate_complcancel"></span>**\_COMPLCANCEL LINEDEVSTATE**
</dt> <dd> <dl> <dt>



Indica che il completamento della chiamata identificato dall'identificatore di completamento contenuto nel parametro *dwParam2* del messaggio [**line \_ LINEDEVSTATE**](line-linedevstate.md) è stato annullato esternamente e non è più considerato valido (se tale valore deve essere passato in una chiamata successiva a [**lineUncompleteCall**](/windows/desktop/api/Tapi/nf-tapi-lineuncompletecall), la funzione avrà esito negativo con LINEERR \_ INVALCOMPLETIONID). Se un provider di servizi invia un messaggio di [**riga \_ LINEDEVSTATE**](line-linedevstate.md) contenente questo valore a TAPI, TAPI lo passerà a applicazioni con la versione 1,4 di TAPI negoziata o successiva. le applicazioni che negoziano una versione precedente dell'API non riceveranno alcuna notifica.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_CONNECTED"></span><span id="linedevstate_connected"></span>**LINEDEVSTATE \_ connesso**
</dt> <dd> <dl> <dt>



La riga è stata precedentemente disconnessa ed è ora connessa a TAPI.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_DEVSPECIFIC"></span><span id="linedevstate_devspecific"></span>**\_DEVSPECIFIC LINEDEVSTATE**
</dt> <dd> <dl> <dt>



Le informazioni specifiche del dispositivo della riga sono state modificate.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_DISCONNECTED"></span><span id="linedevstate_disconnected"></span>**LINEDEVSTATE \_ disconnesso**
</dt> <dd> <dl> <dt>



Questa riga è stata connessa in precedenza ed è ora disconnessa da TAPI.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_INSERVICE"></span><span id="linedevstate_inservice"></span>**LINEDEVSTATE \_ INservice**
</dt> <dd> <dl> <dt>



La linea è connessa a TAPI. Questo errore si verifica quando TAPI viene attivato per la prima volta o quando il cavo di linea è fisicamente collegato al compartmento e in-Service quando TAPI è attivo.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_LOCK"></span><span id="linedevstate_lock"></span>**\_blocco LINEDEVSTATE**
</dt> <dd> <dl> <dt>



Lo stato bloccato del dispositivo a linee è stato modificato. Per ulteriori informazioni, vedere LINEDEVSTATUSFLAGS \_ BLOCCATO nelle [**\_ costanti LINEDEVSTATUSFLAGS**](linedevstatusflags--constants.md).)


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_MAINTENANCE"></span><span id="linedevstate_maintenance"></span>**\_manutenzione LINEDEVSTATE**
</dt> <dd> <dl> <dt>



È in corso l'esecuzione della manutenzione sulla riga del Commuter. Non è possibile usare TAPI per operare sul dispositivo a linee.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_MSGWAITOFF"></span><span id="linedevstate_msgwaitoff"></span>**\_MSGWAITOFF LINEDEVSTATE**
</dt> <dd> <dl> <dt>



L'indicatore di attesa dei messaggi è disattivato.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_MSGWAITON"></span><span id="linedevstate_msgwaiton"></span>**\_MSGWAITON LINEDEVSTATE**
</dt> <dd> <dl> <dt>



L'indicatore di attesa dei messaggi è attivato.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_NUMCALLS"></span><span id="linedevstate_numcalls"></span>**\_NUMCALLS LINEDEVSTATE**
</dt> <dd> <dl> <dt>



Il numero di chiamate sul dispositivo a linee è stato modificato.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_NUMCOMPLETIONS"></span><span id="linedevstate_numcompletions"></span>**\_NUMCOMPLETIONS LINEDEVSTATE**
</dt> <dd> <dl> <dt>



Il numero di completamenti di chiamate in attesa sul dispositivo a linee è stato modificato.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_OPEN"></span><span id="linedevstate_open"></span>**LINEDEVSTATE \_ aperto**
</dt> <dd> <dl> <dt>



La riga è stata aperta da un'altra applicazione.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_OTHER"></span><span id="linedevstate_other"></span>**LINEDEVSTATE \_ altro**
</dt> <dd> <dl> <dt>



Gli elementi di stato del dispositivo diversi da quelli elencati di seguito sono stati modificati. L'applicazione deve controllare lo stato corrente del dispositivo per determinare quali elementi sono stati modificati.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_OUTOFSERVICE"></span><span id="linedevstate_outofservice"></span>**\_OUTOFSERVICE LINEDEVSTATE**
</dt> <dd> <dl> <dt>



La riga non è più in servizio al passaggio o fisicamente disconnessa. Non è possibile usare TAPI per operare sul dispositivo a linee.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_REINIT"></span><span id="linedevstate_reinit"></span>**LINEDEVSTATE \_ REinit**
</dt> <dd> <dl> <dt>



Gli elementi sono stati modificati nella configurazione dei dispositivi line. Per acquisire familiarità con queste modifiche (per quanto riguarda l'aspetto dei nuovi dispositivi linea), l'applicazione deve reinizializzare l'uso di TAPI.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_REMOVED"></span><span id="linedevstate_removed"></span>**LINEDEVSTATE \_ rimosso**
</dt> <dd> <dl> <dt>



Indica che il dispositivo è stato rimosso dal sistema dal provider di servizi (più probabile tramite l'azione dell'utente, tramite un pannello di controllo o un'utilità simile). Un messaggio di [**riga \_ LINEDEVSTATE**](line-linedevstate.md) con questo valore sarà in genere seguito immediatamente da un messaggio di [**\_ chiusura riga**](line-close.md) sul dispositivo. I tentativi successivi di accesso al dispositivo prima della reinizializzazione di TAPI comporteranno \_ la restituzione di LINEERR NODEVICE all'applicazione. Se un provider di servizi invia un messaggio di [**riga \_ LINEDEVSTATE**](line-linedevstate.md) contenente questo valore a TAPI, TAPI lo passerà a applicazioni con la versione 1,4 di TAPI negoziata o successiva. le applicazioni che negoziano una versione precedente dell'API non riceveranno alcuna notifica.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_RINGING"></span><span id="linedevstate_ringing"></span>**\_suoneria LINEDEVSTATE**
</dt> <dd> <dl> <dt>



L'opzione indica alla riga di avvisare l'utente.

**TAPI:** I provider di servizi inviano notifiche alle applicazioni in ogni ciclo circolare inviando ripetutamente messaggi di [**riga \_ LINEDEVSTATE**](line-linedevstate.md) contenenti questa costante. Nel Stati Uniti, ad esempio, i provider di servizi inviano un messaggio con questa costante ogni sei secondi.

**TSPI:** In un dispositivo POTS, il provider di servizi può inviare il messaggio ogni volta che l'ufficio centrale Invia la tensione di anello. Nei dispositivi digitali, ad esempio ISDN, il provider di servizi potrebbe dover sintetizzare la ripetizione del messaggio se il Commuter genera una sola richiesta ring. Ogni ripetizione del messaggio dovrebbe mostrare il numero di squilli in aumento, in modo che le funzioni di salvataggio a pedaggio funzionino correttamente.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_ROAMMODE"></span><span id="linedevstate_roammode"></span>**\_ROAMMODE LINEDEVSTATE**
</dt> <dd> <dl> <dt>



La modalità roaming del dispositivo a linee è cambiata.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_SIGNAL"></span><span id="linedevstate_signal"></span>**\_segnale LINEDEVSTATE**
</dt> <dd> <dl> <dt>



Il livello del segnale è stato modificato significativamente (cellulare).


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_TERMINALS"></span><span id="linedevstate_terminals"></span>**\_terminali LINEDEVSTATE**
</dt> <dd> <dl> <dt>



Le impostazioni del terminale sono state modificate. Questo può accadere, ad esempio, se più dispositivi linea condividono terminali tra di essi, ad esempio due righe che condividono un terminale telefonico.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_TRANSLATECHANGE"></span><span id="linedevstate_translatechange"></span>**\_TRANSLATECHANGE LINEDEVSTATE**
</dt> <dd> <dl> <dt>



Indica che, a causa delle modifiche di configurazione apportate dall'utente o altre circostanze, uno o più membri della struttura [**LINETRANSLATECAPS**](/windows/desktop/api/Tapi/ns-tapi-linetranslatecaps) sono stati modificati. Per leggere la struttura aggiornata, l'applicazione deve usare [**lineGetTranslateCaps**](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps) . Se un provider di servizi invia un messaggio di [**riga \_ LINEDEVSTATE**](line-linedevstate.md) contenente questo valore a TAPI, TAPI lo passerà a applicazioni che hanno negoziato la versione di TAPI 1,4 o versioni successive. le applicazioni che trattano una versione precedente di TAPI riceveranno i messaggi di **riga \_ LINEDEVSTATE** specificando LINEDEVSTATE \_ reinit, richiedendo di arrestare e reinizializzare la connessione a TAPI per ottenere le informazioni aggiornate.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

Nessuna estensibilità. Tutti i 32 bit sono riservati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2,0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_chiusura riga**](line-close.md)
</dt> <dt>

[**LINEA \_ LINEDEVSTATE**](line-linedevstate.md)
</dt> <dt>

[**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps)
</dt> <dt>

[**lineGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetdevcaps)
</dt> <dt>

[**lineGetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig)
</dt> <dt>

[**lineGetTranslateCaps**](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps)
</dt> <dt>

[**LINETRANSLATECAPS**](/windows/desktop/api/Tapi/ns-tapi-linetranslatecaps)
</dt> <dt>

[**lineUncompleteCall**](/windows/desktop/api/Tapi/nf-tapi-lineuncompletecall)
</dt> </dl>

 

 




