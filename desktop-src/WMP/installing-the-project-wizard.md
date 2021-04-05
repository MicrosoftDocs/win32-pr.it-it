---
title: Installazione guidata progetto
description: Installazione guidata progetto
ms.assetid: bb27e5f0-d49e-46e5-a15f-be1a0a752c1c
keywords:
- Windows Media Player Online Stores, plug-in
- archivi online, plug-in
- digitare 2 archivi online, plug-in
- Windows Media Player Online Stores, creazione guidata plug-in
- negozi online, creazione guidata plug-in
- digitare 2 archivi online, creazione guidata plug-in
- Windows Media Player Online Stores, creazione guidata progetto
- negozi online, creazione guidata progetto
- digitare 2 archivi online, creazione guidata progetto
- Windows Media Player Online Stores, installazione guidata plug-in
- negozi online, installazione guidata plug-in
- digitare 2 archivi online, installazione guidata plug-in
- Windows Media Player Online Stores, installazione guidata progetto
- negozi online, installazione guidata progetto
- digitare 2 archivi online, installazione guidata progetto
- plug-in, archivi Windows Media Player online
- plug-in, archivi online
- plug-in, digitare 2 archivi online
- plug-in, installazione guidata plug-in
- plug-in, creazione guidata plug-in
- plug-in, installazione guidata progetto
- plug-in, creazione guidata progetto
- Plug-in di Windows Media Player, digitare 2 archivi online
- Plug-in di Windows Media Player, archivi online
- Plug-in di Windows Media Player, archivi Windows Media Player online
- Plug-in di Windows Media Player, installazione guidata plug-in
- Plug-in di Windows Media Player, creazione guidata plug-in
- Plug-in di Windows Media Player, installazione guidata progetto
- Plug-in di Windows Media Player, creazione guidata progetto
- installazione guidata plug-in
- procedura guidata plug-in
- installazione guidata progetto
- Creazione guidata progetto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc37754a028d73114b1b425dcbc80e268559355d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711989"
---
# <a name="installing-the-project-wizard"></a><span data-ttu-id="cca36-136">Installazione guidata progetto</span><span class="sxs-lookup"><span data-stu-id="cca36-136">Installing the Project Wizard</span></span>

<span data-ttu-id="cca36-137">Per configurare l'ambiente di sviluppo per la creazione di plug-in di archivio online di tipo 2, è necessario installare gli elementi seguenti:</span><span class="sxs-lookup"><span data-stu-id="cca36-137">To set up your development environment for creating type 2 online store plug-ins, you must install the following items:</span></span>

-   <span data-ttu-id="cca36-138">Microsoft Visual Studio .NET 2003 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="cca36-138">Microsoft Visual Studio .NET 2003 or later</span></span>
-   <span data-ttu-id="cca36-139">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="cca36-139">Windows Media Player 9 Series or later</span></span>
-   <span data-ttu-id="cca36-140">Windows SDK, che include Windows Media Player SDK</span><span class="sxs-lookup"><span data-stu-id="cca36-140">Windows SDK, which includes the Windows Media Player SDK</span></span>
-   <span data-ttu-id="cca36-141">Procedura guidata plug-in di archivio online</span><span class="sxs-lookup"><span data-stu-id="cca36-141">Online store plug-in wizard</span></span>

## <a name="installing-the-wizard"></a><span data-ttu-id="cca36-142">Installazione della procedura guidata</span><span class="sxs-lookup"><span data-stu-id="cca36-142">Installing the Wizard</span></span>

<span data-ttu-id="cca36-143">Usare la procedura seguente per installare la procedura guidata plug-in di negozio online in Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="cca36-143">Use the following steps to install the online store plug-in wizard in Visual Studio.</span></span>

1.  <span data-ttu-id="cca36-144">Individuare la cartella in cui è stato installato il Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="cca36-144">Locate the folder where you installed the Windows SDK.</span></span> <span data-ttu-id="cca36-145">Espandere la cartella per visualizzare le relative sottocartelle e passare a esempi \\ Multimedia \\ WMP \\ Wizards \\ Services.</span><span class="sxs-lookup"><span data-stu-id="cca36-145">Expand the folder to view its subfolders, and navigate to Samples\\Multimedia\\WMP\\wizards\\services.</span></span>
2.  <span data-ttu-id="cca36-146">Individuare i tre file seguenti:</span><span class="sxs-lookup"><span data-stu-id="cca36-146">Locate the following three files:</span></span>
    -   <span data-ttu-id="cca36-147">wmpservices. vsz</span><span class="sxs-lookup"><span data-stu-id="cca36-147">wmpservices.vsz</span></span>
    -   <span data-ttu-id="cca36-148">wmpservices. vsdir</span><span class="sxs-lookup"><span data-stu-id="cca36-148">wmpservices.vsdir</span></span>
    -   <span data-ttu-id="cca36-149">wmpservices. ico</span><span class="sxs-lookup"><span data-stu-id="cca36-149">wmpservices.ico</span></span>
