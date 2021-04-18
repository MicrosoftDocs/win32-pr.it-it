---
description: Le \_ costanti del flag di bit LINEDISCONNECTMODE descrivono motivi diversi per una richiesta di disconnessione remota. Una modalità di disconnessione è disponibile come stato della chiamata all'applicazione dopo la transizione dello stato della chiamata a disconnected.
ms.assetid: 1b26f13c-b0bf-4d2c-8514-f0c376e36bcd
title: Costanti LINEDISCONNECTMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c70ba70175685e2c264343f9345227ee64c206f4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331778"
---
# <a name="linedisconnectmode_-constants"></a>\_Costanti LINEDISCONNECTMODE

Le costanti del flag di bit **LINEDISCONNECTMODE \_** descrivono motivi diversi per una richiesta di disconnessione remota. Una modalità di disconnessione è disponibile come stato della chiamata all'applicazione dopo la transizione dello stato della chiamata a disconnected.

<dl> <dt>

<span id="LINEDISCONNECTMODE_BADADDRESS"></span><span id="linedisconnectmode_badaddress"></span>**\_BADADDRESS LINEDISCONNECTMODE**
</dt> <dd> <dl> <dt>



L'indirizzo di destinazione non è valido.


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_BLOCKED"></span><span id="linedisconnectmode_blocked"></span>**LINEDISCONNECTMODE \_ bloccati**
</dt> <dd> <dl> <dt>



Impossibile connettere la chiamata poiché le chiamate dall'indirizzo di origine non vengono accettate nell'indirizzo di destinazione. Questo comportamento è diverso da quello di LINEDISCONNECTMODE, \_ in quanto il blocco viene implementato nella rete (un rifiuto passivo), mentre un rifiuto viene implementato nell'attrezzatura di destinazione (rifiuto attivo). Il blocco può essere causato da un'esclusione specifica dell'indirizzo di origine o dal fatto che la destinazione accetta chiamate solo da un set di indirizzi di origine (gruppo di utenti chiusi) selezionato. (Versioni TAPI 2,0 e successive)

Il \_ blocco LINEDISCONNECTMODE è appropriato come risposta Blocklisting. Ad esempio, un modem ha ricevuto una risposta, più di sei secondi senza rilevare la rilevanza, non è stato possibile connettere un numero definito di volte, determina che il numero di telefono non è valido per la chiamata ed emette una risposta "Blocklisting".


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_BUSY"></span><span id="linedisconnectmode_busy"></span>**LINEDISCONNECTMODE \_ occupato**
</dt> <dd> <dl> <dt>



La stazione dell'utente remoto è occupata.


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_CANCELLED"></span><span id="linedisconnectmode_cancelled"></span>**LINEDISCONNECTMODE \_ annullato**
</dt> <dd> <dl> <dt>



La chiamata è stata annullata. (Versioni TAPI 2,0 e successive)


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_CONGESTION"></span><span id="linedisconnectmode_congestion"></span>**congestione LINEDISCONNECTMODE \_**
</dt> <dd> <dl> <dt>



La rete è congestionata.


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_DONOTDISTURB"></span><span id="linedisconnectmode_donotdisturb"></span>**\_DONOTDISTURB LINEDISCONNECTMODE**
</dt> <dd> <dl> <dt>



Impossibile connettere la chiamata perché la destinazione ha richiamato la funzionalità non disturbare. (Versioni TAPI 2,0 e successive)


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_FORWARDED"></span><span id="linedisconnectmode_forwarded"></span>**LINEDISCONNECTMODE di \_ trasmissione**
</dt> <dd> <dl> <dt>



La chiamata è stata trasmessa dall'opzione.


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_INCOMPATIBLE"></span><span id="linedisconnectmode_incompatible"></span>**LINEDISCONNECTMODE \_ INcompatibile**
</dt> <dd> <dl> <dt>



L'apparecchiatura della stazione dell'utente remoto non è compatibile con il tipo di chiamata richiesta.


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_NOANSWER"></span><span id="linedisconnectmode_noanswer"></span>**LINEDISCONNECTMODE \_ NOanswer**
</dt> <dd> <dl> <dt>



La stazione dell'utente remoto non risponde.


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_NODIALTONE"></span><span id="linedisconnectmode_nodialtone"></span>**\_NODIALTONE LINEDISCONNECTMODE**
</dt> <dd> <dl> <dt>



Un tono di composizione non è stato rilevato all'interno di un timeout definito dal provider di servizi, in un determinato momento durante la composizione quando ne era previsto uno (ad esempio, "W" nella stringa di connessione remota). Questo può verificarsi anche senza un periodo di timeout definito dal provider di servizi o senza un valore specificato nel membro **dwWaitForDialTone** della struttura [**LINEDIALPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linedialparams) . (Versioni TAPI 1,4 e successive)


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_NORMAL"></span><span id="linedisconnectmode_normal"></span>**LINEDISCONNECTMODE \_ normale**
</dt> <dd> <dl> <dt>



