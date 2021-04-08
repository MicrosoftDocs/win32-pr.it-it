---
title: Digitare 1 plug-in di archivio online
description: Digitare 1 plug-in di archivio online
ms.assetid: 3aa74282-522b-4240-8d72-73bd3015abeb
keywords:
- Windows Media Player Online Stores, plug-in
- archivi online, plug-in
- digitare 1 negozi online, plug-in
- Windows Media Player Online Stores, interfaccia IWMPContentPartner
- negozi online, interfaccia IWMPContentPartner
- tipo 1 Store online, interfaccia IWMPContentPartner
- plug-in, archivi Windows Media Player online
- plug-in, archivi online
- plug-in, digitare 1 negozi online
- plug-in, interfaccia IWMPContentPartner
- Plug-in di Windows Media Player, digitare 1 negozi online
- Plug-in di Windows Media Player, archivi online
- Plug-in di Windows Media Player, archivi Windows Media Player online
- Plug-in di Windows Media Player, interfaccia IWMPContentPartner
- IWMPContentPartner
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fe42095d08262520734603a5418ac6831ce6685
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2020
ms.locfileid: "104046444"
---
# <a name="type-1-online-store-plug-in"></a><span data-ttu-id="a4ae0-118">Digitare 1 plug-in di archivio online</span><span class="sxs-lookup"><span data-stu-id="a4ae0-118">Type 1 Online Store Plug-in</span></span>

<span data-ttu-id="a4ae0-119">Per sfruttare i vantaggi delle funzionalità di integrazione delle librerie, è necessario che i provider di archivio online di tipo 1 creino un plug-in che implementi l'interfaccia [IWMPContentPartner](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner) .</span><span class="sxs-lookup"><span data-stu-id="a4ae0-119">To take advantage of library integration features, type 1 online store providers must create a plug-in that implements the [IWMPContentPartner](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner) interface.</span></span> <span data-ttu-id="a4ae0-120">Questa interfaccia fornisce i metodi che Windows Media Player chiama per inviare una notifica al negozio online sulle attività eseguite nel lettore e recuperare informazioni specifiche sul contenuto del negozio online, sul catalogo o sull'archivio.</span><span class="sxs-lookup"><span data-stu-id="a4ae0-120">This interface provides the methods that Windows Media Player calls to notify the online store about activities taking place in the Player and to retrieve specific information about online store content, the catalog, or the store itself.</span></span>

<span data-ttu-id="a4ae0-121">Dopo che Windows Media Player crea un'istanza del plug-in, il lettore chiama [IWMPContentPartner:: filecallback](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-setcallback)e fornisce un puntatore all'interfaccia **IWMPContentPartnerCallback** .</span><span class="sxs-lookup"><span data-stu-id="a4ae0-121">After Windows Media Player instantiates the plug-in, the Player calls [IWMPContentPartner::SetCallback](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-setcallback), and provides a pointer to the **IWMPContentPartnerCallback** interface.</span></span> <span data-ttu-id="a4ae0-122">Questa interfaccia consente al negozio online di effettuare chiamate a Windows Media Player per fornire informazioni sullo stato o per avviare processi specifici, ad esempio il download di un brano musicale.</span><span class="sxs-lookup"><span data-stu-id="a4ae0-122">This interface gives the online store a way to make calls into Windows Media Player to provide status information or to initiate specific processes, such as downloading a music track.</span></span>

<span data-ttu-id="a4ae0-123">Windows Media Player e il plug-in vengono eseguiti in processi distinti.</span><span class="sxs-lookup"><span data-stu-id="a4ae0-123">Windows Media Player and the plug-in run in separate processes.</span></span> <span data-ttu-id="a4ae0-124">Il plug-in è un server in-process eseguito nel surrogato predefinito della DLL, dllhost.exe.</span><span class="sxs-lookup"><span data-stu-id="a4ae0-124">The plug-in is an in-process server that runs in the default DLL surrogate, dllhost.exe.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a4ae0-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a4ae0-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a4ae0-126">**Informazioni sugli archivi online di tipo 1**</span><span class="sxs-lookup"><span data-stu-id="a4ae0-126">**About Type 1 Online Stores**</span></span>](about-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="a4ae0-127">**Interfaccia IWMPContentPartner**</span><span class="sxs-lookup"><span data-stu-id="a4ae0-127">**IWMPContentPartner Interface**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner)
</dt> <dt>

[<span data-ttu-id="a4ae0-128">**Interfaccia IWMPContentPartnerCallback**</span><span class="sxs-lookup"><span data-stu-id="a4ae0-128">**IWMPContentPartnerCallback Interface**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartnercallback)
</dt> </dl>

 

 




