---
title: Personalizzazione del progetto di esempio
description: Personalizzazione del progetto di esempio
ms.assetid: 26031971-3d1b-4175-8fb3-f13b6c17dd01
keywords:
- Windows Media Player Online Stores, personalizzazione di progetti di esempio
- negozi online, personalizzazione di progetti di esempio
- digitare 2 archivi online, personalizzazione di progetti di esempio
- Windows Media Player Online Stores, progetti di esempio
- negozi online, progetti di esempio
- digitare 2 archivi online, progetti di esempio
- personalizzazione di progetti di esempio
- esempi, digitare 2 archivi online
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0aeec3ebcb74304cd5181783e9c457d6a149b0cc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955757"
---
# <a name="customizing-the-sample-project"></a><span data-ttu-id="68757-111">Personalizzazione del progetto di esempio</span><span class="sxs-lookup"><span data-stu-id="68757-111">Customizing the Sample Project</span></span>

<span data-ttu-id="68757-112">Quando si crea un archivio online personalizzato, è necessario modificare le implementazioni dei metodi seguenti nel file denominato Progettoutente. cpp:</span><span class="sxs-lookup"><span data-stu-id="68757-112">When creating your own online store, you will want to change the implementations of the following methods in the file named YourProject.cpp:</span></span>

-   <span data-ttu-id="68757-113">**CYourProject:: allowPlay**.</span><span class="sxs-lookup"><span data-stu-id="68757-113">**CYourProject::allowPlay**.</span></span> <span data-ttu-id="68757-114">Usare questa funzione per applicare le regole business per consentire la riproduzione di contenuto protetto.</span><span class="sxs-lookup"><span data-stu-id="68757-114">Use this function to apply your business rules for permitting playback of protected content.</span></span>
-   <span data-ttu-id="68757-115">**CYourProject:: Allow cdburn**.</span><span class="sxs-lookup"><span data-stu-id="68757-115">**CYourProject::allow CDBurn**.</span></span> <span data-ttu-id="68757-116">Usare questa funzione per applicare le regole business per consentire agli utenti di copiare il contenuto protetto in un CD.</span><span class="sxs-lookup"><span data-stu-id="68757-116">Use this function to apply your business rules for allowing users to copy protected content to a CD.</span></span>
-   <span data-ttu-id="68757-117">**CYourProject:: allowPDATransfer**.</span><span class="sxs-lookup"><span data-stu-id="68757-117">**CYourProject::allowPDATransfer**.</span></span> <span data-ttu-id="68757-118">Usare questa funzione per applicare le regole business per consentire agli utenti di trasferire contenuti protetti a un dispositivo portatile.</span><span class="sxs-lookup"><span data-stu-id="68757-118">Use this function to apply your business rules for allowing users to transfer protected content to a portable device.</span></span>
-   <span data-ttu-id="68757-119">**CYourProject:: startBackgroundProcessing**.</span><span class="sxs-lookup"><span data-stu-id="68757-119">**CYourProject::startBackgroundProcessing**.</span></span> <span data-ttu-id="68757-120">Usare questa funzione per avviare le attività di elaborazione in background necessarie.</span><span class="sxs-lookup"><span data-stu-id="68757-120">Use this function to initiate any background processing tasks you require.</span></span> <span data-ttu-id="68757-121">È possibile, ad esempio, usarlo come opportunità per verificare la presenza di licenze scadute.</span><span class="sxs-lookup"><span data-stu-id="68757-121">For example, you might use this as an opportunity to check for expired licenses.</span></span>
-   <span data-ttu-id="68757-122">**CYourProject::D eviceavailable**.</span><span class="sxs-lookup"><span data-stu-id="68757-122">**CYourProject::deviceAvailable**.</span></span> <span data-ttu-id="68757-123">Usare questa funzione per avviare le attività correlate a un dispositivo connesso.</span><span class="sxs-lookup"><span data-stu-id="68757-123">Use this function to initiate any tasks related to a connected device.</span></span>
-   <span data-ttu-id="68757-124">**CYourProject::P repareforsync**.</span><span class="sxs-lookup"><span data-stu-id="68757-124">**CYourProject::prepareForSync**.</span></span> <span data-ttu-id="68757-125">Usare questa funzione per eseguire le attività necessarie poco prima di sincronizzare i supporti digitali con il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="68757-125">Use this function to perform necessary tasks just before synchronizing digital media to the device.</span></span>
-   <span data-ttu-id="68757-126">**CYourProject:: serviceEvent**.</span><span class="sxs-lookup"><span data-stu-id="68757-126">**CYourProject::serviceEvent**.</span></span> <span data-ttu-id="68757-127">Utilizzare questa funzione per iniziare e terminare le attività che si desidera eseguire quando lo Store online è quello attivo.</span><span class="sxs-lookup"><span data-stu-id="68757-127">Use this function to begin and end tasks that you want to run when your online store is the active one.</span></span>
-   <span data-ttu-id="68757-128">**CYourProject:: stopBackgroundProcessing**.</span><span class="sxs-lookup"><span data-stu-id="68757-128">**CYourProject::stopBackgroundProcessing**.</span></span> <span data-ttu-id="68757-129">Usare questa funzione per arrestare le attività di elaborazione in background avviate quando Windows Media Player denominato **CYourProject:: startBackgroundProcessing**.</span><span class="sxs-lookup"><span data-stu-id="68757-129">Use this function to stop any background processing tasks you started when Windows Media Player called **CYourProject::startBackgroundProcessing**.</span></span>

## <a name="working-with-media-and-playlist-objects"></a><span data-ttu-id="68757-130">Utilizzo di oggetti multimediali e playlist</span><span class="sxs-lookup"><span data-stu-id="68757-130">Working with Media and Playlist Objects</span></span>

