---
description: Un blocco opportunistico (detto anche oplock) è un blocco inserito da un client in un file che risiede in un server.
ms.assetid: b4c2f5f0-a29b-4598-a49b-da99e93d2991
title: Blocchi opportunistici
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89d3e984c5a8a1a1dc9cc1cb0c0c56e92434433b334747e832ea7f3bdf62d3da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119683401"
---
# <a name="opportunistic-locks"></a>Blocchi opportunistici

Un blocco opportunistico (detto anche oplock) è un blocco inserito da un client in un file che risiede in un server. Nella maggior parte dei casi, un client richiede un blocco opportunistico in modo che possa memorizzare i dati nella cache locale, riducendo così il traffico di rete e migliorando il tempo di risposta apparente. I blocchi opportunistici vengono usati dai redirector di rete nei client con server remoti, nonché dalle applicazioni client nei server locali.

I blocchi opportunistici coordinano la memorizzazione nella cache e la coesistenza dei dati tra client e server e tra più client. I dati coerenti sono dati uguali in tutta la rete. In altre parole, se i dati sono coerenti, i dati nel server e in tutti i client vengono sincronizzati.

I blocchi opportunistici non sono comandi del client al server. Si tratta di richieste dal client al server. Dal punto di vista del client, sono opportunistici. In altre parole, il server concede tali blocchi ogni volta che altri fattori rendono possibili i blocchi.

Quando un'applicazione locale richiede l'accesso a un file remoto, l'implementazione di blocchi opportunistici è trasparente per l'applicazione. Il redirector di rete e il server interessato aprono e chiudono automaticamente i blocchi opportunistici. Tuttavia, i blocchi opportunistici possono essere usati anche quando un'applicazione locale richiede l'accesso a un file locale e l'accesso da parte di altre applicazioni e processi deve essere delegato per evitare il danneggiamento del file. In questo caso, l'applicazione locale richiede direttamente un blocco opportunistico dal file system locale e memorizza il file nella cache locale. Se usato in questo modo, il blocco opportunistico è in effetti un semaforo gestito dal server locale e viene usato principalmente ai fini della coesistenza dei dati nella notifica di accesso a file e file.

Prima di usare blocchi opportunistici nell'applicazione, è necessario avere familiarità con le modalità di accesso e condivisione dei file descritte in [Creazione e apertura di file](creating-and-opening-files.md).

Il numero massimo di blocchi opportunistici simultanei che è possibile creare è limitato solo dalla quantità di memoria disponibile.

Le applicazioni locali non devono tentare di richiedere blocchi opportunistici ai server remoti. Se si tenta di eseguire questa operazione, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) restituirà un errore.

I blocchi opportunistici sono di uso molto limitato per le applicazioni. L'unico uso pratico è testare un redirector di rete o un gestore di blocco opportunistico del server. In genere, i file system implementano il supporto per i blocchi opportunistici. Le applicazioni in genere lasciano la gestione dei blocchi opportunistica ai file system driver. Chiunque implementa un file system deve usare [Installable File System (IFS) Kit](https://www.microsoft.com/whdc/devtools/ifskit/default.mspx). Chiunque sviluppi un driver di dispositivo diverso da un file system installabile deve usare [Windows Driver Kit (WDK).](https://www.microsoft.com/?ref=go)

I blocchi opportunistici e le operazioni associate sono un superset della parte di blocco opportunistica del protocollo CIFS (Common Internet File System), una bozza Internet. Il protocollo CIFS è una versione avanzata del protocollo Server Message Block (SMB). Per altre informazioni, vedere [Panoramica del protocollo SMB Microsoft e del protocollo CIFS.](microsoft-smb-protocol-and-cifs-protocol-overview.md) La bozza Internet CIFS identifica in modo esplicito che un'implementazione CIFS può implementare blocchi opportunistici rifiutando di concederli.

Gli argomenti seguenti identificano i blocchi opportunistici.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                                               | Descrizione                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Impostazioni Caching](local-caching.md)<br/>                                                                       | *La memorizzazione nella cache* locale dei dati è una tecnica usata per velocizzare l'accesso di rete ai file di dati. Comporta la memorizzazione nella cache dei dati nei client anziché nei server, quando possibile.<br/>                                                                                                                           |
| [Coesistenza dei dati](data-coherency.md)<br/>                                                                     | Se i dati sono coerenti, i dati nel server e in tutti i client vengono sincronizzati. Un tipo di sistema software che fornisce coesistenza dei dati è un sistema di controllo delle revisioni (RCS).<br/>                                                                                                              |
| [Come richiedere un blocco opportunistico](how-to-request-an-opportunistic-lock.md)<br/>                         | I blocchi opportunistici vengono richiesti aprendo prima un file con le autorizzazioni e i flag appropriati all'applicazione che apre il file. Tutti i file per cui verranno richiesti blocchi opportunistici devono essere aperti per l'operazione sovrapposta (asincrona).<br/>                                |
| [Risposta del server alle richieste aperte nei file bloccati](server-response-to-open-requests-on-locked-files.md)<br/> | È possibile ridurre al minimo l'impatto dell'applicazione su altri client e l'impatto che hanno sull'applicazione concedendo il maggior numero possibile di condivisioni, richiedendo il livello di accesso minimo necessario e usando il blocco opportunistico meno intrusivo adatto per l'applicazione.<br/> |
| [Tipi di blocchi opportunistici](types-of-opportunistic-locks.md)<br/>                                         | Descrive i blocchi opportunistici di livello 1, livello 2, batch e filtro.<br/>                                                                                                                                                                                                                     |
| [Interruzione di blocchi opportunistici](breaking-opportunistic-locks.md)<br/>                                         | L'interruzione di un blocco opportunistico è il processo di riduzione del blocco di un client in un file in modo che un altro client possa aprire il file, con o senza un blocco opportunistico.<br/>                                                                                                     |
| [Esempi di blocco opportunistico](opportunistic-lock-examples.md)<br/>                                           | Diagrammi delle viste del traffico di rete per un blocco opportunistico di livello 1, un blocco opportunistico batch e un blocco opportunistico di filtro.<br/>                                                                                                                                                       |
| [Operazioni di blocco opportunistiche](opportunistic-lock-operations.md)<br/>                                       | Se un'applicazione richiede blocchi opportunistici, tutti i file per cui richiede blocchi devono essere aperti per l'input e l'output sovrapposti (asincroni) usando la funzione [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) con il flag **FILE FLAG \_ \_ OVERLAPPED.**<br/>                                   |



 

Per altre informazioni sui blocchi opportunistici, vedere il documento Bozza Internet CIFS. Eventuali discrepanze tra questo argomento e la bozza Internet CIFS corrente devono essere risolte a favore della bozza Internet CIFS.

 

