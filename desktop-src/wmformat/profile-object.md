---
title: Oggetto profilo
description: Oggetto profilo
ms.assetid: ec42889e-580e-4a65-9fe6-4a5f15c97eb0
keywords:
- Windows Media Format SDK, oggetti profilo
- ASF (Advanced Systems Format), oggetti profilo
- ASF (formato avanzato dei sistemi), oggetti profilo
- oggetti, profili
- profili, oggetti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d6763d098819bde7d5db404aeffef3cd333d9b1
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2020
ms.locfileid: "103858081"
---
# <a name="profile-object"></a><span data-ttu-id="9ad92-108">Oggetto profilo</span><span class="sxs-lookup"><span data-stu-id="9ad92-108">Profile Object</span></span>

<span data-ttu-id="9ad92-109">Un oggetto profilo gestisce le impostazioni di un profilo.</span><span class="sxs-lookup"><span data-stu-id="9ad92-109">A profile object manages the settings of a profile.</span></span> <span data-ttu-id="9ad92-110">Gli oggetti profilo possono essere creati per i dati di profilo esistenti oppure possono essere creati vuoti, pronti per la ricezione di nuovi dati.</span><span class="sxs-lookup"><span data-stu-id="9ad92-110">Profile objects can be created for existing profile data or can be created empty, ready to receive new data.</span></span> <span data-ttu-id="9ad92-111">Un oggetto profilo viene inoltre creato dall'oggetto Reader (e dall'oggetto Reader sincrono) quando un file viene caricato per la lettura.</span><span class="sxs-lookup"><span data-stu-id="9ad92-111">A profile object is also created by the reader object (and the synchronous reader object) when a file is loaded for reading.</span></span> <span data-ttu-id="9ad92-112">In questo caso l'oggetto viene popolato con le informazioni sul profilo archiviate nell'intestazione del file.</span><span class="sxs-lookup"><span data-stu-id="9ad92-112">In this case the object is populated with the profile information stored in the header of the file.</span></span>

<span data-ttu-id="9ad92-113">Per salvare il contenuto di un oggetto profilo, è necessario chiamare [**IWMProfileManager:: SaveProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-saveprofile).</span><span class="sxs-lookup"><span data-stu-id="9ad92-113">To save the contents of a profile object, you must call [**IWMProfileManager::SaveProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-saveprofile).</span></span>

<span data-ttu-id="9ad92-114">Un profilo contiene più oggetti che controllano vari aspetti del profilo, ad esempio i flussi.</span><span class="sxs-lookup"><span data-stu-id="9ad92-114">A profile contains multiple objects that control various aspects of the profile (such as streams).</span></span> <span data-ttu-id="9ad92-115">Tutti questi oggetti sono subordinati all'oggetto profilo.</span><span class="sxs-lookup"><span data-stu-id="9ad92-115">All of these objects are subordinate to the profile object.</span></span> <span data-ttu-id="9ad92-116">Questi oggetti non vengono creati con le funzioni di creazione come si farebbe con gli oggetti principali di questo SDK.</span><span class="sxs-lookup"><span data-stu-id="9ad92-116">You do not create these objects with creation functions as you would with the major objects of this SDK.</span></span> <span data-ttu-id="9ad92-117">Al contrario, le interfacce dell'oggetto profilo contengono metodi che creano gli oggetti subordinati.</span><span class="sxs-lookup"><span data-stu-id="9ad92-117">Instead, the interfaces of the profile object contain methods that create the subordinate objects.</span></span>

<span data-ttu-id="9ad92-118">Per creare un oggetto profilo, chiamare uno dei metodi seguenti.</span><span class="sxs-lookup"><span data-stu-id="9ad92-118">To create a profile object, call one of the following methods.</span></span>



