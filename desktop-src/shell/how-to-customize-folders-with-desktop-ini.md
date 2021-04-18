---
description: Personalizzazione dell'aspetto e del comportamento di una singola cartella con Desktop.ini.
ms.assetid: 0361b7da-bfb3-4880-b982-85d2fe419805
title: Come personalizzare le cartelle con Desktop.ini
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eaac3e6a96257e63b5e4210da0aa6e6e1db77eaf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104553380"
---
# <a name="how-to-customize-folders-with-desktopini"></a><span data-ttu-id="4d11f-103">Come personalizzare le cartelle con Desktop.ini</span><span class="sxs-lookup"><span data-stu-id="4d11f-103">How to Customize Folders with Desktop.ini</span></span>

<span data-ttu-id="4d11f-104">Le cartelle del file System vengono in genere visualizzate con un'icona standard e un set di proprietà, che specificano, ad esempio, se la cartella è condivisa.</span><span class="sxs-lookup"><span data-stu-id="4d11f-104">File system folders are commonly displayed with a standard icon and set of properties, which specify, for instance, whether the folder is shared.</span></span> <span data-ttu-id="4d11f-105">È possibile personalizzare l'aspetto e il comportamento di una singola cartella creando un file di Desktop.ini per la cartella.</span><span class="sxs-lookup"><span data-stu-id="4d11f-105">You can customize the appearance and behavior of an individual folder by creating a Desktop.ini file for that folder.</span></span>

## <a name="instructions"></a><span data-ttu-id="4d11f-106">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="4d11f-106">Instructions</span></span>

### <a name="using-desktopini-files"></a><span data-ttu-id="4d11f-107">Uso di file di Desktop.ini</span><span class="sxs-lookup"><span data-stu-id="4d11f-107">Using Desktop.ini Files</span></span>

<span data-ttu-id="4d11f-108">Le cartelle vengono normalmente visualizzate con l'icona della cartella standard.</span><span class="sxs-lookup"><span data-stu-id="4d11f-108">Folders are normally displayed with the standard folder icon.</span></span> <span data-ttu-id="4d11f-109">Un uso comune del file Desktop.ini consiste nell'assegnare un'icona personalizzata o un'immagine di anteprima a una cartella.</span><span class="sxs-lookup"><span data-stu-id="4d11f-109">A common use of the Desktop.ini file is to assign a custom icon or thumbnail image to a folder.</span></span> <span data-ttu-id="4d11f-110">È inoltre possibile utilizzare Desktop.ini per creare un *infotip* che visualizza informazioni sulla cartella e controlla alcuni aspetti del comportamento della cartella, ad esempio specificando nomi localizzati per la cartella o gli elementi nella cartella.</span><span class="sxs-lookup"><span data-stu-id="4d11f-110">You can also use Desktop.ini to create an *infotip* that displays information about the folder and controls some aspects of the folder's behavior, such as specifying localized names for the folder or items in the folder.</span></span>

<span data-ttu-id="4d11f-111">**Utilizzare la procedura seguente per personalizzare lo stile di una cartella con Desktop.ini:**</span><span class="sxs-lookup"><span data-stu-id="4d11f-111">**Use the following procedure to customize a folder's style with Desktop.ini:**</span></span>

1.  <span data-ttu-id="4d11f-112">Usare [**PathMakeSystemFolder**](/windows/desktop/api/Shlwapi/nf-shlwapi-pathmakesystemfoldera) per rendere la cartella una cartella di sistema.</span><span class="sxs-lookup"><span data-stu-id="4d11f-112">Use [**PathMakeSystemFolder**](/windows/desktop/api/Shlwapi/nf-shlwapi-pathmakesystemfoldera) to make the folder a system folder.</span></span> <span data-ttu-id="4d11f-113">In questo modo viene impostato il bit di sola lettura nella cartella per indicare che è necessario abilitare il comportamento speciale riservato per Desktop.ini.</span><span class="sxs-lookup"><span data-stu-id="4d11f-113">This sets the read-only bit on the folder to indicate that the special behavior reserved for Desktop.ini should be enabled.</span></span> <span data-ttu-id="4d11f-114">È anche possibile creare una cartella di sistema dalla riga di comando usando **attrib + s** *FolderName*.</span><span class="sxs-lookup"><span data-stu-id="4d11f-114">You can also make a folder a system folder from the command line by using **attrib +s** *FolderName*.</span></span>
2.  <span data-ttu-id="4d11f-115">Creare un file di Desktop.ini per la cartella.</span><span class="sxs-lookup"><span data-stu-id="4d11f-115">Create a Desktop.ini file for the folder.</span></span> <span data-ttu-id="4d11f-116">È necessario contrassegnarlo come *nascosto* e *sistema* per assicurarsi che sia nascosto agli utenti normali.</span><span class="sxs-lookup"><span data-stu-id="4d11f-116">You should mark it as *hidden* and *system* to ensure that it is hidden from normal users.</span></span>
3.  <span data-ttu-id="4d11f-117">Verificare che il file Desktop.ini creato sia in formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="4d11f-117">Make sure the Desktop.ini file that you create is in the Unicode format.</span></span> <span data-ttu-id="4d11f-118">Questa operazione è necessaria per archiviare le stringhe localizzate che possono essere visualizzate dagli utenti.</span><span class="sxs-lookup"><span data-stu-id="4d11f-118">This is necessary to store the localized strings that can be displayed to users.</span></span>

