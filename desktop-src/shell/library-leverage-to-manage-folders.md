---
description: In questo argomento vengono descritte le librerie e il modo in cui possono trarre vantaggio da utenti e sviluppatori.
ms.assetid: D5F5FE96-11D2-4fc5-A68B-6E594C09BE20
title: Informazioni sulle librerie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e577e7b5df0a1e072a07a096434af84ff8e2c26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104561171"
---
# <a name="about-libraries"></a>Informazioni sulle librerie

In questo argomento vengono descritte le librerie e il modo in cui possono trarre vantaggio da utenti e sviluppatori.

Le librerie sono raccolte di cartelle definite dall'utente. Una libreria tiene traccia della posizione di archiviazione fisica di ogni cartella, che consente di alleggerire l'utente e il software di tale attività. Gli utenti possono raggruppare le cartelle correlate in una raccolta anche se tali cartelle vengono archiviate in dischi rigidi diversi o in computer diversi.

In una raccolta, le cartelle e i file vengono visualizzati all'utente come una singola raccolta e, usando l'API della libreria shell, il contenuto della libreria può anche apparire in un'unica posizione per un programma.

In una raccolta, il contenuto, ad esempio i documenti, le foto, i video o la musica di un utente, può essere ordinato e visualizzato quando l'utente desidera e non semplicemente come il file system richiede. Gli utenti possono ad esempio organizzare il contenuto di una libreria usando le proprietà degli elementi della libreria, in modo che gli elementi correlati vengano ordinati insieme anche se vengono archiviati in cartelle diverse.