| <span data-ttu-id="9ad92-119">Metodo</span><span class="sxs-lookup"><span data-stu-id="9ad92-119">Method</span></span>                                                                                | <span data-ttu-id="9ad92-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9ad92-120">Description</span></span>                                                                                                                                                     |
|---------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9ad92-121">**IWMProfileManager::CreateEmptyProfile**</span><span class="sxs-lookup"><span data-stu-id="9ad92-121">**IWMProfileManager::CreateEmptyProfile**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-createemptyprofile) | <span data-ttu-id="9ad92-122">Crea un oggetto profilo senza dati del profilo.</span><span class="sxs-lookup"><span data-stu-id="9ad92-122">Creates a profile object without any profile data.</span></span>                                                                                                              |
| [<span data-ttu-id="9ad92-123">**IWMProfileManager::LoadProfileByData**</span><span class="sxs-lookup"><span data-stu-id="9ad92-123">**IWMProfileManager::LoadProfileByData**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadprofilebydata)   | <span data-ttu-id="9ad92-124">Crea un oggetto profilo popolato con i dati di un profilo salvato sotto forma di stringa.</span><span class="sxs-lookup"><span data-stu-id="9ad92-124">Creates a profile object populated with data from a profile saved as a string.</span></span> <span data-ttu-id="9ad92-125">Questo è l'unico modo per creare un oggetto profilo con i dati di un profilo personalizzato.</span><span class="sxs-lookup"><span data-stu-id="9ad92-125">This is the only way to create a profile object with data from a custom profile.</span></span> |
| [<span data-ttu-id="9ad92-126">**IWMProfileManager::LoadProfileByID**</span><span class="sxs-lookup"><span data-stu-id="9ad92-126">**IWMProfileManager::LoadProfileByID**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadprofilebyid)       | <span data-ttu-id="9ad92-127">Crea un oggetto profilo popolato con i dati di un profilo di sistema.</span><span class="sxs-lookup"><span data-stu-id="9ad92-127">Creates a profile object populated with data from a system profile.</span></span> <span data-ttu-id="9ad92-128">Usa il GUID per identificare il profilo di sistema desiderato.</span><span class="sxs-lookup"><span data-stu-id="9ad92-128">Uses the GUID to identify the desired system profile.</span></span>                                       |
| [<span data-ttu-id="9ad92-129">**IWMProfileManager::LoadSystemProfile**</span><span class="sxs-lookup"><span data-stu-id="9ad92-129">**IWMProfileManager::LoadSystemProfile**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadsystemprofile)   | <span data-ttu-id="9ad92-130">Crea un oggetto profilo popolato con i dati di un profilo di sistema.</span><span class="sxs-lookup"><span data-stu-id="9ad92-130">Creates a profile object populated with data from a system profile.</span></span> <span data-ttu-id="9ad92-131">Usa l'indice del profilo per identificare il profilo di sistema desiderato.</span><span class="sxs-lookup"><span data-stu-id="9ad92-131">Uses the profile index to identify the desired system profile.</span></span>                              |



 

<span data-ttu-id="9ad92-132">Tutti i metodi della tabella precedente impostano un puntatore a un'interfaccia **IWMProfile** .</span><span class="sxs-lookup"><span data-stu-id="9ad92-132">All of the methods in the preceding table set a pointer to an **IWMProfile** interface.</span></span> <span data-ttu-id="9ad92-133">Le altre interfacce dell'oggetto profilo possono essere ottenute chiamando il metodo **QueryInterface** .</span><span class="sxs-lookup"><span data-stu-id="9ad92-133">The other interfaces of the profile object can be obtained by calling the **QueryInterface** method.</span></span>

<span data-ttu-id="9ad92-134">Le interfacce seguenti sono supportate da ogni oggetto profilo.</span><span class="sxs-lookup"><span data-stu-id="9ad92-134">The following interfaces are supported by every profile object.</span></span>



