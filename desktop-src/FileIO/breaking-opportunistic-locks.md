---
description: L'interruzione di un blocco opportunistico è il processo di riduzione del blocco di un client in un file in modo che un altro client possa aprire il file, con o senza un blocco opportunistico.
ms.assetid: 0356c167-2973-4820-85a9-bc14abcbf163
title: Interruzione di blocchi opportunistici
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74b797feed06c5f02f1b87ff4e05e2d82d44a34f0efe86d7a0881ec1d722023f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119582601"
---
# <a name="breaking-opportunistic-locks"></a>Interruzione di blocchi opportunistici

L'interruzione di un blocco opportunistico è il processo di riduzione del blocco di un client in un file in modo che un altro client possa aprire il file, con o senza un blocco opportunistico. Quando l'altro client richiede l'operazione di apertura, il server ritarda l'operazione di apertura e invia una notifica al client che contiene il blocco opportunistico.

Il client che tiene il blocco quindi adotta le azioni appropriate per il tipo di blocco, ad esempio l'abbandono dei buffer di lettura, la chiusura del file e così via. Solo quando il client che contiene il blocco opportunistico notifica al server che l'operazione è stata eseguita, il server apre il file per il client che richiede l'operazione di apertura. Tuttavia, quando un blocco di livello 2 viene interrotto, il server segnala al client che è stato interrotto ma non attende alcun riconoscimento, poiché non sono presenti dati memorizzati nella cache da scaricare nel server.

Nel riconoscere un'interruzione di qualsiasi blocco esclusivo (filtro, livello 1 o batch), il titolare di un blocco interrotto non può richiedere un altro blocco esclusivo. Può ridurre un blocco esclusivo a un blocco di livello 2 o nessun blocco. Il titolare rilascia in genere il blocco e chiude il file quando sta per chiudere comunque il file.

Alle applicazioni viene notificato che un blocco opportunistico viene interrotto usando il membro **hEvent** della struttura [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) associata al file in cui il blocco viene interrotto. Le applicazioni possono anche usare funzioni come [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) e [**HasOverlappedIoCompleted**](/windows/desktop/api/winbase/nf-winbase-hasoverlappediocompleted).

 

 
