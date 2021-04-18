---
description: Le \_ costanti del flag di bit LINECONNECTEDMODE descrivono i diversi sottostati di una chiamata connessa.
ms.assetid: d75a5989-3f4e-4e5d-90b1-4e450def017e
title: Costanti LINECONNECTEDMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5191d3a575ef353c54c91c0e53b3228621b703cf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328905"
---
# <a name="lineconnectedmode_-constants"></a>\_Costanti LINECONNECTEDMODE

Le costanti del flag di bit **LINECONNECTEDMODE \_** descrivono i diversi sottostati di una chiamata connessa. Una modalità è disponibile come stato della chiamata all'applicazione dopo che lo stato della chiamata passa a connesso e all'interno del \_ messaggio di riga CALLSTATE che indica che la chiamata si trova in LINECALLSTATE \_ connesso. Questi valori vengono usati quando la chiamata si trova su un indirizzo condiviso (con bridging) con altre stazioni (per altre informazioni, vedere [**\_ costanti LINEADDRESSSHARING**](lineaddresssharing--constants.md)), principalmente sistemi di chiave elettronica. Le **\_ costanti LINECONNECTEDMODE** presentano i valori seguenti:

<dl> <dt>

<span id="LINECONNECTEDMODE_ACTIVE"></span><span id="lineconnectedmode_active"></span>**LINECONNECTEDMODE \_ attivo**
</dt> <dd> <dl> <dt>



Indica che la chiamata è connessa alla stazione corrente (la stazione corrente è un partecipante alla chiamata). Se la modalità di stato della chiamata è pari a 0 (zero), l'applicazione deve presupporre che il valore sia "Active" (che corrisponderebbe alla situazione di un indirizzo non con bridging). La modalità può passare tra ACTIVE e inactive durante una chiamata se l'utente si unisce e lascia la chiamata attraverso un'azione manuale. In una situazione di questo tipo, un'operazione [**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop) o [**lineHold**](/windows/desktop/api/Tapi/nf-tapi-linehold) potrebbe non eliminare effettivamente la chiamata o inserirla in attesa, perché lo stato di altre stazioni della chiamata può governare, ad esempio il tentativo di "mantenere" una chiamata quando le altre stazioni non sono possibili. al contrario, la chiamata può essere modificata in modalità inattiva se rimane connessa in altre stazioni.


</dt> </dl> </dd> <dt>

<span id="LINECONNECTEDMODE_ACTIVEHELD"></span><span id="lineconnectedmode_activeheld"></span>**\_ACTIVEHELD LINECONNECTEDMODE**
</dt> <dd> <dl> <dt>



