---
description: Viene illustrato come implementare un'estensione dello spazio dei nomi della shell, inclusi il comportamento del menu di scelta rapida e le attività personalizzate nel browser.
title: Esempio di provider di dati Explorer
ms.topic: article
ms.date: 05/31/2018
ms.assetid: B1B20AF8-3DDE-467b-A49E-A77849CF9F1B
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 6bd15cbef62ff69efcccd28fcb625fc1432fdf89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233566"
---
# <a name="explorer-data-provider-sample"></a><span data-ttu-id="6ae1a-103">Esempio di provider di dati Explorer</span><span class="sxs-lookup"><span data-stu-id="6ae1a-103">Explorer Data Provider Sample</span></span>

<span data-ttu-id="6ae1a-104">Viene illustrato come implementare un'estensione dello spazio dei nomi della shell, inclusi il comportamento del menu di scelta rapida e le attività personalizzate nel browser.</span><span class="sxs-lookup"><span data-stu-id="6ae1a-104">Demonstrates how to implement a Shell namespace extension, including context menu behavior and custom tasks in the browser.</span></span>

<span data-ttu-id="6ae1a-105">In questo argomento sono contenute le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="6ae1a-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="6ae1a-106">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6ae1a-106">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="6ae1a-107">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="6ae1a-107">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="6ae1a-108">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="6ae1a-108">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="6ae1a-109">Esecuzione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="6ae1a-109">Running the Sample</span></span>](#running-the-sample)

## <a name="requirements"></a><span data-ttu-id="6ae1a-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6ae1a-110">Requirements</span></span>



| <span data-ttu-id="6ae1a-111">Prodotto</span><span class="sxs-lookup"><span data-stu-id="6ae1a-111">Product</span></span>                                | <span data-ttu-id="6ae1a-112">Versione minima del prodotto</span><span class="sxs-lookup"><span data-stu-id="6ae1a-112">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="6ae1a-113">Windows</span><span class="sxs-lookup"><span data-stu-id="6ae1a-113">Windows</span></span>                                | <span data-ttu-id="6ae1a-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6ae1a-114">Windows Vista</span></span>           |
| <span data-ttu-id="6ae1a-115">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="6ae1a-115">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="6ae1a-116">6.1</span><span class="sxs-lookup"><span data-stu-id="6ae1a-116">6.1</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="6ae1a-117">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="6ae1a-117">Downloading the Sample</span></span>

| <span data-ttu-id="6ae1a-118">Location</span><span class="sxs-lookup"><span data-stu-id="6ae1a-118">Location</span></span>      | <span data-ttu-id="6ae1a-119">URL percorso</span><span class="sxs-lookup"><span data-stu-id="6ae1a-119">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ae1a-120">GitHub</span><span class="sxs-lookup"><span data-stu-id="6ae1a-120">GitHub</span></span>  | [<span data-ttu-id="6ae1a-121">Esempio ExplorerDataProvider</span><span class="sxs-lookup"><span data-stu-id="6ae1a-121">ExplorerDataProvider sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/shellextensibility/explorerdataprovider) |

## <a name="building-the-sample"></a><span data-ttu-id="6ae1a-122">Compilazione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="6ae1a-122">Building the Sample</span></span>

<span data-ttu-id="6ae1a-123">Per compilare l'esempio dal prompt dei comandi:</span><span class="sxs-lookup"><span data-stu-id="6ae1a-123">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="6ae1a-124">Aprire la finestra del prompt dei comandi e passare alla directory del progetto **ExplorerDataProvider** .</span><span class="sxs-lookup"><span data-stu-id="6ae1a-124">Open the command prompt window and navigate to the **ExplorerDataProvider** project directory.</span></span>
2.  <span data-ttu-id="6ae1a-125">Immettere `msbuild ExplorerDataProvider.sln`.</span><span class="sxs-lookup"><span data-stu-id="6ae1a-125">Enter `msbuild ExplorerDataProvider.sln`.</span></span>

<span data-ttu-id="6ae1a-126">Per compilare l'esempio usando Microsoft Visual Studio (scelta consigliata):</span><span class="sxs-lookup"><span data-stu-id="6ae1a-126">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="6ae1a-127">Aprire Esplora risorse e passare alla directory del progetto **ExplorerDataProvider** .</span><span class="sxs-lookup"><span data-stu-id="6ae1a-127">Open Windows Explorer and navigate to the **ExplorerDataProvider** project directory.</span></span>
2.  <span data-ttu-id="6ae1a-128">Fare doppio clic sull'icona per il file ExplorerDataProvider. sln per aprire il progetto in Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="6ae1a-128">Double-click the icon for the ExplorerDataProvider.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="6ae1a-129">Scegliere **Compila soluzione** dal menu **Compila** .</span><span class="sxs-lookup"><span data-stu-id="6ae1a-129">From the **Build** menu, select **Build Solution**.</span></span> <span data-ttu-id="6ae1a-130">La DLL verrà compilata nella \\ directory di debug o di \\ versione predefinita.</span><span class="sxs-lookup"><span data-stu-id="6ae1a-130">The DLL will be built in the default \\Debug or \\Release directory.</span></span>

> [!Note]  
> <span data-ttu-id="6ae1a-131">Nella versione di questo esempio inclusa nella Windows SDK la configurazione per la build di rilascio a 64 bit non include il file ExplorerDataProvider. def nell'opzione del **file di definizione del modulo** del linker.</span><span class="sxs-lookup"><span data-stu-id="6ae1a-131">In the version of this sample included in the Windows SDK, the configuration for the 64-bit Release build does not include the ExplorerDataProvider.def file in the linker's **Module Definition File** option.</span></span> <span data-ttu-id="6ae1a-132">È necessario specificare il file manualmente prima della compilazione in un ambiente a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="6ae1a-132">You must specify that file yourself before building in a 64-bit environment.</span></span> <span data-ttu-id="6ae1a-133">Aggiungere la riga `ModuleDefinitionFile="ExplorerDataProvider.def"` alla sezione VCLinkerTool (inizia alla riga 329) del file ExplorerDataProvider. vcproj, come illustrato di seguito:</span><span class="sxs-lookup"><span data-stu-id="6ae1a-133">Add the line `ModuleDefinitionFile="ExplorerDataProvider.def"` to the VCLinkerTool section (begins at line 329) of the ExplorerDataProvider.vcproj file as shown here:</span></span>
>
> <span codelanguage=""></span>
>
> <table>
> <colgroup>
> <col style="width: 100%" />
> </colgroup>
> <tbody>
> <tr class="odd">
> <td><pre><code>LinkIncremental=&quot;1&quot;
> AdditionalLibraryDirectories=&quot;&quot;c:\Program Files\Microsoft SDKs\Windows\v6.0\Lib\x64&quot;&quot;
> ModuleDefinitionFile=&quot;ExplorerDataProvider.def&quot;
> GenerateDebugInformation=&quot;true&quot;</code></pre></td>
> </tr>
> </tbody>
> </table> 
>
> <span data-ttu-id="6ae1a-134">La versione di questo esempio scaricabile dalla raccolta codici è stata corretta per questo problema e non è richiesta alcuna azione aggiuntiva da parte dell'utente.</span><span class="sxs-lookup"><span data-stu-id="6ae1a-134">The version of this sample downloadable from Code Gallery has been corrected for this issue and no extra action is required on your part.</span></span>
>
>  
>
> ## <a name="running-the-sample"></a><span data-ttu-id="6ae1a-135">Esecuzione dell'esempio</span><span class="sxs-lookup"><span data-stu-id="6ae1a-135">Running the Sample</span></span>
>
> 1.  <span data-ttu-id="6ae1a-136">Passare alla directory che contiene il nuovo file. dll e. propdesc, utilizzando il prompt dei comandi o Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="6ae1a-136">Navigate to the directory that contains the new .dll and .propdesc file, using the command prompt or Windows Explorer.</span></span>
> 2.  <span data-ttu-id="6ae1a-137">Nella riga di comando digitare `regsvr32.exe` .</span><span class="sxs-lookup"><span data-stu-id="6ae1a-137">At the command line, type `regsvr32.exe`.</span></span>
>     > [!Note]  
>     > <span data-ttu-id="6ae1a-138">Se si esegue questo comando da un prompt dei comandi con privilegi elevati, la registrazione automatica registrerà automaticamente anche il file con estensione propdesc.</span><span class="sxs-lookup"><span data-stu-id="6ae1a-138">If you run this command from an elevated command prompt, the self-registration will also register the .propdesc file automatically.</span></span> <span data-ttu-id="6ae1a-139">Se viene eseguito da un prompt dei comandi non con privilegi elevati, l'estensione dello spazio dei nomi funzionerà, ma senza la funzionalità personalizzata della proprietà.</span><span class="sxs-lookup"><span data-stu-id="6ae1a-139">If it is run from a non-elevated command prompt then the namespace extension will work, but without custom property functionality.</span></span>
>
>      
>
> 3.  <span data-ttu-id="6ae1a-140">Aprire la cartella **computer locale** e visualizzare la nuova estensione dello spazio dei nomi presente in tale cartella.</span><span class="sxs-lookup"><span data-stu-id="6ae1a-140">Open the **My Computer** folder and browse the new namespace extension present there.</span></span>
>
>  
>
>  
>


