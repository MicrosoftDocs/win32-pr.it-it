---
title: Modifica del registro di sistema di Windows 95
description: È possibile utilizzare REGEDIT per modificare il registro di sistema di Windows 95 per designare un NSP.
ms.assetid: 109daf4a-722f-4a25-a778-72360ee07ad9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c622ea44a5e365ca631d6d4db34af8e939ea6487
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856773"
---
# <a name="editing-the-windows-95-registry"></a><span data-ttu-id="569a1-103">Modifica del registro di sistema di Windows 95</span><span class="sxs-lookup"><span data-stu-id="569a1-103">Editing the Windows 95 Registry</span></span>

<span data-ttu-id="569a1-104">È possibile utilizzare REGEDIT per modificare il registro di sistema di Windows 95 per designare un NSP.</span><span class="sxs-lookup"><span data-stu-id="569a1-104">You can use REGEDIT to edit the Windows 95 registry to designate an NSP.</span></span>

<span data-ttu-id="569a1-105">**Per designare un provider di servizi di nome localizzatore Microsoft per Windows 95**</span><span class="sxs-lookup"><span data-stu-id="569a1-105">**To designate a Microsoft Locator name service provider for Windows 95**</span></span>

1.  <span data-ttu-id="569a1-106">Select</span><span class="sxs-lookup"><span data-stu-id="569a1-106">Select</span></span>

    <span data-ttu-id="569a1-107">**HKEY \_ SOFTWARE del \_ computer locale** \\  \\ **Microsoft** \\ **RPC**</span><span class="sxs-lookup"><span data-stu-id="569a1-107">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**Rpc**</span></span>

2.  <span data-ttu-id="569a1-108">Crea una nuova chiave denominata</span><span class="sxs-lookup"><span data-stu-id="569a1-108">Create a new key called</span></span>

    <span data-ttu-id="569a1-109">**NameService**</span><span class="sxs-lookup"><span data-stu-id="569a1-109">**NameService**</span></span>

3.  <span data-ttu-id="569a1-110">Con la chiave **NameService** selezionata, creare i nuovi nomi **StringValue** e modificarli in modo che contengano i dati, come illustrato nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="569a1-110">With the **NameService** key selected, create the new **StringValue** names and modify them to contain data as shown in the following table.</span></span>

    

    | <span data-ttu-id="569a1-111">Nome</span><span class="sxs-lookup"><span data-stu-id="569a1-111">Name</span></span>                     | <span data-ttu-id="569a1-112">Data</span><span class="sxs-lookup"><span data-stu-id="569a1-112">Data</span></span>                                                                        |
    |--------------------------|-----------------------------------------------------------------------------|
    | <span data-ttu-id="569a1-113">**DefaultSyntax**</span><span class="sxs-lookup"><span data-stu-id="569a1-113">**DefaultSyntax**</span></span>        | <span data-ttu-id="569a1-114">3</span><span class="sxs-lookup"><span data-stu-id="569a1-114">3</span></span><br/>                                                                |
    | <span data-ttu-id="569a1-115">**Protocollo**</span><span class="sxs-lookup"><span data-stu-id="569a1-115">**Protocol**</span></span>             | <span data-ttu-id="569a1-116">\_NP ncacn</span><span class="sxs-lookup"><span data-stu-id="569a1-116">ncacn\_np</span></span><br/>                                                        |
    | <span data-ttu-id="569a1-117">**Endpoint**</span><span class="sxs-lookup"><span data-stu-id="569a1-117">**Endpoint**</span></span>             | <span data-ttu-id="569a1-118">\\\\localizzatore pipe</span><span class="sxs-lookup"><span data-stu-id="569a1-118">\\pipe\\locator</span></span><br/>                                                  |
    | <span data-ttu-id="569a1-119">**NetworkAddress**</span><span class="sxs-lookup"><span data-stu-id="569a1-119">**NetworkAddress**</span></span>       | <span data-ttu-id="569a1-120">MyServer (dove MyServer è il nome del computer Windows NT)</span><span class="sxs-lookup"><span data-stu-id="569a1-120">myserver (where myserver is the name of the Windows NT computer)</span></span><br/> |
    | <span data-ttu-id="569a1-121">**ServerNetworkAddress**</span><span class="sxs-lookup"><span data-stu-id="569a1-121">**ServerNetworkAddress**</span></span> | <span data-ttu-id="569a1-122">MyServer</span><span class="sxs-lookup"><span data-stu-id="569a1-122">myserver</span></span><br/>                                                         |

    

     

