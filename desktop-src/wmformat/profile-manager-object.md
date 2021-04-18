---
title: Oggetto Gestione profili
description: Oggetto Gestione profili
ms.assetid: 8d174243-334e-418e-a1c8-77486b940de7
keywords:
- Windows Media Format SDK, oggetti Profile Manager
- ASF (Advanced Systems Format), oggetti Profile Manager
- ASF (Advanced Systems Format), oggetti Profile Manager
- oggetti, oggetti di gestione profili
- profili, oggetti
- profili, oggetti Profile Manager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ce3d77598f52e43a840c1b6b3ef58baa47f77bd
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2020
ms.locfileid: "106299517"
---
# <a name="profile-manager-object"></a><span data-ttu-id="259d3-109">Oggetto Gestione profili</span><span class="sxs-lookup"><span data-stu-id="259d3-109">Profile Manager Object</span></span>

<span data-ttu-id="259d3-110">Un profilo è un set di parametri multimediali utilizzati per creare un file ASF.</span><span class="sxs-lookup"><span data-stu-id="259d3-110">A profile is a set of media parameters used to create an ASF file.</span></span> <span data-ttu-id="259d3-111">L'oggetto Gestione profili crea oggetti profilo per la modifica.</span><span class="sxs-lookup"><span data-stu-id="259d3-111">The profile manager object creates profile objects for editing.</span></span> <span data-ttu-id="259d3-112">È possibile creare oggetti profilo senza dati in essi o compilati da dati di profilo esistenti.</span><span class="sxs-lookup"><span data-stu-id="259d3-112">Profile objects can be created without any data in them or built from existing profile data.</span></span> <span data-ttu-id="259d3-113">L'oggetto Profile Manager fornisce anche metodi per l'enumerazione dei codec supportati e l'esecuzione di query su tali codec per ottenere informazioni.</span><span class="sxs-lookup"><span data-stu-id="259d3-113">The profile manager object also provides methods for enumerating supported codecs and querying those codecs for information.</span></span>

<span data-ttu-id="259d3-114">L'oggetto di gestione dei profili viene creato dalla funzione [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) , che imposta un puntatore a un'interfaccia [**IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) .</span><span class="sxs-lookup"><span data-stu-id="259d3-114">The profile manager object is created by the [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) function, which sets a pointer to an [**IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) interface.</span></span> <span data-ttu-id="259d3-115">È possibile ottenere le altre interfacce dell'oggetto Profile Manager chiamando il metodo **QueryInterface** .</span><span class="sxs-lookup"><span data-stu-id="259d3-115">The other interfaces of the profile manager object can be obtained by calling the **QueryInterface** method.</span></span>

<span data-ttu-id="259d3-116">Le interfacce seguenti sono supportate dall'oggetto Gestione profili.</span><span class="sxs-lookup"><span data-stu-id="259d3-116">The following interfaces are supported by the profile manager object.</span></span>



