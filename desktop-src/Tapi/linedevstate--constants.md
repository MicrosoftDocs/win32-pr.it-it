---
description: Le costanti del flag di bit LINEDEVSTATE \_ descrivono vari eventi di stato della riga.
ms.assetid: 41e8a777-a57a-4d6c-850f-e21b58081b0d
title: LINEDEVSTATE_ costanti (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb11959614999ff50e421e0b77c63d1215a831040774e3123b43aa3534a3f853
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140064"
---
# <a name="linedevstate_-constants"></a>Costanti \_ LINEDEVSTATE

Le costanti del flag di bit **LINEDEVSTATE \_** descrivono vari eventi di stato della riga.

<dl> <dt>

<span id="LINEDEVSTATE_BATTERY"></span><span id="linedevstate_battery"></span>**BATTERIA \_ LINEDEVSTATE**
</dt> <dd> <dl> <dt>



Il livello della batteria è cambiato in modo significativo (cellulare).


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_CAPSCHANGE"></span><span id="linedevstate_capschange"></span>**LINEDEVSTATE \_ CAPSCHANGE**
</dt> <dd> <dl> <dt>



Indica che, a causa delle modifiche di configurazione apportate dall'utente o in altre circostanze, uno o più membri nella struttura [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) per l'indirizzo sono stati modificati. L'applicazione deve [**usare lineGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetdevcaps) per leggere la struttura aggiornata. Se un provider di servizi invia un messaggio [**LINE \_ LINEDEVSTATE**](line-linedevstate.md) contenente questo valore a TAPI, TAPI lo passerà alle applicazioni che hanno negoziato TAPI versione 1.4 o successiva. Le applicazioni che negoziano una versione TAPI precedente riceveranno messaggi **LINE \_ LINEDEVSTATE** che specificano LINEDEVSTATE REINIT, richiedendo loro di arrestare e reinizializzare la connessione a TAPI per ottenere le informazioni \_ aggiornate.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_CLOSE"></span><span id="linedevstate_close"></span>**LINEDEVSTATE \_ CLOSE**
</dt> <dd> <dl> <dt>



La riga è stata chiusa da un'altra applicazione.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_CONFIGCHANGE"></span><span id="linedevstate_configchange"></span>**LINEDEVSTATE \_ CONFIGCHANGE**
</dt> <dd> <dl> <dt>



Indica che sono state apportate modifiche alla configurazione a uno o più dispositivi multimediali associati al dispositivo line. L'applicazione, se lo desidera, può usare [**lineGetDevConfig per**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig) leggere le informazioni aggiornate. Se un provider di servizi invia un messaggio [**LINE \_ LINEDEVSTATE**](line-linedevstate.md) contenente questo valore a TAPI, TAPI lo passerà alle applicazioni che hanno negoziato TAPI versione 1.4 o successiva. Le applicazioni che negoziano una versione precedente dell'API non riceveranno alcuna notifica.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_COMPLCANCEL"></span><span id="linedevstate_complcancel"></span>**LINEDEVSTATE \_ COMPLCANCEL**
</dt> <dd> <dl> <dt>



Indica che il completamento della chiamata identificato dall'identificatore di completamento contenuto nel *parametro dwParam2* del messaggio [**\_ LINEDEVSTATE**](line-linedevstate.md) è stato annullato esternamente e non è più considerato valido (se tale valore deve essere passato in una chiamata successiva a [**lineUncompleteCall**](/windows/desktop/api/Tapi/nf-tapi-lineuncompletecall), la funzione avrà esito negativo con LINEERR \_ INVALCOMPLETIONID). Se un provider di servizi invia un messaggio [**LINE \_ LINEDEVSTATE**](line-linedevstate.md) contenente questo valore a TAPI, TAPI lo passerà alle applicazioni che hanno negoziato TAPI versione 1.4 o successiva. Le applicazioni che negoziano una versione precedente dell'API non riceveranno alcuna notifica.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_CONNECTED"></span><span id="linedevstate_connected"></span>**LINEDEVSTATE \_ CONNESSO**
</dt> <dd> <dl> <dt>



La riga era precedentemente disconnessa ed è ora connessa a TAPI.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_DEVSPECIFIC"></span><span id="linedevstate_devspecific"></span>**LINEDEVSTATE \_ DEVSPECIFIC**
</dt> <dd> <dl> <dt>



Le informazioni specifiche del dispositivo della riga sono state modificate.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_DISCONNECTED"></span><span id="linedevstate_disconnected"></span>**LINEDEVSTATE \_ DISCONNESSO**
</dt> <dd> <dl> <dt>



Questa linea era precedentemente connessa ed è ora disconnessa da TAPI.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_INSERVICE"></span><span id="linedevstate_inservice"></span>**LINEDEVSTATE \_ INSERVICE**
</dt> <dd> <dl> <dt>



La linea è connessa a TAPI. Ciò si verifica quando TAPI viene attivato per la prima volta o quando il cavo di linea è fisicamente collegato e in servizio al commutatore mentre TAPI è attivo.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_LOCK"></span><span id="linedevstate_lock"></span>**BLOCCO \_ LINEDEVSTATE**
</dt> <dd> <dl> <dt>



Lo stato bloccato del dispositivo line è stato modificato. Per altre informazioni, vedere LINEDEVSTATUSFLAGS \_ Costanti LOCKED in [**LINEDEVSTATUSFLAGS \_**](linedevstatusflags--constants.md).


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_MAINTENANCE"></span><span id="linedevstate_maintenance"></span>**MANUTENZIONE \_ LINEDEVSTATE**
</dt> <dd> <dl> <dt>



La manutenzione viene eseguita sulla riga all'interruttore. Non è possibile usare TAPI per operare sul dispositivo line.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_MSGWAITOFF"></span><span id="linedevstate_msgwaitoff"></span>**LINEDEVSTATE \_ MSGWAITOFF**
</dt> <dd> <dl> <dt>



L'indicatore di attesa del messaggio è disattivato.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_MSGWAITON"></span><span id="linedevstate_msgwaiton"></span>**LINEDEVSTATE \_ MSGWAITON**
</dt> <dd> <dl> <dt>



L'indicatore di attesa del messaggio è attivato.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_NUMCALLS"></span><span id="linedevstate_numcalls"></span>**LINEDEVSTATE \_ NUMCALLS**
</dt> <dd> <dl> <dt>



Il numero di chiamate sul dispositivo line è stato modificato.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_NUMCOMPLETIONS"></span><span id="linedevstate_numcompletions"></span>**LINEDEVSTATE \_ NUMCOMPLETIONS**
</dt> <dd> <dl> <dt>



Il numero di completamenti di chiamata in sospeso nel dispositivo a linee è stato modificato.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_OPEN"></span><span id="linedevstate_open"></span>**LINEDEVSTATE \_ OPEN**
</dt> <dd> <dl> <dt>



La riga è stata aperta da un'altra applicazione.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_OTHER"></span><span id="linedevstate_other"></span>**LINEDEVSTATE \_ OTHER**
</dt> <dd> <dl> <dt>



Gli elementi di stato del dispositivo diversi da quelli elencati di seguito sono stati modificati. L'applicazione deve controllare lo stato corrente del dispositivo per determinare quali elementi sono stati modificati.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_OUTOFSERVICE"></span><span id="linedevstate_outofservice"></span>**LINEDEVSTATE \_ OUTOFSERVICE**
</dt> <dd> <dl> <dt>



La linea è fuori servizio al commutatore o fisicamente disconnessa. Non è possibile usare TAPI per operare sul dispositivo line.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_REINIT"></span><span id="linedevstate_reinit"></span>**LINEDEVSTATE \_ REINIT**
</dt> <dd> <dl> <dt>



Gli elementi sono stati modificati nella configurazione dei dispositivi line. Per essere a conoscenza di queste modifiche (come per l'aspetto dei dispositivi di nuova riga), l'applicazione deve reinizializzare l'uso di TAPI.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_REMOVED"></span><span id="linedevstate_removed"></span>**LINEDEVSTATE \_ RIMOSSO**
</dt> <dd> <dl> <dt>



Indica che il dispositivo viene rimosso dal sistema dal provider di servizi (molto probabilmente tramite un'azione dell'utente, tramite un pannello di controllo o un'utilità simile). Un [**messaggio \_ LINE LINEDEVSTATE**](line-linedevstate.md) con questo valore verrà in genere seguito immediatamente da un messaggio [**LINE \_ CLOSE**](line-close.md) nel dispositivo. I successivi tentativi di accesso al dispositivo prima della reinizializzazione di TAPI comportano la restituire LINEERR \_ NODEVICE all'applicazione. Se un provider di servizi invia un messaggio [**LINE \_ LINEDEVSTATE**](line-linedevstate.md) contenente questo valore a TAPI, TAPI lo passerà alle applicazioni che hanno negoziato TAPI versione 1.4 o successiva. Le applicazioni che negoziano una versione precedente dell'API non riceveranno alcuna notifica.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_RINGING"></span><span id="linedevstate_ringing"></span>**LINEDEVSTATE \_ RINGING**
</dt> <dd> <dl> <dt>



L'opzione indica alla riga di avvisare l'utente.

**TAPI:** I provider di servizi inviano notifiche alle applicazioni in ogni ciclo circolare inviando ripetutamente [**messaggi LINE \_ LINEDEVSTATE**](line-linedevstate.md) contenenti questa costante. Ad esempio, nel Stati Uniti, i provider di servizi inviano un messaggio con questa costante ogni sei secondi.

**TSPI:** In un dispositivo POTS, il provider di servizi può inviare il messaggio ogni volta che l'ufficio centrale invia la tensione dell'anello. Nei dispositivi digitali, ad esempio ISDN, il provider di servizi potrebbe dover sintetizzare la ripetizione del messaggio se il commutatore genera una sola richiesta ring. Ogni ripetizione del messaggio dovrebbe mostrare l'aumento del numero di anelli, in modo che le funzioni di salvataggio del pedaggio funzionino correttamente.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_ROAMMODE"></span><span id="linedevstate_roammode"></span>**LINEDEVSTATE \_ ROAMMODE**
</dt> <dd> <dl> <dt>



La modalità di roaming del dispositivo line è stata modificata.


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_SIGNAL"></span><span id="linedevstate_signal"></span>**SEGNALE \_ LINEDEVSTATE**
</dt> <dd> <dl> <dt>



Il livello del segnale è cambiato in modo significativo (cellulare).


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_TERMINALS"></span><span id="linedevstate_terminals"></span>**\_TERMINALI LINEDEVSTATE**
</dt> <dd> <dl> <dt>



Le impostazioni del terminale sono state modificate. Ciò può verificarsi, ad esempio, se più dispositivi line condividono terminali tra di essi (ad esempio, due linee che condividono un terminale telefonico).


</dt> </dl> </dd> <dt>

<span id="LINEDEVSTATE_TRANSLATECHANGE"></span><span id="linedevstate_translatechange"></span>**LINEDEVSTATE \_ TRANSLATECHANGE**
</dt> <dd> <dl> <dt>



Indica che, a causa delle modifiche di configurazione apportate dall'utente o in altre circostanze, uno o più membri nella struttura [**LINETRANSLATECAPS**](/windows/desktop/api/Tapi/ns-tapi-linetranslatecaps) sono stati modificati. L'applicazione deve [**usare lineGetTranslateCaps**](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps) per leggere la struttura aggiornata. Se un provider di servizi invia un messaggio [**LINE \_ LINEDEVSTATE**](line-linedevstate.md) contenente questo valore a TAPI, TAPI lo passerà alle applicazioni che hanno negoziato TAPI versione 1.4 o successiva. Le applicazioni che negoziano una versione TAPI precedente riceveranno messaggi **LINE \_ LINEDEVSTATE** che specificano LINEDEVSTATE REINIT, richiedendo loro di arrestare e reinizializzare la connessione a TAPI per ottenere le informazioni \_ aggiornate.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

Nessuna estendibilità. Tutti i 32 bit sono riservati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2.0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CHIUSURA \_ RIGA**](line-close.md)
</dt> <dt>

[**LINE \_ LINEDEVSTATE**](line-linedevstate.md)
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

 

 