3.  <span data-ttu-id="cca36-150">Utilizzando un editor di testo, ad esempio Blocco note, modificare il file wmpservices. vsz.</span><span class="sxs-lookup"><span data-stu-id="cca36-150">Using a text editor such as Notepad, edit the wmpservices.vsz file.</span></span>

    <span data-ttu-id="cca36-151">Individuare la riga seguente:</span><span class="sxs-lookup"><span data-stu-id="cca36-151">Locate the following line:</span></span>

    ```
    Wizard=VsWizard.<VsWizardEngine version goes here>
    ```

    

    <span data-ttu-id="cca36-152">Passare `<VsWizardEngine version goes here>` a uno dei valori seguenti, a seconda della versione di Visual Studio installata.</span><span class="sxs-lookup"><span data-stu-id="cca36-152">Change `<VsWizardEngine version goes here>` to one of the following values, depending on which version of Visual Studio you have installed.</span></span>

    

    | <span data-ttu-id="cca36-153">Valore</span><span class="sxs-lookup"><span data-stu-id="cca36-153">Value</span></span>              | <span data-ttu-id="cca36-154">Versione di Visual Studio</span><span class="sxs-lookup"><span data-stu-id="cca36-154">Visual Studio version</span></span>   |
    |--------------------|-------------------------|
    | <span data-ttu-id="cca36-155">VsWizardEngine. 7.1</span><span class="sxs-lookup"><span data-stu-id="cca36-155">VsWizardEngine.7.1</span></span> | <span data-ttu-id="cca36-156">Visual Studio .NET 2003</span><span class="sxs-lookup"><span data-stu-id="cca36-156">Visual Studio .NET 2003</span></span> |
    | <span data-ttu-id="cca36-157">VsWizardEngine. 8.0</span><span class="sxs-lookup"><span data-stu-id="cca36-157">VsWizardEngine.8.0</span></span> | <span data-ttu-id="cca36-158">Visual Studio 2005</span><span class="sxs-lookup"><span data-stu-id="cca36-158">Visual Studio 2005</span></span>      |
    | <span data-ttu-id="cca36-159">VsWizardEngine. 9.0</span><span class="sxs-lookup"><span data-stu-id="cca36-159">VsWizardEngine.9.0</span></span> | <span data-ttu-id="cca36-160">Visual Studio 2008</span><span class="sxs-lookup"><span data-stu-id="cca36-160">Visual Studio 2008</span></span>      |

    

     

    <span data-ttu-id="cca36-161">Individuare la riga seguente:</span><span class="sxs-lookup"><span data-stu-id="cca36-161">Locate the following line:</span></span>

    ```
    Param="ABSOLUTE_PATH = <path to wmpservices directory goes here>"
    ```

    

    <span data-ttu-id="cca36-162">Passare `<path to wmpservices directory goes here>` al percorso in cui si trovano i file della procedura guidata.</span><span class="sxs-lookup"><span data-stu-id="cca36-162">Change `<path to wmpservices directory goes here>` to the path where the wizard files are located.</span></span>

    <span data-ttu-id="cca36-163">Si supponga, ad esempio, di avere Visual Studio 2008 e che i file della procedura guidata siano qui: C: \\ programmi \\ Microsoft SDK \\ Windows \\ v 7.0 \\ esempi di \\ Multimedia \\ WMP \\ Wizards \\ Services.</span><span class="sxs-lookup"><span data-stu-id="cca36-163">For example, suppose you have Visual Studio 2008, and your wizard files are here: C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\WMP\\wizards\\services.</span></span> <span data-ttu-id="cca36-164">Il file wmpservices. vsz avrà un aspetto simile al seguente:</span><span class="sxs-lookup"><span data-stu-id="cca36-164">Then your wmpservices.vsz file would look like this:</span></span>

    ```
    VSWIZARD 7.0
    Wizard=VsWizard.VsWizardEngine.9.0

    Param="WIZARD_NAME = wmpservices"
    Param="ABSOLUTE_PATH = C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\Multimedia\WMP\wizards\services"
    Param="FALLBACK_LCID = 1033"
    ```

    

4.  <span data-ttu-id="cca36-165">Individuare la cartella in cui è installato Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="cca36-165">Locate the folder where you installed Visual Studio.</span></span> <span data-ttu-id="cca36-166">Espandere la cartella per visualizzare le relative sottocartelle e individuare una cartella denominata vcprojects.</span><span class="sxs-lookup"><span data-stu-id="cca36-166">Expand the folder to view its subfolders, and locate a folder named vcprojects.</span></span>
5.  <span data-ttu-id="cca36-167">Copiare i tre file elencati nel passaggio 2 nella cartella VCProjects.</span><span class="sxs-lookup"><span data-stu-id="cca36-167">Copy the three files listed in step 2 to the vcprojects folder.</span></span> <span data-ttu-id="cca36-168">Ora è installata la procedura guidata.</span><span class="sxs-lookup"><span data-stu-id="cca36-168">The wizard is now installed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cca36-169">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="cca36-169">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cca36-170">**Creazione del plug-in per un negozio online di tipo 2**</span><span class="sxs-lookup"><span data-stu-id="cca36-170">**Building the Plug-in for a Type 2 Online Store**</span></span>](building-the-plug-in-for-a-type-2-online-store.md)
</dt> </dl>

 

 




