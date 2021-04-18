---
description: Le \_ costanti del flag di bit LINECALLREASON descrivono il motivo di una chiamata.
ms.assetid: 16278146-886f-433a-afe5-64f4894b1428
title: Costanti LINECALLREASON_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab6d2411c652c13add1620ca6029cabbf2b878e6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324879"
---
# <a name="linecallreason_-constants"></a>\_Costanti LINECALLREASON

Le costanti del flag di bit **LINECALLREASON \_** descrivono il motivo di una chiamata.

<dl> <dt>

<span id="LINECALLREASON_CALLCOMPLETION"></span><span id="linecallreason_callcompletion"></span>**\_CALLCOMPLETION LINECALLREASON**
</dt> <dd> <dl> <dt>



La chiamata è stata il risultato di una richiesta di completamento della chiamata.


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_CAMPEDON"></span><span id="linecallreason_campedon"></span>**\_CAMPEDON LINECALLREASON**
</dt> <dd> <dl> <dt>



La chiamata è stata campata sull'indirizzo. Generalmente, viene visualizzato inizialmente nello stato onHolding e può essere passato all'uso di [**lineSwapHold**](/windows/desktop/api/Tapi/nf-tapi-lineswaphold). Se una chiamata attiva diventa inattiva, la chiamata camped-on può variare in base allo stato dell'offerta e il dispositivo inizia a squillare.


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_DIRECT"></span><span id="linecallreason_direct"></span>**LINECALLREASON \_ Direct**
</dt> <dd> <dl> <dt>



Si tratta di una chiamata diretta in ingresso o in uscita.


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_FWDBUSY"></span><span id="linecallreason_fwdbusy"></span>**\_FWDBUSY LINECALLREASON**
</dt> <dd> <dl> <dt>



Questa chiamata è stata trasmessa da un'altra estensione occupata al momento della chiamata.


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_FWDNOANSWER"></span><span id="linecallreason_fwdnoanswer"></span>**\_FWDNOANSWER LINECALLREASON**
</dt> <dd> <dl> <dt>



La chiamata è stata trasmessa da un'altra estensione che non ha risposto alla chiamata dopo un certo numero di anelli.


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_FWDUNCOND"></span><span id="linecallreason_fwduncond"></span>**\_FWDUNCOND LINECALLREASON**
</dt> <dd> <dl> <dt>



La chiamata è stata trasmessa in modo incondizionato da un altro numero.


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_INTRUDE"></span><span id="linecallreason_intrude"></span>**LINECALLREASON \_ intrusione**
</dt> <dd> <dl> <dt>



Chiamata interstata sulla riga, da un'azione di completamento della chiamata richiamata da un'altra stazione o da un'azione dell'operatore. A seconda dell'implementazione del Commuter, è possibile che la chiamata venga visualizzata nello stato connesso o in conferenza con una chiamata attiva esistente sulla riga.


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_PARKED"></span><span id="linecallreason_parked"></span>**LINECALLREASON \_ parcheggiata**
</dt> <dd> <dl> <dt>



La chiamata è stata parcheggiata sull'indirizzo. Viene in genere visualizzato inizialmente nello stato onHolding.


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_PICKUP"></span><span id="linecallreason_pickup"></span>**LINECALLREASON \_ pickup**
</dt> <dd> <dl> <dt>



La chiamata è stata rilevata da un'altra estensione.


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_REDIRECT"></span><span id="linecallreason_redirect"></span>**\_Reindirizzamento LINECALLREASON**
</dt> <dd> <dl> <dt>



La chiamata è stata reindirizzata a questa stazione.


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_REMINDER"></span><span id="linecallreason_reminder"></span>**promemoria LINECALLREASON \_**
</dt> <dd> <dl> <dt>



La chiamata è un promemoria (o "richiamo") per cui l'utente ha una chiamata parcheggiata o in attesa (potenzialmente) per un lungo periodo di tempo.


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_ROUTEREQUEST"></span><span id="linecallreason_routerequest"></span>**\_ROUTEREQUEST LINECALLREASON**
</dt> <dd> <dl> <dt>



La chiamata viene visualizzata sull'indirizzo perché per il commute sono necessarie istruzioni di routing dall'applicazione. L'applicazione deve esaminare il membro **CalledID** in [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo)e utilizzare la funzione [**lineRedirect**](/windows/desktop/api/Tapi/nf-tapi-lineredirect) per fornire un nuovo indirizzo di connessione per la chiamata. Se invece la chiamata deve essere bloccata, l'applicazione può chiamare [**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop). Se l'applicazione non riesce a eseguire un'azione all'interno di un periodo di timeout definito dallo switch, viene eseguita un'azione predefinita. Un provider di servizi può usare questa costante solo se la versione negoziata nella riga è 2,0 o successiva. In caso contrario, il provider di servizi deve sostituire LINECALLREASON \_ undisp.


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_TRANSFER"></span><span id="linecallreason_transfer"></span>**\_trasferimento LINECALLREASON**
</dt> <dd> <dl> <dt>



La chiamata è stata trasferita da un altro numero.


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_UNAVAIL"></span><span id="linecallreason_unavail"></span>**LINECALLREASON non \_ disponibile**
</dt> <dd> <dl> <dt>



Il motivo della chiamata non è disponibile e non verrà più noto in seguito.


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_UNKNOWN"></span><span id="linecallreason_unknown"></span>**LINECALLREASON \_ sconosciuto**
</dt> <dd> <dl> <dt>



Il motivo della chiamata è attualmente sconosciuto, ma può diventare noto in un secondo momento.


</dt> </dl> </dd> <dt>

<span id="LINECALLREASON_UNPARK"></span><span id="linecallreason_unpark"></span>**LINECALLREASON \_ UNpark**
</dt> <dd> <dl> <dt>



La chiamata è stata recuperata come chiamata parcheggiata.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

Nessuna estensibilità. Tutti i 32 bit sono riservati.

Le \_ costanti LINECALLREASON vengono usate nel membro **dwReason** della struttura di dati [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2,0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo)
</dt> <dt>

[**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop)
</dt> <dt>

[**lineRedirect**](/windows/desktop/api/Tapi/nf-tapi-lineredirect)
</dt> <dt>

[**lineSwapHold**](/windows/desktop/api/Tapi/nf-tapi-lineswaphold)
</dt> </dl>

 

 




