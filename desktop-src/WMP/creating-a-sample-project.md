---
title: Creazione di un progetto di esempio
description: Creazione di un progetto di esempio
ms.assetid: 9cbbd1a7-88e7-4947-8dca-e06e364102f7
keywords:
- Windows Media Player Online Stores, creazione di progetti di esempio
- negozi online, creazione di progetti di esempio
- digitare 2 archivi online, creazione di progetti di esempio
- Windows Media Player Online Stores, progetti di esempio
- negozi online, progetti di esempio
- digitare 2 archivi online, progetti di esempio
- Windows Media Player Online Stores, creazione guidata progetto
- negozi online, creazione guidata progetto
- digitare 2 archivi online, creazione guidata progetto
- plug-in, creazione guidata progetto
- Plug-in di Windows Media Player, creazione guidata progetto
- creazione di progetti di esempio
- esempi, digitare 2 archivi online
- Creazione guidata progetto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4756cc7ae8d27c2a790a7ac96af638eea72d861
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/21/2020
ms.locfileid: "104117435"
---
# <a name="creating-a-sample-project"></a><span data-ttu-id="7b6c9-117">Creazione di un progetto di esempio</span><span class="sxs-lookup"><span data-stu-id="7b6c9-117">Creating a Sample Project</span></span>

<span data-ttu-id="7b6c9-118">Per creare un nuovo progetto utilizzando la creazione guidata progetto, attenersi alla seguente procedura:</span><span class="sxs-lookup"><span data-stu-id="7b6c9-118">To create a new project using the project wizard, follow these steps:</span></span>

1.  <span data-ttu-id="7b6c9-119">Aprire Microsoft Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="7b6c9-119">Open Microsoft Visual Studio.</span></span>
2.  <span data-ttu-id="7b6c9-120">Scegliere **Nuovo** dal menu **File**, quindi fare clic su **Progetto**.</span><span class="sxs-lookup"><span data-stu-id="7b6c9-120">From the **File** menu, point to **New**, and then click **Project**.</span></span>
3.  <span data-ttu-id="7b6c9-121">Nella casella di riepilogo **Tipi progetto** scegliere **Visual C++ progetti**.</span><span class="sxs-lookup"><span data-stu-id="7b6c9-121">In the **Project Types** list box, choose **Visual C++ Projects**.</span></span>
4.  <span data-ttu-id="7b6c9-122">Nella casella di riepilogo **modelli** scegliere **Windows Media Player procedura guidata degli archivi online**.</span><span class="sxs-lookup"><span data-stu-id="7b6c9-122">In the **Templates** list box, choose **Windows Media Player Online Stores Wizard**.</span></span>
5.  <span data-ttu-id="7b6c9-123">Digitare un nome e un percorso per il progetto.</span><span class="sxs-lookup"><span data-stu-id="7b6c9-123">Type a name and location for your project.</span></span>
6.  <span data-ttu-id="7b6c9-124">Fare clic su **OK** per avviare la creazione guidata progetto.</span><span class="sxs-lookup"><span data-stu-id="7b6c9-124">Click **OK** to start the project wizard.</span></span>
7.  <span data-ttu-id="7b6c9-125">Selezionare il **tipo 2 (integrazione di base)** e fare clic su **Avanti**.</span><span class="sxs-lookup"><span data-stu-id="7b6c9-125">Select **Type 2 (Basic integration)**, and click **Next**.</span></span>
8.  <span data-ttu-id="7b6c9-126">Digitare il nome descrittivo e l'ID del server di distribuzione del contenuto per il servizio.</span><span class="sxs-lookup"><span data-stu-id="7b6c9-126">Type the friendly name and content distributor ID for your service.</span></span> <span data-ttu-id="7b6c9-127">Digitare l'URL della pagina Web che rimuove il servizio dal computer dell'utente.</span><span class="sxs-lookup"><span data-stu-id="7b6c9-127">Type the URL for the webpage that removes the service from the user's computer.</span></span>
    > [!Note]  
    > <span data-ttu-id="7b6c9-128">Il valore fornito per l'ID del server di distribuzione del contenuto non deve contenere spazi.</span><span class="sxs-lookup"><span data-stu-id="7b6c9-128">The value you provide for the content distributor ID must not contain spaces.</span></span> <span data-ttu-id="7b6c9-129">La procedura guidata consente di rimuovere gli spazi dalla stringa fornita.</span><span class="sxs-lookup"><span data-stu-id="7b6c9-129">The wizard removes any spaces from the string you provide.</span></span>

     

9.  <span data-ttu-id="7b6c9-130">Fare clic su **Finish** (Fine) per creare il progetto.</span><span class="sxs-lookup"><span data-stu-id="7b6c9-130">Click **Finish** to create the project.</span></span>

