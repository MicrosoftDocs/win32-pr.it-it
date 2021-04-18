---
description: Il servizio di rilevamento dei collegamenti distribuiti consente alle applicazioni client di rilevare le origini dei collegamenti che sono state spostate.
ms.assetid: 6f438c72-f23d-4ca4-83bd-fe3bc433ceeb
title: Rilevamento dei collegamenti distribuiti e identificatori di oggetto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62d28e151c21fd5320a41950be7647c1e8e0a88b
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/10/2021
ms.locfileid: "106322036"
---
# <a name="distributed-link-tracking-and-object-identifiers"></a>Rilevamento dei collegamenti distribuiti e identificatori di oggetto

L'archiviazione di un riferimento a un file o a una directory utilizzando il percorso e il nome file non è affidabile. Se un utente rinomina un file, interrompe i collegamenti al file. Se un utente rinomina la directory, interrompe i collegamenti al file e a tutti i file e le sottodirectory nella struttura di directory.

Il **servizio di rilevamento dei collegamenti distribuiti** consente alle applicazioni client di rilevare le origini dei collegamenti che sono state spostate. I client che sottoscrivono il servizio di rilevamento dei collegamenti possono mantenere l'integrità dei relativi riferimenti e gli oggetti possono essere rilevati in modo trasparente per l'utente.

## <a name="object-identifiers"></a>Identificatori di oggetto

Il servizio di rilevamento dei collegamenti mantiene il collegamento a un oggetto utilizzando un **identificatore di oggetto (ID)**. Un ID oggetto è un attributo facoltativo che identifica in modo univoco un file o una directory in un volume.

Un indice di tutti gli ID oggetto viene archiviato nel volume. Le operazioni di ridenominazione, backup e ripristino mantengono gli ID oggetto. Tuttavia, le operazioni di copia non mantengono gli ID oggetto, perché ciò violerebbe l'univocità.

È possibile eseguire le operazioni seguenti sugli ID oggetto:

-   Creazione
-   Eliminazione
-   Query

Quando si crea un ID oggetto, si stabilisce l'identità del file nel servizio di rilevamento dei collegamenti. Viceversa, quando si elimina un ID oggetto, il servizio di rilevamento dei collegamenti interrompe la gestione dei collegamenti al file. Per un elenco dei codici di controllo file system che eseguono operazioni sugli ID oggetto, vedere [codici di controllo di gestione file](file-management-control-codes.md).

Il servizio di rilevamento dei collegamenti distribuiti rileva le origini dei collegamenti per i collegamenti della shell e i collegamenti OLE all'interno di volumi file system NTFS. Il client di collegamento può correggere un collegamento interruppe con informazioni aggiornate sul nuovo percorso dell'origine del collegamento.

## <a name="link-tracking-features"></a>Funzionalità di rilevamento dei collegamenti

I collegamenti della shell includono il rilevamento dei collegamenti euristici che usa un algoritmo di ricerca albero per trovare una corrispondenza per un'origine di collegamento spostata. L'algoritmo di ricerca è basato sull'ultimo percorso noto delle informazioni su file e file che include la data di creazione, le dimensioni del file e il nome file e l'estensione.

Il collegamento OLE include lo stesso rilevamento dei collegamenti euristici. Windows include anche lo stesso monitoraggio dei collegamenti euristici con alcuni miglioramenti aggiunti per la ricerca di spazi dei nomi per produrre risultati in alcuni scenari comuni. I miglioramenti includono la seguente procedura che dipende dai limiti di tempo imposti da un'applicazione client.

**Per cercare gli spazi dei nomi**

1.  Eseguire la ricerca di quattro livelli di directory verso il basso dall'ultima directory.
2.  Spostare verso l'alto di una directory e ripetere i passaggi 1 e 2 altre tre volte, che può produrre risultati se l'oggetto è stato spostato in prossimità.
3.  Eseguire la ricerca di quattro livelli verso il basso dalla radice desktop, che può produrre risultati se l'oggetto è stato spostato in una posizione sullo stesso desktop.
4.  Eseguire la ricerca di quattro livelli verso il basso dalla radice in ogni unità fissa locale.
5.  Ripetere i passaggi 1-3 senza il limite di quattro directory.

> [!Note]  
> Questi schemi di rilevamento dei collegamenti sono trasparenti per l'utente finale. Tuttavia, non sempre producono risultati positivi e possono richiedere molto tempo.

 

Per ulteriori informazioni sui collegamenti della shell, vedere [**IShellLink**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinka).

Per ulteriori informazioni sui collegamenti OLE, vedere [**IOleLink**](/windows/win32/api/oleidl/nn-oleidl-iolelink).

Se viene eseguito un collegamento a un file in NTFS 3,0 o versione successiva e il file viene spostato in qualsiasi altro volume con NTFS 3,0 o versione successiva all'interno dello stesso dominio, il file può essere trovato dal servizio di rilevamento, in base alle considerazioni relative al tempo. Inoltre, se il file viene spostato all'esterno del dominio o all'interno di un gruppo di lavoro, viene trovato.

Per ottenere la versione NTFS di un volume, aprire un prompt dei comandi con diritti di accesso di amministratore ed eseguire il comando seguente:

**fsutil fsinfo ntfsinfo** *X * * *:**

dove *X* è la lettera di unità del volume.

Quando viene creato un collegamento a un file, il file di destinazione viene considerato l' **origine del collegamento** e l'autore del collegamento è il **client di collegamento**. Se, ad esempio, viene creato un collegamento della Shell per il collegamento a un documento di testo, il documento di testo è l'origine del collegamento e il collegamento della shell è il client di collegamento.

