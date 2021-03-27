---
description: La radice di un'estensione dello spazio dei nomi viene in genere visualizzata da Esplora risorse come cartella nelle visualizzazioni albero e cartella.
title: Impostazione della posizione di un'estensione dello spazio dei nomi
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2c1fdd5d-b359-4d5c-a20e-0622f3a1cb1d
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 7617c7361c5f2ae76331c5f1b59eb845f6806395
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882805"
---
# <a name="specifying-a-namespace-extensions-location"></a><span data-ttu-id="f2786-103">Impostazione della posizione di un'estensione dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f2786-103">Specifying a Namespace Extension's Location</span></span>

<span data-ttu-id="f2786-104">La radice di un'estensione dello spazio dei nomi viene in genere visualizzata da Esplora risorse come cartella nelle visualizzazioni albero e cartella.</span><span class="sxs-lookup"><span data-stu-id="f2786-104">The root of a namespace extension is normally displayed by Windows Explorer as a folder in both tree and folder views.</span></span> <span data-ttu-id="f2786-105">Per visualizzare le sottocartelle e i file dell'estensione in Esplora risorse, è necessario specificare la posizione della cartella radice nella gerarchia dello spazio dei nomi della shell.</span><span class="sxs-lookup"><span data-stu-id="f2786-105">For Windows Explorer to display your extension's files and subfolders, you must specify where the root folder is located in the Shell namespace hierarchy.</span></span> <span data-ttu-id="f2786-106">Questo percorso viene definito *punto di giunzione*.</span><span class="sxs-lookup"><span data-stu-id="f2786-106">This location is referred to as a *junction point*.</span></span>