### <a name="creating-a-desktopini-file"></a><span data-ttu-id="4d11f-119">Creazione di un file di Desktop.ini</span><span class="sxs-lookup"><span data-stu-id="4d11f-119">Creating a Desktop.ini File</span></span>

<span data-ttu-id="4d11f-120">Il file di Desktop.ini è un file di testo che consente di specificare la modalità di visualizzazione di una cartella file system.</span><span class="sxs-lookup"><span data-stu-id="4d11f-120">The Desktop.ini file is a text file that allows you to specify how a file system folder is viewed.</span></span> <span data-ttu-id="4d11f-121">Oggetto \[ . \] La sezione ShellClassInfo consente di personalizzare la visualizzazione della cartella assegnando valori a diverse voci:</span><span class="sxs-lookup"><span data-stu-id="4d11f-121">The \[.ShellClassInfo\] section, allows you to customize the folder's view by assigning values to several entries:</span></span>

|                   |                                                                                                                                                                                                                                                                                                                                                                                |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d11f-122">**Voce**</span><span class="sxs-lookup"><span data-stu-id="4d11f-122">**Entry**</span></span>         | <span data-ttu-id="4d11f-123">**Valore**</span><span class="sxs-lookup"><span data-stu-id="4d11f-123">**Value**</span></span>                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="4d11f-124">**ConfirmFileOp**</span><span class="sxs-lookup"><span data-stu-id="4d11f-124">**ConfirmFileOp**</span></span> | <span data-ttu-id="4d11f-125">Impostare questa voce su 0 per evitare che venga visualizzato l'avviso "si sta eliminando una cartella di sistema" quando si elimina o si trasferisce la cartella.</span><span class="sxs-lookup"><span data-stu-id="4d11f-125">Set this entry to 0 to avoid a "You Are Deleting a System Folder" warning when deleting or moving the folder.</span></span>                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="4d11f-126">**Nosharing**</span><span class="sxs-lookup"><span data-stu-id="4d11f-126">**NoSharing**</span></span>     | <span data-ttu-id="4d11f-127">Non supportato in Windows Vista o versioni successive.</span><span class="sxs-lookup"><span data-stu-id="4d11f-127">Not supported under Windows Vista or later.</span></span> <span data-ttu-id="4d11f-128">Impostare questa voce su 1 per impedire la condivisione della cartella.</span><span class="sxs-lookup"><span data-stu-id="4d11f-128">Set this entry to 1 to prevent the folder from being shared.</span></span>                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="4d11f-129">**IconFile**</span><span class="sxs-lookup"><span data-stu-id="4d11f-129">**IconFile**</span></span>      | <span data-ttu-id="4d11f-130">Se si desidera specificare un'icona personalizzata per la cartella, impostare questa voce sul nome file dell'icona.</span><span class="sxs-lookup"><span data-stu-id="4d11f-130">If you want to specify a custom icon for the folder, set this entry to the icon's file name.</span></span> <span data-ttu-id="4d11f-131">L'estensione del nome di file ico è preferibile, ma è anche possibile specificare file con estensione bmp o exe e DLL contenenti icone.</span><span class="sxs-lookup"><span data-stu-id="4d11f-131">The .ico file name extension is preferred, but it is also possible to specify .bmp files, or .exe and .dll files that contain icons.</span></span> <span data-ttu-id="4d11f-132">Se si usa un percorso relativo, l'icona è disponibile per gli utenti che visualizzano la cartella sulla rete.</span><span class="sxs-lookup"><span data-stu-id="4d11f-132">If you use a relative path, the icon is available to people who view the folder over the network.</span></span> <span data-ttu-id="4d11f-133">È anche necessario impostare la voce **IconIndex** .</span><span class="sxs-lookup"><span data-stu-id="4d11f-133">You must also set the **IconIndex** entry.</span></span> |
| <span data-ttu-id="4d11f-134">**IconIndex**</span><span class="sxs-lookup"><span data-stu-id="4d11f-134">**IconIndex**</span></span>     | <span data-ttu-id="4d11f-135">Impostare questa voce per specificare l'indice per un'icona personalizzata.</span><span class="sxs-lookup"><span data-stu-id="4d11f-135">Set this entry to specify the index for a custom icon.</span></span> <span data-ttu-id="4d11f-136">Se il file assegnato a **IconFile** contiene solo una singola icona, impostare **IconIndex** su 0.</span><span class="sxs-lookup"><span data-stu-id="4d11f-136">If the file assigned to **IconFile** only contains a single icon, set **IconIndex** to 0.</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="4d11f-137">**InfoTip**</span><span class="sxs-lookup"><span data-stu-id="4d11f-137">**InfoTip**</span></span>       | <span data-ttu-id="4d11f-138">Impostare questa voce su una stringa di testo informativo.</span><span class="sxs-lookup"><span data-stu-id="4d11f-138">Set this entry to an informational text string.</span></span> <span data-ttu-id="4d11f-139">Viene visualizzato come infotip quando il cursore passa il puntatore del mouse sulla cartella.</span><span class="sxs-lookup"><span data-stu-id="4d11f-139">It is displayed as an infotip when the cursor hovers over the folder.</span></span> <span data-ttu-id="4d11f-140">Se l'utente fa clic sulla cartella, il testo delle informazioni viene visualizzato nel blocco di informazioni della cartella, sotto le informazioni standard.</span><span class="sxs-lookup"><span data-stu-id="4d11f-140">If the user clicks the folder, the information text is displayed in the folder's information block, below the standard information.</span></span>                                                                                                                      |



 

