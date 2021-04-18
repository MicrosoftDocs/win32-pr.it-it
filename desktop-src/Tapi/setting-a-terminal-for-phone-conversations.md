---
description: Il computer degli utenti può accedere a più dispositivi selezionabili dall'utente e usati per condurre conversazioni vocali interattive.
ms.assetid: cc7ad70a-157e-4db4-b5e4-00d25686a9dd
title: Impostazione di un terminale per le conversazioni telefoniche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75b12e772d8f941cb7c68e25136a843ec5f9a1f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318936"
---
# <a name="setting-a-terminal-for-phone-conversations"></a>Impostazione di un terminale per le conversazioni telefoniche

Il computer dell'utente può avere accesso a più dispositivi selezionabili dall'utente e usati per condurre conversazioni vocali interattive. Prima di tutto, c'è il dispositivo telefonico stesso, completo di lampade, pulsanti, schermo, suoneria e dispositivo di I/O vocale (portatile, vivavoce, auricolare). Il computer dell'utente può anche avere un dispositivo di I/O distinto, ad esempio una cuffia o una combinazione di microfono/altoparlante collegata a una scheda audio, da usare con le conversazioni telefoniche.

TSPI consente all'utente di selezionare la posizione in cui instradare le informazioni inviate dal comcambio alla riga, all'indirizzo o alla chiamata. Il compensatore prevede normalmente che questo sia uno dei set di telefono e invia richieste di squillo, eventi Lamp (per telefoni di stimolo), dati di visualizzazione e dati vocali appropriati. Il telefono invia a sua volta gli eventi hookswitch, gli eventi di pressione dei pulsanti (per i telefoni degli stimoli) e i dati vocali al commutatore.

La parte della *riga* di TSPI rende disponibili gli eventi della lampada, gli eventi di visualizzazione e gli eventi Ring, sia come codici restituiti funzionali alle diverse operazioni di riga in TSPI, sia come messaggi di stato di chiamata funzionale non richiesti inviati al callback dell'applicazione. L'implementazione del provider di servizi è responsabile del mapping tra il livello di TSPI funzionale e lo stimolo sottostante o i messaggi funzionali utilizzati dalla rete di telefonia. Negli ambienti di telefonia funzionale, le funzioni TSPI sono mappate al protocollo funzionale.

Usando la funzione [**TSPI \_ LINESETTERMINAL**](/windows/win32/api/tspi/nf-tspi-tspi_linesetterminal) , TAPI può controllare il routing di eventi di basso livello diversi scambiati tra il commutatore e la stazione; può anche decidere di non indirizzare alcuni di questi eventi di basso livello a un dispositivo. Il routing delle diverse classi di eventi può essere controllato individualmente. Ad esempio, il flusso multimediale di una chiamata (ad esempio, Voice) può essere inviato a qualsiasi dispositivo trasduttore se il provider di servizi e l'hardware sono in grado di eseguire questa operazione. Gli eventi ring dallo switch al telefono possono essere mappati a un avviso visivo sullo schermo del computer oppure possono essere instradati a un dispositivo telefonico. Gli eventi LAMP e gli eventi di visualizzazione possono essere ignorati o indirizzati a un dispositivo telefonico, che sembra comportarsi come un normale set di telefono. Infine, le pressioni dei pulsanti in un dispositivo telefonico possono o non essere passate alla riga. In ogni caso, questo routing di segnali di basso livello dalla riga non influisce sul funzionamento della parte della riga di TSPI, che esegue sempre il mapping degli eventi di basso livello all'equivalente funzionale. Le applicazioni possono consultare le funzionalità del dispositivo di una linea per determinare i terminali disponibili.

In altre parole, la funzione [**TSPI \_ lineSetTerminal**](/windows/win32/api/tspi/nf-tspi-tspi_linesetterminal) specifica il dispositivo terminal a cui vengono indirizzati gli eventi di riga, di indirizzo o di chiamata di un flusso di supporti specificati. È possibile specificare terminali separati per ogni classe di evento. Le classi di evento includono lampade, pulsanti, schermo, suoneria, hookswitch e flusso multimediale.

 

 
