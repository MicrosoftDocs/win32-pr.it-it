---
description: Il valore restituito delle funzioni PDH indica l'esito positivo o negativo della chiamata di funzione, che è diverso dallo stato dei dati del contatore.
ms.assetid: 00ea5521-bc28-4a87-aba9-46c911631503
title: Controllo dei codici di stato dei dati dei contatori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a34c433e1c45badd3a2211a0e53051ad40d495f63a67b0ca509ae74a5cd99972
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119978881"
---
# <a name="checking-counter-data-status-codes"></a>Controllo dei codici di stato dei dati dei contatori

Il valore restituito delle funzioni PDH indica l'esito positivo o negativo della chiamata di funzione, che è diverso dallo stato dei dati del contatore. Controllare sempre il **membro CStatus** di un valore del contatore restituito nelle strutture PDH per assicurarsi che i dati restituiti siano validi prima di usarlo. Se il valore del **membro CStatus** non indica l'esito positivo, non usare i dati. Di seguito sono riportati i valori di stato possibili per i contatori:



| Valore                              | Significato                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PDH \_ CSTATUS \_ NO \_ MACHINE          | PDH non è riuscito a connettersi al computer specificato nel percorso del contatore. Se questo stato viene restituito quando viene aggiunto il contatore, il contatore non viene inizializzato completamente. Ogni volta che la query viene aggiornata, PDH ritenta la connessione. Quando viene stabilita la connessione, viene ripresa la normale raccolta dei dati.                                                                  |
| PDH \_ CSTATUS \_ NO \_ OBJECT           | Il computer specificato è stato trovato, ma l'oggetto prestazioni specificato è stato trovato nel computer. Se questo stato viene restituito quando viene aggiunto il contatore, il contatore specificato non viene incluso nella query. Se questo stato viene restituito da un contatore attivo, i dati per tale contatore non sono validi. Ogni volta che vengono richiesti i dati, PDH tenta di ottenere questi dati del contatore. |
| PDH \_ CSTATUS \_ NO \_ INSTANCE         | L'istanza specificata non è stata trovata nell'oggetto . Se questo stato viene restituito mentre il contatore viene aggiunto alla query, il contatore viene aggiunto correttamente alla query, ma non sono disponibili dati fino a quando non viene visualizzata l'istanza specifica e non viene restituito uno stato con esito positivo.                                                                                                  |
| PDH \_ CSTATUS \_ NO \_ COUNTER          | Il contatore specificato non è stato trovato nell'oggetto specificato. Se questo stato viene restituito quando viene aggiunto il contatore, il contatore non viene aggiunto alla query. Se questo stato viene restituito dopo la raccolta dei dati, i dati per tale contatore non sono validi. Ogni volta che vengono richiesti i dati, PDH tenta di ottenere questi dati del contatore.                                             |
| PDH \_ CSTATUS \_ INVALID \_ DATA        | Il contatore è stato trovato correttamente, ma i dati restituiti non sono validi. Questo errore può verificarsi se il valore del contatore è minore del valore precedente. Poiché i valori dei contatori aumentano sempre, il valore del contatore viene eseguito il roll over a zero quando raggiunge il valore massimo. Un'altra possibile causa è un timer di sistema non corretto.                                              |
| PDH \_ CSTATUS \_ VALID \_ DATA          | I dati per il contatore sono stati restituiti correttamente, ma rimangono invariati rispetto all'ultima lettura del contatore.                                                                                                                                                                                                                                                                    |
| PDH \_ CSTATUS \_ NEW \_ DATA            | I dati per il contatore sono stati restituiti correttamente ed è diverso dall'ultima lettura del contatore. PDH CSTATUS NEW DATA può essere restituito in un contatore di frequenza anche se la frequenza risultante è la stessa \_ \_ \_ dell'ultimo campione. Ciò è dovuto al fatto che il valore dei dati non elaborati usato nella determinazione di questo valore di stato è cambiato, non la frequenza calcolata.                  |
| PDH \_ MORE \_ DATA                    | Le dimensioni del buffer fornito non sono sufficienti per archiviare tutti i dati del contatore. Allocare un buffer più grande ed eseguire di nuovo la funzione.                                                                                                                                                                                                                                              |
| ELEMENTO \_ CSTATUS PDH \_ NON \_ \_ CONVALIDATO | Il contatore è stato aggiunto alla query, ma non è stato convalidato né è stato eseguito l'accesso. Non sono disponibili informazioni aggiuntive sullo stato di questo contatore.                                                                                                                                                                                                                                 |
| PDH \_ CSTATUS \_ NO \_ COUNTERNAME      | Nella query non è stato specificato alcun nome di contatore.                                                                                                                                                                                                                                                                                                                                      |
| PDH \_ CSTATUS \_ NO \_ COUNTER          | Impossibile trovare il nome del contatore specificato.                                                                                                                                                                                                                                                                                                                                   |
| PDH \_ CSTATUS \_ NO \_ OBJECT           | Impossibile trovare l'oggetto prestazioni specificato.                                                                                                                                                                                                                                                                                                                             |
| PDH \_ CALC \_ NEGATIVE \_ DENOMINATOR   | Un contatore ha un valore denominatore negativo.                                                                                                                                                                                                                                                                                                                                      |
| PDH \_ CALC \_ NEGATIVE \_ TIMEBASE      | Un contatore ha un valore timebase negativo.                                                                                                                                                                                                                                                                                                                                         |
| PDH \_ CALC \_ NEGATIVE \_ VALUE         | Un contatore ha un valore negativo.                                                                                                                                                                                                                                                                                                                                                  |
| PDH \_ CSTATUS \_ NO \_ COUNTERNAME      | Non è stato specificato alcun percorso del contatore.                                                                                                                                                                                                                                                                                                                                                   |
| PDH \_ CSTATUS \_ BAD \_ COUNTERNAME     | Il formato del percorso del contatore non è corretto.                                                                                                                                                                                                                                                                                                                                            |



 

 

 