-   [<span data-ttu-id="f2786-107">Uso delle cartelle virtuali come punti di giunzione</span><span class="sxs-lookup"><span data-stu-id="f2786-107">Using Virtual Folders as Junction Points</span></span>](#using-virtual-folders-as-junction-points)
-   [<span data-ttu-id="f2786-108">Uso delle cartelle del file System come punti di giunzione</span><span class="sxs-lookup"><span data-stu-id="f2786-108">Using File System Folders as Junction Points</span></span>](#using-file-system-folders-as-junction-points)
-   [<span data-ttu-id="f2786-109">Apertura di una visualizzazione di un'estensione dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f2786-109">Opening a View of a Namespace Extension</span></span>](#opening-a-view-of-a-namespace-extension)

## <a name="using-virtual-folders-as-junction-points"></a><span data-ttu-id="f2786-110">Uso delle cartelle virtuali come punti di giunzione</span><span class="sxs-lookup"><span data-stu-id="f2786-110">Using Virtual Folders as Junction Points</span></span>

<span data-ttu-id="f2786-111">Il modo più semplice per definire il punto di giunzione di un'estensione consiste nel rendere la cartella radice una sottocartella di una cartella virtuale di sistema.</span><span class="sxs-lookup"><span data-stu-id="f2786-111">The simplest way to define an extension's junction point is to make the root folder a subfolder of a system virtual folder.</span></span> <span data-ttu-id="f2786-112">Questo tipo di punto di giunzione viene definito punto di *giunzione virtuale*.</span><span class="sxs-lookup"><span data-stu-id="f2786-112">This type of junction point is referred to as a *virtual junction point*.</span></span> <span data-ttu-id="f2786-113">Le cartelle **Desktop** e **computer locale** sono le località tipiche per i punti di giunzione virtuali, ma è anche possibile definire un punto di giunzione virtuale in un computer remoto oppure nelle cartelle **risorse di rete**, **Internet Explorer** e **Pannello di controllo** .</span><span class="sxs-lookup"><span data-stu-id="f2786-113">The **Desktop** and **My Computer** folders are the typical locations for virtual junction points, but you can also define a virtual junction point on a remote computer or under the **My Network Places**, **Internet Explorer**, and **Control Panel** folders.</span></span>

<span data-ttu-id="f2786-114">Per definire un punto di giunzione virtuale, creare una sottochiave della chiave che rappresenti la cartella virtuale appropriata e denominarla con il formato stringa dell'identificatore di classe dell'estensione (CLSID).</span><span class="sxs-lookup"><span data-stu-id="f2786-114">To define a virtual junction point, create a subkey of the key that represents the appropriate virtual folder and name it with the string form of your extension's class identifier (CLSID).</span></span> <span data-ttu-id="f2786-115">Il CLSID registrato verrà visualizzato come segue.</span><span class="sxs-lookup"><span data-stu-id="f2786-115">The registered CLSID would appear as follows.</span></span>

```
HKEY_LOCAL_MACHINE or HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  Virtual Folder Name
                     NameSpace
                        {Extension CLSID}
                           (Default) = Junction Point Name
```

<span data-ttu-id="f2786-116">Il *nome della cartella virtuale* è una delle sottochiavi riportate nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="f2786-116">*Virtual Folder Name* is one of the subkeys in the following table.</span></span>



| <span data-ttu-id="f2786-117">Location</span><span class="sxs-lookup"><span data-stu-id="f2786-117">Location</span></span>          | <span data-ttu-id="f2786-118">Nome cartella virtuale</span><span class="sxs-lookup"><span data-stu-id="f2786-118">Virtual Folder Name</span></span>                        |
|-------------------|--------------------------------------------|
| <span data-ttu-id="f2786-119">Control panel</span><span class="sxs-lookup"><span data-stu-id="f2786-119">Control Panel</span></span>     | <span data-ttu-id="f2786-120">**ControlPanel**</span><span class="sxs-lookup"><span data-stu-id="f2786-120">**ControlPanel**</span></span>                           |
| <span data-ttu-id="f2786-121">Desktop</span><span class="sxs-lookup"><span data-stu-id="f2786-121">Desktop</span></span>           | <span data-ttu-id="f2786-122">**Desktop**</span><span class="sxs-lookup"><span data-stu-id="f2786-122">**Desktop**</span></span>                                |
| <span data-ttu-id="f2786-123">Rete intera</span><span class="sxs-lookup"><span data-stu-id="f2786-123">Entire Network</span></span>    | <span data-ttu-id="f2786-124">**NetworkNeighborhood** \\ **EntireNetwork**</span><span class="sxs-lookup"><span data-stu-id="f2786-124">**NetworkNeighborhood**\\**EntireNetwork**</span></span> |
| <span data-ttu-id="f2786-125">Risorse del computer</span><span class="sxs-lookup"><span data-stu-id="f2786-125">My Computer</span></span>       | <span data-ttu-id="f2786-126">**MyComputer**</span><span class="sxs-lookup"><span data-stu-id="f2786-126">**MyComputer**</span></span>                             |
| <span data-ttu-id="f2786-127">Risorse di rete</span><span class="sxs-lookup"><span data-stu-id="f2786-127">My Network Places</span></span> | <span data-ttu-id="f2786-128">**NetworkNeighborhood**</span><span class="sxs-lookup"><span data-stu-id="f2786-128">**NetworkNeighborhood**</span></span>                    |
| <span data-ttu-id="f2786-129">Computer remoto</span><span class="sxs-lookup"><span data-stu-id="f2786-129">Remote Computer</span></span>   | <span data-ttu-id="f2786-130">**ComputerRemoto**</span><span class="sxs-lookup"><span data-stu-id="f2786-130">**RemoteComputer**</span></span>                         |
| <span data-ttu-id="f2786-131">File utente</span><span class="sxs-lookup"><span data-stu-id="f2786-131">Users Files</span></span>       | <span data-ttu-id="f2786-132">**UsersFiles**</span><span class="sxs-lookup"><span data-stu-id="f2786-132">**UsersFiles**</span></span>                             |



 

<span data-ttu-id="f2786-133">Le estensioni remote devono essere inizializzate con [**IRemoteComputer**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iremotecomputer).</span><span class="sxs-lookup"><span data-stu-id="f2786-133">Remote extensions must be initialized with [**IRemoteComputer**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iremotecomputer).</span></span>

## <a name="using-file-system-folders-as-junction-points"></a><span data-ttu-id="f2786-134">Uso delle cartelle del file System come punti di giunzione</span><span class="sxs-lookup"><span data-stu-id="f2786-134">Using File System Folders as Junction Points</span></span>

<span data-ttu-id="f2786-135">Esistono due modi per definire file system cartelle come punti di giunzione.</span><span class="sxs-lookup"><span data-stu-id="f2786-135">There are two ways to define file system folders as junction points.</span></span> <span data-ttu-id="f2786-136">L'approccio più semplice consiste nel creare una cartella nel percorso appropriato e aggiungere un punto al nome della cartella, seguito dal formato stringa del CLSID dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="f2786-136">The simplest approach is to create a folder in the appropriate location and append a period to the folder's name, followed by the string form of the CLSID of your extension.</span></span> <span data-ttu-id="f2786-137">Solo il nome della cartella sarà visibile in Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="f2786-137">Only the folder name will be visible in Windows Explorer.</span></span> <span data-ttu-id="f2786-138">Nell'esempio seguente viene creato un punto di giunzione con un nome visualizzato di cartella.</span><span class="sxs-lookup"><span data-stu-id="f2786-138">The following example creates a junction point with a display name of MyFolder.</span></span>


```
MyFolder.{Extension CLSID}
```



<span data-ttu-id="f2786-139">In alternativa, è possibile definire una cartella denominata convenzionalmente come punto di giunzione per:</span><span class="sxs-lookup"><span data-stu-id="f2786-139">Alternatively, you can define a conventionally named folder as a junction point by:</span></span>

-   <span data-ttu-id="f2786-140">Rendere la cartella di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="f2786-140">Making the folder read-only.</span></span>
-   <span data-ttu-id="f2786-141">Creazione della cartella di una cartella di sistema chiamando [**PathMakeSystemFolder**](/windows/desktop/api/Shlwapi/nf-shlwapi-pathmakesystemfoldera).</span><span class="sxs-lookup"><span data-stu-id="f2786-141">Making the folder a system folder by calling [**PathMakeSystemFolder**](/windows/desktop/api/Shlwapi/nf-shlwapi-pathmakesystemfoldera).</span></span>
-   <span data-ttu-id="f2786-142">Inserimento di un file di Desktop.ini nascosto nella cartella che include il CLSID dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="f2786-142">Placing a hidden Desktop.ini file in the folder that includes the extension's CLSID.</span></span>

<span data-ttu-id="f2786-143">Desktop.ini è un file di testo standard che può essere aggiunto a qualsiasi cartella per personalizzare alcuni aspetti del comportamento della cartella.</span><span class="sxs-lookup"><span data-stu-id="f2786-143">Desktop.ini is a standard text file that can be added to any folder to customize certain aspects of the folder's behavior.</span></span> <span data-ttu-id="f2786-144">Per informazioni generali su come usare questo file, vedere [How to Customize Folders with Desktop.ini](how-to-customize-folders-with-desktop-ini.md).</span><span class="sxs-lookup"><span data-stu-id="f2786-144">For a general discussion of how to use this file, see [How to Customize Folders with Desktop.ini](how-to-customize-folders-with-desktop-ini.md).</span></span> <span data-ttu-id="f2786-145">Per definire una cartella come punto di giunzione, il \[ . \] La sezione ShellClassInfo di Desktop.ini deve contenere il CLSID dell'estensione, come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="f2786-145">To define a folder as a junction point, the \[.ShellClassInfo\] section of Desktop.ini must contain the extension's CLSID as follows:</span></span>


```
[.ShellClassInfo]
CLSID={Extension CLSID}
```



## <a name="opening-a-view-of-a-namespace-extension"></a><span data-ttu-id="f2786-146">Apertura di una visualizzazione di un'estensione dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f2786-146">Opening a View of a Namespace Extension</span></span>

<span data-ttu-id="f2786-147">Quando un utente accede a un punto di giunzione, Esplora risorse crea automaticamente una visualizzazione della cartella radice.</span><span class="sxs-lookup"><span data-stu-id="f2786-147">When a user browses into a junction point, Windows Explorer automatically creates a view of the root folder.</span></span> <span data-ttu-id="f2786-148">È anche possibile creare una vista avviando esplicitamente Explorer.exe con il CLSID dell'estensione come argomento.</span><span class="sxs-lookup"><span data-stu-id="f2786-148">You can also create a view by explicitly launching Explorer.exe with the extension's CLSID as an argument.</span></span> <span data-ttu-id="f2786-149">È possibile, ad esempio, usare questo approccio per avviare una visualizzazione di un'estensione da un menu di scelta rapida o da un collegamento.</span><span class="sxs-lookup"><span data-stu-id="f2786-149">You can, for instance, use this approach to launch a view of an extension from a shortcut menu or shortcut.</span></span> <span data-ttu-id="f2786-150">Ad esempio, per avviare una visualizzazione di estensione che include una visualizzazione albero, è possibile usare la stringa di comando seguente.</span><span class="sxs-lookup"><span data-stu-id="f2786-150">For example, to launch a view of MyExtension that includes a tree view, you can use the following command string.</span></span>


```
%SystemRoot%\Explorer.exe /e,::{MyExtension CLSID}
```



<span data-ttu-id="f2786-151">Una stringa di comando alternativa può essere usata per avviare una visualizzazione di un oggetto all'interno dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="f2786-151">An alternative command string can be used to launch a view of an object within the extension.</span></span> <span data-ttu-id="f2786-152">Questa funzionalità può essere utile, ad esempio, per un'estensione che utilizza una visualizzazione cartelle per consentire agli utenti di visualizzare il contenuto di uno dei diversi file compressi.</span><span class="sxs-lookup"><span data-stu-id="f2786-152">This feature would be useful, for instance, for an extension that uses a folder view to allow users to view the contents of one of a number of compressed files.</span></span>


```
%SystemRoot%\Explorer.exe /e,::{MyExtension CLSID},objectname
```



<span data-ttu-id="f2786-153">Il parametro *ObjectName* è il nome dell'oggetto che deve essere visualizzato.</span><span class="sxs-lookup"><span data-stu-id="f2786-153">The *objectname* parameter is the name of the object that is to be viewed.</span></span> <span data-ttu-id="f2786-154">Esplora risorse converte il nome nel PIDL corrispondente e passa il PIDL al metodo [**IPersistFolder:: Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistfolder-initialize) dell'oggetto nuova cartella.</span><span class="sxs-lookup"><span data-stu-id="f2786-154">Windows Explorer converts the name to its corresponding PIDL and passes the PIDL to the new folder object's [**IPersistFolder::Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistfolder-initialize) method.</span></span>

> [!Note]  
> <span data-ttu-id="f2786-155">La stringa CLSID deve essere preceduta da una coppia di due punti (::) in alternativa, il comando avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="f2786-155">The CLSID string must be preceded by a pair of colons (::) or the command will fail.</span></span> <span data-ttu-id="f2786-156">Il flag Slash-e (/e) usato nelle due righe di comando di esempio illustrate in precedenza indica a Esplora risorse di visualizzare una visualizzazione albero.</span><span class="sxs-lookup"><span data-stu-id="f2786-156">The slash-e (/e) flag used in the two sample command lines shown previously instructs Windows Explorer to display a tree view.</span></span> <span data-ttu-id="f2786-157">Il flag deve essere separato dai due puntini di una virgola.</span><span class="sxs-lookup"><span data-stu-id="f2786-157">The flag must be separated from the two colons by a comma.</span></span> <span data-ttu-id="f2786-158">Se non si desidera una visualizzazione albero, omettere il flag/e e la virgola.</span><span class="sxs-lookup"><span data-stu-id="f2786-158">If you do not want a tree view, omit the /e flag and the comma.</span></span>

 

 

 



