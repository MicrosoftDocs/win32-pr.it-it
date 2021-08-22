---
description: Le costanti del flag di bit LINEDISCONNECTMODE \_ descrivono diversi motivi per una richiesta di disconnessione remota. Una modalità di disconnessione è disponibile come stato della chiamata all'applicazione dopo la transizione dello stato della chiamata a disconnesso.
ms.assetid: 1b26f13c-b0bf-4d2c-8514-f0c376e36bcd
title: LINEDISCONNECTMODE_ costanti (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41ad56f993d746e5d09e33e4dcfb74d29766dd359fa47302053e0af13513a7da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119060669"
---
# <a name="linedisconnectmode_-constants"></a>Costanti \_ LINEDISCONNECTMODE

Le costanti del flag di bit **LINEDISCONNECTMODE \_** descrivono diversi motivi per una richiesta di disconnessione remota. Una modalità di disconnessione è disponibile come stato della chiamata all'applicazione dopo la transizione dello stato della chiamata a disconnesso.

<dl> <dt>

<span id="LINEDISCONNECTMODE_BADADDRESS"></span><span id="linedisconnectmode_badaddress"></span>**LINEDISCONNECTMODE \_ BADADDRESS**
</dt> <dd> <dl> <dt>



L'indirizzo di destinazione non è valido.


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_BLOCKED"></span><span id="linedisconnectmode_blocked"></span>**LINEDISCONNECTMODE \_ BLOCCATO**
</dt> <dd> <dl> <dt>



La chiamata non è stata connessa perché le chiamate dall'indirizzo di origine non vengono accettate all'indirizzo di destinazione. Questo comportamento è diverso da LINEDISCONNECTMODE REJECT perché il blocco viene implementato nella rete (rifiuto passivo) mentre un rifiuto viene implementato nell'apparecchiatura di destinazione \_ (rifiuto attivo). Il blocco può essere dovuto a un'esclusione specifica dell'indirizzo di origine o perché la destinazione accetta chiamate solo da un set selezionato di indirizzi di origine (gruppo di utenti chiuso). (TAPI versioni 2.0 e successive)

LINEDISCONNECTMODE \_ BLOCKED è appropriato come risposta in blocco. Ad esempio, un modem ha ricevuto una risposta, è passato più di sei secondi senza rilevare Ringback, non è riuscito a connettersi a un numero definito di volte, determina che il numero di telefono non è valido per la chiamata ed esegue una risposta "in blocco".


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_BUSY"></span><span id="linedisconnectmode_busy"></span>**LINEDISCONNECTMODE \_ OCCUPATO**
</dt> <dd> <dl> <dt>



La stazione dell'utente remoto è occupata.


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_CANCELLED"></span><span id="linedisconnectmode_cancelled"></span>**LINEDISCONNECTMODE \_ ANNULLATO**
</dt> <dd> <dl> <dt>



La chiamata è stata annullata. (TAPI versioni 2.0 e successive)


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_CONGESTION"></span><span id="linedisconnectmode_congestion"></span>**CONGESTIONE LINEDISCONNECTMODE \_**
</dt> <dd> <dl> <dt>



La rete è congestionata.


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_DONOTDISTURB"></span><span id="linedisconnectmode_donotdisturb"></span>**LINEDISCONNECTMODE \_ DONOTDISTURB**
</dt> <dd> <dl> <dt>



La chiamata non è stata connessa perché la destinazione ha richiamato la funzionalità Non disturbare. (TAPI versioni 2.0 e successive)


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_FORWARDED"></span><span id="linedisconnectmode_forwarded"></span>**LINEDISCONNECTMODE \_ INOLTRATO**
</dt> <dd> <dl> <dt>



La chiamata è stata inoltrata dall'opzione .


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_INCOMPATIBLE"></span><span id="linedisconnectmode_incompatible"></span>**LINEDISCONNECTMODE \_ INCOMPATIBILE**
</dt> <dd> <dl> <dt>



Le apparecchiature di stazione dell'utente remoto non sono compatibili con il tipo di chiamata richiesto.


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_NOANSWER"></span><span id="linedisconnectmode_noanswer"></span>**LINEDISCONNECTMODE \_ NOANSWER**
</dt> <dd> <dl> <dt>



La stazione dell'utente remoto non risponde.


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_NODIALTONE"></span><span id="linedisconnectmode_nodialtone"></span>**LINEDISCONNECTMODE \_ NODIALTONE**
</dt> <dd> <dl> <dt>



Non è stato rilevato un segnale acustico all'interno di un timeout definito dal provider di servizi, in un punto durante la composizione quando ne era previsto uno (ad esempio in una "W" nella stringa dialable). Ciò può verificarsi anche senza un periodo di timeout definito dal provider di servizi o senza un valore specificato nel membro **dwWaitForDialTone** della struttura [**LINEDIALPARAMS.**](/windows/desktop/api/Tapi/ns-tapi-linedialparams) (TAPI versioni 1.4 e successive)


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_NORMAL"></span><span id="linedisconnectmode_normal"></span>**LINEDISCONNECTMODE \_ NORMAL**
</dt> <dd> <dl> <dt>



Si tratta di una normale richiesta di disconnessione da parte dell'entità remota. La chiamata è stata terminata normalmente.


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_NUMBERCHANGED"></span><span id="linedisconnectmode_numberchanged"></span>**LINEDISCONNECTMODE \_ NUMBERCHANGED**
</dt> <dd> <dl> <dt>



La chiamata non è stata connessa perché il numero di destinazione è stato modificato, ma non viene fornito il reindirizzamento automatico al nuovo numero. (TAPI versioni 2.0 e successive)


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_OUTOFORDER"></span><span id="linedisconnectmode_outoforder"></span>**LINEDISCONNECTMODE \_ OUTOFORDER**
</dt> <dd> <dl> <dt>



La chiamata non è stata connessa o è stata disconnessa perché il dispositivo di destinazione non è in ordine (errore hardware). (TAPI versioni 2.0 e successive)


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_PICKUP"></span><span id="linedisconnectmode_pickup"></span>**RITIRO LINEDISCONNECTMODE \_**
</dt> <dd> <dl> <dt>



La chiamata è stata prelevata da un'altra posizione.


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_QOSUNAVAIL"></span><span id="linedisconnectmode_qosunavail"></span>**LINEDISCONNECTMODE \_ QOSUNAVAIL**
</dt> <dd> <dl> <dt>



La chiamata non è stata connessa o è stata disconnessa perché non è stato possibile ottenere o sostenere la qualità minima del servizio. Questo comportamento è diverso da LINEDISCONNECTMODE INCOMPATIBLE in base al fatto che la mancanza di risorse può essere una condizione \_ temporanea nella destinazione. (TAPI versioni 2.0 e successive)


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_REJECT"></span><span id="linedisconnectmode_reject"></span>**LINEDISCONNECTMODE \_ REJECT**
</dt> <dd> <dl> <dt>



L'utente remoto ha rifiutato la chiamata.


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_TEMPFAILURE"></span><span id="linedisconnectmode_tempfailure"></span>**LINEDISCONNECTMODE \_ TEMPFAILURE**
</dt> <dd> <dl> <dt>



La chiamata non è stata connessa o è stata disconnessa a causa di un errore temporaneo nella rete. La chiamata può essere tentata nuovamente in un secondo momento e dovrebbe essere completata. (TAPI versioni 2.0 e successive)

LINEDISCONNECTMODE \_ TEMPFAILURE è appropriato come risposta ritardata. Ad esempio, un modem che riceve un segnale occupato o un numero di volte equivalente in un determinato periodo di tempo conclude che il numero non deve essere chiamato di nuovo fino a quando non è trascorso un tempo definito e non elava una risposta "ritardata".


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_UNAVAIL"></span><span id="linedisconnectmode_unavail"></span>**LINEDISCONNECTMODE \_ UNAVAIL**
</dt> <dd> <dl> <dt>



Il motivo della disconnessione non è disponibile e non sarà noto in un secondo momento.


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_UNKNOWN"></span><span id="linedisconnectmode_unknown"></span>**LINEDISCONNECTMODE \_ UNKNOWN**
</dt> <dd> <dl> <dt>



Il motivo della richiesta di disconnessione è sconosciuto, ma potrebbe diventare noto in un secondo momento.


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_UNREACHABLE"></span><span id="linedisconnectmode_unreachable"></span>**LINEDISCONNECTMODE \_ NON RAGGIUNGIBILE**
</dt> <dd> <dl> <dt>



Impossibile raggiungere l'utente remoto.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

I 16 bit di ordine elevato possono essere assegnati per le estensioni specifiche del dispositivo. I 16 bit di ordine basso sono riservati.

Una richiesta di disconnessione remota per una determinata chiamata comporta la transizione dello stato della chiamata allo stato disconnesso e viene inviato un messaggio [**LINE \_ CALLSTATE**](line-callstate.md) all'applicazione. Le informazioni LINEDISCONNECTMODE \_ forniscono informazioni dettagliate sulla richiesta di disconnessione remota. È disponibile nella struttura [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) della chiamata quando la chiamata è nello stato disconnesso. Mentre una chiamata si trova in questo stato, l'applicazione può comunque eseguire query sulle informazioni e sullo stato della chiamata. Ad esempio, le informazioni utente-utente ricevute come parte della disconnessione remota sono quindi disponibili. L'applicazione può cancellare una chiamata disconnessa eliminando la chiamata.

Per la compatibilità con le versioni precedenti, è responsabilità del provider di servizi esaminare la versione dell'API negoziata nella riga e non usare questo valore LINEDISCONNECTMODE se non è supportato nella versione negoziata (è invece possibile usare \_ LINEDISCONNECTMODE NORMAL o \_ \_ UNKNOWN).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2.0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**LINE \_ CALLSTATE**](line-callstate.md)
</dt> <dt>

[**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus)
</dt> <dt>

[**LINEDIALPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linedialparams)
</dt> </dl>

 

 




