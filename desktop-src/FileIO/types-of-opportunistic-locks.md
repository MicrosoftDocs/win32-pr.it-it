---
description: Descrive i blocchi opportunistici di livello 1, livello 2, batch e filtro.
ms.assetid: 06136348-0c08-4e9c-9c96-fd3af33cbdc0
title: Tipi di blocchi opportunistici
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a755a6ff766f5d19e13d4b269c1ba4bb9803e934
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884334"
---
# <a name="types-of-opportunistic-locks"></a>Tipi di blocchi opportunistici

Le operazioni di blocco opportunistiche funzionano con quattro tipi di blocchi opportunistici: livello 1, livello 2, batch e filtro. I *blocchi opportunistici esclusivi* sono i blocchi di livello 1, batch e filtro. Se un thread ha un tipo di blocco esclusivo su un file, non può avere anche un blocco di livello 2 nello stesso file.

## <a name="level-1-opportunistic-locks"></a>Blocchi opportunistici di livello 1

Un blocco opportunistico di livello 1 su un file consente a un client di leggere in anticipo nel file e memorizzare nella cache sia i dati read-ahead che quelli di scrittura dal file in locale. Fino a quando il client dispone di accesso esclusivo a un file, non vi sono pericoli per i dati coerenza nel fornire un blocco opportunistico di livello 1.

Il client può richiedere un blocco opportunistico di livello 1 dopo l'apertura di un file. Se il file non è aperto per nessun altro client (o nessun altro thread nello stesso client), il server può concedere il blocco opportunistico. Il client può quindi memorizzare nella cache i dati di lettura e scrittura dal file in locale. Se un altro client ha aperto il file, il server rifiuta il blocco opportunistico e il client non esegue la memorizzazione nella cache locale. Il server può rifiutare il blocco opportunistico anche per altri motivi, ad esempio per non supportare i blocchi opportunistici.

Quando il server apre un file che ha già un blocco opportunistico di livello 1, il server esamina lo stato di condivisione del file prima di suddividere il blocco opportunistico di livello 1. Se il server interrompe il blocco dopo questo esame, il momento in cui il client con il primo blocco impiega lo scaricamento della cache di scrittura è il momento in cui il client che richiede il file deve attendere. Questo dispendio di tempo significa che i blocchi opportunistici di livello 1 devono essere evitati nei file aperti da molti client.

Tuttavia, poiché il server verifica lo stato di condivisione prima che interrompa il blocco, nel caso in cui il server neghi una richiesta aperta a causa di un conflitto di condivisione, il server non interrompe il blocco. Se, ad esempio, è stato aperto un file, è stata negata la condivisione per le operazioni di scrittura e si è ottenuto un blocco di livello 1, il server rifiuta la richiesta di un altro client di aprire il file per la scrittura prima di esaminare il blocco sul file. In questo caso, il blocco opportunistico non è stato danneggiato.

Per un esempio di come funziona un blocco opportunistico di livello 1, vedere esempio di blocco opportunistico di livello 1. Per ulteriori informazioni sull'arresto dei blocchi opportunistici, vedere la pagina relativa alla [suddivisione dei blocchi opportunistici](breaking-opportunistic-locks.md).

## <a name="level-2-opportunistic-locks"></a>Blocchi opportunistici di livello 2

Un blocco opportunistico di livello 2 informa un client che sono presenti più client simultanei di un file e che nessuno lo ha ancora modificato. Questo blocco consente al client di eseguire operazioni di lettura e ottenere attributi di file utilizzando informazioni locali memorizzate nella cache o Read-ahead, ma il client deve inviare al server tutte le altre richieste, ad esempio per le operazioni di scrittura. L'applicazione deve usare il blocco opportunistico di livello 2 quando si prevede che altre applicazioni scrivano il file in modo casuale o leggano il file in modo casuale o sequenziale.

Un blocco opportunistico di livello 2 è molto simile a un blocco opportunistico di filtro. Nella maggior parte dei casi, l'applicazione deve usare il blocco opportunistico di livello 2. Usare il blocco del filtro solo se non si desidera che le operazioni di lettura per la lettura causino violazioni della modalità di condivisione nell'intervallo di tempo tra l'apertura del file e la ricezione del blocco da parte dell'applicazione. Per altre informazioni, vedere filtrare i blocchi opportunistici e la [risposta del server per aprire le richieste sui file bloccati](server-response-to-open-requests-on-locked-files.md).

Per ulteriori informazioni sull'arresto dei blocchi opportunistici, vedere la pagina relativa alla [suddivisione dei blocchi opportunistici](breaking-opportunistic-locks.md).

