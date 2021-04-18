---
description: Fornisce i dati per un evento di sospensione dell'app.
ms.assetid: 2590AFAA-679C-49F1-804F-D429BB971727
title: Interfaccia ISuspendingEventArgs (Windows. ApplicationModel. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISuspendingEventArgs
api_type:
- COM
api_location:
- Windows.ApplicationModel.h
ms.openlocfilehash: 687ecbb056a057338091b21a862816985ed0186a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307070"
---
# <a name="isuspendingeventargs-interface"></a><span data-ttu-id="2fba4-103">Interfaccia ISuspendingEventArgs</span><span class="sxs-lookup"><span data-stu-id="2fba4-103">ISuspendingEventArgs interface</span></span>

<span data-ttu-id="2fba4-104">Fornisce i dati per un evento di sospensione dell'app.</span><span class="sxs-lookup"><span data-stu-id="2fba4-104">Provides data for an app suspending event.</span></span>

## <a name="members"></a><span data-ttu-id="2fba4-105">Membri</span><span class="sxs-lookup"><span data-stu-id="2fba4-105">Members</span></span>

<span data-ttu-id="2fba4-106">L'interfaccia **ISuspendingEventArgs** eredita da [**IInspectable**](/windows/win32/api/inspectable/nn-inspectable-iinspectable).</span><span class="sxs-lookup"><span data-stu-id="2fba4-106">The **ISuspendingEventArgs** interface inherits from [**IInspectable**](/windows/win32/api/inspectable/nn-inspectable-iinspectable).</span></span> <span data-ttu-id="2fba4-107">**ISuspendingEventArgs** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="2fba4-107">**ISuspendingEventArgs** also has these types of members:</span></span>

-   [<span data-ttu-id="2fba4-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2fba4-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2fba4-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2fba4-109">Properties</span></span>

<span data-ttu-id="2fba4-110">L'interfaccia **ISuspendingEventArgs** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="2fba4-110">The **ISuspendingEventArgs** interface has these properties.</span></span>



| <span data-ttu-id="2fba4-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2fba4-111">Property</span></span>                                                                           | <span data-ttu-id="2fba4-112">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="2fba4-112">Access type</span></span>           | <span data-ttu-id="2fba4-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2fba4-113">Description</span></span>                                   |
|:-----------------------------------------------------------------------------------|:----------------------|:----------------------------------------------|
| [<span data-ttu-id="2fba4-114">**SuspendingOperation**</span><span class="sxs-lookup"><span data-stu-id="2fba4-114">**SuspendingOperation**</span></span>](isuspendingeventargs-suspendingoperation.md)<br/> | <span data-ttu-id="2fba4-115">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="2fba4-115">Read/write</span></span><br/> | <span data-ttu-id="2fba4-116">Ottiene l'operazione di sospensione dell'app.</span><span class="sxs-lookup"><span data-stu-id="2fba4-116">Gets the app suspending operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2fba4-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="2fba4-117">Remarks</span></span>

<span data-ttu-id="2fba4-118">È possibile accedere a questo oggetto quando si implementano i gestori eventi come [**SuspendingEventHandler**](/uwp/api/windows.ui.webui.suspendingeventhandler?view=winrt-19041), [**SuspendingEventHandler**](/uwp/api/windows.ui.xaml.suspendingeventhandler?view=winrt-19041)e si [**aggiunge la \_ sospensione**](/previous-versions//hh438376(v=vs.85)) per rispondere agli eventi di sospensione dell'app.</span><span class="sxs-lookup"><span data-stu-id="2fba4-118">This object is accessed when you implement event handlers like [**SuspendingEventHandler**](/uwp/api/windows.ui.webui.suspendingeventhandler?view=winrt-19041), [**SuspendingEventHandler**](/uwp/api/windows.ui.xaml.suspendingeventhandler?view=winrt-19041), and [**add\_Suspending**](/previous-versions//hh438376(v=vs.85)) to respond to app suspending events.</span></span>

## <a name="requirements"></a><span data-ttu-id="2fba4-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2fba4-119">Requirements</span></span>



| <span data-ttu-id="2fba4-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="2fba4-120">Requirement</span></span> | <span data-ttu-id="2fba4-121">Valore</span><span class="sxs-lookup"><span data-stu-id="2fba4-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2fba4-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2fba4-122">Minimum supported client</span></span><br/> | <span data-ttu-id="2fba4-123">Windows 8</span><span class="sxs-lookup"><span data-stu-id="2fba4-123">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="2fba4-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2fba4-124">Minimum supported server</span></span><br/> | <span data-ttu-id="2fba4-125">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2fba4-125">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="2fba4-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2fba4-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="2fba4-127"><dt>Windows. ApplicationModel. h</dt></span><span class="sxs-lookup"><span data-stu-id="2fba4-127"><dt>Windows.ApplicationModel.h</dt></span></span> </dl>   |
| <span data-ttu-id="2fba4-128">IDL</span><span class="sxs-lookup"><span data-stu-id="2fba4-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2fba4-129"><dt>Windows. ApplicationModel. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2fba4-129"><dt>Windows.ApplicationModel.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2fba4-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2fba4-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2fba4-131">**IInspectable**</span><span class="sxs-lookup"><span data-stu-id="2fba4-131">**IInspectable**</span></span>](/windows/win32/api/inspectable/nn-inspectable-iinspectable)
</dt> <dt>

[<span data-ttu-id="2fba4-132">**ISuspendingOperation**</span><span class="sxs-lookup"><span data-stu-id="2fba4-132">**ISuspendingOperation**</span></span>](isuspendingoperation.md)
</dt> <dt>

[<span data-ttu-id="2fba4-133">**ISuspendingDeferral**</span><span class="sxs-lookup"><span data-stu-id="2fba4-133">**ISuspendingDeferral**</span></span>](isuspendingdeferral.md)
</dt> </dl>

 

 
