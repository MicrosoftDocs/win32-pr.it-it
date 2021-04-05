---
title: Installazione guidata plug-in di Store online
description: Installazione guidata plug-in di Store online
ms.assetid: 75f7c279-4800-4146-8198-1dc76472237d
keywords:
- Windows Media Player Online Stores, plug-in
- archivi online, plug-in
- digitare 1 negozi online, plug-in
- Windows Media Player Online Stores, creazione guidata plug-in
- negozi online, creazione guidata plug-in
- digitare 1 archivi online, creazione guidata plug-in
- Windows Media Player Online Stores, installazione guidata plug-in
- negozi online, installazione guidata plug-in
- digitare 1 negozi online, installazione guidata plug-in
- plug-in, archivi Windows Media Player online
- plug-in, archivi online
- plug-in, digitare 1 negozi online
- plug-in, installazione guidata plug-in
- plug-in, creazione guidata plug-in
- Plug-in di Windows Media Player, digitare 1 negozi online
- Plug-in di Windows Media Player, archivi online
- Plug-in di Windows Media Player, archivi Windows Media Player online
- Plug-in di Windows Media Player, installazione guidata plug-in
- Plug-in di Windows Media Player, creazione guidata plug-in
- installazione guidata plug-in
- procedura guidata plug-in
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13d236c2160c5783f909430e6b49ef2e6361de22
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044829"
---
# <a name="installing-the-online-store-plug-in-wizard"></a><span data-ttu-id="90995-124">Installazione guidata plug-in di Store online</span><span class="sxs-lookup"><span data-stu-id="90995-124">Installing the Online Store Plug-in Wizard</span></span>

<span data-ttu-id="90995-125">Per configurare l'ambiente di sviluppo per la creazione di plug-in di archivio online di tipo 1, è necessario installare gli elementi seguenti:</span><span class="sxs-lookup"><span data-stu-id="90995-125">To set up your development environment for creating type 1 online store plug-ins, you must install the following items:</span></span>

-   <span data-ttu-id="90995-126">Microsoft Visual Studio 2005 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="90995-126">Microsoft Visual Studio 2005 or later</span></span>
-   <span data-ttu-id="90995-127">Windows Media Player 11 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="90995-127">Windows Media Player 11 or later</span></span>
-   <span data-ttu-id="90995-128">Windows SDK, che include Windows Media Player SDK</span><span class="sxs-lookup"><span data-stu-id="90995-128">Windows SDK, which includes the Windows Media Player SDK</span></span>
-   <span data-ttu-id="90995-129">Procedura guidata plug-in di archivio online</span><span class="sxs-lookup"><span data-stu-id="90995-129">Online store plug-in wizard</span></span>

## <a name="installing-the-wizard"></a><span data-ttu-id="90995-130">Installazione della procedura guidata</span><span class="sxs-lookup"><span data-stu-id="90995-130">Installing the Wizard</span></span>

<span data-ttu-id="90995-131">Usare la procedura seguente per installare la procedura guidata plug-in di negozio online in Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="90995-131">Use the following steps to install the online store plug-in wizard in Visual Studio.</span></span>

1.  <span data-ttu-id="90995-132">Individuare la cartella in cui è stato installato il Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="90995-132">Locate the folder where you installed the Windows SDK.</span></span> <span data-ttu-id="90995-133">Espandere la cartella per visualizzare le relative sottocartelle e passare a esempi \\ Multimedia \\ WMP \\ Wizards \\ Services.</span><span class="sxs-lookup"><span data-stu-id="90995-133">Expand the folder to view its subfolders, and navigate to Samples\\Multimedia\\WMP\\wizards\\services.</span></span>
2.  <span data-ttu-id="90995-134">Individuare i tre file seguenti:</span><span class="sxs-lookup"><span data-stu-id="90995-134">Locate the following three files:</span></span>
    -   <span data-ttu-id="90995-135">wmpservices. vsz</span><span class="sxs-lookup"><span data-stu-id="90995-135">wmpservices.vsz</span></span>
    -   <span data-ttu-id="90995-136">wmpservices. vsdir</span><span class="sxs-lookup"><span data-stu-id="90995-136">wmpservices.vsdir</span></span>
    -   <span data-ttu-id="90995-137">wmpservices. ico</span><span class="sxs-lookup"><span data-stu-id="90995-137">wmpservices.ico</span></span>
