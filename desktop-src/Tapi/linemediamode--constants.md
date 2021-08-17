---
description: Le costanti LINEMEDIAMODE \_ descrivono i tipi di supporti (o le modalità) di una sessione o di una chiamata di comunicazione.
ms.assetid: cbb758be-3ecd-4ac4-b1b5-57136a1aad8e
title: LINEMEDIAMODE_ costanti (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c11e40a81fffc967afd534ce6de591b524d835cbe97a919903bd97b1eeb4daf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140014"
---
# <a name="linemediamode_-constants"></a>Costanti \_ LINEMEDIAMODE

Le **costanti \_ LINEMEDIAMODE** descrivono i tipi di supporti (o le modalità) di una sessione o di una chiamata di comunicazione.

<dl> <dt>

<span id="LINEMEDIAMODE_AUTOMATEDVOICE"></span><span id="linemediamode_automatedvoice"></span>**LINEMEDIAMODE \_ AUTOMATEDVOICE**
</dt> <dd> <dl> <dt>



L'energia vocale è stata rilevata durante la chiamata e la voce viene gestita in locale da un'applicazione automatizzata, ad esempio con un'applicazione answering machine. Quando un provider di servizi non riesce a distinguere tra la voce interattiva e la voce automatizzata in una chiamata in ingresso, segnala la chiamata come voce interattiva.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_DATAMODEM"></span><span id="linemediamode_datamodem"></span>**LINEMEDIAMODE \_ DATAMODEM**
</dt> <dd> <dl> <dt>



Sessione del modem dati nella chiamata. I protocolli modem correnti richiedono che la stazione chiamata avvii l'handshake. Per una chiamata modem dati in ingresso, l'applicazione in genere non può effettuare alcun rilevamento positivo. Il modo in cui il provider di servizi effettua questa determinazione è la scelta scelta. Ad esempio, un periodo di silenzio subito dopo la risposta a una chiamata in ingresso può essere usato come euristica per decidere che potrebbe trattarsi di una chiamata del modem dati.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_ADSI"></span><span id="linemediamode_adsi"></span>**LINEMEDIAMODE \_ ADSI**
</dt> <dd> <dl> <dt>



Sessione ADSI (Analog Display Services Interface) nella chiamata. ADSI migliora le chiamate vocali con informazioni alfanumeriche scaricate nel telefono e l'uso di pulsanti soft sul telefono.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_DIGITALDATA"></span><span id="linemediamode_digitaldata"></span>**LINEMEDIAMODE \_ DIGITALDATA**
</dt> <dd> <dl> <dt>



Flusso di dati digitale di formato non specificato.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_G3FAX"></span><span id="linemediamode_g3fax"></span>**LINEMEDIAMODE \_ G3FAX**
</dt> <dd> <dl> <dt>



Un fax di gruppo 3 viene inviato o ricevuto tramite la chiamata.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_G4FAX"></span><span id="linemediamode_g4fax"></span>**LINEMEDIAMODE \_ G4FAX**
</dt> <dd> <dl> <dt>



Un fax di gruppo 4 viene inviato o ricevuto tramite la chiamata.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_INTERACTIVEVOICE"></span><span id="linemediamode_interactivevoice"></span>**LINEMEDIAMODE \_ INTERACTIVEVOICE**
</dt> <dd> <dl> <dt>



L'energia vocale è stata rilevata durante la chiamata e la chiamata viene gestita come una chiamata vocale interattiva con gli esseri umani su entrambe le estremità.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_MIXED"></span><span id="linemediamode_mixed"></span>**LINEMEDIAMODE \_ MISTO**
</dt> <dd> <dl> <dt>



Sessione mista nella chiamata. Misto è uno dei servizi telematici ISDN.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_TDD"></span><span id="linemediamode_tdd"></span>**LINEMEDIAMODE \_ TDD**
</dt> <dd> <dl> <dt>



Una sessione TDD (Telephony Devices for the Deaf) sulla chiamata.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_TELETEX"></span><span id="linemediamode_teletex"></span>**LINEMEDIAMODE \_ TELETEX**
</dt> <dd> <dl> <dt>



Una sessione di teletex sulla chiamata. Teletex è uno dei servizi telematici.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_TELEX"></span><span id="linemediamode_telex"></span>**LINEMEDIAMODE \_ TELEX**
</dt> <dd> <dl> <dt>



Una sessione telex nella chiamata. Telex è uno dei servizi telematici.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_VIDEO"></span><span id="linemediamode_video"></span>**LINEMEDIAMODE \_ VIDEO**
</dt> <dd> <dl> <dt>



Il tipo di supporto della chiamata è video. (TAPI versioni 2.1 e successive)


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_VIDEOTEX"></span><span id="linemediamode_videotex"></span>**LINEMEDIAMODE \_ VIDEOTEX**
</dt> <dd> <dl> <dt>



Una sessione videotex sulla chiamata. Videotex è uno dei servizi telematici.


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_VOICEVIEW"></span><span id="linemediamode_voiceview"></span>**LINEMEDIAMODE \_ VOICEVIEW**
</dt> <dd> <dl> <dt>



Il tipo di supporto della chiamata è VoiceView. (TAPI versioni 1.4 e successive)


</dt> </dl> </dd> <dt>

<span id="LINEMEDIAMODE_UNKNOWN"></span><span id="linemediamode_unknown"></span>**LINEMEDIAMODE \_ UNKNOWN**
</dt> <dd> <dl> <dt>



Esiste un flusso multimediale, ma la relativa modalità non è attualmente nota e potrebbe diventare nota in un secondo momento. Corrisponderebbe a una chiamata con un tipo di supporto non classificato. Negli ambienti di telefonia analoghi tipici, il tipo di supporto di una chiamata in ingresso può essere sconosciuto fino a quando non viene data una risposta alla chiamata e il flusso multimediale è stato filtrato per effettuare una determinazione.

Se è impostato il flag di modalità multimediale sconosciuto, è possibile impostare anche altri flag multimediali. Viene usato per indicare che il supporto è sconosciuto, ma che è probabile che sia uno degli altri tipi di supporti selezionati.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

Tutti i 32 bit sono riservati.

Si noti che la modalità di bearer e il tipo di supporto sono nozioni diverse. La modalità connessione di una chiamata è un'indicazione della qualità della connessione telefonica fornita principalmente dalla rete. Il tipo di supporto di una chiamata è un'indicazione del tipo di flusso di informazioni scambiato su tale chiamata. Il fax o il modem dati di gruppo 3 sono tipi di supporti che usano una chiamata con modalità di connessione vocale a 3,1 kHz.

Per la compatibilità con le versioni precedenti, è responsabilità del provider di servizi esaminare la versione dell'API negoziata nella riga e non usare questo valore LINEMEDIAMODE se non supportato nella versione \_ negoziata.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2.0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




