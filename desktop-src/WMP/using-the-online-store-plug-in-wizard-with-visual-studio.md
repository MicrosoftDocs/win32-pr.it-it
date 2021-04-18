---
title: Uso della procedura guidata plug-in di Store online con Visual Studio
description: Uso della procedura guidata plug-in di Store online con Visual Studio
ms.assetid: 0bf670cd-897d-4cd6-ae95-ae16b2dacc96
keywords:
- Windows Media Player Online Stores, plug-in
- archivi online, plug-in
- digitare 1 negozi online, plug-in
- Windows Media Player Online Stores, creazione guidata plug-in
- negozi online, creazione guidata plug-in
- digitare 1 archivi online, creazione guidata plug-in
- Windows Media Player Online Stores, Visual Studio
- negozi online, Visual Studio
- digitare 1 negozi online, Visual Studio
- plug-in, archivi Windows Media Player online
- plug-in, archivi online
- plug-in, digitare 1 negozi online
- plug-in, Visual Studio
- plug-in, creazione guidata plug-in
- Plug-in di Windows Media Player, digitare 1 negozi online
- Plug-in di Windows Media Player, archivi online
- Plug-in di Windows Media Player, archivi Windows Media Player online
- Plug-in di Windows Media Player, Visual Studio
- Plug-in di Windows Media Player, creazione guidata plug-in
- Visual Studio, procedura guidata per gli archivi online di Windows Media Player
- procedura guidata plug-in
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0c9aadbb9cef4b44cb421bf8a4737cc408c5220
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297793"
---
# <a name="using-the-online-store-plug-in-wizard-with-visual-studio"></a><span data-ttu-id="8d20a-124">Uso della procedura guidata plug-in di Store online con Visual Studio</span><span class="sxs-lookup"><span data-stu-id="8d20a-124">Using the Online Store Plug-in Wizard with Visual Studio</span></span>

<span data-ttu-id="8d20a-125">Dopo aver installato i componenti necessari, è possibile creare rapidamente un plug-in che funge da punto di partenza.</span><span class="sxs-lookup"><span data-stu-id="8d20a-125">After you have installed the necessary components, you can quickly create a plug-in that will serve as a starting point.</span></span> <span data-ttu-id="8d20a-126">La procedura seguente consentirà di:</span><span class="sxs-lookup"><span data-stu-id="8d20a-126">The following steps will guide you:</span></span>

1.  <span data-ttu-id="8d20a-127">Avviare Microsoft Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="8d20a-127">Start Microsoft Visual Studio.</span></span>
2.  <span data-ttu-id="8d20a-128">Scegliere **nuovo** dal menu **file** , quindi fare clic su **progetto**.</span><span class="sxs-lookup"><span data-stu-id="8d20a-128">From the **File** menu, point to **New** and then click **Project**.</span></span>
3.  <span data-ttu-id="8d20a-129">In **Tipi progetto** fare clic su **progetti Visual C++**.</span><span class="sxs-lookup"><span data-stu-id="8d20a-129">In **Project Types**, click **Visual C++ Projects**.</span></span>
4.  <span data-ttu-id="8d20a-130">In **modelli** fare clic su **creazione guidata di Windows Media Player Online Stores**.</span><span class="sxs-lookup"><span data-stu-id="8d20a-130">In **Templates**, click **Windows Media Player Online Stores Wizard**.</span></span>
5.  <span data-ttu-id="8d20a-131">Immettere un nome per il progetto.</span><span class="sxs-lookup"><span data-stu-id="8d20a-131">Enter a name for your project.</span></span>
6.  <span data-ttu-id="8d20a-132">Immettere un percorso per il progetto.</span><span class="sxs-lookup"><span data-stu-id="8d20a-132">Enter a location for your project.</span></span> <span data-ttu-id="8d20a-133">Si tratta della cartella in cui verranno copiati i file di progetto.</span><span class="sxs-lookup"><span data-stu-id="8d20a-133">This is the folder to which your project files will be copied.</span></span>
7.  <span data-ttu-id="8d20a-134">Fare clic su **OK** per avviare la procedura guidata.</span><span class="sxs-lookup"><span data-stu-id="8d20a-134">Click **OK** to start the wizard.</span></span>
8.  <span data-ttu-id="8d20a-135">Selezionare il **tipo 1 (integrazione completa)** e fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="8d20a-135">Select **Type 1 (Deep integration)**, and click **Next**.</span></span>
9.  <span data-ttu-id="8d20a-136">Immettere un nome descrittivo e un server di distribuzione del contenuto.</span><span class="sxs-lookup"><span data-stu-id="8d20a-136">Enter a friendly name and a content distributor.</span></span> <span data-ttu-id="8d20a-137">Fare clic su **Fine**.</span><span class="sxs-lookup"><span data-stu-id="8d20a-137">Click **Finish**.</span></span>
10. <span data-ttu-id="8d20a-138">Usare l'ambiente di sviluppo di Visual Studio per compilare il progetto.</span><span class="sxs-lookup"><span data-stu-id="8d20a-138">Use the Visual Studio development environment to build your project.</span></span>
    > [!Note]  
    > <span data-ttu-id="8d20a-139">In Windows Vista e versioni successive il progetto non viene compilato correttamente a meno che non si esegua Visual Studio con un token di accesso amministratore completo.</span><span class="sxs-lookup"><span data-stu-id="8d20a-139">In Windows Vista and later, the project will not build successfully unless you run Visual Studio with a full administrator access token.</span></span> <span data-ttu-id="8d20a-140">Fare clic con il pulsante destro del mouse sul nome o sull'icona di Visual Studio e scegliere **Esegui come amministratore**.</span><span class="sxs-lookup"><span data-stu-id="8d20a-140">Right-click the Visual Studio name or icon, and click **Run as administrator**.</span></span>

     

