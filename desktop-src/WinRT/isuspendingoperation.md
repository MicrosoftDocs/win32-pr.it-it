---
description: Fornisce informazioni su un'operazione di sospensione dell'app.
ms.assetid: B380AEA2-6486-46CC-AD0A-CF25C144DC01
title: Interfaccia ISuspendingOperation (Windows. ApplicationModel. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISuspendingOperation
api_type:
- COM
api_location:
- Windows.ApplicationModel.h
ms.openlocfilehash: 09a3c37216298fa672cdd676e835454b4e0f4bd2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526221"
---
# <a name="isuspendingoperation-interface"></a><span data-ttu-id="d5d5b-103">Interfaccia ISuspendingOperation</span><span class="sxs-lookup"><span data-stu-id="d5d5b-103">ISuspendingOperation interface</span></span>

<span data-ttu-id="d5d5b-104">Fornisce informazioni su un'operazione di sospensione dell'app.</span><span class="sxs-lookup"><span data-stu-id="d5d5b-104">Provides information about an app suspending operation.</span></span>

## <a name="members"></a><span data-ttu-id="d5d5b-105">Membri</span><span class="sxs-lookup"><span data-stu-id="d5d5b-105">Members</span></span>

<span data-ttu-id="d5d5b-106">L'interfaccia **ISuspendingOperation** eredita da [**IInspectable**](/windows/win32/api/inspectable/nn-inspectable-iinspectable).</span><span class="sxs-lookup"><span data-stu-id="d5d5b-106">The **ISuspendingOperation** interface inherits from [**IInspectable**](/windows/win32/api/inspectable/nn-inspectable-iinspectable).</span></span> <span data-ttu-id="d5d5b-107">**ISuspendingOperation** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="d5d5b-107">**ISuspendingOperation** also has these types of members:</span></span>

-   [<span data-ttu-id="d5d5b-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="d5d5b-108">Methods</span></span>](#methods)
-   [<span data-ttu-id="d5d5b-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d5d5b-109">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="d5d5b-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="d5d5b-110">Methods</span></span>

<span data-ttu-id="d5d5b-111">L'interfaccia **ISuspendingOperation** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="d5d5b-111">The **ISuspendingOperation** interface has these methods.</span></span>



| <span data-ttu-id="d5d5b-112">Metodo</span><span class="sxs-lookup"><span data-stu-id="d5d5b-112">Method</span></span>                                                  | <span data-ttu-id="d5d5b-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d5d5b-113">Description</span></span>                                                       |
|:--------------------------------------------------------|:------------------------------------------------------------------|
| [<span data-ttu-id="d5d5b-114">**GetDeferral**</span><span class="sxs-lookup"><span data-stu-id="d5d5b-114">**GetDeferral**</span></span>](isuspendingoperation-getdeferral.md) | <span data-ttu-id="d5d5b-115">Richiede che l'operazione di sospensione dell'app venga posticipata.</span><span class="sxs-lookup"><span data-stu-id="d5d5b-115">Requests that the app suspending operation be delayed.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="d5d5b-116">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d5d5b-116">Properties</span></span>

<span data-ttu-id="d5d5b-117">L'interfaccia **ISuspendingOperation** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="d5d5b-117">The **ISuspendingOperation** interface has these properties.</span></span>



| <span data-ttu-id="d5d5b-118">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d5d5b-118">Property</span></span>                                                     | <span data-ttu-id="d5d5b-119">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="d5d5b-119">Access type</span></span>           | <span data-ttu-id="d5d5b-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d5d5b-120">Description</span></span>                                                                             |
|:-------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------|
| [<span data-ttu-id="d5d5b-121">**Scadenza**</span><span class="sxs-lookup"><span data-stu-id="d5d5b-121">**Deadline**</span></span>](isuspendingoperation-deadline.md)<br/> | <span data-ttu-id="d5d5b-122">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="d5d5b-122">Read/write</span></span><br/> | <span data-ttu-id="d5d5b-123">Ottiene il tempo rimanente prima che un'operazione di sospensione dell'app ritardata continui.</span><span class="sxs-lookup"><span data-stu-id="d5d5b-123">Gets the time remaining before a delayed app suspending operation continues.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="d5d5b-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d5d5b-124">Requirements</span></span>



| <span data-ttu-id="d5d5b-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5d5b-125">Requirement</span></span> | <span data-ttu-id="d5d5b-126">Valore</span><span class="sxs-lookup"><span data-stu-id="d5d5b-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5d5b-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d5d5b-127">Minimum supported client</span></span><br/> | <span data-ttu-id="d5d5b-128">Windows 8</span><span class="sxs-lookup"><span data-stu-id="d5d5b-128">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="d5d5b-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d5d5b-129">Minimum supported server</span></span><br/> | <span data-ttu-id="d5d5b-130">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d5d5b-130">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="d5d5b-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d5d5b-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="d5d5b-132"><dt>Windows. ApplicationModel. h</dt></span><span class="sxs-lookup"><span data-stu-id="d5d5b-132"><dt>Windows.ApplicationModel.h</dt></span></span> </dl>   |
| <span data-ttu-id="d5d5b-133">IDL</span><span class="sxs-lookup"><span data-stu-id="d5d5b-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d5d5b-134"><dt>Windows. ApplicationModel. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d5d5b-134"><dt>Windows.ApplicationModel.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5d5b-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d5d5b-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5d5b-136">**IInspectable**</span><span class="sxs-lookup"><span data-stu-id="d5d5b-136">**IInspectable**</span></span>](/windows/win32/api/inspectable/nn-inspectable-iinspectable)
</dt> <dt>

[<span data-ttu-id="d5d5b-137">**ISuspendingDeferral**</span><span class="sxs-lookup"><span data-stu-id="d5d5b-137">**ISuspendingDeferral**</span></span>](isuspendingdeferral.md)
</dt> <dt>

[<span data-ttu-id="d5d5b-138">**ISuspendingEventArgs**</span><span class="sxs-lookup"><span data-stu-id="d5d5b-138">**ISuspendingEventArgs**</span></span>](isuspendingeventargs.md)
</dt> </dl>

 

 
