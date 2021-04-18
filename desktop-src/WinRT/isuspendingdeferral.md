---
description: Gestisce un'operazione di sospensione dell'app ritardata.
ms.assetid: 9F40659E-9B16-4FC9-B320-5679BB8A8161
title: Interfaccia ISuspendingDeferral (Windows. ApplicationModel. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISuspendingDeferral
api_type:
- COM
api_location:
- Windows.ApplicationModel.h
ms.openlocfilehash: e4f1801960f2d3b9183550e18fb76378bf4f17f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307071"
---
# <a name="isuspendingdeferral-interface"></a><span data-ttu-id="d1e34-103">Interfaccia ISuspendingDeferral</span><span class="sxs-lookup"><span data-stu-id="d1e34-103">ISuspendingDeferral interface</span></span>

<span data-ttu-id="d1e34-104">Gestisce un'operazione di sospensione dell'app ritardata.</span><span class="sxs-lookup"><span data-stu-id="d1e34-104">Manages a delayed app suspending operation.</span></span>

## <a name="members"></a><span data-ttu-id="d1e34-105">Membri</span><span class="sxs-lookup"><span data-stu-id="d1e34-105">Members</span></span>

<span data-ttu-id="d1e34-106">L'interfaccia **ISuspendingDeferral** eredita da [**IInspectable**](/windows/win32/api/inspectable/nn-inspectable-iinspectable).</span><span class="sxs-lookup"><span data-stu-id="d1e34-106">The **ISuspendingDeferral** interface inherits from [**IInspectable**](/windows/win32/api/inspectable/nn-inspectable-iinspectable).</span></span> <span data-ttu-id="d1e34-107">**ISuspendingDeferral** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="d1e34-107">**ISuspendingDeferral** also has these types of members:</span></span>

-   [<span data-ttu-id="d1e34-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="d1e34-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="d1e34-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="d1e34-109">Methods</span></span>

<span data-ttu-id="d1e34-110">L'interfaccia **ISuspendingDeferral** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="d1e34-110">The **ISuspendingDeferral** interface has these methods.</span></span>



| <span data-ttu-id="d1e34-111">Metodo</span><span class="sxs-lookup"><span data-stu-id="d1e34-111">Method</span></span>                                           | <span data-ttu-id="d1e34-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d1e34-112">Description</span></span>                                                                                  |
|:-------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d1e34-113">**Operazione completata**</span><span class="sxs-lookup"><span data-stu-id="d1e34-113">**Complete**</span></span>](isuspendingdeferral-complete.md) | <span data-ttu-id="d1e34-114">Notifica al sistema che l'app ha salvato i dati ed è pronta per essere sospesa.</span><span class="sxs-lookup"><span data-stu-id="d1e34-114">Notifies the system that the app has saved its data and is ready to be suspended.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="d1e34-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d1e34-115">Requirements</span></span>



| <span data-ttu-id="d1e34-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1e34-116">Requirement</span></span> | <span data-ttu-id="d1e34-117">Valore</span><span class="sxs-lookup"><span data-stu-id="d1e34-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1e34-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d1e34-118">Minimum supported client</span></span><br/> | <span data-ttu-id="d1e34-119">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="d1e34-119">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="d1e34-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d1e34-120">Minimum supported server</span></span><br/> | <span data-ttu-id="d1e34-121">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="d1e34-121">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d1e34-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d1e34-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="d1e34-123"><dt>Windows. ApplicationModel. h</dt></span><span class="sxs-lookup"><span data-stu-id="d1e34-123"><dt>Windows.ApplicationModel.h</dt></span></span> </dl>   |
| <span data-ttu-id="d1e34-124">IDL</span><span class="sxs-lookup"><span data-stu-id="d1e34-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d1e34-125"><dt>Windows. ApplicationModel. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d1e34-125"><dt>Windows.ApplicationModel.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1e34-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d1e34-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1e34-127">**IInspectable**</span><span class="sxs-lookup"><span data-stu-id="d1e34-127">**IInspectable**</span></span>](/windows/win32/api/inspectable/nn-inspectable-iinspectable)
</dt> <dt>

[<span data-ttu-id="d1e34-128">**ISuspendingEventArgs**</span><span class="sxs-lookup"><span data-stu-id="d1e34-128">**ISuspendingEventArgs**</span></span>](isuspendingeventargs.md)
</dt> <dt>

[<span data-ttu-id="d1e34-129">**ISuspendingOperation**</span><span class="sxs-lookup"><span data-stu-id="d1e34-129">**ISuspendingOperation**</span></span>](isuspendingoperation.md)
</dt> </dl>

 

 