![screenshot dell'interfaccia utente delle librerie](images/libraries-whatare.png)

In questo argomento

-   [Vantaggi della libreria](#library-benefits)
    -   [Vantaggi dell'utente](#user-benefits)
    -   [Vantaggi per gli sviluppatori](#developer-benefits)
-   [Gestione delle cartelle nelle librerie](#managing-folders-in-libraries)
-   [Argomenti correlati](#related-topics)

## <a name="library-benefits"></a>Vantaggi della libreria

Questa sezione descrive alcuni dei vantaggi delle librerie dal punto di vista dell'utente finale e dal punto di vista dello sviluppatore del programma.

### <a name="user-benefits"></a>Vantaggi dell'utente

L'aggiunta del supporto per le librerie al programma offre i seguenti vantaggi all'utente:

-   **Le librerie forniscono un'interfaccia utente coerente in Windows 7**

    Le finestre di dialogo file comuni supportano le librerie e offrono la stessa esperienza utente di Esplora risorse in Windows 7. Le librerie di supporto nel programma contribuiranno a offrire un'interazione più semplice per l'utente quando si usa il programma in Windows 7.

-   **Utenti che decidono dove archiviare il contenuto**

    Le librerie consentono agli utenti di controllare la posizione in cui è archiviato il contenuto. Allo stesso tempo, le librerie forniscono impostazioni predefinite ragionevoli per gli utenti che non desiderano gestire il livello di dettaglio nel computer. Gli utenti decidono quanto, o quanto meno, il controllo che vogliono esercitare su dove e come viene archiviato il contenuto e la libreria funziona correttamente in entrambi i casi.

### <a name="developer-benefits"></a>Vantaggi per gli sviluppatori

È possibile utilizzare le librerie del programma per fornire un'interfaccia utente più flessibile e comoda senza dover aggiungere una grande quantità di codice programma complesso. Di seguito sono riportati alcuni dei vantaggi offerti dall'aggiunta del supporto per le librerie:

-   **Librerie di supporto libreria e accesso al file System**

    Usando l' [**API della libreria shell**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary), i programmi possono fornire supporto per le librerie per l'utente, riducendo la complessità del codice di gestione di file e cartelle. Se il programma usa già l'API del file System, è possibile conservare il maggior parte del codice esistente desiderato e fornire comunque supporto per la libreria all'utente ottenendo le informazioni necessarie sul file System dall' **API della libreria della shell**.

-   **Notifica di modifica più semplice**

    Sia il file System che l'API shell possono inviare notifiche al programma quando viene modificato il contenuto di una cartella o di una libreria monitorata. Usando l'API shell, tuttavia, è possibile monitorare tutte le cartelle nella libreria con una sola notifica, anche se la cartella nella libreria può essere archiviata in unità diverse o anche in computer diversi.

-   **Le librerie utilizzano le proprietà del file**

    I programmi possono utilizzare le proprietà del file per controllare quali file vengono visualizzati durante le operazioni di apertura e salvataggio che utilizzano le finestre di dialogo file comuni. I programmi possono anche accedere alle proprietà dei file usando le interfacce [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) . Le finestre di dialogo file comuni possono anche essere configurate consente agli utenti di aggiornare le proprietà associate al relativo contenuto.

-   **I programmi possono creare librerie dedicate**

    È possibile creare una nuova libreria quando le librerie utente esistenti non soddisfano le esigenze del programma, ad esempio se un programma crea un nuovo tipo di contenuto utente. La nuova libreria può essere configurata con un'icona univoca che rappresenta il contenuto e rende la libreria semplice da identificare in Esplora risorse.

## <a name="managing-folders-in-libraries"></a>Gestione delle cartelle nelle librerie

Gli utenti possono organizzare le proprie librerie aggiungendo, spostando o rimuovendo cartelle nella libreria. Non tutte le cartelle supportano tuttavia tutte le funzionalità che possono essere fornite da una libreria. Molte funzionalità della libreria richiedono accesso rapido alle diverse proprietà della cartella e al relativo contenuto disponibili solo tramite la ricerca di Windows. Per fornire funzionalità complete della libreria, è necessario che una cartella possa essere indicizzata tramite la ricerca di Windows.

Una libreria non consente a un utente di aggiungere cartelle che non offrono funzionalità complete della libreria. Tuttavia, l' [**API della libreria shell**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary) può aggiungere tali cartelle. Se una raccolta contiene una cartella che non supporta la funzionalità di libreria completa, la libreria funzionerà in modalità provvisoria e fornirà una funzionalità limitata. Nella tabella seguente vengono descritte le cartelle che supportano le funzionalità complete della libreria e quelle che non lo sono.



| Tipi di cartelle che supportano la funzionalità della libreria completa                                                               | Tipi di cartelle che non supportano la funzionalità di libreria completa                                  |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| Dischi rigidi NTFS e FAT32 fissi ed esterni.                                                                     | Unità rimovibili, ad esempio unità flash USB o schede di memoria digitali sicure (SD).               |
| Condivisioni file indicizzate da ricerca di Windows, ad esempio server di reparto, Windows 7 o PC Windows Vista. | Supporti rimovibili, ad esempio CD-ROM o DVD.                                                 |
| Condivisioni file disponibili offline, ad esempio una cartella **documenti** reindirizzata o una cache Client-Side.        | Condivisioni di rete non disponibili né offline né indicizzate in modalità remota, ad esempio unità NAS.   |
|                                                                                                                    | Altre origini dati, ad esempio Microsoft SharePoint, Microsoft Exchange e Microsoft OneDrive. |



 

Nell'immagine seguente viene illustrata la visualizzazione limitata del contenuto della libreria in modalità provvisoria.

![Apri la finestra di dialogo quando le librerie sono in modalità provvisoria](images/libraries-supportedfolders.png)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sulle librerie](library-leverage-to-manage-folders.md)
</dt> <dt>

[**IShellLibrary**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary)
</dt> <dt>

[Collegamenti Shell](./links.md)
</dt> <dt>

[Cartelle note](known-folders.md)
</dt> <dt>

[Schema Descrizione libreria](library-schema-entry.md)
</dt> </dl>

 

 