<span data-ttu-id="4d11f-141">Le illustrazioni seguenti sono della cartella Music con un file di Desktop.ini personalizzato.</span><span class="sxs-lookup"><span data-stu-id="4d11f-141">The following illustrations are of the Music folder with a custom Desktop.ini file.</span></span> <span data-ttu-id="4d11f-142">La cartella ora:</span><span class="sxs-lookup"><span data-stu-id="4d11f-142">The folder now:</span></span>

-   <span data-ttu-id="4d11f-143">Dispone di un'icona personalizzata.</span><span class="sxs-lookup"><span data-stu-id="4d11f-143">Has a custom icon.</span></span>
-   <span data-ttu-id="4d11f-144">Non Visualizza l'avviso "si sta eliminando una cartella di sistema" se la cartella viene spostata o eliminata.</span><span class="sxs-lookup"><span data-stu-id="4d11f-144">Does not display a "You Are Deleting a System Folder" warning if the folder is moved or deleted.</span></span>
-   <span data-ttu-id="4d11f-145">Non può essere condivisa.</span><span class="sxs-lookup"><span data-stu-id="4d11f-145">Cannot be shared.</span></span>
-   <span data-ttu-id="4d11f-146">Visualizza il testo informativo quando il cursore passa sulla cartella.</span><span class="sxs-lookup"><span data-stu-id="4d11f-146">Displays informational text when the cursor hovers over the folder.</span></span>

<span data-ttu-id="4d11f-147">Le opzioni della cartella nelle illustrazioni seguenti sono impostate per visualizzare i file nascosti, in modo che Desktop.ini sia visibile.</span><span class="sxs-lookup"><span data-stu-id="4d11f-147">The folder options in the following illustrations are set to show hidden files so that Desktop.ini is visible.</span></span> <span data-ttu-id="4d11f-148">La cartella ha un aspetto simile al seguente:</span><span class="sxs-lookup"><span data-stu-id="4d11f-148">The folder looks like this:</span></span>

![screenshot della cartella con icona personalizzata](images/webview4.jpg)

<span data-ttu-id="4d11f-150">Quando il cursore viene posizionato sulla cartella, viene visualizzato infotip.</span><span class="sxs-lookup"><span data-stu-id="4d11f-150">When the cursor hovers over the folder, the infotip is displayed.</span></span>

![screenshot della cartella con un infotip](images/webview6.jpg)

<span data-ttu-id="4d11f-152">L'icona personalizzata sostituisce l'icona della cartella in qualsiasi posizione in cui viene visualizzato il nome della cartella.</span><span class="sxs-lookup"><span data-stu-id="4d11f-152">The custom icon replaces the folder icon everywhere the folder name appears.</span></span>

![screenshot dell'icona personalizzata che sostituisce la cartella](images/webview5.jpg)

<span data-ttu-id="4d11f-154">Il file di desktop.ini seguente è stato usato per personalizzare la cartella Music, come illustrato nelle illustrazioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="4d11f-154">The following desktop.ini file was used to customize the Music folder, as seen in the preceding illustrations.</span></span>


```
[.ShellClassInfo]
ConfirmFileOp=0
NoSharing=1
IconFile=Folder.ico
IconIndex=0
InfoTip=Some sensible information.
```



 

 



