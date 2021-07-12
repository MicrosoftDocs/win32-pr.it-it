---
description: Shell offre diversi modi per gestire i file system.
ms.assetid: d9ffda6f-adc0-44a3-b410-e23bf5f4f165
title: Gestione del file system
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee0f3b47e17e691c540a9775f3b8588b311b9878
ms.sourcegitcommit: 822413efb4a70dd464e5db4d9e8693ef74f8132f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/09/2021
ms.locfileid: "113581619"
---
# <a name="managing-the-file-system"></a><span data-ttu-id="1344a-103">Gestione del file system</span><span class="sxs-lookup"><span data-stu-id="1344a-103">Managing the File System</span></span>

<span data-ttu-id="1344a-104">Shell offre diversi modi per gestire i file system.</span><span class="sxs-lookup"><span data-stu-id="1344a-104">The Shell provides a number of ways to manage file systems.</span></span> <span data-ttu-id="1344a-105">Shell fornisce una funzione, [**SHFileOperation**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa), che consente a un'applicazione di spostare, copiare, rinominare ed eliminare file a livello di codice.</span><span class="sxs-lookup"><span data-stu-id="1344a-105">The Shell provides a function, [**SHFileOperation**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa), that allows an application to programmatically move, copy, rename, and delete files.</span></span> <span data-ttu-id="1344a-106">Shell supporta anche alcune funzionalità di gestione dei file aggiuntive.</span><span class="sxs-lookup"><span data-stu-id="1344a-106">The Shell also supports some additional file management capabilities.</span></span>

-   <span data-ttu-id="1344a-107">I documenti HTML possono *essere connessi* a file correlati, ad esempio file di grafica o fogli di stile.</span><span class="sxs-lookup"><span data-stu-id="1344a-107">HTML documents can be *connected* to related files, such as graphics files or style sheets.</span></span> <span data-ttu-id="1344a-108">Quando il documento viene spostato o copiato, anche i file connessi vengono spostati o copiati automaticamente.</span><span class="sxs-lookup"><span data-stu-id="1344a-108">When the document is moved or copied, the connected files are automatically moved or copied as well.</span></span>
-   <span data-ttu-id="1344a-109">Per i sistemi disponibili per più utenti, i file possono essere gestiti in base all'utente.</span><span class="sxs-lookup"><span data-stu-id="1344a-109">For systems that are available to more than one user, files can be managed on a per-user basis.</span></span> <span data-ttu-id="1344a-110">Gli utenti possono accedere facilmente ai file di dati, ma non ai file appartenenti ad altri utenti.</span><span class="sxs-lookup"><span data-stu-id="1344a-110">Users have easy access to their data files, but not to files belonging to other users.</span></span>
-   <span data-ttu-id="1344a-111">Se i file di documento vengono aggiunti o modificati, possono essere aggiunti all'elenco di documenti recenti della shell.</span><span class="sxs-lookup"><span data-stu-id="1344a-111">If document files are added or modified, they can be added to the Shell's list of recent documents.</span></span> <span data-ttu-id="1344a-112">Quando l'utente fa clic **sul comando** Documenti nel menu Start, viene visualizzato un elenco di collegamenti ai documenti.</span><span class="sxs-lookup"><span data-stu-id="1344a-112">When the user clicks the **Documents** command on the Start menu, a list of links to the documents appears.</span></span>

<span data-ttu-id="1344a-113">Questo documento illustra il funzionamento di queste tecnologie di gestione dei file.</span><span class="sxs-lookup"><span data-stu-id="1344a-113">This document discusses how these file management technologies work.</span></span> <span data-ttu-id="1344a-114">Descrive quindi come usare Shell per spostare, copiare, rinominare ed eliminare file e come gestire gli oggetti nel Cestino.</span><span class="sxs-lookup"><span data-stu-id="1344a-114">It then outlines how to use the Shell to move, copy, rename, and delete files, and how to manage objects in the Recycle Bin.</span></span>

