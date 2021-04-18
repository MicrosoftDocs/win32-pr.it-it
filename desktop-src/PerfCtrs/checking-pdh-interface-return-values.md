---
description: Il valore restituito delle funzioni PDH indica l'esito positivo o negativo della chiamata di funzione, che è diversa dallo stato dei dati del contatore.
ms.assetid: 00ea5521-bc28-4a87-aba9-46c911631503
title: Controllo dei codici di stato dei dati del contatore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7daed51ba6e8df385170b9a23b419267409ef497
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312185"
---
# <a name="checking-counter-data-status-codes"></a>Controllo dei codici di stato dei dati del contatore

Il valore restituito delle funzioni PDH indica l'esito positivo o negativo della chiamata di funzione, che è diversa dallo stato dei dati del contatore. Controllare sempre il membro **CStatus** di un valore del contatore restituito nelle strutture PDH per assicurarsi che i dati restituiti siano validi prima di usarli. Se il valore del membro **CStatus** non indica esito positivo, non usare i dati. Di seguito sono riportati i possibili valori di stato per i contatori:



| Valore                              | Significato                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PDH \_ CSTATUS \_ nessun \_ computer          | PDH non è riuscito a connettersi al computer specificato nel percorso del contatore. Se questo stato viene restituito quando il contatore viene aggiunto, il contatore non è completamente inizializzato. Ogni volta che la query viene aggiornata, PDH ritenta la connessione. Quando viene stabilita la connessione, la raccolta dei dati normale riprende.                                                                  |
| PDH \_ CSTATUS \_ nessun \_ oggetto           | Il computer specificato è stato trovato, ma l'oggetto prestazione specificato è stato trovato nel computer. Se questo stato viene restituito quando il contatore viene aggiunto, il contatore specificato non è incluso nella query. Se questo stato viene restituito da un contatore attivo, i dati relativi a tale contatore non sono validi. Ogni volta che vengono richiesti i dati, PDH tenta di ottenere i dati del contatore. |
| PDH \_ CSTATUS \_ Nessuna \_ istanza         | L'istanza specificata non è stata trovata nell'oggetto. Se questo stato viene restituito mentre il contatore viene aggiunto alla query, il contatore viene aggiunto correttamente alla query, ma non sono disponibili dati finché non viene visualizzata l'istanza specifica e viene restituito uno stato di esito positivo.                                                                                                  |
| PDH \_ CSTATUS \_ senza \_ contatore          | Impossibile trovare il contatore specificato nell'oggetto specificato. Se questo stato viene restituito quando il contatore viene aggiunto, il contatore non viene aggiunto alla query. Se questo stato viene restituito dopo la raccolta dei dati, i dati relativi a tale contatore non sono validi. Ogni volta che vengono richiesti i dati, PDH tenta di ottenere i dati del contatore.                                             |
| PDH \_ CSTATUS \_ dati non validi \_        | Il contatore è stato trovato, ma i dati restituiti non sono validi. Questo errore può verificarsi se il valore del contatore è minore del valore precedente. Poiché i valori dei contatori vengono sempre incrementati, il valore del contatore viene spostato su zero quando raggiunge il valore massimo. Un'altra possibile cause è un timer di sistema non corretto.                                              |
| \_ \_ dati validi CSTATUS di PDH \_          | I dati per il contatore sono stati restituiti correttamente, ma sono rimasti invariati dall'ultima lettura del contatore.                                                                                                                                                                                                                                                                    |
| PDH \_ CSTATUS \_ nuovi \_ dati            | I dati per il contatore sono stati restituiti correttamente ed è diversa dall'ultima volta in cui il contatore è stato letto. PDH \_ CSTATUS i \_ nuovi \_ dati possono essere restituiti in un contatore di velocità anche se la frequenza risultante è uguale all'ultimo campione. Ciò è dovuto al fatto che il valore dei dati non elaborati utilizzato nella determinazione del valore di stato è stato modificato, non della velocità calcolata.                  |
| PDH \_ altri \_ dati                    | Il buffer fornito non era sufficientemente grande per archiviare tutti i dati del contatore. Allocare un buffer più grande ed eseguire di nuovo la funzione.                                                                                                                                                                                                                                              |
| \_elemento CSTATUS \_ PDH \_ non \_ convalidato | Il contatore è stato aggiunto alla query, ma non è stato convalidato né accessibile. Non sono disponibili informazioni aggiuntive sullo stato del contatore.                                                                                                                                                                                                                                 |
| PDH \_ CSTATUS \_ No \_ counterName      | Nella query non è stato specificato alcun nome contatore.                                                                                                                                                                                                                                                                                                                                      |
| PDH \_ CSTATUS \_ senza \_ contatore          | Impossibile trovare il nome del contatore specificato.                                                                                                                                                                                                                                                                                                                                   |
| PDH \_ CSTATUS \_ nessun \_ oggetto           | Impossibile trovare l'oggetto prestazione specificato.                                                                                                                                                                                                                                                                                                                             |
| \_ \_ denominatore PDH calcolo negativo \_   | Un contatore ha un valore denominatore negativo.                                                                                                                                                                                                                                                                                                                                      |
| \_TIMEBASE di calcolo PDH \_ negativo \_      | Un contatore ha un valore timebase negativo.                                                                                                                                                                                                                                                                                                                                         |
| \_ \_ valore negativo calcolo \_ PDH         | Un contatore presenta un valore negativo.                                                                                                                                                                                                                                                                                                                                                  |
| PDH \_ CSTATUS \_ No \_ counterName      | Non è stato specificato alcun percorso del contatore.                                                                                                                                                                                                                                                                                                                                                   |
| PDH \_ CSTATUS \_ - \_ counterName non valido     | Il formato del percorso del contatore non è corretto.                                                                                                                                                                                                                                                                                                                                            |



 

 

 



