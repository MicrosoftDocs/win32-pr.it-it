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
# <a name="about-libraries"></a><span data-ttu-id="c237c-103">Informazioni sulle librerie</span><span class="sxs-lookup"><span data-stu-id="c237c-103">About Libraries</span></span>

<span data-ttu-id="c237c-104">In questo argomento vengono descritte le librerie e il modo in cui possono trarre vantaggio da utenti e sviluppatori.</span><span class="sxs-lookup"><span data-stu-id="c237c-104">This topic describes what libraries are and how they can benefit users and developers.</span></span>

<span data-ttu-id="c237c-105">Le librerie sono raccolte di cartelle definite dall'utente.</span><span class="sxs-lookup"><span data-stu-id="c237c-105">Libraries are user-defined collections of folders.</span></span> <span data-ttu-id="c237c-106">Una libreria tiene traccia della posizione di archiviazione fisica di ogni cartella, che consente di alleggerire l'utente e il software di tale attività.</span><span class="sxs-lookup"><span data-stu-id="c237c-106">A library keeps track of each folder's physical storage location, which relieves the user and the software of that task.</span></span> <span data-ttu-id="c237c-107">Gli utenti possono raggruppare le cartelle correlate in una raccolta anche se tali cartelle vengono archiviate in dischi rigidi diversi o in computer diversi.</span><span class="sxs-lookup"><span data-stu-id="c237c-107">Users can group related folders together in a library even if those folders are stored on different hard drives or different computers.</span></span>

<span data-ttu-id="c237c-108">In una raccolta, le cartelle e i file vengono visualizzati all'utente come una singola raccolta e, usando l'API della libreria shell, il contenuto della libreria può anche apparire in un'unica posizione per un programma.</span><span class="sxs-lookup"><span data-stu-id="c237c-108">In a library, the folders and files appear to the user as a single collection and, using the Shell Library API, the library's contents can also appear to be in a single location to a program.</span></span>

<span data-ttu-id="c237c-109">In una raccolta, il contenuto, ad esempio i documenti, le foto, i video o la musica di un utente, può essere ordinato e visualizzato quando l'utente desidera e non semplicemente come il file system richiede.</span><span class="sxs-lookup"><span data-stu-id="c237c-109">In a library, the contents, such as a user's documents, photos, videos, or music, can be sorted and displayed as the user wants and not simply as how the file system requires.</span></span> <span data-ttu-id="c237c-110">Gli utenti possono ad esempio organizzare il contenuto di una libreria usando le proprietà degli elementi della libreria, in modo che gli elementi correlati vengano ordinati insieme anche se vengono archiviati in cartelle diverse.</span><span class="sxs-lookup"><span data-stu-id="c237c-110">For example, users can organize the contents of a library using the properties of the items in the library so that related items will sort together even if they are stored in different folders.</span></span>

