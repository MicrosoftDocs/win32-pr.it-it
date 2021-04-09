---
title: Introduzione con la procedura guidata plug-in
description: Introduzione con la procedura guidata plug-in
ms.assetid: 77fc1b0c-20f5-434d-9142-f112489a7f08
keywords:
- Plug-in di Windows Media Player, installazione guidata plug-in
- plug-in, installazione guidata plug-in
- creazione di plug-in, installazione guidata plug-in
- Creazione guidata plug-in di Windows Media Player, installazione
- installazione guidata plug-in
- procedura guidata plug-in
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a4feb9cfa60c120bfc5bb675ea8a8078b95ad14
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955678"
---
# <a name="getting-started-with-the-plug-in-wizard"></a><span data-ttu-id="2227a-109">Introduzione con la procedura guidata plug-in</span><span class="sxs-lookup"><span data-stu-id="2227a-109">Getting Started with the Plug-in Wizard</span></span>

<span data-ttu-id="2227a-110">Per configurare l'ambiente di sviluppo per la creazione di plug-in di Windows Media Player, è necessario installare gli elementi seguenti:</span><span class="sxs-lookup"><span data-stu-id="2227a-110">To set up your development environment for creating Windows Media Player plug-ins, you must install the following items:</span></span>

-   <span data-ttu-id="2227a-111">Microsoft Visual Studio .NET 2003 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="2227a-111">Microsoft Visual Studio .NET 2003 or later</span></span>
-   <span data-ttu-id="2227a-112">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="2227a-112">Windows Media Player 9 Series or later</span></span>
-   <span data-ttu-id="2227a-113">Windows SDK, che include Windows Media Player SDK</span><span class="sxs-lookup"><span data-stu-id="2227a-113">Windows SDK, which includes the Windows Media Player SDK</span></span>
-   <span data-ttu-id="2227a-114">Procedura guidata plug-in di Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="2227a-114">Windows Media Player Plug-in Wizard</span></span>

## <a name="installing-the-wizard"></a><span data-ttu-id="2227a-115">Installazione della procedura guidata</span><span class="sxs-lookup"><span data-stu-id="2227a-115">Installing the Wizard</span></span>

<span data-ttu-id="2227a-116">Per installare la creazione guidata plug-in di Windows Media Player, attenersi alla procedura riportata di seguito.</span><span class="sxs-lookup"><span data-stu-id="2227a-116">Perform the following steps to install the Windows Media Player Plug-in Wizard.</span></span>

1.  <span data-ttu-id="2227a-117">Individuare la cartella in cui è stato installato il Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="2227a-117">Locate the folder where you installed the Windows SDK.</span></span> <span data-ttu-id="2227a-118">Espandere la cartella per visualizzare le relative sottocartelle e passare a esempi di \\ strumenti multimediali per \\ WMP \\ \\ wmpwiz.</span><span class="sxs-lookup"><span data-stu-id="2227a-118">Expand the folder to view its subfolders, and navigate to Samples\\Multimedia\\WMP\\wizards\\wmpwiz.</span></span>
2.  <span data-ttu-id="2227a-119">Individuare i tre file seguenti:</span><span class="sxs-lookup"><span data-stu-id="2227a-119">Locate the following three files:</span></span>
    -   <span data-ttu-id="2227a-120">wmpwiz. vsz</span><span class="sxs-lookup"><span data-stu-id="2227a-120">wmpwiz.vsz</span></span>
    -   <span data-ttu-id="2227a-121">wmpwiz. vsdir</span><span class="sxs-lookup"><span data-stu-id="2227a-121">wmpwiz.vsdir</span></span>
    -   <span data-ttu-id="2227a-122">wmpwiz. ico</span><span class="sxs-lookup"><span data-stu-id="2227a-122">wmpwiz.ico</span></span>
