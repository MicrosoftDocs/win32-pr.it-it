---
description: Questo argomento descrive le librerie e come possono essere vantaggiose per utenti e sviluppatori.
ms.assetid: D5F5FE96-11D2-4fc5-A68B-6E594C09BE20
title: Informazioni sulle librerie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14e63aef55513fb36f9a3cbfa71c1b7a79040fd7848468bd1216779cd034132d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118049324"
---
# <a name="about-libraries"></a>Informazioni sulle librerie

Questo argomento descrive le librerie e come possono essere vantaggiose per utenti e sviluppatori.

Le librerie sono raccolte di cartelle definite dall'utente. Una libreria tiene traccia della posizione di archiviazione fisica di ogni cartella, che allevia l'utente e il software di tale attività. Gli utenti possono raggruppare le cartelle correlate in una raccolta anche se tali cartelle sono archiviate in dischi rigidi o computer diversi.

In una libreria, le cartelle e i file vengono visualizzati all'utente come una singola raccolta e, usando l'API della libreria shell, il contenuto della libreria può anche apparire in un'unica posizione di un programma.

In una raccolta, il contenuto, ad esempio i documenti, le foto, i video o la musica di un utente, può essere ordinato e visualizzato come richiesto dall'utente e non semplicemente come richiesto dal file system. Ad esempio, gli utenti possono organizzare il contenuto di una libreria usando le proprietà degli elementi nella libreria in modo che gli elementi correlati siano ordinati insieme anche se sono archiviati in cartelle diverse.

![Screenshot dell'interfaccia utente delle librerie](images/libraries-whatare.png)

In questo argomento

-   [Vantaggi della libreria](#library-benefits)
    -   [Vantaggi per gli utenti](#user-benefits)
    -   [Vantaggi per gli sviluppatori](#developer-benefits)
-   [Gestione di cartelle nelle librerie](#managing-folders-in-libraries)
-   [Argomenti correlati](#related-topics)

## <a name="library-benefits"></a>Vantaggi della libreria

Questa sezione descrive alcuni dei vantaggi delle librerie dal punto di vista dell'utente finale e dal punto di vista dello sviluppatore del programma.

### <a name="user-benefits"></a>Vantaggi per gli utenti

L'aggiunta del supporto della libreria al programma offre all'utente i vantaggi seguenti:

-   **Le librerie offrono un'interfaccia utente coerente in Windows 7**

    Le finestre di dialogo file comuni supportano le librerie e offrono la stessa esperienza utente di Windows Explorer in Windows 7. Le librerie di supporto nel programma consentono un'interazione più semplice per l'utente quando usa il programma in Windows 7.

-   **Gli utenti decidono dove archiviare il contenuto**

    Le librerie consentono agli utenti di controllare la posizione di archiviazione del contenuto. Allo stesso tempo, le librerie forniscono impostazioni predefinite ragionevoli per gli utenti che non vogliono gestire tale livello di dettaglio nel computer. Gli utenti decidono quanto, o quanto poco, controllare se vogliono esercitarsi su dove e come viene archiviato il contenuto e la raccolta funziona correttamente in entrambi i casi.

### <a name="developer-benefits"></a>Vantaggi per gli sviluppatori

È possibile usare le librerie nel programma per fornire un'interfaccia utente più flessibile e pratica senza dover aggiungere molto codice di programma complesso. Alcuni dei vantaggi dell'aggiunta del supporto della libreria includono:

-   **Le librerie supportano l'accesso a librerie e file system**

    Usando [**l'API della libreria shell**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary), i programmi possono fornire all'utente il supporto della libreria riducendo al tempo stesso la complessità del codice di gestione di file e cartelle. Se il programma usa già l'API del file system, è possibile conservare la quantità di codice esistente desiderata e fornire comunque il supporto della libreria all'utente ottenendo le informazioni necessarie sul file system **dall'API** della libreria shell .

-   **Notifica di modifica più semplice**

    Sia il file system che l'API shell possono inviare una notifica al programma quando il contenuto di una cartella monitorata o di una libreria cambia. Usando l'API shell, tuttavia, è possibile monitorare tutte le cartelle nella libreria con una singola notifica, anche se la cartella nella libreria può essere archiviata in unità diverse o anche in computer diversi.

-   **Le librerie usano le proprietà dei file**

    I programmi possono utilizzare le proprietà dei file per controllare quali file vengono visualizzati durante le operazioni di apertura e salvataggio che utilizzano le finestre di dialogo comuni dei file. I programmi possono anche avere accesso alle proprietà dei file usando [**le interfacce IPropertyStore.**](/windows/win32/api/propsys/nn-propsys-ipropertystore) Le finestre di dialogo file comuni possono essere configurate anche per consentire agli utenti di aggiornare le proprietà associate al relativo contenuto.

-   **I programmi possono creare librerie dedicate**

    È possibile creare una nuova libreria quando le librerie utente esistenti non soddisfano le esigenze del programma, ad esempio se un programma crea un nuovo tipo di contenuto utente. La nuova libreria può essere configurata con un'icona univoca che ne rappresenta il contenuto e semplifica l'identificazione della raccolta in Windows Explorer.

## <a name="managing-folders-in-libraries"></a>Gestione di cartelle nelle librerie

Gli utenti possono organizzare le librerie aggiungendo, spostando o rimuovendo cartelle nella libreria. Non tutte le cartelle, tuttavia, supportano tutte le funzionalità che possono essere fornite da una libreria. Molte funzionalità della libreria richiedono l'accesso rapido alle diverse proprietà della cartella e al relativo contenuto disponibili solo tramite Windows ricerca. Per fornire la funzionalità completa della libreria, è necessario che una cartella possa essere indicizzata Windows ricerca.

Una libreria non consente a un utente di aggiungere cartelle che non forniscono la funzionalità completa della libreria. [**L'API della libreria shell**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary) può tuttavia aggiungere tali cartelle. Se una libreria contiene una cartella che non supporta la funzionalità completa della libreria, la libreria funzionerà in modalità sicura e fornirà una funzionalità limitata. Nella tabella seguente vengono descritte le cartelle che supportano la funzionalità di libreria completa e quelle che non lo supportano.



| Tipi di cartelle che supportano la funzionalità di libreria completa                                                               | Tipi di cartelle che non supportano la funzionalità di libreria completa                                  |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| Dischi rigidi NTFS e FAT32 fissi ed esterni.                                                                     | Unità rimovibili, ad esempio unità flash USB o schede di memoria SD (Secure Digital).               |
| Condivisioni file indicizzate da Windows ricerca, ad esempio server di reparto, Windows 7 o pc Windows Vista home. | Supporti rimovibili, ad esempio supporti CD-ROM o DVD.                                                 |
| Condivisioni file disponibili offline, ad  esempio una cartella Documenti o una Client-Side cache.        | Condivisioni di rete che non sono disponibili offline né indicizzate in remoto, ad esempio le unità NAS.   |
|                                                                                                                    | Altre origini dati, ad esempio Microsoft SharePoint, Microsoft Exchange e Microsoft OneDrive. |



 

L'immagine seguente mostra la visualizzazione limitata del contenuto della libreria in modalità sicura.

![Aprire la finestra di dialogo quando le librerie sono in modalità sicura](images/libraries-supportedfolders.png)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sulle librerie](library-leverage-to-manage-folders.md)
</dt> <dt>

[**Libreria IShell**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary)
</dt> <dt>

[Collegamenti della shell](./links.md)
</dt> <dt>

[Cartelle note](known-folders.md)
</dt> <dt>

[Schema di descrizione della libreria](library-schema-entry.md)
</dt> </dl>

 

 