## <a name="batch-opportunistic-locks"></a>Blocchi opportunistici batch

Un blocco opportunistico batch manipola le aperture e le chiusure di file. Ad esempio, durante l'esecuzione di un file batch, il file batch può essere aperto e chiuso una volta per ogni riga del file. Un blocco opportunistico batch apre il file batch sul server e lo mantiene aperto. Quando il processore del comando "apre" e "chiude" il file batch, il redirector di rete intercetta i comandi di apertura e chiusura. Tutte le ricevute del server sono i comandi seek e Read. Se anche il client sta leggendo in anticipo, il server riceve una particolare richiesta di lettura al massimo una volta.

Quando si apre un file che ha già un blocco opportunistico batch, il server verifica lo stato di condivisione del file dopo l'arresto del blocco. Questo controllo fornisce al titolare del blocco la possibilità di completare lo scaricamento della cache e di chiudere l'handle di file. Un'operazione di apertura tentata durante il controllo di condivisione non determina l'esito negativo della verifica della condivisione se il titolare del blocco rilascia il blocco.

Per un esempio del funzionamento di un blocco opportunistico batch, vedere esempio di blocco opportunistico batch. Per ulteriori informazioni sull'arresto dei blocchi opportunistici, vedere la pagina relativa alla [suddivisione dei blocchi opportunistici](breaking-opportunistic-locks.md).

## <a name="filter-opportunistic-locks"></a>Filtrare i blocchi opportunistici

Un blocco opportunistico di filtro blocca un file in modo che non possa essere aperto per l'accesso in scrittura o eliminazione. Tutti i client devono essere in grado di condividere il file. I blocchi di filtro consentono alle applicazioni di eseguire operazioni di filtro non intrusive sui dati dei file (ad esempio, un compilatore che apre codice sorgente o un programma di catalogazione).

Un blocco opportunistico di filtro differisce da un blocco opportunistico di livello 2 in quanto consente di eseguire operazioni di lettura senza violazioni in modalità di condivisione nell'intervallo di tempo tra l'apertura del file e la ricezione del blocco da parte dell'applicazione. Il filtro di blocco opportunistico è il blocco migliore da usare quando è importante consentire ad altri client di leggere l'accesso. In altri casi, l'applicazione deve usare un blocco opportunistico di livello 2. Un blocco opportunistico di filtro differisce da un blocco opportunistico di batch in quanto non consente la gestione di più aperture e chiusure da parte del redirector di rete nel modo in cui viene utilizzato un blocco opportunistico batch.

L'applicazione deve richiedere un blocco opportunistico di filtro su un file in tre passaggi:

1.  Utilizzare la funzione [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) per aprire un handle per il file con il parametro *desiredAccess* impostato su zero, che indica nessun accesso e il parametro *dwShareMode* impostato sul flag di **\_ \_ lettura della condivisione file** per consentire la condivisione per la lettura. L'handle ottenuto a questo punto è denominato handle di blocco.
2.  Richiedere un blocco su questo handle con il codice di controllo [**\_ \_ \_ blocco opportunistico del filtro richieste FSCTL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_filter_oplock) .
3.  Quando il blocco viene concesso, utilizzare [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) per aprire nuovamente il file con *desiredAccess* impostato sul flag **di \_ lettura generico** . Impostare *dwShareMode* sul flag **di \_ \_ lettura della condivisione file** per consentire ad altri utenti di leggere il file mentre è aperto, il flag di **\_ \_ eliminazione della condivisione file** per consentire ad altri di contrassegnare il file per l'eliminazione mentre è aperto o entrambi. L'handle ottenuto a questo punto è denominato handle di lettura.

Utilizzare l'handle di lettura per leggere o scrivere nel contenuto del file.

Quando si apre un file che ha già un blocco opportunistico di filtro, il server interrompe il blocco e quindi controlla lo stato di condivisione del file. Questo controllo fornisce al client che ha mantenuto il blocco opportunistico precedente la possibilità di abbandonare i dati memorizzati nella cache e di confermare l'interruzione. Un'operazione di apertura tentata durante questo controllo di condivisione non determina l'esito negativo della verifica della condivisione se il blocco del primo blocco viene rilasciato. Il file system include la sospensione dell'operazione di apertura fino a quando il proprietario del blocco non chiude sia l'handle di lettura che l'handle di blocco. Al termine di questa operazione, la richiesta di apertura dell'altro client può continuare.

Per ulteriori informazioni sull'arresto dei blocchi opportunistici, vedere la pagina relativa alla [suddivisione dei blocchi opportunistici](breaking-opportunistic-locks.md).

 

 