Si tratta di una normale richiesta di disconnessione da parte della parte remota. La chiamata è stata terminata normalmente.


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_NUMBERCHANGED"></span><span id="linedisconnectmode_numberchanged"></span>**\_NUMBERCHANGED LINEDISCONNECTMODE**
</dt> <dd> <dl> <dt>



Non è stato possibile connettere la chiamata perché il numero di destinazione è stato modificato, ma non è stato specificato il reindirizzamento automatico al nuovo numero. (Versioni TAPI 2,0 e successive)


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_OUTOFORDER"></span><span id="linedisconnectmode_outoforder"></span>**\_OUTOFORDER LINEDISCONNECTMODE**
</dt> <dd> <dl> <dt>



La chiamata non è stata connessa o è stata disconnessa perché il dispositivo di destinazione non è in ordine (errore hardware). (Versioni TAPI 2,0 e successive)


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_PICKUP"></span><span id="linedisconnectmode_pickup"></span>**LINEDISCONNECTMODE \_ pickup**
</dt> <dd> <dl> <dt>



La chiamata è stata prelevata da un'altra posizione.


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_QOSUNAVAIL"></span><span id="linedisconnectmode_qosunavail"></span>**\_QOSUNAVAIL LINEDISCONNECTMODE**
</dt> <dd> <dl> <dt>



Non è stato possibile connettere la chiamata o è stata disconnessa perché non è stato possibile ottenere o sostenere la qualità del servizio minima. Questo comportamento è diverso da LINEDISCONNECTMODE \_ incompatibile perché la mancanza di risorse può essere una condizione temporanea nella destinazione. (Versioni TAPI 2,0 e successive)


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_REJECT"></span><span id="linedisconnectmode_reject"></span>**LINEDISCONNECTMODE \_ rifiuta**
</dt> <dd> <dl> <dt>



La chiamata è stata rifiutata dall'utente remoto.


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_TEMPFAILURE"></span><span id="linedisconnectmode_tempfailure"></span>**\_TEMPFAILURE LINEDISCONNECTMODE**
</dt> <dd> <dl> <dt>



Non è stato possibile connettere la chiamata o è stata disconnessa a causa di un errore temporaneo nella rete. la chiamata può essere ritentata in un secondo momento ed è prevista la fine del completamento. (Versioni TAPI 2,0 e successive)

LINEDISCONNECTMODE \_ TEMPFAILURE è appropriato come risposta ritardata. Ad esempio, un modem che riceve un segnale occupato o equivalente troppe volte in un determinato periodo di tempo conclude che il numero non deve essere chiamato di nuovo fino a quando non è trascorso un periodo definito e genera una risposta "ritardata".


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_UNAVAIL"></span><span id="linedisconnectmode_unavail"></span>**LINEDISCONNECTMODE non \_ disponibile**
</dt> <dd> <dl> <dt>



Il motivo della disconnessione non è disponibile e non verrà più noto in seguito.


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_UNKNOWN"></span><span id="linedisconnectmode_unknown"></span>**LINEDISCONNECTMODE \_ sconosciuto**
</dt> <dd> <dl> <dt>



Il motivo della richiesta di disconnessione è sconosciuto, ma potrebbe essere noto in seguito.


</dt> </dl> </dd> <dt>

<span id="LINEDISCONNECTMODE_UNREACHABLE"></span><span id="linedisconnectmode_unreachable"></span>**LINEDISCONNECTMODE \_ irraggiungibile**
</dt> <dd> <dl> <dt>



Non è stato possibile raggiungere l'utente remoto.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

È possibile assegnare i 16 bit più significativi per le estensioni specifiche del dispositivo. I 16 bit di ordine inferiore sono riservati.

Una richiesta di disconnessione remota per una determinata chiamata determina la transizione dello stato della chiamata allo stato disconnesso e all'applicazione viene inviato un messaggio di [**riga \_ CALLSTATE**](line-callstate.md) . Le \_ informazioni LINEDISCONNECTMODE forniscono informazioni dettagliate sulla richiesta di disconnessione remota. È disponibile nella struttura [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) della chiamata quando la chiamata è nello stato disconnected. Mentre una chiamata si trova in questo stato, l'applicazione può comunque eseguire query sulle informazioni e sullo stato della chiamata. Ad esempio, le informazioni utente utente ricevute come parte della disconnessione remota sono disponibili. L'applicazione può cancellare una chiamata disconnessa eliminando la chiamata.

Per compatibilità con le versioni precedenti, è responsabilità del provider di servizi esaminare la versione dell'API negoziata sulla riga e non usare questo \_ valore LINEDISCONNECTMODE se non è supportato nella versione negoziata (in alternativa, è possibile usare LINEDISCONNECTMODE \_ Normal o \_ Unknown).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2,0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**LINEA \_ CALLSTATE**](line-callstate.md)
</dt> <dt>

[**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus)
</dt> <dt>

[**LINEDIALPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linedialparams)
</dt> </dl>

 

 