![screenshot dell'interfaccia utente delle librerie](images/libraries-whatare.png)

<span data-ttu-id="c237c-112">In questo argomento</span><span class="sxs-lookup"><span data-stu-id="c237c-112">In this topic:</span></span>

-   [<span data-ttu-id="c237c-113">Vantaggi della libreria</span><span class="sxs-lookup"><span data-stu-id="c237c-113">Library Benefits</span></span>](#library-benefits)
    -   [<span data-ttu-id="c237c-114">Vantaggi dell'utente</span><span class="sxs-lookup"><span data-stu-id="c237c-114">User Benefits</span></span>](#user-benefits)
    -   [<span data-ttu-id="c237c-115">Vantaggi per gli sviluppatori</span><span class="sxs-lookup"><span data-stu-id="c237c-115">Developer Benefits</span></span>](#developer-benefits)
-   [<span data-ttu-id="c237c-116">Gestione delle cartelle nelle librerie</span><span class="sxs-lookup"><span data-stu-id="c237c-116">Managing Folders in Libraries</span></span>](#managing-folders-in-libraries)
-   [<span data-ttu-id="c237c-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c237c-117">Related topics</span></span>](#related-topics)

## <a name="library-benefits"></a><span data-ttu-id="c237c-118">Vantaggi della libreria</span><span class="sxs-lookup"><span data-stu-id="c237c-118">Library Benefits</span></span>

<span data-ttu-id="c237c-119">Questa sezione descrive alcuni dei vantaggi delle librerie dal punto di vista dell'utente finale e dal punto di vista dello sviluppatore del programma.</span><span class="sxs-lookup"><span data-stu-id="c237c-119">This section describes some of the benefits of libraries from the end-user's perspective and the program developer's perspective.</span></span>

### <a name="user-benefits"></a><span data-ttu-id="c237c-120">Vantaggi dell'utente</span><span class="sxs-lookup"><span data-stu-id="c237c-120">User Benefits</span></span>

<span data-ttu-id="c237c-121">L'aggiunta del supporto per le librerie al programma offre i seguenti vantaggi all'utente:</span><span class="sxs-lookup"><span data-stu-id="c237c-121">Adding library support to your program provides the following benefits to the user:</span></span>

-   <span data-ttu-id="c237c-122">**Le librerie forniscono un'interfaccia utente coerente in Windows 7**</span><span class="sxs-lookup"><span data-stu-id="c237c-122">**Libraries provide a consistent user interface in Windows 7**</span></span>

    <span data-ttu-id="c237c-123">Le finestre di dialogo file comuni supportano le librerie e offrono la stessa esperienza utente di Esplora risorse in Windows 7.</span><span class="sxs-lookup"><span data-stu-id="c237c-123">The common file dialog boxes support libraries and provide the same user experience as the Windows Explorer in Windows 7.</span></span> <span data-ttu-id="c237c-124">Le librerie di supporto nel programma contribuiranno a offrire un'interazione più semplice per l'utente quando si usa il programma in Windows 7.</span><span class="sxs-lookup"><span data-stu-id="c237c-124">Supporting libraries in your program will help provide a more seamless interaction for the user when using your program in Windows 7.</span></span>

-   <span data-ttu-id="c237c-125">**Utenti che decidono dove archiviare il contenuto**</span><span class="sxs-lookup"><span data-stu-id="c237c-125">**Users decide where to store content**</span></span>

    <span data-ttu-id="c237c-126">Le librerie consentono agli utenti di controllare la posizione in cui è archiviato il contenuto.</span><span class="sxs-lookup"><span data-stu-id="c237c-126">Libraries make it possible for users to control where their content is stored.</span></span> <span data-ttu-id="c237c-127">Allo stesso tempo, le librerie forniscono impostazioni predefinite ragionevoli per gli utenti che non desiderano gestire il livello di dettaglio nel computer.</span><span class="sxs-lookup"><span data-stu-id="c237c-127">At the same time, libraries provide reasonable defaults for users who do not want to manage that level of detail in their computer.</span></span> <span data-ttu-id="c237c-128">Gli utenti decidono quanto, o quanto meno, il controllo che vogliono esercitare su dove e come viene archiviato il contenuto e la libreria funziona correttamente in entrambi i casi.</span><span class="sxs-lookup"><span data-stu-id="c237c-128">Users decide how much, or how little, control they want to exercise over where and how their content is stored and the library works fine either way.</span></span>

### <a name="developer-benefits"></a><span data-ttu-id="c237c-129">Vantaggi per gli sviluppatori</span><span class="sxs-lookup"><span data-stu-id="c237c-129">Developer Benefits</span></span>

<span data-ttu-id="c237c-130">È possibile utilizzare le librerie del programma per fornire un'interfaccia utente più flessibile e comoda senza dover aggiungere una grande quantità di codice programma complesso.</span><span class="sxs-lookup"><span data-stu-id="c237c-130">You can use libraries in your program to provide a more flexible and convenient user interface without having to add a lot of complex program code.</span></span> <span data-ttu-id="c237c-131">Di seguito sono riportati alcuni dei vantaggi offerti dall'aggiunta del supporto per le librerie:</span><span class="sxs-lookup"><span data-stu-id="c237c-131">Some of the advantages of adding library support include:</span></span>

-   <span data-ttu-id="c237c-132">**Librerie di supporto libreria e accesso al file System**</span><span class="sxs-lookup"><span data-stu-id="c237c-132">**Libraries support library and file-system access**</span></span>

    <span data-ttu-id="c237c-133">Usando l' [**API della libreria shell**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary), i programmi possono fornire supporto per le librerie per l'utente, riducendo la complessità del codice di gestione di file e cartelle.</span><span class="sxs-lookup"><span data-stu-id="c237c-133">Using the [**Shell Library API**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary), programs can provide library support for the user while reducing the complexity of their file and folder management code.</span></span> <span data-ttu-id="c237c-134">Se il programma usa già l'API del file System, è possibile conservare il maggior parte del codice esistente desiderato e fornire comunque supporto per la libreria all'utente ottenendo le informazioni necessarie sul file System dall' **API della libreria della shell**.</span><span class="sxs-lookup"><span data-stu-id="c237c-134">If your program already uses the file-system API, you can preserve as much of that existing code as you want and still provide library support to the user by getting the necessary file-system information from the **Shell Library API**.</span></span>

-   <span data-ttu-id="c237c-135">**Notifica di modifica più semplice**</span><span class="sxs-lookup"><span data-stu-id="c237c-135">**Simpler change notification**</span></span>

    <span data-ttu-id="c237c-136">Sia il file System che l'API shell possono inviare notifiche al programma quando viene modificato il contenuto di una cartella o di una libreria monitorata.</span><span class="sxs-lookup"><span data-stu-id="c237c-136">Both the file-system and the Shell API can notify your program when the contents of a monitored folder or library change.</span></span> <span data-ttu-id="c237c-137">Usando l'API shell, tuttavia, è possibile monitorare tutte le cartelle nella libreria con una sola notifica, anche se la cartella nella libreria può essere archiviata in unità diverse o anche in computer diversi.</span><span class="sxs-lookup"><span data-stu-id="c237c-137">Using the Shell API, however, you can monitor all the folders in the library with a single notification, even though the folder in the library may be stored on different drives or even different computers.</span></span>

-   <span data-ttu-id="c237c-138">**Le librerie utilizzano le proprietà del file**</span><span class="sxs-lookup"><span data-stu-id="c237c-138">**Libraries use file properties**</span></span>

    <span data-ttu-id="c237c-139">I programmi possono utilizzare le proprietà del file per controllare quali file vengono visualizzati durante le operazioni di apertura e salvataggio che utilizzano le finestre di dialogo file comuni.</span><span class="sxs-lookup"><span data-stu-id="c237c-139">Programs can use the file properties to control which files are displayed during open and save operations that use the common file dialog boxes.</span></span> <span data-ttu-id="c237c-140">I programmi possono anche accedere alle proprietà dei file usando le interfacce [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) .</span><span class="sxs-lookup"><span data-stu-id="c237c-140">Programs can also have access to file properties by using the [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) interfaces.</span></span> <span data-ttu-id="c237c-141">Le finestre di dialogo file comuni possono anche essere configurate consente agli utenti di aggiornare le proprietà associate al relativo contenuto.</span><span class="sxs-lookup"><span data-stu-id="c237c-141">The common file dialog boxes can also be configured allow users to update the properties that are associated with their content.</span></span>

-   <span data-ttu-id="c237c-142">**I programmi possono creare librerie dedicate**</span><span class="sxs-lookup"><span data-stu-id="c237c-142">**Programs can create dedicated libraries**</span></span>

    <span data-ttu-id="c237c-143">È possibile creare una nuova libreria quando le librerie utente esistenti non soddisfano le esigenze del programma, ad esempio se un programma crea un nuovo tipo di contenuto utente.</span><span class="sxs-lookup"><span data-stu-id="c237c-143">A new library can be created when an existing user libraries does not meet the program's needs—for example, if a program creates a new type of user content.</span></span> <span data-ttu-id="c237c-144">La nuova libreria può essere configurata con un'icona univoca che rappresenta il contenuto e rende la libreria semplice da identificare in Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="c237c-144">The new library can be configured with a unique icon that represents their content and makes the library easy to identify in the Windows Explorer.</span></span>

## <a name="managing-folders-in-libraries"></a><span data-ttu-id="c237c-145">Gestione delle cartelle nelle librerie</span><span class="sxs-lookup"><span data-stu-id="c237c-145">Managing Folders in Libraries</span></span>

<span data-ttu-id="c237c-146">Gli utenti possono organizzare le proprie librerie aggiungendo, spostando o rimuovendo cartelle nella libreria.</span><span class="sxs-lookup"><span data-stu-id="c237c-146">Users can organize their libraries by adding, moving, or removing folders in the library.</span></span> <span data-ttu-id="c237c-147">Non tutte le cartelle supportano tuttavia tutte le funzionalità che possono essere fornite da una libreria.</span><span class="sxs-lookup"><span data-stu-id="c237c-147">Not all folders, however, support all the functionality that a library can provide.</span></span> <span data-ttu-id="c237c-148">Molte funzionalità della libreria richiedono accesso rapido alle diverse proprietà della cartella e al relativo contenuto disponibili solo tramite la ricerca di Windows.</span><span class="sxs-lookup"><span data-stu-id="c237c-148">Many library features require quick access to the different properties of the folder and its contents that are only available through Windows Search.</span></span> <span data-ttu-id="c237c-149">Per fornire funzionalità complete della libreria, è necessario che una cartella possa essere indicizzata tramite la ricerca di Windows.</span><span class="sxs-lookup"><span data-stu-id="c237c-149">To provide full library functionality, a folder must be able to be indexed by Windows Search.</span></span>

<span data-ttu-id="c237c-150">Una libreria non consente a un utente di aggiungere cartelle che non offrono funzionalità complete della libreria.</span><span class="sxs-lookup"><span data-stu-id="c237c-150">A library does not allow a user to add folders that do not provide full library functionality.</span></span> <span data-ttu-id="c237c-151">Tuttavia, l' [**API della libreria shell**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary) può aggiungere tali cartelle.</span><span class="sxs-lookup"><span data-stu-id="c237c-151">The [**Shell Library API**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary) can, however, add such folders.</span></span> <span data-ttu-id="c237c-152">Se una raccolta contiene una cartella che non supporta la funzionalità di libreria completa, la libreria funzionerà in modalità provvisoria e fornirà una funzionalità limitata.</span><span class="sxs-lookup"><span data-stu-id="c237c-152">If a library contains a folder that does not support full library functionality, the library will operate in a safe mode and provide a limited functionality.</span></span> <span data-ttu-id="c237c-153">Nella tabella seguente vengono descritte le cartelle che supportano le funzionalità complete della libreria e quelle che non lo sono.</span><span class="sxs-lookup"><span data-stu-id="c237c-153">The following table describes the folders that support full library functionality and those that do not.</span></span>



| <span data-ttu-id="c237c-154">Tipi di cartelle che supportano la funzionalità della libreria completa</span><span class="sxs-lookup"><span data-stu-id="c237c-154">Folder types that support full library functionality</span></span>                                                               | <span data-ttu-id="c237c-155">Tipi di cartelle che non supportano la funzionalità di libreria completa</span><span class="sxs-lookup"><span data-stu-id="c237c-155">Folder types that do not support full library functionality</span></span>                                  |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c237c-156">Dischi rigidi NTFS e FAT32 fissi ed esterni.</span><span class="sxs-lookup"><span data-stu-id="c237c-156">Fixed and external NTFS and FAT32 hard drives.</span></span>                                                                     | <span data-ttu-id="c237c-157">Unità rimovibili, ad esempio unità flash USB o schede di memoria digitali sicure (SD).</span><span class="sxs-lookup"><span data-stu-id="c237c-157">Removable drives such as USB flash drives or Secure Digital (SD) memory cards.</span></span>               |
| <span data-ttu-id="c237c-158">Condivisioni file indicizzate da ricerca di Windows, ad esempio server di reparto, Windows 7 o PC Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="c237c-158">File shares that are indexed by Windows Search such as departmental servers, Windows 7, or Windows Vista home PCs.</span></span> | <span data-ttu-id="c237c-159">Supporti rimovibili, ad esempio CD-ROM o DVD.</span><span class="sxs-lookup"><span data-stu-id="c237c-159">Removable media such as CD-ROM or DVD media.</span></span>                                                 |
| <span data-ttu-id="c237c-160">Condivisioni file disponibili offline, ad esempio una cartella **documenti** reindirizzata o una cache Client-Side.</span><span class="sxs-lookup"><span data-stu-id="c237c-160">File shares that are available offline such as a redirected **My Documents** folder or a Client-Side Cache.</span></span>        | <span data-ttu-id="c237c-161">Condivisioni di rete non disponibili né offline né indicizzate in modalità remota, ad esempio unità NAS.</span><span class="sxs-lookup"><span data-stu-id="c237c-161">Network shares that are neither available offline nor remotely indexed such as NAS drives.</span></span>   |
|                                                                                                                    | <span data-ttu-id="c237c-162">Altre origini dati, ad esempio Microsoft SharePoint, Microsoft Exchange e Microsoft OneDrive.</span><span class="sxs-lookup"><span data-stu-id="c237c-162">Other data sources such as Microsoft SharePoint, Microsoft Exchange, and Microsoft OneDrive.</span></span> |



 

<span data-ttu-id="c237c-163">Nell'immagine seguente viene illustrata la visualizzazione limitata del contenuto della libreria in modalità provvisoria.</span><span class="sxs-lookup"><span data-stu-id="c237c-163">The following image shows the limited display of library contents while in safe mode.</span></span>

![Apri la finestra di dialogo quando le librerie sono in modalità provvisoria](images/libraries-supportedfolders.png)

## <a name="related-topics"></a><span data-ttu-id="c237c-165">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c237c-165">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c237c-166">Informazioni sulle librerie</span><span class="sxs-lookup"><span data-stu-id="c237c-166">About Libraries</span></span>](library-leverage-to-manage-folders.md)
</dt> <dt>

[<span data-ttu-id="c237c-167">**IShellLibrary**</span><span class="sxs-lookup"><span data-stu-id="c237c-167">**IShellLibrary**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary)
</dt> <dt>

[<span data-ttu-id="c237c-168">Collegamenti Shell</span><span class="sxs-lookup"><span data-stu-id="c237c-168">Shell Links</span></span>](./links.md)
</dt> <dt>

[<span data-ttu-id="c237c-169">Cartelle note</span><span class="sxs-lookup"><span data-stu-id="c237c-169">Known Folders</span></span>](known-folders.md)
</dt> <dt>

[<span data-ttu-id="c237c-170">Schema Descrizione libreria</span><span class="sxs-lookup"><span data-stu-id="c237c-170">Library Description Schema</span></span>](library-schema-entry.md)
</dt> </dl>

 

 
