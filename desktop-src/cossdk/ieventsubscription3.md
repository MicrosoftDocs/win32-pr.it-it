---
description: Archivia e recupera le informazioni sulle sottoscrizioni di eventi. Questa interfaccia estende l'interfaccia IEventSubscription2.
ms.assetid: fd1c136e-6e4e-42ca-a951-4aa5fcdfaa49
title: Interfaccia IEventSubscription3
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSubscription3
api_type:
- COM
api_location: ''
ms.openlocfilehash: 94225faf957b2eac3388422d74df3cfdb8bf6d90
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305219"
---
# <a name="ieventsubscription3-interface"></a><span data-ttu-id="f1490-104">Interfaccia IEventSubscription3</span><span class="sxs-lookup"><span data-stu-id="f1490-104">IEventSubscription3 interface</span></span>

<span data-ttu-id="f1490-105">Archivia e recupera le informazioni sulle sottoscrizioni di eventi.</span><span class="sxs-lookup"><span data-stu-id="f1490-105">Stores and retrieves information about event subscriptions.</span></span> <span data-ttu-id="f1490-106">Questa interfaccia estende l'interfaccia [**IEventSubscription2**](ieventsubscription2.md) .</span><span class="sxs-lookup"><span data-stu-id="f1490-106">This interface extends the [**IEventSubscription2**](ieventsubscription2.md) interface.</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="f1490-107">Quando implementare</span><span class="sxs-lookup"><span data-stu-id="f1490-107">When to implement</span></span>

<span data-ttu-id="f1490-108">Non è necessario implementare l'interfaccia **IEventSubscription3** .</span><span class="sxs-lookup"><span data-stu-id="f1490-108">You do not need to implement the **IEventSubscription3** interface.</span></span> <span data-ttu-id="f1490-109">Una classe di oggetti evento fornita dal sistema (CLSID \_ CEventSubscription) implementa **IEventSubscription3**.</span><span class="sxs-lookup"><span data-stu-id="f1490-109">A system-supplied event object class (CLSID\_CEventSubscription) implements **IEventSubscription3**.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="f1490-110">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="f1490-110">When to use</span></span>

<span data-ttu-id="f1490-111">Il sistema [degli eventi com+](com--events.md) utilizza questa interfaccia per ottenere informazioni sulle singole sottoscrizioni.</span><span class="sxs-lookup"><span data-stu-id="f1490-111">The [COM+ Events](com--events.md) system uses this interface to obtain information about individual subscriptions.</span></span>

## <a name="members"></a><span data-ttu-id="f1490-112">Membri</span><span class="sxs-lookup"><span data-stu-id="f1490-112">Members</span></span>

<span data-ttu-id="f1490-113">L'interfaccia **IEventSubscription3** eredita da **IEventSubscription2**.</span><span class="sxs-lookup"><span data-stu-id="f1490-113">The **IEventSubscription3** interface inherits from **IEventSubscription2**.</span></span> <span data-ttu-id="f1490-114">**IEventSubscription3** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="f1490-114">**IEventSubscription3** also has these types of members:</span></span>

-   [<span data-ttu-id="f1490-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f1490-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f1490-116">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f1490-116">Properties</span></span>

<span data-ttu-id="f1490-117">L'interfaccia **IEventSubscription3** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="f1490-117">The **IEventSubscription3** interface has these properties.</span></span>



| <span data-ttu-id="f1490-118">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f1490-118">Property</span></span>                                                                                  | <span data-ttu-id="f1490-119">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="f1490-119">Access type</span></span>           | <span data-ttu-id="f1490-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f1490-120">Description</span></span>                                                |
|:------------------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------|
| [<span data-ttu-id="f1490-121">**EventClassApplicationID**</span><span class="sxs-lookup"><span data-stu-id="f1490-121">**EventClassApplicationID**</span></span>](ieventsubscription3-eventclassapplicationid.md)<br/> | <span data-ttu-id="f1490-122">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="f1490-122">Read/write</span></span><br/> | <span data-ttu-id="f1490-123">GUID dell'applicazione dell'oggetto della classe di evento.</span><span class="sxs-lookup"><span data-stu-id="f1490-123">The application GUID of the event class object.</span></span><br/> |
| [<span data-ttu-id="f1490-124">**EventClassPartitionID**</span><span class="sxs-lookup"><span data-stu-id="f1490-124">**EventClassPartitionID**</span></span>](ieventsubscription3-eventclasspartitionid.md)<br/>     | <span data-ttu-id="f1490-125">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="f1490-125">Read/write</span></span><br/> | <span data-ttu-id="f1490-126">GUID della partizione dell'oggetto della classe di evento.</span><span class="sxs-lookup"><span data-stu-id="f1490-126">The partition GUID of the event class object.</span></span><br/>   |
| [<span data-ttu-id="f1490-127">**SubscriberApplicationID**</span><span class="sxs-lookup"><span data-stu-id="f1490-127">**SubscriberApplicationID**</span></span>](ieventsubscription3-subscriberapplicationid.md)<br/> | <span data-ttu-id="f1490-128">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="f1490-128">Read/write</span></span><br/> | <span data-ttu-id="f1490-129">GUID dell'applicazione del Sottoscrittore.</span><span class="sxs-lookup"><span data-stu-id="f1490-129">The application GUID of the subscriber.</span></span><br/>         |
| [<span data-ttu-id="f1490-130">**SubscriberPartitionID**</span><span class="sxs-lookup"><span data-stu-id="f1490-130">**SubscriberPartitionID**</span></span>](ieventsubscription3-subscriberpartitionid.md)<br/>     | <span data-ttu-id="f1490-131">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="f1490-131">Read/write</span></span><br/> | <span data-ttu-id="f1490-132">GUID della partizione del Sottoscrittore.</span><span class="sxs-lookup"><span data-stu-id="f1490-132">The partition GUID of the subscriber.</span></span><br/>           |



 

## <a name="requirements"></a><span data-ttu-id="f1490-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f1490-133">Requirements</span></span>



| <span data-ttu-id="f1490-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="f1490-134">Requirement</span></span> | <span data-ttu-id="f1490-135">Valore</span><span class="sxs-lookup"><span data-stu-id="f1490-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="f1490-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f1490-136">Minimum supported client</span></span><br/> | <span data-ttu-id="f1490-137">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f1490-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="f1490-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f1490-138">Minimum supported server</span></span><br/> | <span data-ttu-id="f1490-139">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f1490-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="f1490-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f1490-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1490-141">**IEventSubscription2**</span><span class="sxs-lookup"><span data-stu-id="f1490-141">**IEventSubscription2**</span></span>](ieventsubscription2.md)
</dt> </dl>

 

 




