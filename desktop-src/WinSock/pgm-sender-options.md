---
description: I mittenti PGM sono forniti con determinate impostazioni predefinite che influiscono sulle prestazioni della trasmissione dei dati e per quanto tempo i dati vengono memorizzati nel buffer per tenere conto della perdita di pacchetti e delle richieste di ritrasmissione del client PGM associate.
ms.assetid: 56b15eac-ea0d-4d18-b5f6-2f1a7b1bb25f
title: Opzioni mittente PGM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1c2e83ec7b098b9a82f74d4a3e0b6aa3ab03b63
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306910"
---
# <a name="pgm-sender-options"></a>Opzioni mittente PGM

I mittenti PGM sono forniti con determinate impostazioni predefinite che influiscono sulle prestazioni della trasmissione dei dati e per quanto tempo i dati vengono memorizzati nel buffer per tenere conto della perdita di pacchetti e delle richieste di ritrasmissione del client PGM associate. I paragrafi seguenti descrivono queste impostazioni predefinite.

## <a name="window-size-and-transmission-rate"></a>Dimensioni della finestra e frequenza di trasmissione

La possibilità di impostare le dimensioni della finestra e la velocità di trasmissione consente alle applicazioni di controllare la quantità di dati che i buffer di trasporto devono ritrasmettere e la velocità con cui viene trasmesso il flusso di byte.

I dati di ritrasmissione vengono archiviati in un file, pertanto le dimensioni massime della finestra sono limitate dallo spazio su disco utilizzabile dal trasporto. Le dimensioni predefinite della finestra sono di 10 MB. Sebbene sia possibile che le dimensioni di un messaggio o di trasmissione superino la dimensione della finestra o del buffer, il flusso di dati resta ininterrotto; l'invio è in sospeso fino a quando non vengono inviati tutti i dati.

> [!Note]  
> Lo spazio massimo del buffer è limitato dal numero massimo di pacchetti che possono essere conservati nella finestra in un determinato momento, che è uguale a 2 ^ 31-1.

 

La velocità di trasmissione è il flusso combinato dei pacchetti di dati originali (ODATA), i pacchetti di dati ritrasmessi (RDATA) e i pacchetti di contabilità specifici del trasporto (SMSP), espressi al secondo. Se il limite di velocità è impostato su 56 kilobit al secondo per impostazione predefinita. Le dimensioni predefinite della finestra sono pari a 10 megabyte, con una frequenza predefinita di 56 kilobit al secondo. A causa della relazione tra i tre membri della struttura [**della \_ \_ finestra RM Send**](/windows/desktop/api/Wsrm/ns-wsrm-rm_send_window) , le dimensioni predefinite della finestra sono pertanto di 1428 secondi. Per ulteriori informazioni, vedere la **\_ \_ finestra di trasmissione RM** .

## <a name="window-advance-rate"></a>Frequenza di avanzamento finestra

La velocità di avanzamento della finestra viene impostata dall'opzione socket della [ \_ finestra del mittente di \_ \_ \_ RM](socket-options.md) . Questa opzione consente alle applicazioni di specificare l'incremento in corrispondenza del quale la finestra del mittente PGM è avanzata, espressa come valore percentuale diverso da zero della dimensione della finestra. Il valore predefinito è 15% e la frequenza massima è pari al 50%. Se il mittente PGM presenta dati di ripristino in sospeso che rientrano nello spazio della finestra di incremento, la finestra viene avanzata parzialmente mentre ogni pacchetto di ripristino nella finestra viene inviato.

## <a name="forward-error-correction-fec"></a>Correzione errori in diretta (FEC)

La correzione degli errori in diretta viene impostata tramite l'uso dell'opzione di socket di utilizzo del sistema RM \_ use \_ FEC. Questa opzione socket consente al mittente PGM di inviare pacchetti di ripristino come pacchetti di parità anziché pacchetti di dati normali. Questa operazione consente di ridurre al minimo il numero di pacchetti di ripristino inviati per ripristinare sequenze diverse perdute da più ricevitori dall'interno dello stesso gruppo di dati. L'abilitazione di FEC è impostata solo sul mittente PGM. I ricevitori PGM seguono automaticamente i criteri impostati dal mittente. Per una discussione dettagliata su FEC, vedere la specifica PGM disponibile sul sito Web [IETF](https://www.ietf.org/) .

 

 