| <span data-ttu-id="9ad92-135">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="9ad92-135">Interface</span></span>                                  | <span data-ttu-id="9ad92-136">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9ad92-136">Description</span></span>                                                                                                                                       |
|--------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9ad92-137">**IWMLanguageList**</span><span class="sxs-lookup"><span data-stu-id="9ad92-137">**IWMLanguageList**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlanguagelist) | <span data-ttu-id="9ad92-138">Gestisce un elenco di lingue supportate da un file ASF.</span><span class="sxs-lookup"><span data-stu-id="9ad92-138">Manages a list of languages supported by an ASF file.</span></span>                                                                                             |
| [<span data-ttu-id="9ad92-139">**IWMPacketSize**</span><span class="sxs-lookup"><span data-stu-id="9ad92-139">**IWMPacketSize**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize)     | <span data-ttu-id="9ad92-140">Controlla la dimensione massima dei pacchetti in un file.</span><span class="sxs-lookup"><span data-stu-id="9ad92-140">Controls the maximum size of packets in a file.</span></span>                                                                                                   |
| [<span data-ttu-id="9ad92-141">**IWMPacketSize2**</span><span class="sxs-lookup"><span data-stu-id="9ad92-141">**IWMPacketSize2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize2)   | <span data-ttu-id="9ad92-142">Controlla la dimensione minima dei pacchetti in un file.</span><span class="sxs-lookup"><span data-stu-id="9ad92-142">Controls the minimum size of packets in a file.</span></span> <span data-ttu-id="9ad92-143">Eredita tutti i metodi di **IWMPacketSize**.</span><span class="sxs-lookup"><span data-stu-id="9ad92-143">Inherits all of the methods of **IWMPacketSize**.</span></span>                                                 |
| [<span data-ttu-id="9ad92-144">**IWMProfile**</span><span class="sxs-lookup"><span data-stu-id="9ad92-144">**IWMProfile**</span></span>](iwmprofile.md)           | <span data-ttu-id="9ad92-145">Controlla le impostazioni di base e gli oggetti inclusi in un profilo.</span><span class="sxs-lookup"><span data-stu-id="9ad92-145">Controls the basic settings and objects included in a profile.</span></span>                                                                                    |
| [<span data-ttu-id="9ad92-146">**IWMProfile2**</span><span class="sxs-lookup"><span data-stu-id="9ad92-146">**IWMProfile2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile2)         | <span data-ttu-id="9ad92-147">Recupera l'identificatore univoco globale (GUID) associato al profilo.</span><span class="sxs-lookup"><span data-stu-id="9ad92-147">Retrieves the globally unique identifier (GUID) associated with the profile.</span></span> <span data-ttu-id="9ad92-148">Eredita tutti i metodi di **IWMProfile**.</span><span class="sxs-lookup"><span data-stu-id="9ad92-148">Inherits all of the methods of **IWMProfile**.</span></span>                       |
| [<span data-ttu-id="9ad92-149">**IWMProfile3**</span><span class="sxs-lookup"><span data-stu-id="9ad92-149">**IWMProfile3**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3)         | <span data-ttu-id="9ad92-150">Controlla la condivisione della larghezza di banda e le informazioni relative alla priorità del flusso in un profilo.</span><span class="sxs-lookup"><span data-stu-id="9ad92-150">Controls bandwidth sharing and stream prioritization information in a profile.</span></span> <span data-ttu-id="9ad92-151">Eredita tutti i metodi di **IWMProfile** e **IWMProfile2**.</span><span class="sxs-lookup"><span data-stu-id="9ad92-151">Inherits all of the methods of **IWMProfile** and **IWMProfile2**.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="9ad92-152">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9ad92-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9ad92-153">**Oggetti**</span><span class="sxs-lookup"><span data-stu-id="9ad92-153">**Objects**</span></span>](objects.md)
</dt> <dt>

[<span data-ttu-id="9ad92-154">**Oggetto Gestione profili**</span><span class="sxs-lookup"><span data-stu-id="9ad92-154">**Profile Manager Object**</span></span>](profile-manager-object.md)
</dt> <dt>

[<span data-ttu-id="9ad92-155">**Profili**</span><span class="sxs-lookup"><span data-stu-id="9ad92-155">**Profiles**</span></span>](profiles.md)
</dt> </dl>

 

 




