---
title: Metodi (IManipulationProcessor)
description: Questa sezione contiene i metodi per l'interfaccia IManipulationProcessor.
ms.assetid: 33736f79-cb61-449c-80b9-1358db2621e9
keywords:
- Windows Touch, interfaccia IManipulationProcessor
- Windows Touch, metodi di interfaccia
- manipolazioni, interfaccia IManipulationProcessor
- Interfaccia IManipulationProcessor, metodi
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 995a848e18b8308d46ceda717bf7eec291953505
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104400139"
---
# <a name="methods-imanipulationprocessor"></a><span data-ttu-id="0e485-107">Metodi (IManipulationProcessor)</span><span class="sxs-lookup"><span data-stu-id="0e485-107">Methods (IManipulationProcessor)</span></span>

<span data-ttu-id="0e485-108">Questa sezione contiene i metodi per l'interfaccia [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) .</span><span class="sxs-lookup"><span data-stu-id="0e485-108">This section contains the methods for the [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) interface.</span></span>

<span data-ttu-id="0e485-109">I metodi seguenti sono esposti dall'interfaccia [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) .</span><span class="sxs-lookup"><span data-stu-id="0e485-109">The following methods are exposed by the [**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor) interface.</span></span>



| <span data-ttu-id="0e485-110">Metodo</span><span class="sxs-lookup"><span data-stu-id="0e485-110">Method</span></span>                                                                      | <span data-ttu-id="0e485-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0e485-111">Description</span></span>                                                                              |
|-----------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0e485-112">**CompleteManipulation**</span><span class="sxs-lookup"><span data-stu-id="0e485-112">**CompleteManipulation**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-completemanipulation) | <span data-ttu-id="0e485-113">Questo metodo viene chiamato quando lo sviluppatore sceglie di terminare la manipolazione.</span><span class="sxs-lookup"><span data-stu-id="0e485-113">This method is called when the developer chooses to end the manipulation.</span></span>                |
| [<span data-ttu-id="0e485-114">**GetAngularVelocity**</span><span class="sxs-lookup"><span data-stu-id="0e485-114">**GetAngularVelocity**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-getangularvelocity)     | <span data-ttu-id="0e485-115">Calcola la velocità rotazionale in cui viene spostato l'oggetto di destinazione.</span><span class="sxs-lookup"><span data-stu-id="0e485-115">Calculates the rotational velocity that the target object is moving at.</span></span>                  |
| [<span data-ttu-id="0e485-116">**GetExpansionVelocity**</span><span class="sxs-lookup"><span data-stu-id="0e485-116">**GetExpansionVelocity**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-getexpansionvelocity) | <span data-ttu-id="0e485-117">Calcola la frequenza di espansione dell'oggetto di destinazione.</span><span class="sxs-lookup"><span data-stu-id="0e485-117">Calculates the rate that the target object is expanding at.</span></span>                              |
| [<span data-ttu-id="0e485-118">**GetVelocityX**</span><span class="sxs-lookup"><span data-stu-id="0e485-118">**GetVelocityX**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-getvelocityx)                 | <span data-ttu-id="0e485-119">Calcola e restituisce la velocità orizzontale per l'oggetto di destinazione.</span><span class="sxs-lookup"><span data-stu-id="0e485-119">Calculates and returns the horizontal velocity for the target object.</span></span>                    |
| [<span data-ttu-id="0e485-120">**Getvelocityy**</span><span class="sxs-lookup"><span data-stu-id="0e485-120">**GetVelocityY**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-getvelocityy)                 | <span data-ttu-id="0e485-121">Calcola e restituisce la velocità verticale.</span><span class="sxs-lookup"><span data-stu-id="0e485-121">Calculates and returns the vertical velocity.</span></span>                                            |
| [<span data-ttu-id="0e485-122">**ProcessDown**</span><span class="sxs-lookup"><span data-stu-id="0e485-122">**ProcessDown**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processdown)                   | <span data-ttu-id="0e485-123">Inserisce i dati nel processore di manipolazione associato a una destinazione.</span><span class="sxs-lookup"><span data-stu-id="0e485-123">Feeds data to the manipulation processor associated with a target.</span></span>                       |
| [<span data-ttu-id="0e485-124">**ProcessMove**</span><span class="sxs-lookup"><span data-stu-id="0e485-124">**ProcessMove**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processmove)                   | <span data-ttu-id="0e485-125">Inserisce i dati nel processore di manipolazione associato a una destinazione.</span><span class="sxs-lookup"><span data-stu-id="0e485-125">Feeds data to the manipulation processor associated with a target.</span></span>                       |
| [<span data-ttu-id="0e485-126">**ProcessUp**</span><span class="sxs-lookup"><span data-stu-id="0e485-126">**ProcessUp**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processup)                       | <span data-ttu-id="0e485-127">Inserisce i dati nel processore di manipolazione associato a una destinazione.</span><span class="sxs-lookup"><span data-stu-id="0e485-127">Feeds data to the manipulation processor associated with a target.</span></span>                       |
| [<span data-ttu-id="0e485-128">**ProcessDownWithTime**</span><span class="sxs-lookup"><span data-stu-id="0e485-128">**ProcessDownWithTime**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processdownwithtime)   | <span data-ttu-id="0e485-129">Inserisce dati che includono un timestamp per il processore di manipolazione associato a una destinazione.</span><span class="sxs-lookup"><span data-stu-id="0e485-129">Feeds data including a timestamp to the manipulation processor associated with a target.</span></span> |
| [<span data-ttu-id="0e485-130">**ProcessMoveWithTime**</span><span class="sxs-lookup"><span data-stu-id="0e485-130">**ProcessMoveWithTime**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processmovewithtime)   | <span data-ttu-id="0e485-131">Inserisce dati che includono un timestamp per il processore di manipolazione associato a una destinazione.</span><span class="sxs-lookup"><span data-stu-id="0e485-131">Feeds data including a timestamp to the manipulation processor associated with a target.</span></span> |
| [<span data-ttu-id="0e485-132">**ProcessUpWithTime**</span><span class="sxs-lookup"><span data-stu-id="0e485-132">**ProcessUpWithTime**</span></span>](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processupwithtime)       | <span data-ttu-id="0e485-133">Inserisce dati che includono un timestamp per il processore di manipolazione associato a una destinazione.</span><span class="sxs-lookup"><span data-stu-id="0e485-133">Feeds data including a timestamp to the manipulation processor associated with a target.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="0e485-134">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0e485-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0e485-135">**IManipulationProcessor**</span><span class="sxs-lookup"><span data-stu-id="0e485-135">**IManipulationProcessor**</span></span>](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor)
</dt> </dl>

 

 




