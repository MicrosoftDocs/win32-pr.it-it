---
description: La tassonomia descritta in questa sezione distingue innanzitutto il piano di controllo che riguarda se stesso con il modo in cui viene stabilita una sessione multipoint, dal piano dati che gestisce il trasferimento dei dati tra i partecipanti alla sessione.
ms.assetid: f411acd7-5e33-4760-8a12-31c2d615426f
title: Tassonomia multipunto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9d1928dde2935ab803d95d73db225f7b3be0bc051a082d3bdae937e9b8e7da0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097721"
---
# <a name="multipoint-taxonomy"></a>Tassonomia multipunto

La tassonomia descritta in questa sezione distingue innanzitutto il piano di controllo che riguarda se stesso con il modo in cui viene stabilita una sessione multipoint, dal piano dati che gestisce il trasferimento dei dati tra i partecipanti alla sessione.

## <a name="session-establishment-in-the-control-plane"></a>Creazione di sessioni nel piano di controllo

Nel piano di controllo sono disponibili due tipi distinti di definizione delle sessioni:

-   Radicata
-   nonrooted

Nel caso del controllo rooted, esiste un partecipante speciale, c root, diverso dal resto dei membri di questa sessione multipunto, ognuno dei quali è chiamato \_ foglia \_ c. La radice c deve rimanere presente per l'intera durata della sessione multipunto, in quanto la sessione viene suddivisa in assenza della \_ radice \_ c. La radice c in genere avvia la sessione multipoint configurando la connessione a una foglia c o a un \_ \_ numero di foglia \_ c. La radice c \_ può aggiungere altre foglia c o (in alcuni casi) una foglia c può unire la \_ radice c in un secondo \_ \_ momento. Esempi del piano di controllo rooted sono disponibili in ATM e ST-II.

Per un piano di controllo non rooted, tutti i membri appartenenti a una sessione multipunto sono foglia, cio' non esiste alcun partecipante speciale che funge da \_ radice c. Ogni foglia c deve aggiungersi a una sessione multipoint preesistente che è sempre disponibile (come nel caso di un indirizzo multicast IP) o è stata impostata tramite un meccanismo fuori banda (OOB) che non rientra nell'ambito della specifica \_ socket Windows.

Un altro modo per esaminare questo problema è che esiste ancora una radice c, ma può essere considerata nel cloud di rete anziché in uno \_ dei partecipanti. Poiché esiste ancora una radice di controllo, anche un piano di controllo non rooted può essere considerato implicitamente rooted. Di seguito sono riportati alcuni esempi di questo tipo di schemi multipoint con radice implicita:

-   Un ponte di teleconferenza.
-   Sistema multicast IP.
-   Un'unità di controllo multipunto (MCU) in una videoconferenza H.320.

## <a name="data-transfer-in-the-data-plane"></a>Trasferimento dei dati nel piano dati

Nel piano dati sono disponibili due tipi di stili di trasferimento dei dati:

-   Radicata
-   nonrooted

In un piano dati rooted esiste un partecipante speciale denominato d \_ root. Il trasferimento dei dati avviene solo tra la radice d e il resto dei membri di questa sessione multipunto, ognuno dei quali viene definito \_ foglia \_ d. Il traffico può essere unidirezionale o bidirezionale. I dati inviati dalla radice d vengono duplicati (se necessario) e recapitati a ogni foglia d, mentre i dati dalle foglia d passano solo alla \_ \_ radice \_ \_ d. Nel caso di un piano dati rooted, non è consentito traffico tra \_ le foglia d. Un esempio di protocollo radice nel piano dati è ST-II.

In un piano dati non sradicato, tutti i partecipanti sono uguali, vale a significa che tutti i dati inviati vengono recapitati a tutti gli altri partecipanti nella stessa sessione multipunto. Analogamente, ogni nodo foglia d può ricevere dati da tutte le altre foglia d e, in alcuni casi, da altri nodi che non partecipano \_ \_ alla sessione multipoint. Non esiste alcun \_ nodo radice d speciale. Ip-multicast non èrooted nel piano dati.

Si noti che la questione della posizione in cui si verifica la duplicazione di unità dati o se un albero singolo condiviso o più alberi a percorsi più brevi vengono usati per la distribuzione multipoint sono problemi di protocollo e irrilevanti per l'interfaccia usata dall'applicazione per eseguire comunicazioni multipoint. Questi problemi non vengono quindi risolti in questa appendice o nell'Windows Sockets.

La tabella seguente illustra la tassonomia descritta in precedenza e indica il modo in cui gli schemi esistenti rientrano in ognuna delle categorie. Si noti che non sembrano esserci schemi esistenti che utilizzano un piano di controllo non rooted insieme a un piano dati rooted.

|                      | Piano di controllo rooted | Piano di controllo non rooted (radice implicita) |
|----------------------|----------------------|-------------------------------------------|
| Piano dati rooted    | ATM, ST-II           | Nessun esempio noto.                        |
| Piano dati non sradicato | T.120                | IP-multicast, H.320 (MCU)                 |



 

 

 



