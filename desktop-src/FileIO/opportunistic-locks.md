---
description: Un blocco opportunistico (detto anche blocco opportunistico) è un blocco inserito da un client in un file che risiede in un server.
ms.assetid: b4c2f5f0-a29b-4598-a49b-da99e93d2991
title: Blocchi opportunistici
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faec833caae05bff247a7a3655885b1a967f3435
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752399"
---
# <a name="opportunistic-locks"></a>Blocchi opportunistici

Un blocco opportunistico (detto anche blocco opportunistico) è un blocco inserito da un client in un file che risiede in un server. Nella maggior parte dei casi, un client richiede un blocco opportunistico per poter memorizzare i dati nella cache localmente, riducendo così il traffico di rete e migliorando il tempo di risposta apparente. I blocchi opportunistici vengono usati dai redirector di rete nei client con server remoti, nonché dalle applicazioni client nei server locali.

I blocchi opportunistici coordinano la memorizzazione dei dati nella cache e coerenza tra client e server e tra più client. I dati coerenti sono dati identici in tutta la rete. In altre parole, se i dati sono coerenti, i dati nel server e in tutti i client vengono sincronizzati.

I blocchi opportunistici non sono comandi da parte del client al server. Si tratta di richieste inviate dal client al server. Dal punto di vista del client, sono opportunistiche. In altre parole, il server concede tali blocchi ogni volta che gli altri fattori rendono possibili i blocchi.

Quando un'applicazione locale richiede l'accesso a un file remoto, l'implementazione dei blocchi opportunistici è trasparente per l'applicazione. Il redirector di rete e il server hanno richiesto di aprire e chiudere automaticamente i blocchi opportunistici. Tuttavia, i blocchi opportunistici possono essere usati anche quando un'applicazione locale richiede l'accesso a un file locale e l'accesso da parte di altre applicazioni e processi deve essere delegato per impedire il danneggiamento del file. In questo caso, l'applicazione locale richiede direttamente un blocco opportunistico dalla file system locale e memorizza nella cache il file localmente. Quando viene usato in questo modo, il blocco opportunistico è effettivamente un semaforo gestito dal server locale e viene usato principalmente per i dati coerenza nella notifica di accesso ai file e ai file.

Prima di usare i blocchi opportunistici nell'applicazione, è necessario avere familiarità con le modalità di accesso e condivisione dei file descritte in [creazione e apertura di file](creating-and-opening-files.md).

Il numero massimo di blocchi opportunistici simultanei che è possibile creare è limitato solo dalla quantità di memoria disponibile.

Le applicazioni locali non devono tentare di richiedere blocchi opportunistici da server remoti. Se viene effettuato un tentativo di eseguire questa operazione, verrà restituito un errore da [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) .

I blocchi opportunistici sono di uso molto limitato per le applicazioni. L'unico utilizzo pratico consiste nel testare un redirector di rete o un gestore di blocco opportunistico del server. In genere, i file System implementano il supporto per i blocchi opportunistici. Le applicazioni in genere lasciano la gestione dei blocchi opportunistici ai driver file system. Chiunque implementi un file system deve usare il [kit del file system installabile (IFS)](https://www.microsoft.com/whdc/devtools/ifskit/default.mspx). Chiunque sviluppi un driver di dispositivo diverso da un file system installabile deve utilizzare [Windows Driver Kit (WDK)](https://www.microsoft.com/?ref=go).

I blocchi opportunistici e le operazioni associate sono un superset della parte di blocco opportunistica del protocollo CIFS (Common Internet file System), una bozza Internet. Il protocollo CIFS è una versione migliorata del protocollo SMB (Server Message Block). Per altre informazioni, vedere [Cenni preliminari sul protocollo Microsoft SMB e sul protocollo CIFS](microsoft-smb-protocol-and-cifs-protocol-overview.md). La bozza Internet CIFS indica in modo esplicito che un'implementazione di CIFS può implementare blocchi opportunistici rifiutando di concederli.

Gli argomenti seguenti identificano i blocchi opportunistici.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                                               | Descrizione                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Caching locale](local-caching.md)<br/>                                                                       | La *memorizzazione nella cache locale* dei dati è una tecnica che consente di velocizzare l'accesso alla rete ai file di dati. Comporta la memorizzazione nella cache dei dati nei client anziché nei server, quando possibile.<br/>                                                                                                                           |
| [Coerenza dati](data-coherency.md)<br/>                                                                     | Se i dati sono coerenti, i dati nel server e in tutti i client vengono sincronizzati. Un tipo di sistema software che fornisce dati coerenza è un sistema di controllo delle revisioni (RCS).<br/>                                                                                                              |
| [Come richiedere un blocco opportunistico](how-to-request-an-opportunistic-lock.md)<br/>                         | I blocchi opportunistici vengono richiesti aprendo prima un file con le autorizzazioni e i flag appropriati all'applicazione per l'apertura del file. Tutti i file per i quali verranno richiesti blocchi opportunistici devono essere aperti per operazioni sovrapposte (asincrone).<br/>                                |
| [Risposta server per l'apertura di richieste su file bloccati](server-response-to-open-requests-on-locked-files.md)<br/> | È possibile ridurre al minimo l'impatto dell'applicazione su altri client e l'impatto che hanno sull'applicazione concedendo il maggior numero possibile di condivisione, richiedendo il livello di accesso minimo necessario e usando il blocco opportunistico meno intrusivo adatto all'applicazione.<br/> |
| [Tipi di blocchi opportunistici](types-of-opportunistic-locks.md)<br/>                                         | Descrive i blocchi opportunistici di livello 1, livello 2, batch e filtro.<br/>                                                                                                                                                                                                                     |
| [Interruzioni di blocchi opportunistici](breaking-opportunistic-locks.md)<br/>                                         | Suddividere un blocco opportunistico è il processo di riduzione del blocco di un client in un file in modo che un altro client possa aprire il file, con o senza un blocco opportunistico.<br/>                                                                                                     |
| [Esempi di blocco opportunistico](opportunistic-lock-examples.md)<br/>                                           | Diagrammi delle visualizzazioni di traffico di rete per un blocco opportunistico di livello 1, un blocco opportunistico batch e un blocco opportunistico di filtro.<br/>                                                                                                                                                       |
| [Operazioni di blocco opportunistiche](opportunistic-lock-operations.md)<br/>                                       | Se un'applicazione richiede blocchi opportunistici, è necessario aprire tutti i file per cui richiede blocchi per l'input e l'output sovrapposti usando la funzione [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) con il flag **file \_ \_ sovrapposto** .<br/>                                   |



 

Per ulteriori informazioni sui blocchi opportunistici, vedere il documento CIFS Internet bozza. Eventuali discrepanze tra questo argomento e la bozza Internet CIFS corrente devono essere risolte a favore della bozza Internet CIFS.

 