Il servizio di rilevamento dei collegamenti distribuiti gestisce i collegamenti ai file per le situazioni seguenti che si verificano all'interno di un dominio:

-   Il file di origine del collegamento viene spostato da un volume file system NTFS a un altro nello stesso dominio.
-   Il nome del computer che include l'origine del collegamento viene rinominato.
-   Le condivisioni di rete nel computer di origine del collegamento sono state modificate.
-   Il volume che include il file di origine del collegamento viene spostato in un altro computer nello stesso dominio.

Il servizio di rilevamento dei collegamenti distribuiti tenta anche di mantenere i collegamenti nelle situazioni precedenti, anche quando non si verificano all'interno di un dominio, ovvero sono tra domini o all'interno di un gruppo di lavoro. I collegamenti possono sempre essere gestiti in queste situazioni quando la condivisione di rete nel computer di origine del collegamento viene modificata. Possono essere mantenuti anche quando un'origine del collegamento viene spostata in un computer. I collegamenti possono in genere essere mantenuti quando l'origine del collegamento viene spostata in un altro computer, ma questa forma di rilevamento è meno affidabile nel tempo.

## <a name="link-tracking-functionality"></a>Funzionalità di rilevamento dei collegamenti

La funzionalità di rilevamento dei collegamenti viene implementata principalmente sotto forma dei due servizi di sistema seguenti:

-   Manutenzione collegamenti distribuiti client
-   Server di rilevamento collegamento distribuito

<dl> <dt>

<span id="Distributed_Link_Tracking_Client"></span><span id="distributed_link_tracking_client"></span><span id="DISTRIBUTED_LINK_TRACKING_CLIENT"></span>Client di rilevamento dei collegamenti distribuiti
</dt> <dd>

Il client di rilevamento dei collegamenti distribuiti viene eseguito in tutti i computer e gestisce le attività di rilevamento dei collegamenti per tale computer. Queste attività includono la ricerca di origini di collegamento e lo spostamento di origine del collegamento di elaborazione. Quando viene spostata un'origine di collegamento, il servizio passa informazioni al server di rilevamento dei collegamenti distribuiti eseguito nei controller di dominio.

</dd> <dt>

<span id="Distributed_Link_Tracking_Server"></span><span id="distributed_link_tracking_server"></span><span id="DISTRIBUTED_LINK_TRACKING_SERVER"></span>Server di rilevamento collegamento distribuito
</dt> <dd>

Il server di rilevamento dei collegamenti distribuiti viene eseguito in ogni controller di dominio in un dominio. Il servizio accetta le notifiche relative agli spostamenti di file e volumi dal servizio di rilevamento in un computer e consente al client di rilevamento dei collegamenti distribuiti di eseguire una query sul percorso corrente di un'origine del collegamento.

Questo servizio Server gestisce le informazioni nei controller di dominio sui volumi e i file spostati. Le informazioni sugli spostamenti non possono aumentare oltre una dimensione specifica e vengono rimosse automaticamente se non sono necessarie.

</dd> </dl>

I servizi di rilevamento collegamenti sono esposti dalle interfacce [**IShellLink**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinka) e [**IOleLink**](/windows/win32/api/oleidl/nn-oleidl-iolelink) . Pertanto, vengono utilizzati dai tasti di scelta rapida della shell. Quando viene chiamato il metodo [**IShellLink:: Resolve**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllinka-resolve) e non è possibile trovare il file referente, ad esempio quando l'utente attiva un collegamento alla shell, il servizio di rilevamento viene chiamato automaticamente per trovare il file. Analogamente, quando l'implementazione di [**IOleLink**](/windows/win32/api/oleidl/nn-oleidl-iolelink) non riesce a trovare un file, ad esempio nel metodo [**BindToSource**](/windows/desktop/api/oleidl/nf-oleidl-iolelink-bindtosource) , chiama automaticamente il servizio di rilevamento.

## <a name="link-tracking-limitations"></a>Limitazioni del rilevamento dei collegamenti

I servizi di rilevamento dei collegamenti distribuiti sono disponibili solo nel file system NTFS e sono disponibili solo per le origini dei collegamenti in NTFS 3,0 o versioni successive. Se pertanto un'origine del collegamento viene spostata in un volume file system FAT, le informazioni di rilevamento andranno perse. Inoltre, se un'origine del collegamento viene spostata tra NTFS 3,0 o versione successiva, ma il computer che esegue lo spostamento sta eseguendo una versione precedente di Windows, le informazioni di rilevamento dei collegamenti andranno perse. Quando le informazioni di rilevamento dei collegamenti vengono perse, non viene eseguito alcun danneggiamento del file di origine del collegamento, ma non è sufficiente che i servizi di rilevamento dei collegamenti distribuiti vengano rilevati.

Per ottenere la versione NTFS di un volume, aprire un prompt dei comandi con diritti di accesso di amministratore ed eseguire il comando seguente:

**fsutil fsinfo ntfsinfo** *X * * *:**

dove *X* è la lettera di unità del volume.

I collegamenti a file su supporti rimovibili non vengono mantenuti. Inoltre, il servizio di rilevamento non riconosce un nuovo volume di file system NTFS fino al riavvio del sistema. Potrebbe diventare disponibile un nuovo volume a causa del ripartizionamento, la riformattazione di un volume di file system FAT nel file system NTFS o la connessione di una nuova unità esterna.

 

 