<span data-ttu-id="8d20a-141">Prima di provare a compilare il progetto, assicurarsi di configurare l'ambiente di sviluppo in modo che punti alle cartelle denominate include e lib in cui è stato installato il Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="8d20a-141">Before attempting to build the project, be sure to configure your development environment to point to the folders named Include and Lib where you installed the Windows SDK.</span></span> <span data-ttu-id="8d20a-142">Il compilatore e il linker dovranno accedere ad alcuni file in queste cartelle.</span><span class="sxs-lookup"><span data-stu-id="8d20a-142">Your compiler and linker will need access to some of the files in these folders.</span></span>

<span data-ttu-id="8d20a-143">Se è stata eseguita l'utilità di registrazione di Visual Studio fornita con la Windows SDK, è probabile che l'ambiente di sviluppo sia già stato configurato in modo da puntare al Windows SDK includere le cartelle e lib.</span><span class="sxs-lookup"><span data-stu-id="8d20a-143">If you ran the Visual Studio Registration utility that comes with the Windows SDK, your development environment has probably already been configured to point to the Windows SDK Include and Lib folders.</span></span> <span data-ttu-id="8d20a-144">In caso contrario, è necessario configurare manualmente l'ambiente di sviluppo.</span><span class="sxs-lookup"><span data-stu-id="8d20a-144">Otherwise, you must manually configure your development environment.</span></span>

<span data-ttu-id="8d20a-145">Per configurare manualmente Visual Studio, seguire questa procedura.</span><span class="sxs-lookup"><span data-stu-id="8d20a-145">To manually configure Visual Studio, use the following steps.</span></span>

1.  <span data-ttu-id="8d20a-146">Scegliere Opzioni dal menu **strumenti** .</span><span class="sxs-lookup"><span data-stu-id="8d20a-146">On the **Tools** menu, click Options.</span></span>
2.  <span data-ttu-id="8d20a-147">Fare clic su **progetti e soluzioni** e quindi su **directory di VC + +**.</span><span class="sxs-lookup"><span data-stu-id="8d20a-147">Click **Projects and Solutions**, and then click **VC++ Directories**.</span></span>
3.  <span data-ttu-id="8d20a-148">In **Mostra directory per** fare clic su **Includi file** o **file di libreria**.</span><span class="sxs-lookup"><span data-stu-id="8d20a-148">Under **Show directories for**, click **Include files** or **Library files**.</span></span>
4.  <span data-ttu-id="8d20a-149">Aggiungere le directory per i file necessari.</span><span class="sxs-lookup"><span data-stu-id="8d20a-149">Add the directories for the required files.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8d20a-150">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8d20a-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8d20a-151">Creazione del plug-in per un negozio online di tipo 1</span><span class="sxs-lookup"><span data-stu-id="8d20a-151">Building the Plug-in for a Type 1 Online Store</span></span>](building-the-plug-in-for-a-type-1-online-store.md)
</dt> </dl>

 

 




