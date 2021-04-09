---
description: La tassonomia descritta in questa sezione innanzitutto distingue il piano di controllo che si preoccupa con la modalità di creazione di una sessione MultiPoint, dal piano dati che gestisce il trasferimento dei dati tra i partecipanti della sessione.
ms.assetid: f411acd7-5e33-4760-8a12-31c2d615426f
title: Tassonomia multipoint
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f97159312a2e431cb82b73336a13904c6b5ab021
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879202"
---
# <a name="multipoint-taxonomy"></a>Tassonomia multipoint

La tassonomia descritta in questa sezione innanzitutto distingue il piano di controllo che si preoccupa con la modalità di creazione di una sessione MultiPoint, dal piano dati che gestisce il trasferimento dei dati tra i partecipanti della sessione.

## <a name="session-establishment-in-the-control-plane"></a>Creazione della sessione nel piano di controllo

Nel piano di controllo sono presenti due tipi distinti di definizione della sessione:

-   radicata
-   non radice

Nel caso di un controllo radice, esiste un partecipante speciale, \_ radice c, che è diverso dal resto dei membri di questa sessione MultiPoint, ciascuno dei quali è denominato \_ foglia c. La \_ radice c deve rimanere presente per tutta la durata della sessione MultiPoint, perché la sessione viene suddivisa in assenza della \_ radice c. La \_ radice c inizia in genere la sessione multipoint impostando la connessione a una foglia c \_ o un numero di \_ foglia c. La \_ radice c può aggiungere più \_ foglia c oppure, in alcuni casi, una foglia c \_ può unire la radice c \_ in un secondo momento. Esempi del piano di controllo rooted sono reperibili in ATM e ST-II.

Per un piano di controllo non radice, tutti i membri appartenenti a una sessione multipoint sono abbandonati, ovvero non esiste alcun partecipante speciale che funge da \_ radice c. Ogni \_ foglia c deve aggiungersi a una sessione multipoint preesistente, sempre disponibile (come nel caso di un indirizzo multicast IP), oppure è stata configurata tramite un meccanismo fuori banda (OOB) che esula dall'ambito della specifica di Windows Sockets.

Un altro modo per esaminare questo aspetto è che una \_ radice c esiste ancora, ma può essere considerata nel cloud di rete anziché in uno dei partecipanti. Poiché una radice del controllo esiste ancora, un piano di controllo non radice può anche essere considerato come radice implicita. Esempi per questo tipo di schemi multipoint con radice implicita sono:

-   Bridge di teleconferenza.
-   Sistema multicast IP.
-   Un'unità di controllo multipoint (MCU) in una conferenza video H. 320.

## <a name="data-transfer-in-the-data-plane"></a>Trasferimento dati nel piano dati

Nel piano dati sono disponibili due tipi di stili di trasferimento dei dati:

-   radicata
-   non radice

In un piano dati radice, esiste un partecipante speciale denominato d \_ radice. Il trasferimento dei dati avviene solo tra la \_ radice d e il resto dei membri di questa sessione MultiPoint, ciascuno dei quali è denominato \_ foglia d. Il traffico potrebbe essere unidirezionale o bidirezionale. I dati inviati dalla \_ radice d vengono duplicati (se necessario) e recapitati a ogni \_ foglia d, mentre i dati delle \_ foglie d passano solo alla \_ radice d. Nel caso di un piano dati radice, nessun traffico è consentito tra le foglie d \_ . Un esempio di protocollo con radice nel piano dati è ST-II.

In un piano dati senza radice, tutti i partecipanti sono uguali, ovvero tutti i dati inviati vengono recapitati a tutti gli altri partecipanti nella stessa sessione multipoint. Allo stesso modo \_ , ogni nodo foglia d può ricevere dati da tutte le altre \_ foglie d e, in alcuni casi, da altri nodi che non fanno parte della sessione multipoint. Non esiste alcun \_ nodo radice d speciale. IP-multicast non è una radice nel piano dati.

Si noti che la domanda di dove si verifica la duplicazione delle unità dati o se un singolo albero condiviso o più alberi con percorso più breve vengono usati per la distribuzione multipoint sono problemi di protocollo e irrilevante per l'interfaccia che l'applicazione userà per eseguire le comunicazioni multipoint. Pertanto, questi problemi non vengono risolti in questa appendice o nell'interfaccia Windows Sockets.

Nella tabella seguente viene illustrata la tassonomia descritta in precedenza e viene indicato il modo in cui gli schemi esistenti rientrano in ogni categoria. Si noti che non sono presenti schemi esistenti che utilizzano un piano di controllo non radice insieme a un piano dati radice.

|                      | Piano di controllo radice | Piano di controllo non radice (con radice implicita) |
|----------------------|----------------------|-------------------------------------------|
| Piano dati radice    | ATM, ST-II           | Nessun esempio noto.                        |
| Piano dati non radice | T. 120                | IP-multicast, H. 320 (MCU)                 |



 

 

 



