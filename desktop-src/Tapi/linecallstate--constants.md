---
description: Le \_ costanti del flag di bit LINECALLSTATE descrivono gli Stati di chiamata in cui può trovarsi una chiamata.
ms.assetid: 18d881ee-cf98-4dec-a561-333c2518935d
title: Costanti LINECALLSTATE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d50301dfeca49513a919fba90cc960c7ccb572d1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328906"
---
# <a name="linecallstate_-constants"></a>\_Costanti LINECALLSTATE

Le costanti del flag di bit **LINECALLSTATE \_** descrivono gli Stati di chiamata in cui può trovarsi una chiamata.

<dl> <dt>

<span id="LINECALLSTATE_ACCEPTED"></span><span id="linecallstate_accepted"></span>**LINECALLSTATE \_ accettata**
</dt> <dd> <dl> <dt>



La chiamata era nello stato dell'offerta ed è stata accettata. Ciò indica ad altre applicazioni (monitoraggio) che l'applicazione corrente del proprietario ha richiesto la responsabilità di rispondere alla chiamata. In ISDN lo stato accettato viene immesso quando l'apparecchiatura del gruppo chiamato Invia un messaggio all'opzione che indica che è disposto a presentare la chiamata alla persona chiamata. Questo ha l'effetto collaterale degli avvisi (squilli) degli utenti a entrambe le estremità della chiamata. Una chiamata in ingresso può sempre essere immediatamente soddisfatta senza prima essere accettata separatamente.


</dt> </dl> </dd> <dt>

<span id="LINECALLSTATE_BUSY"></span><span id="linecallstate_busy"></span>**LINECALLSTATE \_ occupato**
</dt> <dd> <dl> <dt>



La chiamata sta ricevendo un tono occupato. Un tono occupato indica che non è possibile completare la chiamata, ovvero un circuito (trunk) o la stazione della parte remota è in uso. Vedere [**\_ costanti LINEBUSYMODE**](linebusymode--constants.md).


</dt> </dl> </dd> <dt>

<span id="LINECALLSTATE_CONFERENCED"></span><span id="linecallstate_conferenced"></span>**LINECALLSTATE \_ conferenced**
</dt> <dd> <dl> <dt>



La chiamata è un membro di una chiamata di conferenza ed è logicamente nello stato connesso.


</dt> </dl> </dd> <dt>

<span id="LINECALLSTATE_CONNECTED"></span><span id="linecallstate_connected"></span>**LINECALLSTATE \_ connesso**
</dt> <dd> <dl> <dt>



La chiamata è stata stabilita e viene effettuata la connessione. Le informazioni sono in grado di attraversare la chiamata tra l'indirizzo di origine e l'indirizzo di destinazione.


</dt> </dl> </dd> <dt>

<span id="LINECALLSTATE_DIALING"></span><span id="linecallstate_dialing"></span>**\_composizione LINECALLSTATE**
</dt> <dd> <dl> <dt>



Il creatore sta digitando cifre sulla chiamata. Le cifre componete vengono raccolte dall'opzione. Si noti che né [**lineGenerateDigits**](/windows/desktop/api/Tapi/nf-tapi-linegeneratedigits) né [**TSPI \_ lineGenerateDigits**](/windows/win32/api/tspi/nf-tspi-tspi_linegeneratedigits) la riga viene posizionata nello stato di composizione.


</dt> </dl> </dd> <dt>

<span id="LINECALLSTATE_DIALTONE"></span><span id="linecallstate_dialtone"></span>**LINECALLSTATE \_ DIaltone**
</dt> <dd> <dl> <dt>



La chiamata riceve un tono di connessione dall'opzione, il che significa che l'opzione è pronta a ricevere un numero composto. Vedere [**\_ costanti LINEDIALTONEMODE**](linedialtonemode--constants.md) per gli identificatori dei toni di composizione speciali, ad esempio un tono di balbuzie della posta vocale normale.


</dt> </dl> </dd> <dt>

<span id="LINECALLSTATE_DISCONNECTED"></span><span id="linecallstate_disconnected"></span>**LINECALLSTATE \_ disconnesso**
</dt> <dd> <dl> <dt>



La parte remota è stata disconnessa dalla chiamata.


</dt> </dl> </dd> <dt>

<span id="LINECALLSTATE_IDLE"></span><span id="linecallstate_idle"></span>**LINECALLSTATE \_ inattivo**
</dt> <dd> <dl> <dt>



La chiamata esiste ma non è stata connessa. Non esiste alcuna attività nella chiamata, il che significa che nessuna chiamata è attualmente attiva. Una chiamata non può mai eseguire la transizione fuori dallo stato di inattività.


</dt> </dl> </dd> <dt>