<span data-ttu-id="7b6c9-131">La procedura guidata genera automaticamente un nuovo progetto C++ per la creazione di un plug-in di archiviazione di tipo 2 in cui vengono implementate le interfacce **IWMPSubscriptionService** e **IWMPSubscriptionService2** .</span><span class="sxs-lookup"><span data-stu-id="7b6c9-131">The wizard automatically generates a new C++ project that creates a type 2 online store plug-in that implements the **IWMPSubscriptionService** and **IWMPSubscriptionService2** interfaces.</span></span> <span data-ttu-id="7b6c9-132">Ogni volta che si esegue la procedura guidata, viene creato lo stesso progetto, ma il componente creato quando si compila il progetto ha un ID classe univoco.</span><span class="sxs-lookup"><span data-stu-id="7b6c9-132">Each time you run the wizard it creates the same project, but the component that is created when you compile the project has a unique class ID.</span></span> <span data-ttu-id="7b6c9-133">Il nome del progetto, il nome descrittivo e l'ID del server di distribuzione del contenuto possono anche variare a seconda dei valori specificati al momento dell'esecuzione della procedura guidata.</span><span class="sxs-lookup"><span data-stu-id="7b6c9-133">The project name, the friendly name, and content distributor ID may also be different depending on the values you provided when you ran the wizard.</span></span> <span data-ttu-id="7b6c9-134">Il progetto di esempio registra il componente usando un nome di chiave che corrisponde al valore specificato per il nome descrittivo.</span><span class="sxs-lookup"><span data-stu-id="7b6c9-134">The sample project registers the component by using a key name that matches the value you supplied for the friendly name.</span></span>

<span data-ttu-id="7b6c9-135">Nell'esempio viene utilizzato il codice Active Template Library (ATL) per fornire implementazioni COM.</span><span class="sxs-lookup"><span data-stu-id="7b6c9-135">The sample uses Active Template Library (ATL) code to provide COM implementations.</span></span>

<span data-ttu-id="7b6c9-136">La procedura guidata crea automaticamente i seguenti file:</span><span class="sxs-lookup"><span data-stu-id="7b6c9-136">The wizard creates the following files for you:</span></span>

