---
title: File di codice per l'esempio di provider di origine
description: File di codice per l'esempio di provider di origine
ms.assetid: bd6bfc98-a805-4e04-8a80-7af42ed3dbef
keywords:
- Windows Media Gestione dispositivi, esempi
- Gestione dispositivi, esempi
- Windows Media Gestione dispositivi, esempio di provider di servizi
- Gestione dispositivi, esempio di provider di servizi
- provider di servizi, esempi
- esempi, provider di servizi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64b8af4b34310ae183ce55b2e52d3dd346dc6665
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104116841"
---
# <a name="code-files-for-the-source-provider-sample"></a><span data-ttu-id="7a9bb-109">File di codice per l'esempio di provider di origine</span><span class="sxs-lookup"><span data-stu-id="7a9bb-109">Code Files for the Source Provider Sample</span></span>

<span data-ttu-id="7a9bb-110">Il progetto del provider di origine di esempio include i file di codice sorgente seguenti, con le intestazioni associate:</span><span class="sxs-lookup"><span data-stu-id="7a9bb-110">The sample source provider project includes the following source code files, with associated headers:</span></span>



| <span data-ttu-id="7a9bb-111">File</span><span class="sxs-lookup"><span data-stu-id="7a9bb-111">File</span></span>                   | <span data-ttu-id="7a9bb-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7a9bb-112">Description</span></span>                                                                                                                                                                                                     |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a9bb-113">hdsppch. cpp</span><span class="sxs-lookup"><span data-stu-id="7a9bb-113">hdsppch.cpp</span></span>            | <span data-ttu-id="7a9bb-114">Include file ATL standard.</span><span class="sxs-lookup"><span data-stu-id="7a9bb-114">Includes standard ATL files.</span></span>                                                                                                                                                                                    |
| <span data-ttu-id="7a9bb-115">chiave. c</span><span class="sxs-lookup"><span data-stu-id="7a9bb-115">key.c</span></span>                  | <span data-ttu-id="7a9bb-116">Contiene una chiave di autenticazione fittizia.</span><span class="sxs-lookup"><span data-stu-id="7a9bb-116">Contains a dummy authentication key.</span></span>                                                                                                                                                                            |
| <span data-ttu-id="7a9bb-117">loghelp. cpp</span><span class="sxs-lookup"><span data-stu-id="7a9bb-117">loghelp.cpp</span></span>            | <span data-ttu-id="7a9bb-118">Contiene funzioni che registrano l'attività e gli errori usando la classe **WMDMLogger** , implementata nel file di sistema WMDMLOG.dll.</span><span class="sxs-lookup"><span data-stu-id="7a9bb-118">Contains functions that log activity and errors by using the **WMDMLogger** class, which is implemented in the WMDMLOG.dll system file.</span></span>                                                                         |
| <span data-ttu-id="7a9bb-119">MDServiceProvider. cpp</span><span class="sxs-lookup"><span data-stu-id="7a9bb-119">MDServiceProvider.cpp</span></span>  | <span data-ttu-id="7a9bb-120">Implementa una classe, CMDServiceProvider, che implementa le interfacce [**IMDServiceProvider**](/windows/desktop/api/mswmdm/nn-mswmdm-imdserviceprovider) e IComponentAuthenticate.</span><span class="sxs-lookup"><span data-stu-id="7a9bb-120">Implements a class, CMDServiceProvider, that implements the [**IMDServiceProvider**](/windows/desktop/api/mswmdm/nn-mswmdm-imdserviceprovider) and IComponentAuthenticate interfaces.</span></span>                                                             |
| <span data-ttu-id="7a9bb-121">MDSP. cpp</span><span class="sxs-lookup"><span data-stu-id="7a9bb-121">mdsp.cpp</span></span>               | <span data-ttu-id="7a9bb-122">Il codice di registrazione e il punto di ingresso della DLL.</span><span class="sxs-lookup"><span data-stu-id="7a9bb-122">DLL entry point and registration code.</span></span>                                                                                                                                                                          |
| <span data-ttu-id="7a9bb-123">MDSPDevice. cpp</span><span class="sxs-lookup"><span data-stu-id="7a9bb-123">MDSPDevice.cpp</span></span>         | <span data-ttu-id="7a9bb-124">Implementa una classe, CMDSPDevice, che implementa le interfacce [**IMDSPDevice2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice2), [**IMDSPDeviceControl**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevicecontrol)e **ISpecifyPropertyPages** .</span><span class="sxs-lookup"><span data-stu-id="7a9bb-124">Implements a class, CMDSPDevice, that implements the [**IMDSPDevice2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice2), [**IMDSPDeviceControl**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevicecontrol), and **ISpecifyPropertyPages** interfaces.</span></span>                          |
| <span data-ttu-id="7a9bb-125">MDSPEnumDevice. cpp</span><span class="sxs-lookup"><span data-stu-id="7a9bb-125">MDSPEnumDevice.cpp</span></span>     | <span data-ttu-id="7a9bb-126">Implementa una classe, CMDSPEnumDevice, che implementa l'interfaccia [**IMDSPEnumDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspenumdevice) .</span><span class="sxs-lookup"><span data-stu-id="7a9bb-126">Implements a class, CMDSPEnumDevice, that implements the [**IMDSPEnumDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspenumdevice) interface.</span></span>                                                                                                  |
| <span data-ttu-id="7a9bb-127">MDSPEnumStorage. cpp</span><span class="sxs-lookup"><span data-stu-id="7a9bb-127">MDSPEnumStorage.cpp</span></span>    | <span data-ttu-id="7a9bb-128">Implementa una classe, CMDSPEnumStorage, che implementa l'interfaccia [**IMDSPEnumStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspenumstorage) .</span><span class="sxs-lookup"><span data-stu-id="7a9bb-128">Implements a class, CMDSPEnumStorage, that implements the [**IMDSPEnumStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspenumstorage) interface.</span></span>                                                                                               |
| <span data-ttu-id="7a9bb-129">MDSPStorage. cpp</span><span class="sxs-lookup"><span data-stu-id="7a9bb-129">MDSPStorage.cpp</span></span>        | <span data-ttu-id="7a9bb-130">Implementa una classe, CMDSPStorage, che implementa le interfacce [**IMDSPStorage2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage2), [**IMDSPObjectInfo**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobjectinfo)e [**IMDSPObject**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobject) .</span><span class="sxs-lookup"><span data-stu-id="7a9bb-130">Implements a class, CMDSPStorage, that implements the [**IMDSPStorage2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage2), [**IMDSPObjectInfo**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobjectinfo), and [**IMDSPObject**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobject) interfaces.</span></span>                    |
| <span data-ttu-id="7a9bb-131">MDSPStorageGlobals. cpp</span><span class="sxs-lookup"><span data-stu-id="7a9bb-131">MDSPStorageGlobals.cpp</span></span> | <span data-ttu-id="7a9bb-132">Implementa una classe, CMDSPStorageGlobals, che implementa l'interfaccia [**IMDSPStorageGlobals**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorageglobals) .</span><span class="sxs-lookup"><span data-stu-id="7a9bb-132">Implements a class, CMDSPStorageGlobals, that implements the [**IMDSPStorageGlobals**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorageglobals) interface.</span></span>                                                                                      |
| <span data-ttu-id="7a9bb-133">MDSPutil. cpp</span><span class="sxs-lookup"><span data-stu-id="7a9bb-133">MDSPutil.cpp</span></span>           | <span data-ttu-id="7a9bb-134">Contiene varie funzioni di utilità per la gestione dei dispositivi e dei file.</span><span class="sxs-lookup"><span data-stu-id="7a9bb-134">Contains various utility functions for device and file management.</span></span>                                                                                                                                              |
| <span data-ttu-id="7a9bb-135">pagina di appoggio. cpp</span><span class="sxs-lookup"><span data-stu-id="7a9bb-135">proppage.cpp</span></span>           | <span data-ttu-id="7a9bb-136">Implementa una classe, CPropPage, che eredita le classi ATL **IPropertyPageImpl** (per implementare IPropertyPage) e **CDialogImpl**, che eredita la classe ATL CDialogImpl (per gestire Windows e i messaggi).</span><span class="sxs-lookup"><span data-stu-id="7a9bb-136">Implements a class, CPropPage, that inherits the ATL classes **IPropertyPageImpl** (to implement IPropertyPage) and **CDialogImpl**, which inherits the ATL class CDialogImpl (to manage windows and messages).</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="7a9bb-137">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7a9bb-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7a9bb-138">**Provider di servizi di esempio**</span><span class="sxs-lookup"><span data-stu-id="7a9bb-138">**Sample Service Provider**</span></span>](sample-service-provider.md)
</dt> </dl>

 

 