| <span data-ttu-id="259d3-117">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="259d3-117">Interface</span></span>                                                      | <span data-ttu-id="259d3-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="259d3-118">Description</span></span>                                                                                                                                  |
|----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="259d3-119">**IWMCodecInfo**</span><span class="sxs-lookup"><span data-stu-id="259d3-119">**IWMCodecInfo**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo)                           | <span data-ttu-id="259d3-120">Recupera le informazioni sui codec supportati e i relativi formati.</span><span class="sxs-lookup"><span data-stu-id="259d3-120">Retrieves information about supported codecs and their formats.</span></span>                                                                              |
| [<span data-ttu-id="259d3-121">**IWMCodecInfo2**</span><span class="sxs-lookup"><span data-stu-id="259d3-121">**IWMCodecInfo2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo2)                         | <span data-ttu-id="259d3-122">Recupera i nomi dei codec supportati e le descrizioni dei relativi formati.</span><span class="sxs-lookup"><span data-stu-id="259d3-122">Retrieves the names of the supported codecs and the descriptions of their formats.</span></span> <span data-ttu-id="259d3-123">Eredita tutti i metodi di **IWMCodecInfo**.</span><span class="sxs-lookup"><span data-stu-id="259d3-123">Inherits all of the methods of **IWMCodecInfo**.</span></span>          |
| [<span data-ttu-id="259d3-124">**IWMCodecInfo3**</span><span class="sxs-lookup"><span data-stu-id="259d3-124">**IWMCodecInfo3**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo3)                         | <span data-ttu-id="259d3-125">Recupera le proprietà dei codec e i codec delle query per le funzionalità supportate.</span><span class="sxs-lookup"><span data-stu-id="259d3-125">Retrieves codec properties and queries codecs for supported features.</span></span> <span data-ttu-id="259d3-126">Eredita tutti i metodi di **IWMCodecInfo** e **IWMCodecInfo2**.</span><span class="sxs-lookup"><span data-stu-id="259d3-126">Inherits all of the methods of **IWMCodecInfo** and **IWMCodecInfo2**.</span></span> |
| [<span data-ttu-id="259d3-127">**IWMProfileManager**</span><span class="sxs-lookup"><span data-stu-id="259d3-127">**IWMProfileManager**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager)                 | <span data-ttu-id="259d3-128">Crea nuovi profili, carica i profili esistenti e salva i profili personalizzati.</span><span class="sxs-lookup"><span data-stu-id="259d3-128">Creates new profiles, loads existing profiles, and saves custom profiles.</span></span>                                                                    |
| [<span data-ttu-id="259d3-129">**IWMProfileManager2**</span><span class="sxs-lookup"><span data-stu-id="259d3-129">**IWMProfileManager2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager2)               | <span data-ttu-id="259d3-130">Controlla la versione dei profili di sistema enumerati da Gestione profili.</span><span class="sxs-lookup"><span data-stu-id="259d3-130">Controls the version of system profiles enumerated by the profile manager.</span></span> <span data-ttu-id="259d3-131">Eredita tutti i metodi di **IWMProfileManager**.</span><span class="sxs-lookup"><span data-stu-id="259d3-131">Inherits all of the methods of **IWMProfileManager**.</span></span>             |
| [<span data-ttu-id="259d3-132">**IWMProfileManagerLanguage**</span><span class="sxs-lookup"><span data-stu-id="259d3-132">**IWMProfileManagerLanguage**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanagerlanguage) | <span data-ttu-id="259d3-133">Controlla la lingua dei profili di sistema analizzati da Gestione profili.</span><span class="sxs-lookup"><span data-stu-id="259d3-133">Controls the language of the system profiles parsed by the profile manager.</span></span>                                                                  |



 

## <a name="remarks"></a><span data-ttu-id="259d3-134">Commenti</span><span class="sxs-lookup"><span data-stu-id="259d3-134">Remarks</span></span>

<span data-ttu-id="259d3-135">Quando un oggetto di gestione profili viene creato, analizza tutti i profili di sistema, operazione che può richiedere alcuni secondi.</span><span class="sxs-lookup"><span data-stu-id="259d3-135">When a profile manager object is created, it parses all of the system profiles, which can take several seconds.</span></span> <span data-ttu-id="259d3-136">La creazione e il rilascio di un gestore profili ogni volta che è necessario utilizzarlo influirà negativamente sulle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="259d3-136">Creating and releasing a profile manager every time you need to use it will adversely affect performance.</span></span> <span data-ttu-id="259d3-137">È necessario creare un gestore profili una volta nell'applicazione e rilasciarlo solo quando non è più necessario utilizzarlo.</span><span class="sxs-lookup"><span data-stu-id="259d3-137">You should create a profile manager once in your application and release it only when you no longer need to use it.</span></span>

## <a name="related-topics"></a><span data-ttu-id="259d3-138">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="259d3-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="259d3-139">**Oggetti**</span><span class="sxs-lookup"><span data-stu-id="259d3-139">**Objects**</span></span>](objects.md)
</dt> <dt>

[<span data-ttu-id="259d3-140">**Oggetto profilo**</span><span class="sxs-lookup"><span data-stu-id="259d3-140">**Profile Object**</span></span>](profile-object.md)
</dt> <dt>

[<span data-ttu-id="259d3-141">**Profili**</span><span class="sxs-lookup"><span data-stu-id="259d3-141">**Profiles**</span></span>](profiles.md)
</dt> </dl>

 

 




