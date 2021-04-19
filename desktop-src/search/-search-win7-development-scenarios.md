---
description: Descrive l'introduzione delle librerie per Windows 7.
ms.assetid: 83c47963-4c8e-45ee-b707-bd45cfe048cd
title: Librerie shell di Windows in Windows 7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb94551d80d0230966626f1bd6499801aff889c4
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "106320325"
---
# <a name="windows-shell-libraries-in-windows"></a>Librerie della shell di Windows in Windows

Questo argomento descrive l'introduzione delle librerie per Windows 7 e versioni successive. Le librerie sono una funzionalità della shell di Windows. Per accedere alla funzionalità della shell di Windows, ad esempio le librerie, gli sviluppatori di terze parti di applicazioni Windows Search devono implementare prima di tutto un archivio dati della shell. Per ulteriori informazioni, vedere [implementazione delle interfacce di oggetti della cartella di base](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).

Questo argomento è organizzato nel modo seguente:

- [Raccolte](#libraries)
  - [Punti di ingresso dati utente](#user-data-entry-points)
  - [Raccolte di cartelle](#collections-of-folders)
  - [Cartelle supportate nelle librerie](#supported-folders-in-libraries)
  - [Archiviazione supportata](#storage-backed)
  - [Contenitori della shell non del file System](#non-file-system-shell-containers)
  - [Descrizioni delle librerie](#library-descriptions)
- [Argomenti correlati](#related-topics)

## <a name="libraries"></a>Librerie

In Windows 7 e versioni successive, le librerie sono il repository predefinito dei dati utente. Gli utenti possono esplorare i file nello stesso modo in cui si trovino in una cartella oppure possono visualizzare i file disposti per proprietà quali data, tipo e autore. Diversamente da una cartella, una libreria non archivia effettivamente gli elementi, ma Visualizza i file archiviati in diverse cartelle nello stesso momento. Le librerie offrono un unico punto di accesso e pivot di visualizzazione completa per gli utenti del contenuto aggregato. Se, ad esempio, un utente dispone di file musicali nelle cartelle di un'unità esterna oltre alla cartella **Music** , potrà accedere immediatamente a tutti i file musicali tramite la raccolta musicale.

### <a name="user-data-entry-points"></a>Punti di ingresso dati utente

Le librerie predefinite, ad esempio **documenti**, **Immagini** e così via, sono equivalenti alla [cartella nota](/previous-versions/windows/desktop/legacy/bb776911(v=vs.85)). Le librerie predefinite forniscono punti di ingresso noti agli utenti, ma poiché il contenuto della libreria non è limitato alle librerie di contenuto di cartelle note, gli utenti possono ottenere maggiore libertà per determinare la posizione in cui archiviare documenti e supporti. Le librerie vengono esposte tramite lo spazio dei nomi della shell (origine dati della Shell). L'applicazione può fornire agli utenti gli stessi punti di ingresso noti ai propri dati abilitando la conoscenza della libreria e l'esplorazione.

### <a name="collections-of-folders"></a>Raccolte di cartelle

Le librerie sono raccolte di contenuto definite dall'utente. Windows Search indicizza le cartelle supportate quando sono incluse nelle librerie. In questo modo è possibile abilitare la ricerca immediata e le visualizzazioni di disposizione dello stack basate su proprietà nelle librerie.

### <a name="supported-folders-in-libraries"></a>Cartelle supportate nelle librerie

Per poter supportare le cartelle nelle librerie, è necessario che siano indicizzabili nel computer locale e indicizzate in un computer Windows remoto oppure indicizzate in un server con file indicizzati da Windows Search.

Le cartelle non supportate vengono bloccate dall'aggiunta degli utenti nella finestra di dialogo Gestione libreria Windows. Se le cartelle remote non indicizzate vengono aggiunte a una libreria tramite l'API [IShellLibrary](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishelllibrary) , l'esperienza utente della libreria verrà ripristinata in **modalità provvisoria**. Nelle funzionalità della **modalità provvisoria** , ad esempio le visualizzazioni di disposizione dello stack basate su proprietà, i suggerimenti per i filtri e il supporto per la ricerca dei **menu Start** vengono rimossi dalla libreria interessata.

Nella tabella seguente sono elencate le cartelle incluse nelle librerie utilizzando la finestra di dialogo Gestione libreria Esplora risorse e le cartelle non supportate in **modalità provvisoria**:

| Cartelle supportate                                                                                                                            | Cartelle non supportate                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| Dischi rigidi NTFS e FAT32 fissi ed esterni                                                                                                | Unità rimovibili (ad esempio Thumbdrives e schede SD)                                                     |
| Condivisioni indicizzate da ricerca di Windows (ad esempio i server di reparto e nei computer che eseguono Windows 10 e Windows 7 Home Edition) | Supporti rimovibili, ad esempio CD e DVD                                                                  |
| Condivisioni disponibili offline, ad esempio **Reindirizzamento documenti**, **cache lato client**                                               | Condivisioni di rete non disponibili né offline né indicizzate in modalità remota, ad esempio unità NAS             |
| n/d                                                                                                                                          | Altre origini dati, ad esempio Microsoft SharePoint, Microsoft Exchange, Microsoft OneDrive e così via. |

### <a name="storage-backed"></a>Storage-Backed

Le librerie sono raccolte di cartelle di archiviazione. Gli utenti possono salvare e copiare i file direttamente in una raccolta, poiché ogni libreria dispone di un percorso di salvataggio predefinito a cui inviare tali file. Per le librerie predefinite, si tratta di una cartella nota dall'utente inclusa in una libreria, ad esempio **documenti**, oppure la prima cartella aggiunta a una libreria personalizzata. Si tratta della cartella in cui i file vengono inseriti quando un utente trascina e rilascia i file in una raccolta o li salva in una raccolta con la finestra di dialogo file comune. L'utente può modificare il percorso di salvataggio predefinito di una libreria in qualsiasi momento, ma se rimuove il percorso di salvataggio predefinito, la cartella successiva nella libreria verrà selezionata come nuovo percorso di salvataggio. Gli utenti possono inoltre salvare le cartelle per le quali dispongono delle autorizzazioni incluse in una raccolta.

### <a name="non-file-system-shell-containers"></a>Contenitori della shell non del file System

Le librerie possono contenere contenitori della shell file system, ad esempio il **computer** e il **Pannello di controllo**, ma contengono file System elementi. È possibile enumerare e accedere alle cartelle e ai contenuti della libreria usando le API per file system file e cartelle nei sistemi operativi precedenti. Se l'applicazione dipende molto da file system API specifiche, l'API [IShellLibrary](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishelllibrary) può essere usata per ottenere i percorsi di file System di cartelle e file all'interno delle librerie. Nella maggior parte dei casi è consigliabile usare il modello di programmazione della Shell per supportare più versioni di Windows e la flessibilità degli elementi. Per ulteriori informazioni, vedere [spostamento nello spazio dei nomi della shell](https://msdn.microsoft.com/library/dd378496(VS.85).aspx).

### <a name="library-descriptions"></a>Descrizioni delle librerie

Le descrizioni delle librerie vengono salvate su disco come file XML nella cartella% AppData% Microsoft \\ Windows \\ Libraries e potenzialmente come **\_ librerie FOLDERID**. Per ulteriori informazioni sulle **\_ librerie FOLDERID**, vedere [KNOWNFOLDERID](/windows/desktop/shell/knownfolderid).

I file di descrizione della libreria sono file XML con estensione del nome file. library-ms. I file non devono essere mai accessibili o modificati dalle applicazioni. Il testo del percorso della cartella salvato in modo permanente nei file di descrizione della libreria non è sempre aggiornato. Le cartelle di libreria vengono rese permanente nel file di descrizione della libreria nel formato di [collegamenti della shell](/windows/desktop/shell/links) binaria serializzata. Per ulteriori informazioni sulle librerie e sullo schema di descrizione della libreria, vedere [Library Description schema](../shell/library-schema-entry.md). Per altre informazioni sui connettori di ricerca federati e sullo schema di descrizione del connettore di ricerca, [cercare Connector Description schema](search-sconn-desc-schema-entry.md).

> [NOTA]  
> Le applicazioni devono sempre usare il modello di programmazione shell o l'API [IShellLibrary](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishelllibrary) per utilizzare e modificare il contenuto della libreria e non tentare mai di accedere o modificare manualmente il file di descrizione della libreria.

## <a name="related-topics"></a>Argomenti correlati

[Ricerca di Windows 7](./-search-3x-wds-overview.md)

[Novità per ricerca Windows 7](new-for-windows-7-search.md)

[Indicizzazione delle priorità e degli eventi del set di righe in Windows 7](indexing-prioritization-and-rowset-events.md)