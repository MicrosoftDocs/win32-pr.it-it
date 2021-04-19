---
description: Suddividere un blocco opportunistico è il processo di riduzione del blocco di un client in un file in modo che un altro client possa aprire il file, con o senza un blocco opportunistico.
ms.assetid: 0356c167-2973-4820-85a9-bc14abcbf163
title: Interruzioni di blocchi opportunistici
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a29b6bd36d8c000b5288ea2408897415547c802
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317809"
---
# <a name="breaking-opportunistic-locks"></a>Interruzioni di blocchi opportunistici

Suddividere un blocco opportunistico è il processo di riduzione del blocco di un client in un file in modo che un altro client possa aprire il file, con o senza un blocco opportunistico. Quando l'altro client richiede l'operazione di apertura, il server ritarda l'operazione di apertura e invia una notifica al client che mantiene il blocco opportunistico.

Il client che mantiene il blocco esegue quindi le azioni appropriate per il tipo di blocco, ad esempio abbandonando i buffer di lettura, chiudendo il file e così via. Solo quando il client che mantiene il blocco opportunistico notifica al server che è stato eseguito, il server apre il file per il client che richiede l'operazione di apertura. Tuttavia, quando un blocco di livello 2 viene danneggiato, il server segnala al client che è stato rotto ma non attende il riconoscimento, poiché non sono presenti dati memorizzati nella cache da scaricare nel server.

Nel riconoscere un'interruzione di un blocco esclusivo (filtro, livello 1 o batch), il titolare di un blocco rotto non può richiedere un altro blocco esclusivo. Può compromettere un blocco esclusivo a un blocco di livello 2 o nessun blocco. Il titolare rilascia in genere il blocco e chiude il file quando sta per chiudere comunque il file.

Alle applicazioni viene notificato che un blocco opportunistico viene violato utilizzando il membro **hEvent** della struttura [**sovrapposta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) associata al file in cui il blocco è danneggiato. Le applicazioni possono anche usare funzioni quali [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) e [**HasOverlappedIoCompleted**](/windows/desktop/api/winbase/nf-winbase-hasoverlappediocompleted).

 

 
