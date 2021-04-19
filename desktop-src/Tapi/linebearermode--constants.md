---
description: Le \_ costanti del flag di bit LINEBEARERMODE descrivono diverse modalità di chiamata di una chiamata.
ms.assetid: 87e46ec9-ed5f-4ff5-a382-34eb164f4e66
title: Costanti LINEBEARERMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc7d48689dd435e0a07e1ce9fa5a2a9915b1bf69
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332903"
---
# <a name="linebearermode_-constants"></a>\_Costanti LINEBEARERMODE

Le costanti del flag di bit **LINEBEARERMODE \_** descrivono diverse modalità di chiamata di una chiamata. Quando un'applicazione effettua una chiamata, può richiedere una modalità di porta di tipo specifica. Queste modalità vengono utilizzate per selezionare una determinata qualità del servizio per la connessione richiesta dalla rete telefonica sottostante. Le modalità di porta disponibili in una determinata riga sono una funzionalità del dispositivo della linea.

<dl> <dt>

<span id="LINEBEARERMODE_ALTSPEECHDATA"></span><span id="linebearermode_altspeechdata"></span>**\_ALTSPEECHDATA LINEBEARERMODE**
</dt> <dd> <dl> <dt>



Trasferimento alternativo di dati vocali o senza restrizioni sulla stessa chiamata (ISDN).


</dt> </dl> </dd> <dt>

<span id="LINEBEARERMODE_DATA"></span><span id="linebearermode_data"></span>**\_dati LINEBEARERMODE**
</dt> <dd> <dl> <dt>



Trasferimento di dati senza restrizioni sulla chiamata. La velocità dei dati viene specificata separatamente.


</dt> </dl> </dd> <dt>

<span id="LINEBEARERMODE_MULTIUSE"></span><span id="linebearermode_multiuse"></span>**\_multiuso LINEBEARERMODE**
</dt> <dd> <dl> <dt>



Modalità multiuso definita da ISDN.


</dt> </dl> </dd> <dt>

<span id="LINEBEARERMODE_NONCALLSIGNALING"></span><span id="linebearermode_noncallsignaling"></span>**\_NONCALLSIGNALING LINEBEARERMODE**
</dt> <dd> <dl> <dt>



Corrisponde a una connessione non associata alla chiamata dall'applicazione al provider di servizi o allo switch (considerato come un flusso multimediale da TAPI).


</dt> </dl> </dd> <dt>

<span id="LINEBEARERMODE_PASSTHROUGH"></span><span id="linebearermode_passthrough"></span>**\_PassThrough LINEBEARERMODE**
</dt> <dd> <dl> <dt>



Quando una chiamata è attiva in LINEBEARERMODE \_ PassThrough, il provider di servizi fornisce accesso diretto all'hardware collegato per il controllo da parte dell'applicazione. Questa modalità viene utilizzata principalmente dalle applicazioni che desiderano il controllo diretto temporaneo sui modem asincroni, a cui si accede tramite le [funzioni di comunicazione](/windows/desktop/DevIO/communications-functions), allo scopo di configurare o utilizzare funzionalità speciali non altrimenti supportate dal provider di servizi.


</dt> </dl> </dd> <dt>

<span id="LINEBEARERMODE_RESTRICTEDDATA"></span><span id="linebearermode_restricteddata"></span>**\_RESTRICTEDDATA LINEBEARERMODE**
</dt> <dd> <dl> <dt>



Servizio di Bearer per i dati digitali, in cui solo i sette bit meno significativi di ogni ottetto possono contenere dati utente, ad esempio per il servizio 56Kbit/s attivato.


</dt> </dl> </dd> <dt>

<span id="LINEBEARERMODE_SPEECH"></span><span id="linebearermode_speech"></span>**\_sintesi vocale LINEBEARERMODE**
</dt> <dd> <dl> <dt>



Corrisponde alla trasmissione vocale G. 711 sulla chiamata. La rete può utilizzare tecniche di elaborazione come la trasmissione analoga, l'annullamento di Echo e la compressione/decompressione. L'integrità dei bit non è garantita. La voce non è progettata per supportare i tipi di supporto fax e modem.


</dt> </dl> </dd> <dt>

<span id="LINEBEARERMODE_VOICE"></span><span id="linebearermode_voice"></span>**LINEBEARERMODE \_ Voice**
</dt> <dd> <dl> <dt>



Si tratta di un normale servizio di porta di pari livello di 3,1 kHz. L'integrità dei bit non è garantita. La voce può supportare i tipi di supporto fax e modem.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

È possibile assegnare i 16 bit più significativi per le estensioni specifiche del dispositivo. I 16 bit di ordine inferiore sono riservati.

Si noti che la modalità di porta e il tipo di supporto sono nozioni differenti. La modalità di connessione di una chiamata indica la qualità della connessione telefonica fornita principalmente dalla rete. Il tipo di supporto di una chiamata indica il tipo di flusso di informazioni scambiato tramite la chiamata. Il fax del gruppo 3 o il modem dati sono tipi di supporti che usano una chiamata con la modalità di connessione vocale a 3,1 kHz.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2,0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