<span id="LINECALLSTATE_OFFERING"></span><span id="linecallstate_offering"></span>**\_offerta LINECALLSTATE**
</dt> <dd> <dl> <dt>



La chiamata viene offerta alla stazione, segnalando l'arrivo di una nuova chiamata. Lo stato dell'offerta non è uguale a quello di un telefono o un computer a squillare. In alcuni ambienti, una chiamata nello stato dell'offerta non squilla l'utente fino a quando l'opzione non indica alla riga di squillare. Un esempio di utilizzo potrebbe essere la posizione in cui viene visualizzata una chiamata in ingresso su diversi set di stazioni, ma solo gli anelli di indirizzi primari. L'istruzione da squillare non influisce su alcuno stato di chiamata.


</dt> </dl> </dd> <dt>

<span id="LINECALLSTATE_ONHOLD"></span><span id="linecallstate_onhold"></span>**LINECALLSTATE \_ ONholding**
</dt> <dd> <dl> <dt>



La chiamata è in attesa dall'opzione. In questo modo viene liberata la riga fisica, che consente a un'altra chiamata di utilizzare la riga.


</dt> </dl> </dd> <dt>

<span id="LINECALLSTATE_ONHOLDPENDCONF"></span><span id="linecallstate_onholdpendconf"></span>**\_ONHOLDPENDCONF LINECALLSTATE**
</dt> <dd> <dl> <dt>



La chiamata è attualmente in attesa mentre viene aggiunta a una conferenza.


</dt> </dl> </dd> <dt>

<span id="LINECALLSTATE_ONHOLDPENDTRANSFER"></span><span id="linecallstate_onholdpendtransfer"></span>**\_ONHOLDPENDTRANSFER LINECALLSTATE**
</dt> <dd> <dl> <dt>



La chiamata è attualmente in attesa di trasferimento a un altro numero.


</dt> </dl> </dd> <dt>

<span id="LINECALLSTATE_PROCEEDING"></span><span id="linecallstate_proceeding"></span>**proseguimento di LINECALLSTATE \_**
</dt> <dd> <dl> <dt>



La composizione è stata completata e la chiamata sta procedendo attraverso il Commuter o la rete telefonica. Questo errore si verifica dopo il completamento della connessione e prima che la chiamata raggiunga la parte di composizione, come indicato da riponderone, occupato o risposta.


</dt> </dl> </dd> <dt>

<span id="LINECALLSTATE_RINGBACK"></span><span id="linecallstate_ringback"></span>**LINECALLSTATE \_ risponder**
</dt> <dd> <dl> <dt>



È stata raggiunta la stazione da chiamare e l'opzione della destinazione sta generando un tono di chiamata all'origine. Una  richiamata indica che l'indirizzo di destinazione viene avvisato della chiamata.


</dt> </dl> </dd> <dt>

<span id="LINECALLSTATE_SPECIALINFO"></span><span id="linecallstate_specialinfo"></span>**\_SPECIALINFO LINECALLSTATE**
</dt> <dd> <dl> <dt>



La chiamata riceve un segnale di informazione speciale, che precede un annuncio preregistrato che indica il motivo per cui non è possibile completare una chiamata. Vedere [**\_ costanti LINESPECIALINFO**](linespecialinfo--constants.md).


</dt> </dl> </dd> <dt>

<span id="LINECALLSTATE_UNKNOWN"></span><span id="linecallstate_unknown"></span>**LINECALLSTATE \_ sconosciuto**
</dt> <dd> <dl> <dt>



La chiamata esiste, ma il suo stato è attualmente sconosciuto. Questo potrebbe essere il risultato del rilevamento di stato di chiamata scadente da parte del provider di servizi. Un messaggio di stato di chiamata con lo stato della chiamata impostato su Unknown può essere generato anche per informare la DLL TAPI su una nuova chiamata in un momento in cui lo stato di chiamata effettivo della chiamata non è esattamente noto.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

Gli 8 bit più significativi possono definire uno stato sottostato specifico del dispositivo di uno degli stati predefiniti, a condizione che \_ venga impostato anche uno dei bit LINECALLSTATE definiti sopra. I 24 bit di ordine inferiore sono riservati per gli stati predefiniti.

Le **\_ costanti LINECALLSTATE** vengono utilizzate come parametri dal messaggio di [**riga \_ CALLSTATE**](line-callstate.md) inviato all'applicazione. Il messaggio contiene il nuovo stato di chiamata a cui è stata effettuata la transizione della chiamata. Queste costanti vengono usate anche come membri nella struttura [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) restituita dalla funzione [**lineGetCallStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetcallstatus) .

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

[**lineGenerateDigits**](/windows/desktop/api/Tapi/nf-tapi-linegeneratedigits)
</dt> <dt>

[**lineGetCallStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetcallstatus)
</dt> </dl>

 

