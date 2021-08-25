---
description: I mittenti PGM vengono forniti con determinate impostazioni predefinite che influiscono sulle prestazioni di trasmissione dei dati e per quanto tempo i dati vengono memorizzati nel buffer per la perdita di pacchetti e le richieste di ritrasmissione del client PGM associate.
ms.assetid: 56b15eac-ea0d-4d18-b5f6-2f1a7b1bb25f
title: Opzioni del mittente PGM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04bce19e096f269207a22f8e3078643fefd9a7ced31482305c2caeb0ae8b7749
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857909"
---
# <a name="pgm-sender-options"></a>Opzioni del mittente PGM

I mittenti PGM vengono forniti con determinate impostazioni predefinite che influiscono sulle prestazioni di trasmissione dei dati e per quanto tempo i dati vengono memorizzati nel buffer per la perdita di pacchetti e le richieste di ritrasmissione del client PGM associate. I paragrafi seguenti descrivono queste impostazioni predefinite.

## <a name="window-size-and-transmission-rate"></a>Dimensioni della finestra e velocità di trasmissione

La possibilità di impostare le dimensioni della finestra e la velocità di trasmissione consente alle applicazioni di controllare la quantità di dati dei buffer di trasporto per la ritrasmissione e la velocità di trasmissione del flusso di byte.

I dati di ritrasmissione vengono archiviati in un file, pertanto le dimensioni massime della finestra sono limitate dallo spazio su disco utilizzabile dal trasporto. La dimensione predefinita della finestra è 10 MB. Sebbene sia possibile che le dimensioni di un messaggio o di invio superino le dimensioni della finestra o del buffer, il flusso di dati rimane ininterrotta. L'invio viene inviato finché non vengono inviati tutti i dati.

> [!Note]  
> Lo spazio massimo nel buffer è limitato dal numero massimo di pacchetti che possono essere mantenuti nella finestra in un determinato momento, che è uguale a 2^31 – 1.

 

La velocità di trasmissione è il flusso in uscita combinato dei pacchetti di dati originali (ODATA), dei pacchetti di dati ritrasmessi (RDATA) e dei pacchetti di prenotazione (SPN) specifici del trasporto, espressi al secondo. Se il limite di velocità è impostato su 56 kilobit al secondo per impostazione predefinita. La dimensione predefinita della finestra è 10 megabyte, con una frequenza predefinita di 56 kilobit al secondo. A causa della relazione tra i tre membri della struttura [**RM \_ SEND \_ WINDOW,**](/windows/desktop/api/Wsrm/ns-wsrm-rm_send_window) le dimensioni predefinite della finestra sono quindi di 1428 secondi. Per **altre informazioni, vedere RM \_ SEND \_ WINDOW.**

## <a name="window-advance-rate"></a>Frequenza di avanzamento finestra

La frequenza di avanzamento della finestra viene impostata [dall'opzione \_ socket \_ RM SENDER WINDOW \_ ADV \_ RATE.](socket-options.md) Questa opzione consente alle applicazioni di specificare l'incremento in base al quale la finestra del mittente PGM è avanzata, espressa come valore percentuale diverso da zero delle dimensioni della finestra. Il valore predefinito è 15% e la velocità massima è 50%. Se il mittente PGM ha dati di ripristino in sospeso che rientrano nello spazio della finestra di incremento, la finestra viene avanzata parzialmente quando viene inviato ogni pacchetto di ripristino nella finestra.

## <a name="forward-error-correction-fec"></a>Correzione degli errori di inoltro (FEC)

La correzione degli errori di inoltro viene impostata tramite l'opzione socket RM \_ USE \_ FEC. Questa opzione socket consente al mittente PGM di inviare pacchetti di riparazione come pacchetti di parità anziché come normali pacchetti di dati. In questo modo si riduce al minimo il numero di pacchetti di ripristino inviati per ripristinare sequenze diverse perse da più ricevitori all'interno dello stesso gruppo di dati. L'abilitazione di FEC è impostata solo sul mittente PGM. I ricevitori PGM seguono automaticamente i criteri impostati dal mittente. Per una discussione dettagliata su FEC, fare riferimento a PGM RFC disponibile nel [sito Web IETF.](https://www.ietf.org/)

 

 