<span data-ttu-id="569a1-123">È possibile utilizzare REGEDIT per modificare il registro di sistema di Windows 95 per designare un NSP DCE CDS.</span><span class="sxs-lookup"><span data-stu-id="569a1-123">You can use REGEDIT to edit the Windows 95 registry to designate a DCE CDS NSP.</span></span>

<span data-ttu-id="569a1-124">**Per designare un provider di servizi di nomi di CDS DCE per Windows 95**</span><span class="sxs-lookup"><span data-stu-id="569a1-124">**To designate a DCE CDS name service provider for Windows 95**</span></span>

1.  <span data-ttu-id="569a1-125">Select</span><span class="sxs-lookup"><span data-stu-id="569a1-125">Select</span></span>

    <span data-ttu-id="569a1-126">**HKEY \_ SOFTWARE del \_ computer locale** \\  \\ **Microsoft** \\ **RPC**</span><span class="sxs-lookup"><span data-stu-id="569a1-126">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**Rpc**</span></span>

2.  <span data-ttu-id="569a1-127">Crea una nuova chiave denominata</span><span class="sxs-lookup"><span data-stu-id="569a1-127">Create a new key called</span></span>

    <span data-ttu-id="569a1-128">**NameService**</span><span class="sxs-lookup"><span data-stu-id="569a1-128">**NameService**</span></span>

3.  <span data-ttu-id="569a1-129">Con la chiave **NameService** selezionata, creare i nuovi nomi **StringValue** e modificarli in modo che contengano i dati, come illustrato nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="569a1-129">With the **NameService** key selected, create the new **StringValue** names and modify them to contain data as shown in the following table.</span></span>

    

    | <span data-ttu-id="569a1-130">Nome</span><span class="sxs-lookup"><span data-stu-id="569a1-130">Name</span></span>                     | <span data-ttu-id="569a1-131">Data</span><span class="sxs-lookup"><span data-stu-id="569a1-131">Data</span></span>                                                             |
    |--------------------------|------------------------------------------------------------------|
    | <span data-ttu-id="569a1-132">**DefaultSyntax**</span><span class="sxs-lookup"><span data-stu-id="569a1-132">**DefaultSyntax**</span></span>        | <span data-ttu-id="569a1-133">3</span><span class="sxs-lookup"><span data-stu-id="569a1-133">3</span></span><br/>                                                     |
    | <span data-ttu-id="569a1-134">**Protocollo**</span><span class="sxs-lookup"><span data-stu-id="569a1-134">**Protocol**</span></span>             | <span data-ttu-id="569a1-135">\_TCP IP \_ ncacn</span><span class="sxs-lookup"><span data-stu-id="569a1-135">ncacn\_ip\_tcp</span></span><br/>                                        |
    | <span data-ttu-id="569a1-136">**Endpoint**</span><span class="sxs-lookup"><span data-stu-id="569a1-136">**Endpoint**</span></span>             | <span data-ttu-id="569a1-137">"" (stringa vuota)</span><span class="sxs-lookup"><span data-stu-id="569a1-137">"" (an empty string)</span></span><br/>                                  |
    | <span data-ttu-id="569a1-138">**NetworkAddress**</span><span class="sxs-lookup"><span data-stu-id="569a1-138">**NetworkAddress**</span></span>       | <span data-ttu-id="569a1-139">MyServer (il nome del computer host che esegue NSID)</span><span class="sxs-lookup"><span data-stu-id="569a1-139">myserver (the name of the host computer running nsid)</span></span><br/> |
    | <span data-ttu-id="569a1-140">**ServerNetworkAddress**</span><span class="sxs-lookup"><span data-stu-id="569a1-140">**ServerNetworkAddress**</span></span> | <span data-ttu-id="569a1-141">MyServer (il nome del computer host che esegue NSID)</span><span class="sxs-lookup"><span data-stu-id="569a1-141">myserver (the name of the host computer running nsid)</span></span><br/> |

    

     

    > [!Note]  
    > <span data-ttu-id="569a1-142">Per configurare i CD DCE come provider di servizi di nome, è necessario disporre del prodotto del servizio directory celle DCE Digital Equipment Corporation.</span><span class="sxs-lookup"><span data-stu-id="569a1-142">You must have the Digital Equipment Corporation DCE Cell Directory Service product to configure the DCE CDS as your name service provider.</span></span> <span data-ttu-id="569a1-143">Per informazioni sui CD DCE, vedere la documentazione fornita da Digital Equipment Corporation.</span><span class="sxs-lookup"><span data-stu-id="569a1-143">See the documentation provided by Digital Equipment Corporation for information about DCE CDS.</span></span>

     

 

 