-   <span data-ttu-id="7b6c9-137">*NomeProgetto* dll. cpp.</span><span class="sxs-lookup"><span data-stu-id="7b6c9-137">*ProjectName* dll.cpp.</span></span> <span data-ttu-id="7b6c9-138">Implementa le esportazioni DLL (Dynamic Link Library), ad esempio la funzione principale del punto di ingresso della DLL.</span><span class="sxs-lookup"><span data-stu-id="7b6c9-138">Implements the Dynamic Link Library (DLL) exports such as the main DLL entry point function.</span></span> <span data-ttu-id="7b6c9-139">Contiene anche la dichiarazione del modulo e della mappa dell'oggetto ATL.</span><span class="sxs-lookup"><span data-stu-id="7b6c9-139">Also contains the ATL object map and module declaration.</span></span>
-   <span data-ttu-id="7b6c9-140">*NomeProgetto*. cpp.</span><span class="sxs-lookup"><span data-stu-id="7b6c9-140">*ProjectName*.cpp.</span></span> <span data-ttu-id="7b6c9-141">Contiene le implementazioni predefinite per i metodi delle interfacce IWMPSubscriptionService e IWMPSubscriptionService2.</span><span class="sxs-lookup"><span data-stu-id="7b6c9-141">Contains default implementations for the methods of the IWMPSubscriptionService and IWMPSubscriptionService2 interfaces.</span></span> <span data-ttu-id="7b6c9-142">Contiene inoltre il codice per definire le finestre di dialogo che vengono aperte dall'esempio quando i metodi vengono chiamati da Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="7b6c9-142">Also contains code to define the dialog boxes that the sample opens when methods are called by Windows Media Player.</span></span>
-   <span data-ttu-id="7b6c9-143">*NomeProgetto*. def. Dichiara le esportazioni DLL.</span><span class="sxs-lookup"><span data-stu-id="7b6c9-143">*ProjectName*.def. Declares the DLL exports.</span></span>
-   <span data-ttu-id="7b6c9-144">StdAfx. cpp.</span><span class="sxs-lookup"><span data-stu-id="7b6c9-144">StdAfx.cpp.</span></span> <span data-ttu-id="7b6c9-145">Include intestazioni standard.</span><span class="sxs-lookup"><span data-stu-id="7b6c9-145">Includes standard headers.</span></span>
-   <span data-ttu-id="7b6c9-146">WMP. h.</span><span class="sxs-lookup"><span data-stu-id="7b6c9-146">wmp.h.</span></span> <span data-ttu-id="7b6c9-147">Il file di intestazione Media Player di Windows.</span><span class="sxs-lookup"><span data-stu-id="7b6c9-147">The Windows Media Player header file.</span></span>
-   <span data-ttu-id="7b6c9-148">wmpplug. h.</span><span class="sxs-lookup"><span data-stu-id="7b6c9-148">wmpplug.h.</span></span> <span data-ttu-id="7b6c9-149">Il file di intestazione del plug-in di Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="7b6c9-149">The Windows Media Player plug-in header file.</span></span>
-   <span data-ttu-id="7b6c9-150">SubscriptionServices. h.</span><span class="sxs-lookup"><span data-stu-id="7b6c9-150">subscriptionservices.h.</span></span> <span data-ttu-id="7b6c9-151">Il file di intestazione di Windows Media Player Online Stores.</span><span class="sxs-lookup"><span data-stu-id="7b6c9-151">The Windows Media Player online stores header file.</span></span>
-   <span data-ttu-id="7b6c9-152">Resource. h.</span><span class="sxs-lookup"><span data-stu-id="7b6c9-152">resource.h.</span></span> <span data-ttu-id="7b6c9-153">Contiene le definizioni di risorse.</span><span class="sxs-lookup"><span data-stu-id="7b6c9-153">Contains resource definitions.</span></span>
-   <span data-ttu-id="7b6c9-154">**NomeProgetto**. h.</span><span class="sxs-lookup"><span data-stu-id="7b6c9-154">**ProjectName**.h.</span></span> <span data-ttu-id="7b6c9-155">Contiene le definizioni di classe per l'oggetto di archivio online e le finestre di dialogo.</span><span class="sxs-lookup"><span data-stu-id="7b6c9-155">Contains class definitions for the online store object and the dialog boxes.</span></span> <span data-ttu-id="7b6c9-156">Definisce l'ID classe dell'oggetto e la costante ID del server di distribuzione del contenuto.</span><span class="sxs-lookup"><span data-stu-id="7b6c9-156">Defines the object's class ID and the content distributor ID constant.</span></span>
-   <span data-ttu-id="7b6c9-157">StdAfx. h.</span><span class="sxs-lookup"><span data-stu-id="7b6c9-157">StdAfx.h.</span></span> <span data-ttu-id="7b6c9-158">Contiene le inclusioni di sistema standard.</span><span class="sxs-lookup"><span data-stu-id="7b6c9-158">Contains standard system includes.</span></span>
-   <span data-ttu-id="7b6c9-159">*NomeProgetto*. RC.</span><span class="sxs-lookup"><span data-stu-id="7b6c9-159">*ProjectName*.rc.</span></span> <span data-ttu-id="7b6c9-160">File di script di risorsa.</span><span class="sxs-lookup"><span data-stu-id="7b6c9-160">The resource script file.</span></span> <span data-ttu-id="7b6c9-161">Contiene le definizioni per le risorse e i controlli della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="7b6c9-161">This contains definitions for the dialog box resources and controls.</span></span> <span data-ttu-id="7b6c9-162">Questa è anche la posizione in cui viene archiviata la tabella delle stringhe.</span><span class="sxs-lookup"><span data-stu-id="7b6c9-162">This is also where the string table is stored.</span></span> <span data-ttu-id="7b6c9-163">La tabella delle stringhe contiene il nome del progetto e le costanti di stringa del nome descrittivo.</span><span class="sxs-lookup"><span data-stu-id="7b6c9-163">The string table contains your project name and friendly name string constants.</span></span> <span data-ttu-id="7b6c9-164">In genere si utilizza questo file nell'editor risorse di Visual Studio, non come testo normale.</span><span class="sxs-lookup"><span data-stu-id="7b6c9-164">Usually you work with this file in the Visual Studio resource editor, not as plain text.</span></span>
-   <span data-ttu-id="7b6c9-165">*NomeProgetto*. RGS.</span><span class="sxs-lookup"><span data-stu-id="7b6c9-165">*ProjectName*.rgs.</span></span> <span data-ttu-id="7b6c9-166">File di script del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="7b6c9-166">The registry script file.</span></span> <span data-ttu-id="7b6c9-167">Questo file contiene le informazioni utilizzate per aggiungere la classe Component al registro di sistema in modo che Windows Media Player possa individuarlo.</span><span class="sxs-lookup"><span data-stu-id="7b6c9-167">This file contains the information used to add your component class to the registry so Windows Media Player can locate it.</span></span> <span data-ttu-id="7b6c9-168">È possibile modificare il nome della chiave per il servizio in questo file.</span><span class="sxs-lookup"><span data-stu-id="7b6c9-168">You can change the key name for your service in this file.</span></span>

> [!Note]  
> <span data-ttu-id="7b6c9-169">È necessario impostare l'indirizzo di base per la DLL su 0x0F100000 per evitare conflitti con Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="7b6c9-169">You should set the base address for your DLL to 0x0F100000 to avoid conflicts with Windows Media Player.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="7b6c9-170">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7b6c9-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7b6c9-171">**Creazione del plug-in per un negozio online di tipo 2**</span><span class="sxs-lookup"><span data-stu-id="7b6c9-171">**Building the Plug-in for a Type 2 Online Store**</span></span>](building-the-plug-in-for-a-type-2-online-store.md)
</dt> <dt>

[<span data-ttu-id="7b6c9-172">**Interfaccia IWMPSubscriptionService**</span><span class="sxs-lookup"><span data-stu-id="7b6c9-172">**IWMPSubscriptionService Interface**</span></span>](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice)
</dt> <dt>

[<span data-ttu-id="7b6c9-173">**Interfaccia IWMPSubscriptionService2**</span><span class="sxs-lookup"><span data-stu-id="7b6c9-173">**IWMPSubscriptionService2 Interface**</span></span>](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice2)
</dt> </dl>

 

 




