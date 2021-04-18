---
description: Archivia e recupera le informazioni sulle sottoscrizioni di eventi. Questa interfaccia estende l'interfaccia IEventSubscription.
ms.assetid: f153afb7-c897-40f8-81ed-50308844cac5
title: Interfaccia IEventSubscription2
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSubscription2
api_type:
- COM
api_location: ''
ms.openlocfilehash: bc7e3e41efc4b44c00c23f0910b8b696940fc1df
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305222"
---
# <a name="ieventsubscription2-interface"></a><span data-ttu-id="ccf05-104">Interfaccia IEventSubscription2</span><span class="sxs-lookup"><span data-stu-id="ccf05-104">IEventSubscription2 interface</span></span>

<span data-ttu-id="ccf05-105">Archivia e recupera le informazioni sulle sottoscrizioni di eventi.</span><span class="sxs-lookup"><span data-stu-id="ccf05-105">Stores and retrieves information about event subscriptions.</span></span> <span data-ttu-id="ccf05-106">Questa interfaccia estende l'interfaccia [**IEventSubscription**](/windows/desktop/api/EventSys/nn-eventsys-ieventsubscription) .</span><span class="sxs-lookup"><span data-stu-id="ccf05-106">This interface extends the [**IEventSubscription**](/windows/desktop/api/EventSys/nn-eventsys-ieventsubscription) interface.</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="ccf05-107">Quando implementare</span><span class="sxs-lookup"><span data-stu-id="ccf05-107">When to implement</span></span>

<span data-ttu-id="ccf05-108">Non è necessario implementare l'interfaccia **IEventSubscription2** .</span><span class="sxs-lookup"><span data-stu-id="ccf05-108">You do not need to implement the **IEventSubscription2** interface.</span></span> <span data-ttu-id="ccf05-109">Una classe di oggetti evento fornita dal sistema (CLSID \_ CEventSubscription) implementa **IEventSubscription2**.</span><span class="sxs-lookup"><span data-stu-id="ccf05-109">A system-supplied event object class (CLSID\_CEventSubscription) implements **IEventSubscription2**.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="ccf05-110">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="ccf05-110">When to use</span></span>

<span data-ttu-id="ccf05-111">Il sistema [degli eventi com+](com--events.md) utilizza questa interfaccia per ottenere informazioni sulle singole sottoscrizioni.</span><span class="sxs-lookup"><span data-stu-id="ccf05-111">The [COM+ Events](com--events.md) system uses this interface to obtain information about individual subscriptions.</span></span>

## <a name="members"></a><span data-ttu-id="ccf05-112">Membri</span><span class="sxs-lookup"><span data-stu-id="ccf05-112">Members</span></span>

<span data-ttu-id="ccf05-113">L'interfaccia **IEventSubscription2** eredita da **IEventSubscription**.</span><span class="sxs-lookup"><span data-stu-id="ccf05-113">The **IEventSubscription2** interface inherits from **IEventSubscription**.</span></span> <span data-ttu-id="ccf05-114">**IEventSubscription2** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="ccf05-114">**IEventSubscription2** also has these types of members:</span></span>

-   [<span data-ttu-id="ccf05-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ccf05-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ccf05-116">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ccf05-116">Properties</span></span>

<span data-ttu-id="ccf05-117">L'interfaccia **IEventSubscription2** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="ccf05-117">The **IEventSubscription2** interface has these properties.</span></span>



| <span data-ttu-id="ccf05-118">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ccf05-118">Property</span></span>                                                                      | <span data-ttu-id="ccf05-119">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="ccf05-119">Access type</span></span>           | <span data-ttu-id="ccf05-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ccf05-120">Description</span></span>                                                |
|:------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------|
| [<span data-ttu-id="ccf05-121">**FilterCriteria**</span><span class="sxs-lookup"><span data-stu-id="ccf05-121">**FilterCriteria**</span></span>](ieventsubscription2-filtercriteria.md)<br/>       | <span data-ttu-id="ccf05-122">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="ccf05-122">Read/write</span></span><br/> | <span data-ttu-id="ccf05-123">Criteri di filtro che governano la sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="ccf05-123">The filter criteria governing the subscription.</span></span><br/> |
| [<span data-ttu-id="ccf05-124">**SubscriberMoniker**</span><span class="sxs-lookup"><span data-stu-id="ccf05-124">**SubscriberMoniker**</span></span>](ieventsubscription2-subscribermoniker.md)<br/> | <span data-ttu-id="ccf05-125">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="ccf05-125">Read/write</span></span><br/> | <span data-ttu-id="ccf05-126">Moniker del Sottoscrittore.</span><span class="sxs-lookup"><span data-stu-id="ccf05-126">The subscriber's moniker.</span></span><br/>                       |



 

## <a name="requirements"></a><span data-ttu-id="ccf05-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ccf05-127">Requirements</span></span>



| <span data-ttu-id="ccf05-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="ccf05-128">Requirement</span></span> | <span data-ttu-id="ccf05-129">Valore</span><span class="sxs-lookup"><span data-stu-id="ccf05-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="ccf05-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ccf05-130">Minimum supported client</span></span><br/> | <span data-ttu-id="ccf05-131">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ccf05-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="ccf05-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ccf05-132">Minimum supported server</span></span><br/> | <span data-ttu-id="ccf05-133">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ccf05-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="ccf05-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ccf05-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ccf05-135">**IEventSubscription**</span><span class="sxs-lookup"><span data-stu-id="ccf05-135">**IEventSubscription**</span></span>](/windows/desktop/api/EventSys/nn-eventsys-ieventsubscription)
</dt> </dl>

 

 




