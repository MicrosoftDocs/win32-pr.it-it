---
description: Rappresenta il metodo chiamato al completamento di un'azione asincrona.
ms.assetid: B410E7C1-B108-4204-9AD1-663F7E05BBC3
title: Interfaccia AsyncActionCompletedHandler
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AsyncActionCompletedHandler
api_type:
- COM
api_location:
- Windows.Foundation.idl
ms.openlocfilehash: 639f5c39d0d9e4086009fd08bd0204f9f5f25060
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307085"
---
# <a name="asyncactioncompletedhandler-interface"></a><span data-ttu-id="5725d-103">Interfaccia AsyncActionCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="5725d-103">AsyncActionCompletedHandler interface</span></span>

<span data-ttu-id="5725d-104">Rappresenta il metodo chiamato al completamento di un'azione asincrona.</span><span class="sxs-lookup"><span data-stu-id="5725d-104">Represents the method that is called when an asynchronous action completes.</span></span>

## <a name="members"></a><span data-ttu-id="5725d-105">Membri</span><span class="sxs-lookup"><span data-stu-id="5725d-105">Members</span></span>

<span data-ttu-id="5725d-106">L'interfaccia **asyncActionCompletedHandler** eredita da [**IAsyncInfo**](/windows/win32/api/asyncinfo/nn-asyncinfo-iasyncinfo).</span><span class="sxs-lookup"><span data-stu-id="5725d-106">The **AsyncActionCompletedHandler** interface inherits from [**IAsyncInfo**](/windows/win32/api/asyncinfo/nn-asyncinfo-iasyncinfo).</span></span> <span data-ttu-id="5725d-107">**AsyncActionCompletedHandler** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="5725d-107">**AsyncActionCompletedHandler** also has these types of members:</span></span>

-   [<span data-ttu-id="5725d-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="5725d-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="5725d-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="5725d-109">Methods</span></span>

<span data-ttu-id="5725d-110">L'interfaccia **asyncActionCompletedHandler** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="5725d-110">The **AsyncActionCompletedHandler** interface has these methods.</span></span>



| <span data-ttu-id="5725d-111">Metodo</span><span class="sxs-lookup"><span data-stu-id="5725d-111">Method</span></span>                                               | <span data-ttu-id="5725d-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5725d-112">Description</span></span>                                                                                    |
|:-----------------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5725d-113">**Richiamare**</span><span class="sxs-lookup"><span data-stu-id="5725d-113">**Invoke**</span></span>](asyncactioncompletedhandler-invoke.md) | <span data-ttu-id="5725d-114">Richiama il metodo che viene chiamato quando l'azione asincrona specificata viene completata.</span><span class="sxs-lookup"><span data-stu-id="5725d-114">Invokes the method that is called when the specified asynchronous action completes.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5725d-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="5725d-115">Remarks</span></span>

<span data-ttu-id="5725d-116">Assegnare un **asyncActionCompletedHandler** a un [**IAsyncAction**](/windows/win32/api/windows.foundation/nn-windows-foundation-iasyncaction) per ricevere una notifica al completamento dell'azione asincrona.</span><span class="sxs-lookup"><span data-stu-id="5725d-116">Assign an **AsyncActionCompletedHandler** to an [**IAsyncAction**](/windows/win32/api/windows.foundation/nn-windows-foundation-iasyncaction) to receive a notification when the asynchronous action completes.</span></span>

## <a name="requirements"></a><span data-ttu-id="5725d-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5725d-117">Requirements</span></span>



| <span data-ttu-id="5725d-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="5725d-118">Requirement</span></span> | <span data-ttu-id="5725d-119">Valore</span><span class="sxs-lookup"><span data-stu-id="5725d-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5725d-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5725d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="5725d-121">Windows 8</span><span class="sxs-lookup"><span data-stu-id="5725d-121">Windows 8</span></span><br/>                                                                              |
| <span data-ttu-id="5725d-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5725d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="5725d-123">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5725d-123">Windows Server 2012</span></span><br/>                                                                    |
| <span data-ttu-id="5725d-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5725d-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="5725d-125"><dt>Windows. Foundation. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5725d-125"><dt>Windows.Foundation.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5725d-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5725d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5725d-127">**IAsyncInfo**</span><span class="sxs-lookup"><span data-stu-id="5725d-127">**IAsyncInfo**</span></span>](/windows/win32/api/asyncinfo/nn-asyncinfo-iasyncinfo)
</dt> </dl>

 

