---
description: La tassonomia descritta di seguito distingue innanzitutto il piano di controllo che si preoccupa con la modalità di creazione di una sessione MultiPoint, dal piano dati che gestisce il trasferimento dei dati tra i partecipanti della sessione.
ms.assetid: d138347a-826a-4615-afbd-ffa7726a47eb
title: Tassonomia multipoint e glossario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27ecdfe59640ec58b592aace4e46c66faf752281
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306923"
---
# <a name="multipoint-taxonomy-and-glossary"></a>Tassonomia multipoint e glossario

La tassonomia descritta di seguito distingue innanzitutto il piano di controllo che si preoccupa con la modalità di creazione di una sessione MultiPoint, dal piano dati che gestisce il trasferimento dei dati tra i partecipanti della sessione.

Nel piano di controllo sono presenti due tipi distinti di definizione della sessione:

-   radicata
-   non radice

Per un piano di controllo rooted esiste un partecipante speciale, denominato c \_ root, che è diverso dal resto dei membri di questa sessione MultiPoint, ciascuno dei quali è denominato \_ foglia c. La \_ radice c deve rimanere presente per tutta la durata della sessione MultiPoint, perché la sessione verrà suddivisa in assenza della \_ radice c. La \_ radice c inizia in genere la sessione multipoint impostando la connessione a una foglia c \_ o un numero di \_ foglia c. La \_ radice c può aggiungere più \_ foglia c oppure, in alcuni casi, una foglia c \_ può unire la radice c \_ in un secondo momento. Esempi del piano di controllo rooted sono reperibili in ATM e ST-II.

Per un piano di controllo non radice, tutti i membri appartenenti a una sessione multipoint sono abbandonati, ovvero non esiste alcun partecipante speciale che funge da \_ radice c. Ogni \_ foglia c deve essere aggiunta a una sessione multipoint preesistente, che è sempre disponibile (come nel caso di un indirizzo multicast IP), oppure è stata configurata tramite un meccanismo OOB che esula dall'ambito di questa discussione (e di conseguenza non è stata affrontata nelle estensioni Windows Sockets proposte). Un altro modo per esaminare questo aspetto è che una \_ radice c esiste ancora, ma può essere considerata nel cloud di rete anziché in uno dei partecipanti. Poiché una radice del controllo esiste ancora, un piano di controllo non radice può anche essere considerato come radice implicita. Esempi di questo tipo di schemi multipoint implicitamente radicati sono: un Bridge di teleconferenza, il sistema multicast IP, un'unità di controllo multipoint (MCU) in una conferenza video H. 320 e così via.

Nel piano dati sono disponibili anche due tipi di stili di trasferimento dei dati:

-   radicata
-   non radice

In un piano dati radice, esiste un partecipante speciale denominato d \_ radice. Il trasferimento dei dati avviene solo tra la \_ radice d e il resto dei membri di questa sessione MultiPoint, ciascuno dei quali è denominato \_ foglia d. Il traffico potrebbe essere unidirezionale o bidirezionale. I dati inviati dalla radice d verranno \_ duplicati (se necessario) e recapitati a ogni foglia d \_ , mentre i dati delle foglie d \_ passeranno solo alla \_ radice d. Nel caso di un piano dati radice, non è consentito alcun traffico tra le foglie d \_ . Un esempio di protocollo che usa un piano dati radice è ST-II.

In un piano dati senza radice, tutti i partecipanti sono uguali nel senso che tutti i dati inviati verranno recapitati a tutti gli altri partecipanti nella stessa sessione multipoint. Allo stesso modo \_ , ogni nodo foglia d potrà ricevere dati da tutte le altre \_ foglie d e, in alcuni casi, da altri nodi che non fanno parte anche della sessione multipoint. Non esiste alcun \_ nodo radice d speciale. IP-multicast è un esempio di protocollo che usa un piano dati non radice.

Si noti che la domanda di dove si verifica la duplicazione delle unità dati o se un singolo albero condiviso o più alberi con percorso più breve vengono usati per la distribuzione multipoint sono problemi di protocollo. Di conseguenza, sono irrilevanti per l'interfaccia che il client userà per eseguire le comunicazioni multipoint. Pertanto, questi problemi non vengono risolti dall'interfaccia Windows Sockets.

Nella tabella seguente viene illustrata la tassonomia descritta in precedenza e viene indicato il modo in cui gli schemi esistenti rientrano in ogni categoria di controllo e piano dati. Si noti che non sono presenti schemi multipoint che impiegano un piano di controllo non radice insieme a un piano dati radice.

| Piano dati           | Esempi di piani di controllo rooted | Esempi di piano di controllo con radice non radice (implicito) |
|----------------------|-------------------------------|----------------------------------------------------|
| Piano dati radice    | ATM, ST-II                    | Nessun esempio noto                                  |
| Piano dati non radice | T. 120                         | IP-multicast, H. 320 (MCU)                          |



 

 

 



