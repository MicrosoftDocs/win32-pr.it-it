---
description: Le costanti del flag di bit LINEBEARERMODE \_ descrivono diverse modalità di portamento di una chiamata.
ms.assetid: 87e46ec9-ed5f-4ff5-a382-34eb164f4e66
title: LINEBEARERMODE_ costanti (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87bb03664b6e904cbce7e376eb111675430ea86b8e6880211d76d5b364467097
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117761766"
---
# <a name="linebearermode_-constants"></a>Costanti LINEBEARERMODE \_

Le costanti del flag di bit **LINEBEARERMODE \_** descrivono diverse modalità di portamento di una chiamata. Quando un'applicazione effettua una chiamata, può richiedere una modalità di connessione specifica. Queste modalità vengono usate per selezionare una determinata qualità del servizio per la connessione richiesta dalla rete telefonica sottostante. Le modalità di connessione disponibili in una determinata linea sono una funzionalità del dispositivo della linea.

<dl> <dt>

<span id="LINEBEARERMODE_ALTSPEECHDATA"></span><span id="linebearermode_altspeechdata"></span>**LINEBEARERMODE \_ ALTSPEECHDATA**
</dt> <dd> <dl> <dt>



Trasferimento alternativo di dati vocali o senza restrizioni nella stessa chiamata (ISDN).


</dt> </dl> </dd> <dt>

<span id="LINEBEARERMODE_DATA"></span><span id="linebearermode_data"></span>**DATI LINEBEARERMODE \_**
</dt> <dd> <dl> <dt>



Trasferimento di dati senza restrizioni nella chiamata. La velocità dei dati viene specificata separatamente.


</dt> </dl> </dd> <dt>

<span id="LINEBEARERMODE_MULTIUSE"></span><span id="linebearermode_multiuse"></span>**LINEBEARERMODE \_ MULTIUSE**
</dt> <dd> <dl> <dt>



Modalità multiuso definita da ISDN.


</dt> </dl> </dd> <dt>

<span id="LINEBEARERMODE_NONCALLSIGNALING"></span><span id="linebearermode_noncallsignaling"></span>**LINEBEARERMODE \_ NONCALLSIGNALING**
</dt> <dd> <dl> <dt>



Corrisponde a una connessione di segnalazione non associata alla chiamata dall'applicazione al provider di servizi o al commutatore (considerato come flusso multimediale da TAPI).


</dt> </dl> </dd> <dt>

<span id="LINEBEARERMODE_PASSTHROUGH"></span><span id="linebearermode_passthrough"></span>**LINEBEARERMODE \_ PASSTHROUGH**
</dt> <dd> <dl> <dt>



Quando una chiamata è attiva in LINEBEARERMODE PASSTHROUGH, il provider di servizi concede l'accesso diretto all'hardware collegato per \_ il controllo da parte dell'applicazione. Questa modalità viene utilizzata principalmente dalle applicazioni che desiderano il controllo diretto temporaneo sui modem asincroni, accessibili tramite le funzioni di comunicazione [,](/windows/desktop/DevIO/communications-functions)allo scopo di configurare o utilizzare funzionalità speciali non altrimenti supportate dal provider di servizi.


</dt> </dl> </dd> <dt>

<span id="LINEBEARERMODE_RESTRICTEDDATA"></span><span id="linebearermode_restricteddata"></span>**LINEBEARERMODE \_ RESTRICTEDDATA**
</dt> <dd> <dl> <dt>



Servizio di connessione per i dati digitali in cui solo i sette bit meno validi di ogni ottetto possono contenere dati utente(ad esempio, per il servizio Switched 56kbit/s).


</dt> </dl> </dd> <dt>

<span id="LINEBEARERMODE_SPEECH"></span><span id="linebearermode_speech"></span>**RICONOSCIMENTO VOCALE LINEBEARERMODE \_**
</dt> <dd> <dl> <dt>



Corrisponde alla trasmissione vocale G.711 nella chiamata. La rete può usare tecniche di elaborazione come la trasmissione analogica, l'annullamento dell'eco e la compressione/decompressione. L'integrità dei bit non è garantita. Il riconoscimento vocale non è progettato per supportare i tipi di supporti fax e modem.


</dt> </dl> </dd> <dt>

<span id="LINEBEARERMODE_VOICE"></span><span id="linebearermode_voice"></span>**LINEBEARERMODE \_ VOICE**
</dt> <dd> <dl> <dt>



Si tratta di un normale servizio di connessione di livello vocale analogo a 3,1 kHz. L'integrità dei bit non è garantita. La voce può supportare i tipi di supporti fax e modem.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

I 16 bit di ordine elevato possono essere assegnati per le estensioni specifiche del dispositivo. I 16 bit meno bassi sono riservati.

Si noti che la modalità di accesso e il tipo di supporto sono concetti diversi. La modalità di connessione di una chiamata è un'indicazione della qualità della connessione telefonica fornita principalmente dalla rete. Il tipo di supporto di una chiamata è un'indicazione del tipo di flusso di informazioni scambiato su tale chiamata. Il fax di gruppo 3 o il modem dati sono tipi di supporti che usano una chiamata con una modalità di connessione vocale a 3,1 kHz.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2.0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