3.  <span data-ttu-id="90995-138">Utilizzando un editor di testo, ad esempio Blocco note, modificare il file wmpservices. vsz.</span><span class="sxs-lookup"><span data-stu-id="90995-138">Using a text editor such as Notepad, edit the wmpservices.vsz file.</span></span>

    <span data-ttu-id="90995-139">Individuare la riga seguente:</span><span class="sxs-lookup"><span data-stu-id="90995-139">Locate the following line:</span></span>

    ```
    Wizard=VsWizard.<VsWizardEngine version goes here>
    ```

    

    <span data-ttu-id="90995-140">Passare `<VsWizardEngine version goes here>` a uno dei valori seguenti, a seconda della versione di Visual Studio installata.</span><span class="sxs-lookup"><span data-stu-id="90995-140">Change `<VsWizardEngine version goes here>` to one of the following values, depending on which version of Visual Studio you have installed.</span></span>

    

    | <span data-ttu-id="90995-141">Valore</span><span class="sxs-lookup"><span data-stu-id="90995-141">Value</span></span>              | <span data-ttu-id="90995-142">Versione di Visual Studio</span><span class="sxs-lookup"><span data-stu-id="90995-142">Visual Studio version</span></span> |
    |--------------------|-----------------------|
    | <span data-ttu-id="90995-143">VsWizardEngine. 8.0</span><span class="sxs-lookup"><span data-stu-id="90995-143">VsWizardEngine.8.0</span></span> | <span data-ttu-id="90995-144">Visual Studio 2005</span><span class="sxs-lookup"><span data-stu-id="90995-144">Visual Studio 2005</span></span>    |
    | <span data-ttu-id="90995-145">VsWizardEngine. 9.0</span><span class="sxs-lookup"><span data-stu-id="90995-145">VsWizardEngine.9.0</span></span> | <span data-ttu-id="90995-146">Visual Studio 2008</span><span class="sxs-lookup"><span data-stu-id="90995-146">Visual Studio 2008</span></span>    |

    

     

    <span data-ttu-id="90995-147">Individuare la riga seguente:</span><span class="sxs-lookup"><span data-stu-id="90995-147">Locate the following line:</span></span>

    ```
    Param="ABSOLUTE_PATH = <path to wmpservices directory goes here>"
    ```

    

    <span data-ttu-id="90995-148">Passare `<path to wmpservices directory goes here>` al percorso in cui si trovano i file della procedura guidata.</span><span class="sxs-lookup"><span data-stu-id="90995-148">Change `<path to wmpservices directory goes here>` to the path where the wizard files are located.</span></span>

    <span data-ttu-id="90995-149">Si supponga, ad esempio, di avere Visual Studio 2008 e che i file della procedura guidata siano qui: C: \\ programmi \\ Microsoft SDK \\ Windows \\ v 7.0 \\ esempi di \\ Multimedia \\ WMP \\ Wizards \\ Services.</span><span class="sxs-lookup"><span data-stu-id="90995-149">For example, suppose you have Visual Studio 2008, and your wizard files are here: C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\WMP\\wizards\\services.</span></span> <span data-ttu-id="90995-150">Il file wmpservices. vsz avrà un aspetto simile al seguente:</span><span class="sxs-lookup"><span data-stu-id="90995-150">Then your wmpservices.vsz file would look like this:</span></span>

    ```
    VSWIZARD 7.0
    Wizard=VsWizard.VsWizardEngine.9.0

    Param="WIZARD_NAME = wmpservices"
    Param="ABSOLUTE_PATH = C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\Multimedia\WMP\wizards\services"
    Param="FALLBACK_LCID = 1033"
    ```

    

4.  <span data-ttu-id="90995-151">Individuare la cartella in cui è installato Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="90995-151">Locate the folder where you installed Visual Studio.</span></span> <span data-ttu-id="90995-152">Espandere la cartella per visualizzare le relative sottocartelle e individuare una cartella denominata vcprojects.</span><span class="sxs-lookup"><span data-stu-id="90995-152">Expand the folder to view its subfolders, and locate a folder named vcprojects.</span></span>
5.  <span data-ttu-id="90995-153">Copiare i tre file elencati nel passaggio 2 nella cartella VCProjects.</span><span class="sxs-lookup"><span data-stu-id="90995-153">Copy the three files listed in step 2 to the vcprojects folder.</span></span> <span data-ttu-id="90995-154">Ora è installata la procedura guidata.</span><span class="sxs-lookup"><span data-stu-id="90995-154">The wizard is now installed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="90995-155">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="90995-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="90995-156">Creazione del plug-in per un negozio online di tipo 1</span><span class="sxs-lookup"><span data-stu-id="90995-156">Building the Plug-in for a Type 1 Online Store</span></span>](building-the-plug-in-for-a-type-1-online-store.md)
</dt> </dl>

 

 




