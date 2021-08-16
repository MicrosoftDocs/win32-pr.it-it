---
description: Descrive l'introduzione delle librerie per Windows 7.
ms.assetid: 83c47963-4c8e-45ee-b707-bd45cfe048cd
title: Windows Librerie della shell in Windows 7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28f120f1bc4e4208a7e6bbf35bbcfc4717ed05dfb7344658a80b1ea1d9a3ba50
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118969600"
---
# <a name="windows-shell-libraries-in-windows"></a>Windows Librerie della shell in Windows

Questo argomento descrive l'introduzione delle librerie per Windows 7 e versioni successive. Le librerie sono una Windows shell. Per accedere Windows shell, ad esempio librerie, gli sviluppatori di terze parti di Windows ricerca devono prima implementare un archivio dati shell. Per altre informazioni, vedere [Implementazione delle interfacce dell'oggetto cartella di base.](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85))

Questo argomento è organizzato come segue:

- [Raccolte](#libraries)
  - [Punti di immissione dati utente](#user-data-entry-points)
  - [Raccolte di cartelle](#collections-of-folders)
  - [Cartelle supportate nelle librerie](#supported-folders-in-libraries)
  - [Archiviazione supportato](#storage-backed)
  - [Contenitori della shell non file system](#non-file-system-shell-containers)
  - [Descrizioni delle librerie](#library-descriptions)
- [Argomenti correlati](#related-topics)

## <a name="libraries"></a>Librerie

In Windows 7 e versioni successive, le librerie sono il repository predefinito dei dati utente. Gli utenti possono esplorare i file nello stesso modo in cui si farebbe in una cartella oppure possono visualizzare i file disposti in base a proprietà quali data, tipo e autore. A differenza di una cartella, una libreria non archivia effettivamente gli elementi, ma visualizza i file archiviati in più cartelle contemporaneamente. Le librerie forniscono un singolo punto di accesso e pivot di visualizzazione rtf agli utenti del contenuto aggregato. Ad esempio, se un utente dispone di file musicali in cartelle in un'unità esterna oltre alla cartella **My Musica,** sarà in grado di accedere immediatamente a tutti i file musicali tramite la libreria Musica.

### <a name="user-data-entry-points"></a>Punti di immissione dati utente

Le librerie predefinite **(Documenti,** **Immagini** e così via) sono equivalenti a [Cartella nota.](/previous-versions/windows/desktop/legacy/bb776911(v=vs.85)) Le librerie predefinite offrono agli utenti punti di ingresso familiari, ma poiché il contenuto della raccolta non è limitato alle raccolte contenuto cartella nota, offre agli utenti maggiore libertà per determinare dove archiviare documenti e file multimediali. Le librerie vengono esposte tramite lo spazio dei nomi shell (origine dati shell). L'applicazione può fornire agli utenti gli stessi punti di ingresso familiari ai propri dati abilitando la consapevolezza delle librerie e l'esplorazione.

### <a name="collections-of-folders"></a>Raccolte di cartelle

Le librerie sono raccolte di contenuto definite dall'utente. Windows Cerca negli indici le cartelle supportate quando sono incluse nelle librerie. Ciò consente la ricerca immediata e le visualizzazioni di disposizione degli stack basate su proprietà nelle librerie.

### <a name="supported-folders-in-libraries"></a>Cartelle supportate nelle librerie

Per poter essere supportate nelle librerie, le cartelle devono essere indicizzabili nel computer locale e indicizzate in un computer Windows remoto o indicizzate in un server con file indicizzati da ricerca Windows.

Le cartelle non supportate non possono essere aggiunte dagli utenti nella finestra Windows di gestione delle librerie. Se a una libreria vengono aggiunte cartelle remote non indicizzate usando l'API [IShellLibrary,](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishelllibrary) l'esperienza utente della libreria tornerà alla modalità Cassaforte **libreria.** In **Cassaforte** funzionalità come le visualizzazioni di disposizione degli stack basate su proprietà, i suggerimenti di filtro e il supporto per la ricerca nel **menu Start** vengono rimosse dalla libreria interessata.

Nella tabella seguente sono elencate le cartelle incluse nelle librerie tramite la finestra di dialogo gestione librerie di Windows Explorer e le cartelle non supportate in **Cassaforte modalità :**

| Cartelle supportate                                                                                                                            | Cartelle non supportate                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| Dischi rigidi NTFS e FAT32 fissi ed esterni                                                                                                | Unità rimovibili (ad esempio unità di identificazione personale e schede SD)                                                     |
| Condivisioni indicizzate da Ricerca Windows,ad esempio i server di reparto, e nei computer che eseguono Windows 10 e Windows 7 Home Edition) | Supporti rimovibili (ad esempio CD e DVD)                                                                  |
| Condivisioni disponibili offline ,ad esempio **Reindirizzamento Documenti**, **Cache lato client**)                                               | Condivisioni di rete che non sono disponibili offline né indicizzate in remoto (ad esempio unità NAS)             |
| n/d                                                                                                                                          | Altre origini dati (ad esempio Microsoft SharePoint, Microsoft Exchange, Microsoft OneDrive e così via) |

### <a name="storage-backed"></a>Storage-Backed

Le librerie sono raccolte di cartelle di archiviazione. Gli utenti possono salvare e copiare i file direttamente in una raccolta, poiché ogni libreria ha un percorso di salvataggio predefinito a cui inviare i file. Per le librerie predefinite, si tratta della cartella nota dell'utente **inclusa** in una libreria (ad esempio Documenti ) o della prima cartella aggiunta a una libreria personalizzata. Questa è la cartella in cui vengono copiati i file quando un utente trascina e rilascia i file in una libreria o lo salva in una libreria con la finestra di dialogo file comune. L'utente può modificare il percorso di salvataggio predefinito di una raccolta in qualsiasi momento, ma se rimuove il percorso di salvataggio predefinito, la cartella successiva nella raccolta verrà selezionata come nuovo percorso di salvataggio. Gli utenti possono anche salvare in qualsiasi cartella per cui hanno le autorizzazioni incluse in una libreria.

### <a name="non-file-system-shell-containers"></a>Contenitori della shell non file system

Le librerie possono contenere contenitori file system Shell, ad esempio **Computer** **e Pannello di controllo**, ma possono contenere file system contenitori. Le cartelle e il contenuto della libreria possono essere enumerati e accessibili usando le API per file system file e cartelle nei sistemi operativi precedenti. Se l'applicazione dipende in larga parte file system API specifiche, è possibile usare l'API [IShellLibrary](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishelllibrary) per ottenere i percorsi file system di cartelle e file all'interno delle librerie. Nella maggior parte dei casi è consigliabile usare il modello di programmazione Shell per supportare più versioni Windows e flessibilità degli elementi. Per altre informazioni, vedere [Esplorazione dello spazio dei nomi della shell.](https://msdn.microsoft.com/library/dd378496(VS.85).aspx)

### <a name="library-descriptions"></a>Descrizioni delle librerie

Le descrizioni delle librerie vengono salvate su disco come file XML nella cartella %appdata%Microsoft Windows Libraries (e potenzialmente come \\ \\ **FOLDERID \_ Libraries**). Per altre informazioni sulle **librerie FOLDERID \_**, vedere [KNOWNFOLDERID.](/windows/desktop/shell/knownfolderid)

I file di descrizione della libreria sono file XML con estensione library-ms. I file non devono mai essere accessibili o modificati dalle applicazioni. Il testo del percorso della cartella persistente nei file di descrizione della libreria non è sempre corrente. Le cartelle della libreria sono persistenti nel file di descrizione della libreria nel formato binario serializzato [Shell Links.](/windows/desktop/shell/links) Per altre informazioni sulle librerie e sullo schema di descrizione della libreria, vedere [Schema di descrizione della libreria.](../shell/library-schema-entry.md) Per altre informazioni sui connettori di ricerca federati e sullo schema di descrizione del connettore di ricerca, vedere [Schema di descrizione del connettore di ricerca.](search-sconn-desc-schema-entry.md)

> [NOTA]  
> Le applicazioni devono sempre usare il modello di programmazione Shell o l'API [IShellLibrary](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishelllibrary) per utilizzare e modificare il contenuto della libreria e non tentare mai di accedere o modificare manualmente il file di descrizione della libreria.

## <a name="related-topics"></a>Argomenti correlati

[Windows 7 Ricerca](./-search-3x-wds-overview.md)

[Novità per la Windows 7](new-for-windows-7-search.md)

[Indicizzazione di eventi di priorità e set di righe in Windows 7](indexing-prioritization-and-rowset-events.md)