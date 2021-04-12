---
description: Utilizzato dal servizio di notifica degli eventi di sistema di Microsoft Internet Explorer (SENS) per accedere all'archivio dati degli eventi. Questa interfaccia estende l'interfaccia IEventSystem.
ms.assetid: ad3c38a6-fa2d-4fcd-8782-1fac7595e829
title: Interfaccia IEventSystem2
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSystem2
api_type:
- COM
api_location: ''
ms.openlocfilehash: 3a174c9457dc347257677e8111772ad14f0dc9fd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483597"
---
# <a name="ieventsystem2-interface"></a><span data-ttu-id="943c4-104">Interfaccia IEventSystem2</span><span class="sxs-lookup"><span data-stu-id="943c4-104">IEventSystem2 interface</span></span>

<span data-ttu-id="943c4-105">Utilizzato dal servizio di notifica degli eventi di sistema di Microsoft Internet Explorer (SENS) per accedere all'archivio dati degli eventi.</span><span class="sxs-lookup"><span data-stu-id="943c4-105">Used by the Microsoft Internet Explorer System Event Notification Service (SENS) to access the event data store.</span></span> <span data-ttu-id="943c4-106">Questa interfaccia estende l'interfaccia [**IEventSystem**](/windows/desktop/api/EventSys/nn-eventsys-ieventsystem) .</span><span class="sxs-lookup"><span data-stu-id="943c4-106">This interface extends the [**IEventSystem**](/windows/desktop/api/EventSys/nn-eventsys-ieventsystem) interface.</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="943c4-107">Quando implementare</span><span class="sxs-lookup"><span data-stu-id="943c4-107">When to implement</span></span>

<span data-ttu-id="943c4-108">Non è necessario implementare l'interfaccia **IEventSystem2** .</span><span class="sxs-lookup"><span data-stu-id="943c4-108">You do not need to implement the **IEventSystem2** interface.</span></span> <span data-ttu-id="943c4-109">Un oggetto sistema eventi (CLSID CEventSystem) fornito dal sistema \_ implementa **IEventSystem2**.</span><span class="sxs-lookup"><span data-stu-id="943c4-109">A system-supplied event system object (CLSID\_CEventSystem) implements **IEventSystem2**.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="943c4-110">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="943c4-110">When to use</span></span>

<span data-ttu-id="943c4-111">Se si usa SENS, è possibile chiamare i metodi di **IEventSystem2** per aggiungere e rimuovere oggetti da e verso l'archivio eventi e per ottenere oggetti dall'archivio eventi.</span><span class="sxs-lookup"><span data-stu-id="943c4-111">If you use SENS, you can call the methods of **IEventSystem2** to add and remove objects to and from the event store and to obtain objects from the event store.</span></span>

<span data-ttu-id="943c4-112">Poiché [**IEventPublisher**](/windows/desktop/api/eventsys/nn-eventsys-ieventpublisher) e l'oggetto server di pubblicazione non sono più supportati, [**IEventObjectChange**](/windows/desktop/api/Eventsys/nn-eventsys-ieventobjectchange) non viene chiamato sul metodo [**ChangedPublisher**](/windows/desktop/api/Eventsys/nf-eventsys-ieventobjectchange-changedpublisher) .</span><span class="sxs-lookup"><span data-stu-id="943c4-112">Because [**IEventPublisher**](/windows/desktop/api/eventsys/nn-eventsys-ieventpublisher) and the publisher object are no longer supported, [**IEventObjectChange**](/windows/desktop/api/Eventsys/nn-eventsys-ieventobjectchange) is not called on the [**ChangedPublisher**](/windows/desktop/api/Eventsys/nf-eventsys-ieventobjectchange-changedpublisher) method.</span></span>

## <a name="members"></a><span data-ttu-id="943c4-113">Membri</span><span class="sxs-lookup"><span data-stu-id="943c4-113">Members</span></span>

<span data-ttu-id="943c4-114">L'interfaccia **IEventSystem2** eredita da **IEventSystem**.</span><span class="sxs-lookup"><span data-stu-id="943c4-114">The **IEventSystem2** interface inherits from **IEventSystem**.</span></span> <span data-ttu-id="943c4-115">**IEventSystem2** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="943c4-115">**IEventSystem2** also has these types of members:</span></span>

-   [<span data-ttu-id="943c4-116">Metodi</span><span class="sxs-lookup"><span data-stu-id="943c4-116">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="943c4-117">Metodi</span><span class="sxs-lookup"><span data-stu-id="943c4-117">Methods</span></span>

<span data-ttu-id="943c4-118">L'interfaccia **IEventSystem2** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="943c4-118">The **IEventSystem2** interface has these methods.</span></span>



| <span data-ttu-id="943c4-119">Metodo</span><span class="sxs-lookup"><span data-stu-id="943c4-119">Method</span></span>                                                                         | <span data-ttu-id="943c4-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="943c4-120">Description</span></span>                                                                       |
|:-------------------------------------------------------------------------------|:----------------------------------------------------------------------------------|
| [<span data-ttu-id="943c4-121">**GetVersion**</span><span class="sxs-lookup"><span data-stu-id="943c4-121">**GetVersion**</span></span>](ieventsystem2-getversion.md)                                 | <span data-ttu-id="943c4-122">Recupera il numero di versione del sistema di eventi.</span><span class="sxs-lookup"><span data-stu-id="943c4-122">Retrieves the version number of the event system.</span></span><br/>                      |
| [<span data-ttu-id="943c4-123">**VerifyTransientSubscribers**</span><span class="sxs-lookup"><span data-stu-id="943c4-123">**VerifyTransientSubscribers**</span></span>](ieventsystem2-verifytransientsubscribers.md) | <span data-ttu-id="943c4-124">Verifica l'esistenza di tutti i sottoscrittori temporanei nell'archivio dati.</span><span class="sxs-lookup"><span data-stu-id="943c4-124">Verifies the existence of all transient subscribers in the data store.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="943c4-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="943c4-125">Requirements</span></span>



| <span data-ttu-id="943c4-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="943c4-126">Requirement</span></span> | <span data-ttu-id="943c4-127">Valore</span><span class="sxs-lookup"><span data-stu-id="943c4-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="943c4-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="943c4-128">Minimum supported client</span></span><br/> | <span data-ttu-id="943c4-129">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="943c4-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="943c4-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="943c4-130">Minimum supported server</span></span><br/> | <span data-ttu-id="943c4-131">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="943c4-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="943c4-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="943c4-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="943c4-133">**IEventSystem**</span><span class="sxs-lookup"><span data-stu-id="943c4-133">**IEventSystem**</span></span>](/windows/desktop/api/EventSys/nn-eventsys-ieventsystem)
</dt> </dl>

 

