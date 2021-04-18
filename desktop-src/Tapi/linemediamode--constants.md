---
description: Le \_ costanti LINEMEDIAMODE descrivono i tipi di supporto (o le modalità) di una sessione di comunicazione o di una chiamata.
ms.assetid: cbb758be-3ecd-4ac4-b1b5-57136a1aad8e
title: Costanti LINEMEDIAMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 550a31da0d6de556e28ded14ce0803030be075ed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331026"
---
# <a name="linemediamode_-constants"></a>\_Costanti LINEMEDIAMODE

Le **costanti \_ LINEMEDIAMODE** descrivono i tipi di supporto (o le modalità) di una sessione di comunicazione o di una chiamata.

<dl> <dt>

<span id="LINEMEDIAMODE_AUTOMATEDVOICE"></span><span id="linemediamode_automatedvoice"></span>**\_AUTOMATEDVOICE LINEMEDIAMODE**
</dt> <dd> <dl> <dt>



L'energia vocale è stata rilevata nella chiamata e la voce viene gestita localmente da un'applicazione automatizzata, ad esempio con un'applicazione per la segreteria del computer. Quando un provider di servizi non è in grado di distinguere la voce interattiva e automatica di una chiamata in ingresso, la chiamata verrà segnalata come voce interattiva.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_DATAMODEM"></span><span id="linemediamode_datamodem"></span>**LINEMEDIAMODE \_ DATAmodel**
</dt> <dd> <dl> <dt>



Sessione del modem dati sulla chiamata. Per i protocolli modem correnti è richiesta la stazione chiamata per avviare l'handshake. Per una chiamata al modem dati in ingresso, l'applicazione in genere non può eseguire alcun rilevamento positivo. Il modo in cui il provider di servizi effettua questa determinazione è la scelta. Ad esempio, un periodo di silenzio immediatamente dopo la risposta a una chiamata in ingresso può essere usato come euristica per decidere che potrebbe trattarsi di una chiamata al modem dati.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_ADSI"></span><span id="linemediamode_adsi"></span>**LINEMEDIAMODE \_ ADSI**
</dt> <dd> <dl> <dt>



Una sessione ADSI (analogous display Services Interface) nella chiamata. ADSI migliora le chiamate vocali con le informazioni alfanumeriche scaricate sul telefono e l'uso di pulsanti soft sul telefono.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_DIGITALDATA"></span><span id="linemediamode_digitaldata"></span>**\_DIGITALDATA LINEMEDIAMODE**
</dt> <dd> <dl> <dt>



Flusso di dati digitali di formato non specificato.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_G3FAX"></span><span id="linemediamode_g3fax"></span>**\_G3FAX LINEMEDIAMODE**
</dt> <dd> <dl> <dt>



È in corso l'invio o la ricezione di un fax del gruppo 3 attraverso la chiamata.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_G4FAX"></span><span id="linemediamode_g4fax"></span>**\_G4FAX LINEMEDIAMODE**
</dt> <dd> <dl> <dt>



È in corso l'invio o la ricezione di un fax del gruppo 4 sulla chiamata.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_INTERACTIVEVOICE"></span><span id="linemediamode_interactivevoice"></span>**\_INTERACTIVEVOICE LINEMEDIAMODE**
</dt> <dd> <dl> <dt>



L'energia vocale è stata rilevata nella chiamata e la chiamata viene gestita come chiamata vocale interattiva con gli utenti a entrambe le estremità.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_MIXED"></span><span id="linemediamode_mixed"></span>**LINEMEDIAMODE \_ misto**
</dt> <dd> <dl> <dt>



Sessione mista sulla chiamata. Mixed è uno dei servizi di telematica ISDN.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_TDD"></span><span id="linemediamode_tdd"></span>**LINEMEDIAMODE \_ TDD**
</dt> <dd> <dl> <dt>



Una sessione TDD (dispositivi di telefonia per la sordità) nella chiamata.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_TELETEX"></span><span id="linemediamode_teletex"></span>**\_Teletex LINEMEDIAMODE**
</dt> <dd> <dl> <dt>



Una sessione Teletex sulla chiamata. Teletex è uno dei servizi telematici.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_TELEX"></span><span id="linemediamode_telex"></span>**\_telex LINEMEDIAMODE**
</dt> <dd> <dl> <dt>



Una sessione telex sulla chiamata. Telex è uno dei servizi telematici.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_VIDEO"></span><span id="linemediamode_video"></span>**VIDEO di LINEMEDIAMODE \_**
</dt> <dd> <dl> <dt>



Il tipo di supporto della chiamata è video. (Versioni TAPI 2,1 e successive)


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_VIDEOTEX"></span><span id="linemediamode_videotex"></span>**\_VIDEOTEX LINEMEDIAMODE**
</dt> <dd> <dl> <dt>



Una sessione videotex sulla chiamata. Videotex è uno dei servizi telematici.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_VOICEVIEW"></span><span id="linemediamode_voiceview"></span>**\_VOICEVIEW LINEMEDIAMODE**
</dt> <dd> <dl> <dt>



Il tipo di supporto della chiamata è VoiceView. (Versioni TAPI 1,4 e successive)


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_UNKNOWN"></span><span id="linemediamode_unknown"></span>**LINEMEDIAMODE \_ sconosciuto**
</dt> <dd> <dl> <dt>



Un flusso multimediale esiste ma la relativa modalità non è attualmente nota e potrebbe essere nota in seguito. Corrisponderebbe a una chiamata con un tipo di supporto non classificato. Nei tipici ambienti di telefonia analogica, il tipo di supporto di una chiamata in ingresso può essere sconosciuto fino a quando non viene ricevuta la risposta alla chiamata e il flusso multimediale è stato filtrato per effettuare una determinazione.

Se è impostato il flag della modalità media sconosciuta, è possibile impostare anche altri flag di supporto. Viene utilizzato per indicare che il supporto è sconosciuto, ma che probabilmente è uno degli altri tipi di supporti selezionati.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

Tutti i 32 bit sono riservati.

Si noti che la modalità di porta e il tipo di supporto sono nozioni differenti. La modalità di connessione di una chiamata indica la qualità della connessione telefonica fornita principalmente dalla rete. Il tipo di supporto di una chiamata indica il tipo di flusso di informazioni scambiato tramite la chiamata. Il fax del gruppo 3 o il modem dati sono tipi di supporti che usano una chiamata con la modalità di connessione vocale a 3,1 kHz.

Per compatibilità con le versioni precedenti, è responsabilità del provider di servizi esaminare la versione dell'API negoziata sulla riga e non usare questo \_ valore LINEMEDIAMODE se non è supportato nella versione negoziata.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2,0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