<span data-ttu-id="68757-131">Il metodo **allowPlay** fornisce un puntatore all'interfaccia **IWMPMedia** come parametro.</span><span class="sxs-lookup"><span data-stu-id="68757-131">The **allowPlay** method provides a pointer to the **IWMPMedia** interface as a parameter.</span></span> <span data-ttu-id="68757-132">Questa interfaccia è l'interfaccia di Windows Media Player che rappresenta gli oggetti multimediali.</span><span class="sxs-lookup"><span data-stu-id="68757-132">This interface is the Windows Media Player interface that represents media objects.</span></span> <span data-ttu-id="68757-133">Chiamando i metodi su questa interfaccia, è possibile usare gli attributi e le proprietà di un singolo elemento multimediale.</span><span class="sxs-lookup"><span data-stu-id="68757-133">By calling the methods on this interface, you can work with the attributes and properties of an individual media item.</span></span>

<span data-ttu-id="68757-134">I metodi **allowCDBurn** e **allowPDATransfer** forniscono un puntatore all'interfaccia **IWMPPlaylist** come parametro.</span><span class="sxs-lookup"><span data-stu-id="68757-134">The **allowCDBurn** and **allowPDATransfer** methods provide a pointer to the **IWMPPlaylist** interface as a parameter.</span></span> <span data-ttu-id="68757-135">Questa interfaccia è l'interfaccia di Windows Media Player che rappresenta gli oggetti playlist.</span><span class="sxs-lookup"><span data-stu-id="68757-135">This interface is the Windows Media Player interface that represents playlist objects.</span></span> <span data-ttu-id="68757-136">Chiamando i metodi su questa interfaccia, è possibile usare gli attributi e le proprietà di una playlist, aggiungere elementi a una playlist o rimuovere elementi da una playlist.</span><span class="sxs-lookup"><span data-stu-id="68757-136">By calling the methods on this interface, you can work with the attributes and properties of a playlist, add items to a playlist, or remove items from a playlist.</span></span>

<span data-ttu-id="68757-137">Per informazioni su come rimuovere un elemento da una playlist a livello di codice, vedere l'implementazione di **CAllowBaseDialog <T> :: OnRemoveMediaFromPlaylist**.</span><span class="sxs-lookup"><span data-stu-id="68757-137">To learn how to remove an item from a playlist programmatically, see the implementation of **CAllowBaseDialog<T>::OnRemoveMediaFromPlaylist**.</span></span> <span data-ttu-id="68757-138">Per altre informazioni sull'uso di oggetti multimediali e playlist, vedere il [modello a oggetti del lettore per i linguaggi di scripting](player-object-model-for-scripting-languages.md).</span><span class="sxs-lookup"><span data-stu-id="68757-138">To learn more about working with media and playlist objects, see [Player Object Model for Scripting Languages](player-object-model-for-scripting-languages.md).</span></span>

## <a name="code-that-can-be-removed"></a><span data-ttu-id="68757-139">Codice che può essere rimosso</span><span class="sxs-lookup"><span data-stu-id="68757-139">Code That Can Be Removed</span></span>

<span data-ttu-id="68757-140">Probabilmente si vorrà rimuovere il codice che apre le finestre di dialogo perché è improbabile che gli utenti decidano quali elementi multimediali possono essere riprodotti o copiati.</span><span class="sxs-lookup"><span data-stu-id="68757-140">You will probably want to remove the code that opens dialog boxes because it is unlikely that you will want users deciding which media items can be played or copied.</span></span> <span data-ttu-id="68757-141">Da Progettoutente. h rimuovere il codice seguente:</span><span class="sxs-lookup"><span data-stu-id="68757-141">From YourProject.h, remove the following code:</span></span>

-   <span data-ttu-id="68757-142">Dichiarazione di **CAllowBaseDialog**.</span><span class="sxs-lookup"><span data-stu-id="68757-142">The declaration of **CAllowBaseDialog**.</span></span>
-   <span data-ttu-id="68757-143">Dichiarazione di **CAllowBurnDialog**.</span><span class="sxs-lookup"><span data-stu-id="68757-143">The declaration of **CAllowBurnDialog**.</span></span>
-   <span data-ttu-id="68757-144">Dichiarazione di **CAllowTransferDialog**.</span><span class="sxs-lookup"><span data-stu-id="68757-144">The declaration of **CAllowTransferDialog**.</span></span>

<span data-ttu-id="68757-145">Da Progettoutente. cpp rimuovere il codice seguente:</span><span class="sxs-lookup"><span data-stu-id="68757-145">From YourProject.cpp, remove the following code:</span></span>

-   <span data-ttu-id="68757-146">Implementazione di **CAllowBaseDialog <T> :: OnInitDialog**.</span><span class="sxs-lookup"><span data-stu-id="68757-146">The implementation of **CAllowBaseDialog<T>::OnInitDialog**.</span></span>
-   <span data-ttu-id="68757-147">Implementazione di **CAllowBaseDialog <T> :: OnRemoveMediaFromPlaylist**.</span><span class="sxs-lookup"><span data-stu-id="68757-147">The implementation of **CAllowBaseDialog<T>::OnRemoveMediaFromPlaylist**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="68757-148">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="68757-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="68757-149">**Creazione del plug-in per un negozio online di tipo 2**</span><span class="sxs-lookup"><span data-stu-id="68757-149">**Building the Plug-in for a Type 2 Online Store**</span></span>](building-the-plug-in-for-a-type-2-online-store.md)
</dt> </dl>

 

 




