---
description: Descrive i blocchi opportunistici di livello 1, livello 2, batch e filtro.
ms.assetid: 06136348-0c08-4e9c-9c96-fd3af33cbdc0
title: Tipi di blocchi opportunistici
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39dc450b038013454ea2d0ddd9c78a701dc8f977b4fa3b0aca7cdda076e8b12e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047851"
---
# <a name="types-of-opportunistic-locks"></a>Tipi di blocchi opportunistici

Le operazioni di blocco opportunistiche funzionano con quattro tipi di blocchi opportunistici: livello 1, livello 2, batch e filtro. *I blocchi opportunistici esclusivi* sono blocchi di livello 1, di batch e di filtro. Se un thread ha un tipo di blocco esclusivo su un file, non può avere anche un blocco di livello 2 sullo stesso file.

## <a name="level-1-opportunistic-locks"></a>Blocchi opportunistici di livello 1

Un blocco opportunistico di livello 1 su un file consente a un client di leggere in anticipo il file e memorizzare nella cache sia il read-ahead che la scrittura dei dati dal file in locale. Finché il client ha l'unico accesso a un file, non vi è alcun rischio per la coerenza dei dati nel fornire un blocco opportunistico di livello 1.

Il client può richiedere un blocco opportunistico di livello 1 dopo l'apertura di un file. Se nessun altro client (o nessun altro thread nello stesso client) ha il file aperto, il server può concedere il blocco opportunistico. Il client può quindi memorizzare nella cache i dati di lettura e scrittura dal file in locale. Se il file è stato aperto da un altro client, il server rifiuta il blocco opportunistico e il client non esegue alcuna memorizzazione nella cache locale. Il server può rifiutare il blocco opportunistico anche per altri motivi, ad esempio per non supportare blocchi opportunistici.

Quando il server apre un file che dispone già di un blocco opportunistico di livello 1, il server esamina lo stato di condivisione del file prima di interromperlo. Se il server interrompe il blocco dopo questo esame, il tempo trascorso dal client con il blocco precedente per scaricare la cache di scrittura è il tempo che il client che richiede il file deve attendere. Questo tempo indica che i blocchi opportunistici di livello 1 devono essere evitati nei file aperti da molti client.

Tuttavia, poiché il server controlla lo stato di condivisione prima di interrompere il blocco, nel caso in cui il server neghi una richiesta aperta a causa di un conflitto di condivisione, il server non interrompe il blocco. Ad esempio, se è stato aperto un file, è stata negata la condivisione per le operazioni di scrittura e si è ottenuto un blocco di livello 1, il server nega la richiesta di un altro client di aprire il file per la scrittura prima ancora di esaminare il blocco sul file. In questo caso, il blocco opportunistico non viene interrotto.

Per un esempio del funzionamento di un blocco opportunistico di livello 1, vedere Esempio di blocco opportunistico di livello 1. Per altre informazioni sull'interruzione dei blocchi opportunistici, vedere [Blocco opportunistico di interruzione.](breaking-opportunistic-locks.md)

## <a name="level-2-opportunistic-locks"></a>Blocchi opportunistici di livello 2

Un blocco opportunistico di livello 2 informa un client che sono presenti più client simultanei di un file e che nessuno lo ha ancora modificato. Questo blocco consente al client di eseguire operazioni di lettura e ottenere attributi di file usando le informazioni locali memorizzate nella cache o read-ahead, ma il client deve inviare tutte le altre richieste (ad esempio per le operazioni di scrittura) al server. L'applicazione deve usare il blocco opportunistico di livello 2 quando si prevede che altre applicazioni scrivono nel file in modo casuale o leggono il file in modo casuale o sequenziale.

Un blocco opportunistico di livello 2 è molto simile a un blocco opportunistico di filtro. Nella maggior parte dei casi, l'applicazione deve usare il blocco opportunistico di livello 2. Usare il blocco del filtro solo se non si vuole che le operazioni di apertura per la lettura causano violazioni della modalità di condivisione nell'intervallo di tempo tra l'apertura del file e la ricezione del blocco da parte dell'applicazione. Per altre informazioni, vedere Filtrare blocchi opportunistici e [Risposta del server alle richieste di apertura su file bloccati.](server-response-to-open-requests-on-locked-files.md)

Per altre informazioni sull'interruzione dei blocchi opportunistici, vedere [Blocco opportunistico di interruzione.](breaking-opportunistic-locks.md)

## <a name="batch-opportunistic-locks"></a>Blocchi opportunistici batch