3.  <span data-ttu-id="2227a-123">Utilizzando un editor di testo, ad esempio Blocco note, modificare il file wmpwiz. vsz.</span><span class="sxs-lookup"><span data-stu-id="2227a-123">Using a text editor, such as Notepad, edit the wmpwiz.vsz file.</span></span>

    <span data-ttu-id="2227a-124">Individuare la riga seguente:</span><span class="sxs-lookup"><span data-stu-id="2227a-124">Locate the following line:</span></span>

    ```
    Wizard=VsWizard.<VsWizardEngine version goes here>
    ```

    

    <span data-ttu-id="2227a-125">Passare `<VsWizardEngine version goes here>` a uno dei valori seguenti, a seconda della versione di Visual Studio installata.</span><span class="sxs-lookup"><span data-stu-id="2227a-125">Change `<VsWizardEngine version goes here>` to one of the following values, depending on which version of Visual Studio you have installed.</span></span>

    

    | <span data-ttu-id="2227a-126">Valore</span><span class="sxs-lookup"><span data-stu-id="2227a-126">Value</span></span>              | <span data-ttu-id="2227a-127">Versione di Visual Studio</span><span class="sxs-lookup"><span data-stu-id="2227a-127">Visual Studio version</span></span>   |
    |--------------------|-------------------------|
    | <span data-ttu-id="2227a-128">VsWizardEngine. 7.1</span><span class="sxs-lookup"><span data-stu-id="2227a-128">VsWizardEngine.7.1</span></span> | <span data-ttu-id="2227a-129">Visual Studio .NET 2003</span><span class="sxs-lookup"><span data-stu-id="2227a-129">Visual Studio .NET 2003</span></span> |
    | <span data-ttu-id="2227a-130">VsWizardEngine. 8.0</span><span class="sxs-lookup"><span data-stu-id="2227a-130">VsWizardEngine.8.0</span></span> | <span data-ttu-id="2227a-131">Visual Studio 2005</span><span class="sxs-lookup"><span data-stu-id="2227a-131">Visual Studio 2005</span></span>      |
    | <span data-ttu-id="2227a-132">VsWizardEngine. 9.0</span><span class="sxs-lookup"><span data-stu-id="2227a-132">VsWizardEngine.9.0</span></span> | <span data-ttu-id="2227a-133">Visual Studio 2008</span><span class="sxs-lookup"><span data-stu-id="2227a-133">Visual Studio 2008</span></span>      |

    

     

    <span data-ttu-id="2227a-134">Individuare la riga seguente:</span><span class="sxs-lookup"><span data-stu-id="2227a-134">Locate the following line:</span></span>

    ```
    Param="ABSOLUTE_PATH = <path to wmpwiz directory goes here>"
    ```

    

    <span data-ttu-id="2227a-135">Passare `<path to wmpwiz directory goes here>` al percorso in cui si trovano i file della procedura guidata.</span><span class="sxs-lookup"><span data-stu-id="2227a-135">Change `<path to wmpwiz directory goes here>` to the path where the wizard files are located.</span></span>

    <span data-ttu-id="2227a-136">Si supponga, ad esempio, di avere Visual Studio 2008 e che i file della procedura guidata siano disponibili qui: C: \\ programmi \\ Microsoft SDK \\ Windows \\ v 7.0 \\ esempi di \\ strumenti multimediali per \\ WMP \\ \\ wmpwiz.</span><span class="sxs-lookup"><span data-stu-id="2227a-136">For example, suppose you have Visual Studio 2008, and your wizard files are here: C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\WMP\\wizards\\wmpwiz.</span></span> <span data-ttu-id="2227a-137">Il file wmpwiz. vsz avrà un aspetto simile al seguente:</span><span class="sxs-lookup"><span data-stu-id="2227a-137">Then your wmpwiz.vsz file would look like this:</span></span>

    ```
    VSWIZARD 7.0
    Wizard=VsWizard.VsWizardEngine.9.0

    Param="WIZARD_NAME = Windows Media Player Plug-in Wizard"
    Param="ABSOLUTE_PATH = C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\Multimedia\WMP\wizards\wmpwiz"
    Param="FALLBACK_LCID = 1033"
    ```

    

4.  <span data-ttu-id="2227a-138">Individuare la cartella in cui è installato Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="2227a-138">Locate the folder where you installed Visual Studio.</span></span> <span data-ttu-id="2227a-139">Espandere la cartella per visualizzare le relative sottocartelle e individuare una cartella denominata vcprojects.</span><span class="sxs-lookup"><span data-stu-id="2227a-139">Expand the folder to view its subfolders, and locate a folder named vcprojects.</span></span>
5.  <span data-ttu-id="2227a-140">Copiare i tre file elencati nel passaggio 2 nella cartella VCProjects.</span><span class="sxs-lookup"><span data-stu-id="2227a-140">Copy the three files listed in step 2 to the vcprojects folder.</span></span> <span data-ttu-id="2227a-141">Ora è installata la procedura guidata.</span><span class="sxs-lookup"><span data-stu-id="2227a-141">The wizard is now installed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2227a-142">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2227a-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2227a-143">Creazione di un plug-in</span><span class="sxs-lookup"><span data-stu-id="2227a-143">Building a Plug-in</span></span>](building-a-plug-in.md)
</dt> <dt>

[<span data-ttu-id="2227a-144">Uso della procedura guidata plug-in con Visual Studio</span><span class="sxs-lookup"><span data-stu-id="2227a-144">Using the Plug-in Wizard with Visual Studio</span></span>](using-the-plug-in-wizard-with-visual-studio.md)
</dt> </dl>

 

 