-   [<span data-ttu-id="1344a-115">Gestione file per utente</span><span class="sxs-lookup"><span data-stu-id="1344a-115">Per-User File Management</span></span>](#per-user-file-management)
-   [<span data-ttu-id="1344a-116">cartelle Documenti e Immagini personali</span><span class="sxs-lookup"><span data-stu-id="1344a-116">My Documents and My Pictures Folders</span></span>](#my-documents-and-my-pictures-folders)
-   [<span data-ttu-id="1344a-117">File connessi</span><span class="sxs-lookup"><span data-stu-id="1344a-117">Connected Files</span></span>](#connected-files)
-   [<span data-ttu-id="1344a-118">Spostamento, copia, ridenominazione ed eliminazione di file</span><span class="sxs-lookup"><span data-stu-id="1344a-118">Moving, Copying, Renaming, and Deleting Files</span></span>](#moving-copying-renaming-and-deleting-files)
    -   [<span data-ttu-id="1344a-119">Notifica alla shell</span><span class="sxs-lookup"><span data-stu-id="1344a-119">Notifying the Shell</span></span>](#notifying-the-shell)
-   [<span data-ttu-id="1344a-120">Esempio semplice di gestione dei file con SHFileOperation</span><span class="sxs-lookup"><span data-stu-id="1344a-120">Simple Example of Managing Files with SHFileOperation</span></span>](#simple-example-of-managing-files-with-shfileoperation)
-   [<span data-ttu-id="1344a-121">Aggiunta di file all'elenco di documenti recenti della shell</span><span class="sxs-lookup"><span data-stu-id="1344a-121">Adding Files to the Shell's List of Recent Documents</span></span>](#adding-files-to-the-shells-list-of-recent-documents)

## <a name="per-user-file-management"></a><span data-ttu-id="1344a-122">Per-User Gestione file</span><span class="sxs-lookup"><span data-stu-id="1344a-122">Per-User File Management</span></span>

<span data-ttu-id="1344a-123">La Windows 2000 Shell consente di associare i file a un determinato utente in modo che i file rimangano nascosti ad altri utenti.</span><span class="sxs-lookup"><span data-stu-id="1344a-123">The Windows 2000 Shell allows files to be associated with a particular user so the files remain hidden from other users.</span></span> <span data-ttu-id="1344a-124">In termini di file system, i file vengono archiviati nella cartella del profilo dell'utente, in genere C: Documents e Impostazioni Username nei sistemi \\ \\  \\ Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="1344a-124">In terms of the file system, the files are stored under the user's profile folder, typically C:\\Documents and Settings\\*Username*\\ on Windows 2000 systems.</span></span> <span data-ttu-id="1344a-125">Questa funzionalità consente a molti utenti di usare lo stesso computer, mantenendo la privacy dei file di altri utenti.</span><span class="sxs-lookup"><span data-stu-id="1344a-125">This feature allows many individuals to use the same computer, while maintaining the privacy of their files from other users.</span></span> <span data-ttu-id="1344a-126">Per utenti diversi possono essere disponibili programmi diversi.</span><span class="sxs-lookup"><span data-stu-id="1344a-126">Different users can have different programs available.</span></span> <span data-ttu-id="1344a-127">Offre anche un modo semplice per gli amministratori e le applicazioni di archiviare elementi quali l'inizializzazione (.ini) o i file di collegamento (con estensione lnk).</span><span class="sxs-lookup"><span data-stu-id="1344a-127">It also provides a straightforward way for administrators and applications to store such things as initialization (.ini) or link (.lnk) files.</span></span> <span data-ttu-id="1344a-128">Le applicazioni possono quindi mantenere uno stato diverso per ogni utente e ripristinare facilmente tale stato specifico quando necessario.</span><span class="sxs-lookup"><span data-stu-id="1344a-128">Applications can thus preserve a different state for each user and easily recover that particular state when needed.</span></span> <span data-ttu-id="1344a-129">Esiste anche una cartella del profilo per l'archiviazione di informazioni comuni a tutti gli utenti.</span><span class="sxs-lookup"><span data-stu-id="1344a-129">There is also a profile folder for storing information that is common to all users.</span></span>

<span data-ttu-id="1344a-130">Poiché è poco pratico determinare quale utente è connesso e dove si trovano i file, le cartelle standard per utente sono cartelle speciali e sono identificate da [**CSIDL**](csidl.md).</span><span class="sxs-lookup"><span data-stu-id="1344a-130">Because it is inconvenient to determine which user is logged in and where their files are located, the standard per-user folders are special folders and are identified by a [**CSIDL**](csidl.md).</span></span> <span data-ttu-id="1344a-131">Ad esempio, il linguaggio CSIDL per la cartella Programmi per utente è PROGRAMMI \_ CSIDL.</span><span class="sxs-lookup"><span data-stu-id="1344a-131">For instance, the CSIDL for the per-user Program Files folder is CSIDL\_PROGRAMS.</span></span> <span data-ttu-id="1344a-132">Se l'applicazione chiama [**SHGetFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation) o [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) con uno dei CSIDL per utente, la funzione restituisce il puntatore a un elenco di identificatori di elemento (PIDL) o al percorso appropriato per l'utente attualmente connesso.</span><span class="sxs-lookup"><span data-stu-id="1344a-132">If your application calls [**SHGetFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation) or [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) with one of the per-user CSIDLs, the function returns the pointer to an item identifier list (PIDL) or path appropriate to the currently logged-in user.</span></span> <span data-ttu-id="1344a-133">Se l'applicazione deve recuperare il percorso o il file PIDL della cartella del profilo, CSIDL è **CSIDL \_ PROFILE**.</span><span class="sxs-lookup"><span data-stu-id="1344a-133">If your application needs to retrieve the path or PIDL of the profile folder, its CSIDL is **CSIDL\_PROFILE**.</span></span>

## <a name="my-documents-and-my-pictures-folders"></a><span data-ttu-id="1344a-134">Documenti cartelle Immagini personali</span><span class="sxs-lookup"><span data-stu-id="1344a-134">My Documents and My Pictures Folders</span></span>

<span data-ttu-id="1344a-135">Una delle icone standard presenti sul desktop è **Documenti**.</span><span class="sxs-lookup"><span data-stu-id="1344a-135">One of the standard icons found on the desktop is **My Documents**.</span></span> <span data-ttu-id="1344a-136">Quando si apre questa cartella, contiene i file di documento dell'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="1344a-136">When you open this folder, it contains the current user's document files.</span></span> <span data-ttu-id="1344a-137">L'istanza desktop di Documenti è una cartella virtuale, ovvero un alias del percorso file system usato per archiviare fisicamente i documenti dell'utente, che si trova immediatamente sotto il desktop nella gerarchia dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="1344a-137">The desktop instance of My Documents is a virtual folder—an alias to the file system location used to physically store the user's documents—located immediately below the desktop in the namespace hierarchy.</span></span>

<span data-ttu-id="1344a-138">Lo scopo delle cartelle Documenti e Immagini è fornire agli utenti un modo semplice e sicuro per accedere ai file di documenti e immagini in un sistema che potrebbe avere più utenti.</span><span class="sxs-lookup"><span data-stu-id="1344a-138">The purpose of the My Documents and My Pictures folders is to provide a straightforward and secure way for users to access their document and picture files on a system that might have multiple users.</span></span> <span data-ttu-id="1344a-139">A ogni utente vengono assegnate cartelle file system per i file.</span><span class="sxs-lookup"><span data-stu-id="1344a-139">Each user is assigned separate file system folders for his or her files.</span></span> <span data-ttu-id="1344a-140">Ad esempio, il percorso della cartella documenti di un utente nel file system è in genere simile a C: Documenti e Impostazioni \\ \\ *nome utente* \\ Documenti.</span><span class="sxs-lookup"><span data-stu-id="1344a-140">For example, the location of a user's documents folder in the file system is typically something like C:\\Documents and Settings\\*username*\\My Documents.</span></span> <span data-ttu-id="1344a-141">Non è necessario che gli utenti sappiano nulla sulla posizione fisica delle file system cartelle.</span><span class="sxs-lookup"><span data-stu-id="1344a-141">There is no need for users to know anything about the physical location of their file system folders.</span></span> <span data-ttu-id="1344a-142">È sufficiente accedere ai file tramite l'icona Documenti.</span><span class="sxs-lookup"><span data-stu-id="1344a-142">They simply access their files through the My Documents icon.</span></span>

> [!Note]  
> <span data-ttu-id="1344a-143">Documenti consente a un utente di accedere ai propri file, ma non a quelli di altri utenti.</span><span class="sxs-lookup"><span data-stu-id="1344a-143">My Documents allows a user to access his or her own files but not those of any other user.</span></span> <span data-ttu-id="1344a-144">Se più utenti usano lo stesso computer, un amministratore può bloccare gli utenti dalla parte del file system in cui sono archiviati i file effettivi.</span><span class="sxs-lookup"><span data-stu-id="1344a-144">If multiple individuals use the same computer, an administrator can lock users out of the part of the file system where the actual files are stored.</span></span> <span data-ttu-id="1344a-145">Gli utenti potranno quindi lavorare sui propri documenti tramite la cartella Documenti ma non sui documenti che appartengono ad altri utenti.</span><span class="sxs-lookup"><span data-stu-id="1344a-145">Users will thus be able to work on their own documents through the My Documents folder but not on documents that belong to any other users.</span></span>

 

<span data-ttu-id="1344a-146">In genere non è necessario che un'applicazione sappia quale utente è connesso o dove si trova file system cartella Documenti dell'utente.</span><span class="sxs-lookup"><span data-stu-id="1344a-146">There is usually no need for an application to know which user is logged in or where in the file system that user's My Documents folder is located.</span></span> <span data-ttu-id="1344a-147">L'applicazione può invece recuperare il file PIDL dell'icona del desktop Documenti chiamando il metodo [**IShellFolder::P arseDisplayName del**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname) desktop.</span><span class="sxs-lookup"><span data-stu-id="1344a-147">Instead, your application can retrieve the PIDL of the My Documents desktop icon by calling the desktop's [**IShellFolder::ParseDisplayName**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname) method.</span></span> <span data-ttu-id="1344a-148">Il nome di analisi usato per identificare la cartella Documenti non è un percorso di file, ma piuttosto ::{450d8fba-ad25-11d0-98a8-0800361b1103}.</span><span class="sxs-lookup"><span data-stu-id="1344a-148">The parsing name used to identify the My Documents folder is not a file path but rather ::{450d8fba-ad25-11d0-98a8-0800361b1103}.</span></span> <span data-ttu-id="1344a-149">L'espressione tra parentesi quadre è la forma di testo del GUID Documenti.</span><span class="sxs-lookup"><span data-stu-id="1344a-149">The bracketed expression is the text form of the My Documents GUID.</span></span> <span data-ttu-id="1344a-150">Ad esempio, per recuperare il file PIDL di Documenti, l'applicazione deve usare questa chiamata a **IShellFolder::P arseDisplayName**.</span><span class="sxs-lookup"><span data-stu-id="1344a-150">For example, to retrieve the PIDL of My Documents, your application should use this call to **IShellFolder::ParseDisplayName**.</span></span>


```C++
hr = psfDeskTop->ParseDisplayName(NULL, 
                                  NULL, 
                                  L"::{450d8fba-ad25-11d0-98a8-0800361b1103}", 
                                  &chEaten, 
                                  &pidlDocFiles, 
                                  NULL);
```



<span data-ttu-id="1344a-151">Una volta che l'applicazione ha il Documenti PIDL, può gestire la cartella esattamente come una normale cartella file system, enumerando elementi, analizzando, associando ed eseguendo qualsiasi altra operazione di cartella valida.</span><span class="sxs-lookup"><span data-stu-id="1344a-151">Once your application has the My Documents PIDL, it can handle the folder just as it would a normal file system folder—enumerating items, parsing, binding, and performing any other valid folder operations.</span></span> <span data-ttu-id="1344a-152">Shell esegue automaticamente il mapping delle Documenti o delle relative sottocartelle alle cartelle file system appropriate.</span><span class="sxs-lookup"><span data-stu-id="1344a-152">The Shell automatically maps changes in My Documents or its subfolders to the appropriate file system folders.</span></span>

<span data-ttu-id="1344a-153">Se l'applicazione deve accedere alla cartella file system che contiene i documenti dell'utente corrente, passare CSIDL \_ PERSONAL a [**SHGetFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation).</span><span class="sxs-lookup"><span data-stu-id="1344a-153">If your application needs access to the actual file system folder that contains the current user's documents, pass CSIDL\_PERSONAL to [**SHGetFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation).</span></span> <span data-ttu-id="1344a-154">La funzione restituisce il file PIDL della file system visualizzata nella cartella Documenti dell'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="1344a-154">The function returns the PIDL of the file system folder that is displayed in the current user's My Documents folder.</span></span>

## <a name="connected-files"></a><span data-ttu-id="1344a-155">File connessi</span><span class="sxs-lookup"><span data-stu-id="1344a-155">Connected Files</span></span>

<span data-ttu-id="1344a-156">I documenti HTML hanno spesso una serie di file grafici associati, un file di foglio di stile, diversi file di Microsoft JScript (compatibili con la specifica del linguaggio ECMA 262) e così via.</span><span class="sxs-lookup"><span data-stu-id="1344a-156">HTML documents often have a number of associated graphics files, a style sheet file, several Microsoft JScript (compatible with ECMA 262 language specification ) files, and so on.</span></span> <span data-ttu-id="1344a-157">Quando si sposta o si copia il documento HTML primario, in genere si vogliono anche spostare o copiare i file associati per evitare collegamenti di rilievo.</span><span class="sxs-lookup"><span data-stu-id="1344a-157">When you move or copy the primary HTML document, you also usually want to move or copy its associated files to avoid breaking links.</span></span> <span data-ttu-id="1344a-158">Sfortunatamente, finora non esisteva un modo semplice per determinare quali file sono correlati a un determinato documento HTML se non analizzandone il contenuto.</span><span class="sxs-lookup"><span data-stu-id="1344a-158">Unfortunately, there has been no easy way until now to determine which files are related to any given HTML document other than by analyzing their contents.</span></span> <span data-ttu-id="1344a-159">Per risolvere questo problema, Windows 2000 offre un  modo semplice per connettere un documento HTML primario al gruppo di file associati.</span><span class="sxs-lookup"><span data-stu-id="1344a-159">To alleviate this problem, Windows 2000 provides a simple way to *connect* a primary HTML document to its group of associated files.</span></span> <span data-ttu-id="1344a-160">Se la connessione file è abilitata, quando il documento viene spostato o copiato, vengono associati tutti i file connessi.</span><span class="sxs-lookup"><span data-stu-id="1344a-160">If file connection is enabled, when the document is moved or copied all its connected files go with it.</span></span>

<span data-ttu-id="1344a-161">Per creare un gruppo di file connessi, il documento primario deve avere un'estensione .htm o .html file.</span><span class="sxs-lookup"><span data-stu-id="1344a-161">To create a group of connected files, the primary document must have an .htm or .html file name extension.</span></span> <span data-ttu-id="1344a-162">Creare una sottocartella della cartella padre del documento primario.</span><span class="sxs-lookup"><span data-stu-id="1344a-162">Create a subfolder of the primary document's parent folder.</span></span> <span data-ttu-id="1344a-163">Il nome della sottocartella deve essere il nome del documento primario, meno l'estensione .htm o .html, seguita da una delle estensioni elencate di seguito.</span><span class="sxs-lookup"><span data-stu-id="1344a-163">The subfolder's name must be the name of the primary document, minus the .htm or .html extension, followed by one of the extensions listed below.</span></span> <span data-ttu-id="1344a-164">Le estensioni usate più di frequente sono ".files" o \_ "files".</span><span class="sxs-lookup"><span data-stu-id="1344a-164">The most commonly used extensions are ".files" or "\_files".</span></span> <span data-ttu-id="1344a-165">Ad esempio, se il documento primario è denominato MyDoc.htm, il nome della sottocartella "File MyDoc" definisce la sottocartella come contenitore per i \_ file connessi del documento.</span><span class="sxs-lookup"><span data-stu-id="1344a-165">For instance, if the primary document is named MyDoc.htm, naming the subfolder "MyDoc\_files" defines the subfolder as the container for the document's connected files.</span></span> <span data-ttu-id="1344a-166">Se il documento primario viene spostato o copiato, anche la sottocartella e i relativi file vengono spostati o copiati.</span><span class="sxs-lookup"><span data-stu-id="1344a-166">If the primary document is moved or copied, the subfolder and its files are moved or copied as well.</span></span>

<span data-ttu-id="1344a-167">Per alcune lingue, è possibile usare un equivalente localizzato di \_ "file" per creare una sottocartella per i file connessi.</span><span class="sxs-lookup"><span data-stu-id="1344a-167">For some languages, it is possible to use a localized equivalent of "\_files" to create a subfolder for connected files.</span></span> <span data-ttu-id="1344a-168">Nella tabella seguente sono elencate le stringhe valide che possono essere aggiunte a un nome di documento per creare una sottocartella di file connessi.</span><span class="sxs-lookup"><span data-stu-id="1344a-168">The following table lists the valid strings that can be appended to a document name to create a connected files subfolder.</span></span> <span data-ttu-id="1344a-169">Si noti che alcune di queste stringhe hanno '-' come primo carattere anziché \_ '' o '.'.</span><span class="sxs-lookup"><span data-stu-id="1344a-169">Note that some of these strings have '-' as their first character rather than '\_' or '.'.</span></span>



:::row:::
   :::column span="":::
      <span data-ttu-id="1344a-170">\_"archivos"</span><span class="sxs-lookup"><span data-stu-id="1344a-170">"\_archivos"</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="1344a-171">\_"arquivos"</span><span class="sxs-lookup"><span data-stu-id="1344a-171">"\_arquivos"</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="1344a-172">\_"bestanden"</span><span class="sxs-lookup"><span data-stu-id="1344a-172">"\_bestanden"</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="1344a-173">" \_ bylos"</span><span class="sxs-lookup"><span data-stu-id="1344a-173">"\_bylos"</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="1344a-174">"-Dateien"</span><span class="sxs-lookup"><span data-stu-id="1344a-174">"-Dateien"</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="1344a-175">\_"datoteke"</span><span class="sxs-lookup"><span data-stu-id="1344a-175">"\_datoteke"</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="1344a-176">\_"dosyalar"</span><span class="sxs-lookup"><span data-stu-id="1344a-176">"\_dosyalar"</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="1344a-177">\_"elemei"</span><span class="sxs-lookup"><span data-stu-id="1344a-177">"\_elemei"</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="1344a-178">" \_ failid"</span><span class="sxs-lookup"><span data-stu-id="1344a-178">"\_failid"</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="1344a-179">"ha \_ esito negativo"</span><span class="sxs-lookup"><span data-stu-id="1344a-179">"\_fails"</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="1344a-180">\_"fajlovi"</span><span class="sxs-lookup"><span data-stu-id="1344a-180">"\_fajlovi"</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="1344a-181">\_"ficheiros"</span><span class="sxs-lookup"><span data-stu-id="1344a-181">"\_ficheiros"</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="1344a-182">\_"fichiers"</span><span class="sxs-lookup"><span data-stu-id="1344a-182">"\_fichiers"</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="1344a-183">"-filer"</span><span class="sxs-lookup"><span data-stu-id="1344a-183">"-filer"</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="1344a-184">".files"</span><span class="sxs-lookup"><span data-stu-id="1344a-184">".files"</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="1344a-185">\_"files"</span><span class="sxs-lookup"><span data-stu-id="1344a-185">"\_files"</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="1344a-186">\_"file"</span><span class="sxs-lookup"><span data-stu-id="1344a-186">"\_file"</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="1344a-187">\_"fitxers"</span><span class="sxs-lookup"><span data-stu-id="1344a-187">"\_fitxers"</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="1344a-188">\_"fitxategiak"</span><span class="sxs-lookup"><span data-stu-id="1344a-188">"\_fitxategiak"</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="1344a-189">\_"pliki"</span><span class="sxs-lookup"><span data-stu-id="1344a-189">"\_pliki"</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="1344a-190">\_"soubory"</span><span class="sxs-lookup"><span data-stu-id="1344a-190">"\_soubory"</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="1344a-191">\_"tiedostot"</span><span class="sxs-lookup"><span data-stu-id="1344a-191">"\_tiedostot"</span></span>
   :::column-end:::
   :::column span="":::
   :::column-end:::
   :::column span="":::
   :::column-end:::
:::row-end:::



 

> [!Note]  
> <span data-ttu-id="1344a-192">Questa funzionalità è sensibile al caso dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="1344a-192">This feature is sensitive to the case of the extension.</span></span> <span data-ttu-id="1344a-193">Ad esempio, per l'esempio indicato in precedenza, una sottocartella denominata "MyDoc Files" non verrà connessa a \_ MyDoc.htm.</span><span class="sxs-lookup"><span data-stu-id="1344a-193">For instance, for the example given above, a subfolder named "MyDoc\_Files" will not be connected to MyDoc.htm.</span></span>

 

<span data-ttu-id="1344a-194">Se la connessione file è abilitata o disabilitata è controllata da un valore **\_ DWORD REG,** NoFileFolderConnection, della chiave del Registro di sistema seguente.</span><span class="sxs-lookup"><span data-stu-id="1344a-194">Whether file connection is enabled or disabled is controlled by a **REG\_DWORD** value, NoFileFolderConnection, of the following registry key.</span></span>

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
```

<span data-ttu-id="1344a-195">Questo valore in genere non è definito e la connessione file è abilitata.</span><span class="sxs-lookup"><span data-stu-id="1344a-195">This value normally is not defined, and file connection is enabled.</span></span> <span data-ttu-id="1344a-196">Se necessario, è possibile disabilitare la connessione file aggiungendo questo valore alla chiave e impostandola su 1.</span><span class="sxs-lookup"><span data-stu-id="1344a-196">If necessary, you can disable file connection by adding this value to the key and setting it to 1.</span></span> <span data-ttu-id="1344a-197">Per abilitare nuovamente la connessione file, impostare NoFileFolderConnection su zero.</span><span class="sxs-lookup"><span data-stu-id="1344a-197">To enable file connection again, set NoFileFolderConnection to zero.</span></span>

> [!Note]  
> <span data-ttu-id="1344a-198">La connessione file deve in genere essere abilitata perché altre applicazioni potrebbero dipendere da essa.</span><span class="sxs-lookup"><span data-stu-id="1344a-198">File connection should normally be enabled because other applications might depend on it.</span></span> <span data-ttu-id="1344a-199">Disabilitare la connessione file solo se assolutamente necessario.</span><span class="sxs-lookup"><span data-stu-id="1344a-199">Disable file connection only if absolutely necessary.</span></span>

 

## <a name="moving-copying-renaming-and-deleting-files"></a><span data-ttu-id="1344a-200">Spostamento, copia, ridenominazione ed eliminazione di file</span><span class="sxs-lookup"><span data-stu-id="1344a-200">Moving, Copying, Renaming, and Deleting Files</span></span>

<span data-ttu-id="1344a-201">Lo spazio dei nomi non è statico e le applicazioni in genere devono gestire file system eseguendo una delle operazioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="1344a-201">The namespace is not static, and applications commonly need to manage the file system by performing one of the following operations.</span></span>

-   <span data-ttu-id="1344a-202">Copia di un oggetto in un'altra cartella.</span><span class="sxs-lookup"><span data-stu-id="1344a-202">Copying an object to another folder.</span></span>
-   <span data-ttu-id="1344a-203">Spostamento di un oggetto in un'altra cartella.</span><span class="sxs-lookup"><span data-stu-id="1344a-203">Moving an object to another folder.</span></span>
-   <span data-ttu-id="1344a-204">Eliminazione di un oggetto.</span><span class="sxs-lookup"><span data-stu-id="1344a-204">Deleting an object.</span></span>
-   <span data-ttu-id="1344a-205">Ridenominazione di un oggetto.</span><span class="sxs-lookup"><span data-stu-id="1344a-205">Renaming an object.</span></span>

<span data-ttu-id="1344a-206">Queste operazioni vengono tutte eseguite con [**SHFileOperation**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa).</span><span class="sxs-lookup"><span data-stu-id="1344a-206">These operations are all performed with [**SHFileOperation**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa).</span></span> <span data-ttu-id="1344a-207">Questa funzione accetta uno o più file di origine e produce i file di destinazione corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="1344a-207">This function takes one or more source files and produces corresponding destination files.</span></span> <span data-ttu-id="1344a-208">Nel caso dell'operazione di eliminazione, il sistema tenta di inserire i file eliminati nel Cestino.</span><span class="sxs-lookup"><span data-stu-id="1344a-208">In the case of the delete operation, the system attempts to put the deleted files into the Recycle Bin.</span></span>

<span data-ttu-id="1344a-209">È anche possibile spostare i file usando la [funzionalità di trascinamento della](dragdrop.md) selezione.</span><span class="sxs-lookup"><span data-stu-id="1344a-209">It is also possible to move files using the [drag-and-drop](dragdrop.md) functionality.</span></span>

<span data-ttu-id="1344a-210">Per usare la funzione , è necessario compilare i membri di una struttura [**SHFILEOPSTRUCT**](/windows/desktop/api/Shellapi/ns-shellapi-shfileopstructa) e passarla [**a SHFileOperation**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa).</span><span class="sxs-lookup"><span data-stu-id="1344a-210">To use the function, you must fill in the members of an [**SHFILEOPSTRUCT**](/windows/desktop/api/Shellapi/ns-shellapi-shfileopstructa) structure and pass it to [**SHFileOperation**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa).</span></span> <span data-ttu-id="1344a-211">I membri chiave della struttura sono **pFrom** e **pTo.**</span><span class="sxs-lookup"><span data-stu-id="1344a-211">The key members of the structure are **pFrom** and **pTo**.</span></span>

<span data-ttu-id="1344a-212">Il **membro pFrom** è una stringa con terminazione **Null** doppia che contiene uno o più nomi di file di origine.</span><span class="sxs-lookup"><span data-stu-id="1344a-212">The **pFrom** member is a double **null**-terminated string that contains one or more source file names.</span></span> <span data-ttu-id="1344a-213">Questi nomi possono essere percorsi completi o caratteri jolly DOS standard, ad esempio \* \* .</span><span class="sxs-lookup"><span data-stu-id="1344a-213">These names can be either fully qualified paths or standard DOS wildcards such as \*.\*.</span></span> <span data-ttu-id="1344a-214">Anche se questo membro è dichiarato come stringa con terminazione **Null,** viene usato come buffer per contenere più nomi di file.</span><span class="sxs-lookup"><span data-stu-id="1344a-214">Although this member is declared as a **null**-terminated string, it is used as a buffer to hold multiple file names.</span></span> <span data-ttu-id="1344a-215">Ogni nome di file deve essere terminato dal singolo carattere **NULL** consueto.</span><span class="sxs-lookup"><span data-stu-id="1344a-215">Each file name must be terminated by the usual single **NULL** character.</span></span> <span data-ttu-id="1344a-216">È necessario aggiungere un carattere **NULL** aggiuntivo alla fine del nome finale per indicare la fine di **pFrom.**</span><span class="sxs-lookup"><span data-stu-id="1344a-216">An additional **NULL** character must be appended to the end of the final name to indicate the end of **pFrom**.</span></span>

<span data-ttu-id="1344a-217">Il **membro pTo** è una stringa con terminazione **Null** doppia, in modo molto simile a **pFrom**.</span><span class="sxs-lookup"><span data-stu-id="1344a-217">The **pTo** member is a double **null**-terminated string, much like **pFrom**.</span></span> <span data-ttu-id="1344a-218">Il **membro pTo** contiene i nomi di uno o più nomi di destinazione completi.</span><span class="sxs-lookup"><span data-stu-id="1344a-218">The **pTo** member contains the names of one or more fully qualified destination names.</span></span> <span data-ttu-id="1344a-219">Vengono imballati in **pTo** nello stesso modo in cui sono per **pFrom**.</span><span class="sxs-lookup"><span data-stu-id="1344a-219">They are packed into **pTo** in the same way as they are for **pFrom**.</span></span> <span data-ttu-id="1344a-220">Se **pTo** contiene più nomi, è necessario impostare anche il flag **\_ FOF MULTIDESTFILES** nel **membro fFlags.**</span><span class="sxs-lookup"><span data-stu-id="1344a-220">If **pTo** contains multiple names, you must also set the **FOF\_MULTIDESTFILES** flag in the **fFlags** member.</span></span> <span data-ttu-id="1344a-221">L'utilizzo **di pTo** dipende dall'operazione come descritto di seguito.</span><span class="sxs-lookup"><span data-stu-id="1344a-221">The usage of **pTo** depends on the operation as described here.</span></span>

-   <span data-ttu-id="1344a-222">Per le operazioni di copia e spostamento, se tutti i file vengono spostati in una singola directory, **pTo** contiene il nome completo della directory.</span><span class="sxs-lookup"><span data-stu-id="1344a-222">For copy and move operations, if all the files are going to a single directory, **pTo** contains the fully qualified directory name.</span></span> <span data-ttu-id="1344a-223">Se i file vengono verso destinazioni diverse, **pTo** può contenere anche una directory o un nome file completo per ogni file di origine.</span><span class="sxs-lookup"><span data-stu-id="1344a-223">If the files are going to different destinations, **pTo** can also contain one fully qualified directory or file name for each source file.</span></span> <span data-ttu-id="1344a-224">Se non esiste una directory, il sistema la crea.</span><span class="sxs-lookup"><span data-stu-id="1344a-224">If a directory does not exist, the system creates it.</span></span>
-   <span data-ttu-id="1344a-225">Per le operazioni di **ridenominazione, pTo** contiene un percorso completo per ogni file di origine in **pFrom**.</span><span class="sxs-lookup"><span data-stu-id="1344a-225">For rename operations, **pTo** contains one fully qualified path for each source file in **pFrom**.</span></span>
-   <span data-ttu-id="1344a-226">Per le operazioni di eliminazione, **pTo** non viene usato.</span><span class="sxs-lookup"><span data-stu-id="1344a-226">For delete operations, **pTo** is not used.</span></span>

### <a name="notifying-the-shell"></a><span data-ttu-id="1344a-227">Notifica alla shell</span><span class="sxs-lookup"><span data-stu-id="1344a-227">Notifying the Shell</span></span>

<span data-ttu-id="1344a-228">Notificare alla shell la modifica dopo l'uso di [**SHFileOperation**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa) per spostare, copiare, rinominare o eliminare file o dopo l'azione che interessa lo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="1344a-228">Notify the Shell of the change after using [**SHFileOperation**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa) to move, copy, rename, or delete files, or after taking any other action that affects the namespace.</span></span> <span data-ttu-id="1344a-229">Di seguito sono riportate le azioni che devono essere accompagnate da una notifica:</span><span class="sxs-lookup"><span data-stu-id="1344a-229">Actions that should be accompanied by notification include the following:</span></span>

-   <span data-ttu-id="1344a-230">Aggiunta o eliminazione di file o cartelle.</span><span class="sxs-lookup"><span data-stu-id="1344a-230">Adding or deleting files or folders.</span></span>
-   <span data-ttu-id="1344a-231">Spostamento, copia o ridenominazione di file o cartelle.</span><span class="sxs-lookup"><span data-stu-id="1344a-231">Moving, copying, or renaming files or folders.</span></span>
-   <span data-ttu-id="1344a-232">Modifica di un'associazione di file.</span><span class="sxs-lookup"><span data-stu-id="1344a-232">Changing a file association.</span></span>
-   <span data-ttu-id="1344a-233">Modifica degli attributi del file.</span><span class="sxs-lookup"><span data-stu-id="1344a-233">Changing file attributes.</span></span>
-   <span data-ttu-id="1344a-234">Aggiunta o rimozione di unità o supporti di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="1344a-234">Adding or removing drives or storage media.</span></span>
-   <span data-ttu-id="1344a-235">Creazione o disabilitazione di una cartella condivisa.</span><span class="sxs-lookup"><span data-stu-id="1344a-235">Creating or disabling a shared folder.</span></span>
-   <span data-ttu-id="1344a-236">Modifica dell'elenco di immagini di sistema.</span><span class="sxs-lookup"><span data-stu-id="1344a-236">Changing the system image list.</span></span>

<span data-ttu-id="1344a-237">Un'applicazione invia una notifica alla shell chiamando [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) con i dettagli delle modifiche.</span><span class="sxs-lookup"><span data-stu-id="1344a-237">An application notifies the Shell by calling [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) with the details of what has changed.</span></span> <span data-ttu-id="1344a-238">Shell può quindi aggiornare l'immagine dello spazio dei nomi in modo da riflettere in modo accurato il nuovo stato.</span><span class="sxs-lookup"><span data-stu-id="1344a-238">The Shell can then update its image of the namespace to accurately reflect its new state.</span></span>

## <a name="simple-example-of-managing-files-with-shfileoperation"></a><span data-ttu-id="1344a-239">Esempio semplice di gestione dei file con SHFileOperation</span><span class="sxs-lookup"><span data-stu-id="1344a-239">Simple Example of Managing Files with SHFileOperation</span></span>

<span data-ttu-id="1344a-240">L'applicazione console di esempio seguente illustra l'uso di [**SHFileOperation**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa) per copiare file da una directory a un'altra.</span><span class="sxs-lookup"><span data-stu-id="1344a-240">The following sample console application illustrates the use of [**SHFileOperation**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa) to copy files from one directory to another.</span></span> <span data-ttu-id="1344a-241">Le directory di origine e di destinazione, C: My Docs e \\ \_ C: \\ My \_ Docs2, sono hard-coded nell'applicazione per semplicità.</span><span class="sxs-lookup"><span data-stu-id="1344a-241">The source and destination directories, C:\\My\_Docs and C:\\My\_Docs2, are hard-coded into the application for simplicity.</span></span>


```C++
#include <shlobj.h>
#include <shlwapi.h>
#include <strsafe.h>

int main(void)
{
    IShellFolder *psfDeskTop = NULL;
    IShellFolder *psfDocFiles = NULL;
    LPITEMIDLIST pidlDocFiles = NULL;
    LPITEMIDLIST pidlItems = NULL;
    IEnumIDList *ppenum = NULL;
    SHFILEOPSTRUCT sfo;
    STRRET strDispName;
    TCHAR szParseName[MAX_PATH];
    TCHAR szSourceFiles[256];
    int i;
    int iBufPos = 0;
    ULONG chEaten;
    ULONG celtFetched;
    size_t ParseNameSize = 0;
    HRESULT hr;
    

    szSourceFiles[0] = '\0';
    hr = SHGetDesktopFolder(&psfDeskTop);

    hr = psfDeskTop->ParseDisplayName(NULL, NULL, L"c:\\My_Docs", 
         &chEaten, &pidlDocFiles, NULL);
    hr = psfDeskTop->BindToObject(pidlDocFiles, NULL, IID_IShellFolder, 
         (LPVOID *) &psfDocFiles);
    hr = psfDeskTop->Release();

    hr = psfDocFiles->EnumObjects(NULL,SHCONTF_FOLDERS | SHCONTF_NONFOLDERS, 
         &ppenum);

    while( (hr = ppenum->Next(1,&pidlItems, &celtFetched)) == S_OK 
       && (celtFetched) == 1)
    {
        psfDocFiles->GetDisplayNameOf(pidlItems, SHGDN_FORPARSING, 
            &strDispName);
        StrRetToBuf(&strDispName, pidlItems, szParseName, MAX_PATH);
        
        hr = StringCchLength(szParseName, MAX_PATH, &ParseNameSize);
        
        if (SUCCEEDED(hr))
        {
            for(i=0; i<=ParseNameSize; i++)
            {
                szSourceFiles[iBufPos++] = szParseName[i];
            }
            CoTaskMemFree(pidlItems);
        }
    }
    ppenum->Release();
    
    szSourceFiles[iBufPos] = '\0';

    sfo.hwnd = NULL;
    sfo.wFunc = FO_COPY;
    sfo.pFrom = szSourceFiles;
    sfo.pTo = "c:\\My_Docs2\0";
    sfo.fFlags = FOF_SILENT | FOF_NOCONFIRMATION | FOF_NOCONFIRMMKDIR;

    hr = SHFileOperation(&sfo);
    
    SHChangeNotify(SHCNE_UPDATEDIR, SHCNF_PATH, (LPCVOID) "c:\\My_Docs2", 0);

    CoTaskMemFree(pidlDocFiles);
    psfDocFiles->Release();

    return 0;
}
```



<span data-ttu-id="1344a-242">L'applicazione recupera innanzitutto un puntatore [**all'interfaccia IShellFolder del**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) desktop.</span><span class="sxs-lookup"><span data-stu-id="1344a-242">The application first retrieves a pointer to the desktop's [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) interface.</span></span> <span data-ttu-id="1344a-243">Recupera quindi il file PIDL della directory di origine passando il percorso completo a [**IShellFolder::P arseDisplayName**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname).</span><span class="sxs-lookup"><span data-stu-id="1344a-243">It then retrieves the source directory's PIDL by passing its fully qualified path to [**IShellFolder::ParseDisplayName**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname).</span></span> <span data-ttu-id="1344a-244">Si noti **che IShellFolder::P arseDisplayName** richiede che il percorso della directory sia una stringa Unicode.</span><span class="sxs-lookup"><span data-stu-id="1344a-244">Note that **IShellFolder::ParseDisplayName** requires the directory's path to be a Unicode string.</span></span> <span data-ttu-id="1344a-245">L'applicazione esegue quindi il binding alla directory di origine e usa la relativa **interfaccia IShellFolder** per recuperare l'interfaccia [**IEnumIDList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist) di un oggetto enumeratore.</span><span class="sxs-lookup"><span data-stu-id="1344a-245">The application then binds to the source directory and uses its **IShellFolder** interface to retrieve an enumerator object's [**IEnumIDList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist) interface.</span></span>

<span data-ttu-id="1344a-246">Quando ogni file nella directory di origine viene enumerato, viene usato [**IShellFolder::GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) per recuperarne il nome.</span><span class="sxs-lookup"><span data-stu-id="1344a-246">As each file in the source directory is enumerated, [**IShellFolder::GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) is used to retrieve its name.</span></span> <span data-ttu-id="1344a-247">Il flag SHGDN FORPARSING è impostato \_ e **IShellFolder::GetDisplayNameOf** restituisce il percorso completo del file.</span><span class="sxs-lookup"><span data-stu-id="1344a-247">The SHGDN\_FORPARSING flag is set, which causes **IShellFolder::GetDisplayNameOf** to return the file's fully qualified path.</span></span> <span data-ttu-id="1344a-248">I percorsi di file, inclusi i caratteri **NULL** di terminazione, vengono concatenati in una singola matrice, *szSourceFiles*.</span><span class="sxs-lookup"><span data-stu-id="1344a-248">The file paths, including the terminating **NULL** characters, are concatenated into a single array, *szSourceFiles*.</span></span> <span data-ttu-id="1344a-249">Un secondo **carattere NULL** viene aggiunto al percorso finale per terminare correttamente la matrice.</span><span class="sxs-lookup"><span data-stu-id="1344a-249">A second **NULL** character is appended to the final path to terminate the array properly.</span></span>

<span data-ttu-id="1344a-250">Al termine dell'enumerazione, l'applicazione assegna valori a [**una struttura SHFILEOPSTRUCT.**](/windows/desktop/api/Shellapi/ns-shellapi-shfileopstructa)</span><span class="sxs-lookup"><span data-stu-id="1344a-250">Once the enumeration is complete, the application assigns values to an [**SHFILEOPSTRUCT**](/windows/desktop/api/Shellapi/ns-shellapi-shfileopstructa) structure.</span></span> <span data-ttu-id="1344a-251">Si noti che anche la matrice assegnata a **pTo** per specificare la destinazione deve essere terminata da un valore **NULL doppio.**</span><span class="sxs-lookup"><span data-stu-id="1344a-251">Note that the array assigned to **pTo** to specify the destination must also be terminated by a double **NULL**.</span></span> <span data-ttu-id="1344a-252">In questo caso, viene semplicemente incluso nella stringa assegnata a **pTo**.</span><span class="sxs-lookup"><span data-stu-id="1344a-252">In this case, it is simply included in the string that is assigned to **pTo**.</span></span> <span data-ttu-id="1344a-253">Poiché si tratta di un'applicazione console, i flag FOF \_ SILENT, FOF \_ NOCONFIRMATION e FOF NOCONFIRMMKDIR sono impostati per eliminare eventuali finestre di dialogo che potrebbero \_ essere visualizzate.</span><span class="sxs-lookup"><span data-stu-id="1344a-253">Because this is a console application, the FOF\_SILENT, FOF\_NOCONFIRMATION, and FOF\_NOCONFIRMMKDIR flags are set to suppress any dialog boxes that might appear.</span></span> <span data-ttu-id="1344a-254">Al [**termine di SHFileOperation,**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa) [**viene chiamato SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) per notificare la modifica alla shell.</span><span class="sxs-lookup"><span data-stu-id="1344a-254">After [**SHFileOperation**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa) returns, [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) is called to notify the Shell of the change.</span></span> <span data-ttu-id="1344a-255">L'applicazione esegue quindi la pulizia consueta e restituisce .</span><span class="sxs-lookup"><span data-stu-id="1344a-255">Then the application performs the usual cleanup and returns.</span></span>

## <a name="adding-files-to-the-shells-list-of-recent-documents"></a><span data-ttu-id="1344a-256">Aggiunta di file all'elenco di documenti recenti della shell</span><span class="sxs-lookup"><span data-stu-id="1344a-256">Adding Files to the Shell's List of Recent Documents</span></span>

<span data-ttu-id="1344a-257">Shell gestisce un elenco di documenti aggiunti o modificati di recente per ogni utente.</span><span class="sxs-lookup"><span data-stu-id="1344a-257">The Shell maintains a list of recently added or modified documents for each user.</span></span> <span data-ttu-id="1344a-258">L'utente può visualizzare un elenco di collegamenti a questi file facendo clic su Documenti nel menu Start.</span><span class="sxs-lookup"><span data-stu-id="1344a-258">The user can display a list of links to these files by clicking Documents on the Start menu.</span></span> <span data-ttu-id="1344a-259">Come per Documenti, ogni utente ha una directory file system per contenere i collegamenti effettivi.</span><span class="sxs-lookup"><span data-stu-id="1344a-259">As with My Documents, each user has a file system directory to hold the actual links.</span></span> <span data-ttu-id="1344a-260">Per recuperare il FILE PIDL della directory Recent dell'utente corrente, l'applicazione può chiamare [**SHGetFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation) con CSIDL \_ RECENT oppure chiamare [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) per recuperarne il percorso.</span><span class="sxs-lookup"><span data-stu-id="1344a-260">To retrieve the PIDL of the current user's Recent directory, your application can call [**SHGetFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation) with CSIDL\_RECENT, or call [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) to retrieve its path.</span></span>

<span data-ttu-id="1344a-261">L'applicazione può enumerare il contenuto della cartella Recenti usando le tecniche descritte in precedenza in questo documento.</span><span class="sxs-lookup"><span data-stu-id="1344a-261">Your application can enumerate the contents of the Recent folder using the techniques discussed earlier in this document.</span></span> <span data-ttu-id="1344a-262">Tuttavia, un'applicazione non deve modificare il contenuto della cartella come se fosse una normale file system cartella.</span><span class="sxs-lookup"><span data-stu-id="1344a-262">However, an application should not modify the contents of the folder as if it were a normal file system folder.</span></span> <span data-ttu-id="1344a-263">In questo caso, l'elenco di documenti recenti della Shell non verrà aggiornato correttamente e le modifiche non verranno riflesse nel menu Start.</span><span class="sxs-lookup"><span data-stu-id="1344a-263">If it does so, the Shell's list of recent documents will not be updated properly, and the changes will not be reflected in the Start menu.</span></span> <span data-ttu-id="1344a-264">Al contrario, per aggiungere un collegamento di documento alla cartella Recenti di un utente, l'applicazione può chiamare [**SHAddToRecentDocs**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs).</span><span class="sxs-lookup"><span data-stu-id="1344a-264">Instead, to add a document link to a user's Recent folder, your application can call [**SHAddToRecentDocs**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs).</span></span> <span data-ttu-id="1344a-265">Shell aggiungerà un collegamento alla cartella file system appropriata, oltre ad aggiornare l'elenco dei documenti recenti e il menu Start.</span><span class="sxs-lookup"><span data-stu-id="1344a-265">The Shell will add a link to the appropriate file system folder, as well as updating its list of recent documents and the Start menu.</span></span> <span data-ttu-id="1344a-266">È anche possibile usare questa funzione per cancellare la cartella.</span><span class="sxs-lookup"><span data-stu-id="1344a-266">You can also use this function to clear the folder.</span></span>

 

 