Un blocco batch opportunistico modifica le operazioni di apertura e chiusura dei file. Ad esempio, nell'esecuzione di un file batch, il file batch può essere aperto e chiuso una volta per ogni riga del file. Un blocco batch opportunistico apre il file batch nel server e lo mantiene aperto. Quando il processore dei comandi "apre" e "chiude" il file batch, il redirector di rete intercetta i comandi di apertura e chiusura. Tutti i server ricevuti sono i comandi di ricerca e lettura. Se anche il client sta leggendo in anticipo, il server riceve una particolare richiesta di lettura al massimo una volta.

Quando si apre un file che dispone già di un blocco batch opportunistico, il server controlla lo stato di condivisione del file dopo l'interruzione del blocco. Questo controllo offre al titolare del blocco la possibilità di completare lo scaricamento della cache e di chiudere l'handle di file. Un'operazione di apertura tentata durante il controllo di condivisione non causa l'esito negativo del controllo di condivisione se il titolare del blocco rilascia il blocco.

Per un esempio del funzionamento di un blocco batch opportunistico, vedere Esempio di blocco opportunistico batch. Per altre informazioni sull'interruzione dei blocchi opportunistici, vedere [Blocco opportunistico di interruzione.](breaking-opportunistic-locks.md)

## <a name="filter-opportunistic-locks"></a>Filtrare blocchi opportunistici

Un blocco opportunistico di filtro blocca un file in modo che non possa essere aperto per l'accesso in scrittura o per l'eliminazione. Tutti i client devono essere in grado di condividere il file. I blocchi di filtro consentono alle applicazioni di eseguire operazioni di filtro non intrusive sui dati dei file, ad esempio un compilatore che apre il codice sorgente o un programma di catalogazione.

Un blocco opportunistico di filtro è diverso da un blocco opportunistico di livello 2 perché consente l'esecuzione di operazioni di apertura per la lettura senza violazioni della modalità di condivisione nell'intervallo di tempo tra l'apertura del file e la ricezione del blocco da parte dell'applicazione. Il blocco opportunistico del filtro è il blocco migliore da usare quando è importante consentire ad altri client di leggere l'accesso. In altri casi, l'applicazione deve usare un blocco opportunistico di livello 2. Un blocco opportunistico di filtro è diverso da un blocco opportunistico batch perché non consente la gestione di più aperte e chiusure da parte del redirector di rete come un blocco opportunistico batch.

L'applicazione deve richiedere un blocco opportunistico di filtro su un file in tre passaggi:

1.  Usare la funzione [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) per aprire un handle al file con il parametro *DesiredAccess* impostato su zero, che indica nessun accesso, e il parametro *dwShareMode* impostato sul flag **FILE SHARE \_ \_ READ** per consentire la condivisione per la lettura. L'handle ottenuto a questo punto viene chiamato handle di blocco.
2.  Richiedere un blocco su questo handle con il codice di controllo [**\_ \_ \_ OPLOCK FSCTL REQUEST FILTER.**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_filter_oplock)
3.  Quando viene concesso il blocco, usare [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) per aprire nuovamente il file con *DesiredAccess* impostato sul flag **GENERIC \_ READ.** Impostare *dwShareMode* sul flag **FILE SHARE \_ \_ READ** per consentire ad altri utenti di leggere il file mentre è aperto, il flag **FILE SHARE \_ \_ DELETE** per consentire ad altri utenti di contrassegnare il file per l'eliminazione mentre è aperto o entrambi. L'handle ottenuto a questo punto viene chiamato handle di lettura.

Usare l'handle di lettura per leggere o scrivere nel contenuto del file.

Quando si apre un file che dispone già di un blocco opportunistico di filtro, il server interrompe il blocco e quindi controlla lo stato di condivisione del file. Questo controllo offre al client che ha mantenuto il blocco opportunistico precedente la possibilità di abbandonare tutti i dati memorizzati nella cache e confermare l'interruzione. Un'operazione di apertura tentata durante questo controllo di condivisione non causa l'esito negativo del controllo di condivisione se il proprietario del blocco precedente rilascia il blocco. Il file system mantiene inaltere l'operazione di apertura fino a quando il proprietario del blocco non chiude sia l'handle di lettura che l'handle di blocco. Al termine, la richiesta aperta dell'altro client può continuare.

Per altre informazioni sull'interruzione dei blocchi opportunistici, vedere [Blocco opportunistico di interruzione.](breaking-opportunistic-locks.md)

 

 