Indica che la stazione è un partecipante attivo nella chiamata, ma che la parte remota ha effettuato la chiamata in attesa (l'altra parte considera la chiamata nello stato onHolding). In genere, tali informazioni sono disponibili solo quando entrambi gli endpoint della chiamata rientrano nello stesso dominio di cambio. Questo flag viene esposto solo alle applicazioni che negoziano una versione di TAPI 2,0 o successiva. (Versioni TAPI 2,0 e successive)


</dt> </dl> </dd> <dt>

<span id="LINECONNECTEDMODE_CONFIRMED"></span><span id="lineconnectedmode_confirmed"></span>**LINECONNECTEDMODE \_ confermato**
</dt> <dd> <dl> <dt>



Indica che il provider di servizi ha ricevuto una notifica affermativa che la chiamata è entrata nello stato connesso, ad esempio tramite la supervisione della risposta o meccanismi simili. Questo flag viene esposto solo alle applicazioni che negoziano una versione di TAPI 2,0 o successiva. (Versioni TAPI 2,0 e successive)


</dt> </dl> </dd> <dt>

<span id="LINECONNECTEDMODE_INACTIVE"></span><span id="lineconnectedmode_inactive"></span>**LINECONNECTEDMODE \_ INattivo**
</dt> <dd> <dl> <dt>



Indica che la chiamata è attiva in una o più stazioni, ma la stazione corrente non è un partecipante alla chiamata. Se la modalità di stato della chiamata è pari a ZERO, l'applicazione deve presupporre che il valore sia "Active", ovvero la situazione in un indirizzo non con Bridge. Una chiamata nello stato inattivo può essere unita in join con [**lineAnswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer). Molte operazioni valide nelle chiamate nello stato connesso possono essere impossibili in modalità inattiva, ad esempio il monitoraggio di toni e cifre, perché la stazione non partecipa effettivamente alla chiamata; il monitoraggio viene in genere sospeso (anche se non annullato) mentre la chiamata è in modalità inattiva.


</dt> </dl> </dd> <dt>

<span id="LINECONNECTEDMODE_INACTIVEHELD"></span><span id="lineconnectedmode_inactiveheld"></span>**\_INACTIVEHELD LINECONNECTEDMODE**
</dt> <dd> <dl> <dt>



Indica che la stazione non è un partecipante attivo nella chiamata e che la parte remota ha effettuato la chiamata in attesa. Questo flag viene esposto solo alle applicazioni che negoziano una versione di TAPI 2,0 o successiva. (Versioni TAPI 2,0 e successive)


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

Non estendibile. Tutti i 32 bit sono riservati.

Per compatibilità con le versioni precedenti, è responsabilità del provider di servizi esaminare la versione dell'API negoziata sulla riga e non usare i \_ valori LINECONNECTEDMODE non supportati nella versione negoziata. Per le applicazioni che non sono consapevoli di LINECONNECTEDMODE \_ , probabilmente si presuppone che una chiamata in LINECALLSTATE \_ connessa si trovi in LINECONNECTEDMODE \_ Active.

I \_ valori inattivi di LINECONNECTEDMODE Active e LINECONNECTEDMODE \_ vengono usati quando la chiamata si trova in un indirizzo condiviso con altre stazioni (Bridged; vedere [**\_ costanti LINEADDRESSSHARING**](lineaddresssharing--constants.md)), principalmente sistemi a chiave elettronica. Se la modalità di stato della chiamata connessa è "attiva", significa che la chiamata è connessa alla stazione corrente (la stazione corrente è un partecipante alla chiamata). Se la modalità di stato della chiamata è "inattiva", la chiamata è attiva in una o più stazioni, ma la stazione corrente non è un partecipante alla chiamata. Se la modalità di stato della chiamata è pari a ZERO, l'applicazione deve presupporre che il valore sia "Active", ovvero la situazione in un indirizzo non con Bridge. La modalità può passare tra ACTIVE e inactive durante una chiamata se l'utente si unisce e lascia la chiamata attraverso un'azione manuale.

In una situazione di questo tipo, un'operazione [**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop) o [**lineHold**](/windows/desktop/api/Tapi/nf-tapi-linehold) potrebbe non eliminare effettivamente la chiamata o inserirla in attesa, perché lo stato di altre stazioni della chiamata può governare (ad esempio, il tentativo di "tenere" una chiamata quando altre stazioni partecipano non sarà possibile); al contrario, la chiamata può essere semplicemente modificata in modalità inattiva se rimane connessa in altre stazioni. È possibile unire in join una chiamata nello stato inattivo usando [**lineAnswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer).

Molte operazioni valide nelle chiamate nello stato connesso possono essere impossibili in modalità inattiva, ad esempio il monitoraggio di toni e cifre, perché la stazione non partecipa effettivamente alla chiamata; il monitoraggio viene in genere sospeso (anche se non annullato) mentre la chiamata è in modalità inattiva.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2,0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**lineAnswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer)
</dt> <dt>

[**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop)
</dt> <dt>

[**lineHold**](/windows/desktop/api/Tapi/nf-tapi-linehold)
</dt> </dl>

 

 




