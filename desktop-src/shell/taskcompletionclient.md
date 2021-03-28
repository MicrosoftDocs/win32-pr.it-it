---
description: Consente il completamento dell'attività.
ms.assetid: 323343D6-FC4A-4A5F-B065-DD72B6077F99
title: Interfaccia TaskCompletionClient
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TaskCompletionClient
api_type:
- COM
api_location:
- ExecModelClient.dll
ms.openlocfilehash: a823dc528ea189c70f44689ab69795eb3a430e67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233188"
---
# <a name="taskcompletionclient-interface"></a><span data-ttu-id="cc588-103">Interfaccia TaskCompletionClient</span><span class="sxs-lookup"><span data-stu-id="cc588-103">TaskCompletionClient interface</span></span>

<span data-ttu-id="cc588-104">Consente il completamento dell'attività.</span><span class="sxs-lookup"><span data-stu-id="cc588-104">Enables task completion.</span></span>

## <a name="members"></a><span data-ttu-id="cc588-105">Membri</span><span class="sxs-lookup"><span data-stu-id="cc588-105">Members</span></span>

<span data-ttu-id="cc588-106">L'interfaccia **TaskCompletionClient** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="cc588-106">The **TaskCompletionClient** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="cc588-107">**TaskCompletionClient** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="cc588-107">**TaskCompletionClient** also has these types of members:</span></span>

-   [<span data-ttu-id="cc588-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="cc588-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="cc588-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="cc588-109">Methods</span></span>

<span data-ttu-id="cc588-110">L'interfaccia **TaskCompletionClient** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="cc588-110">The **TaskCompletionClient** interface has these methods.</span></span>



| <span data-ttu-id="cc588-111">Metodo</span><span class="sxs-lookup"><span data-stu-id="cc588-111">Method</span></span>                                                                    | <span data-ttu-id="cc588-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cc588-112">Description</span></span>                            |
|:--------------------------------------------------------------------------|:---------------------------------------|
| [<span data-ttu-id="cc588-113">**ApplyTaskCompletion**</span><span class="sxs-lookup"><span data-stu-id="cc588-113">**ApplyTaskCompletion**</span></span>](taskcompletionclient-applytaskcompletion.md)   | <span data-ttu-id="cc588-114">Inizia il completamento dell'attività.</span><span class="sxs-lookup"><span data-stu-id="cc588-114">Begins the task completion.</span></span><br/> |
| [<span data-ttu-id="cc588-115">**RevokeTaskCompletion**</span><span class="sxs-lookup"><span data-stu-id="cc588-115">**RevokeTaskCompletion**</span></span>](taskcompletionclient-revoketaskcompletion.md) | <span data-ttu-id="cc588-116">Termina il completamento dell'attività.</span><span class="sxs-lookup"><span data-stu-id="cc588-116">Ends the task completion.</span></span><br/>   |



 

## <a name="remarks"></a><span data-ttu-id="cc588-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="cc588-117">Remarks</span></span>

<span data-ttu-id="cc588-118">Il GUID per questa interfaccia è "E97D552D-9AE9-46AA-9151-D2DA4BBB5E96".</span><span class="sxs-lookup"><span data-stu-id="cc588-118">The GUID for this interface is "E97D552D-9AE9-46AA-9151-D2DA4BBB5E96".</span></span>

<span data-ttu-id="cc588-119">Questa API è deprecata e potrebbe non essere disponibile nelle versioni future di Windows.</span><span class="sxs-lookup"><span data-stu-id="cc588-119">This API is deprecated and may not be available in future versions of Windows.</span></span> <span data-ttu-id="cc588-120">In alternativa, le app devono usare le API nello spazio dei nomi [**Windows. ApplicationModel. ExtendedExecution**](/uwp/api/Windows.ApplicationModel.ExtendedExecution?view=winrt-19041) .</span><span class="sxs-lookup"><span data-stu-id="cc588-120">Apps should use the APIs in the [**Windows.ApplicationModel.ExtendedExecution**](/uwp/api/Windows.ApplicationModel.ExtendedExecution?view=winrt-19041) namespace instead.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc588-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cc588-121">Requirements</span></span>



| <span data-ttu-id="cc588-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="cc588-122">Requirement</span></span> | <span data-ttu-id="cc588-123">Valore</span><span class="sxs-lookup"><span data-stu-id="cc588-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc588-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cc588-124">Minimum supported client</span></span><br/> | <span data-ttu-id="cc588-125">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="cc588-125">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="cc588-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cc588-126">Minimum supported server</span></span><br/> | <span data-ttu-id="cc588-127">\[Solo app desktop Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="cc588-127">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="cc588-128">DLL</span><span class="sxs-lookup"><span data-stu-id="cc588-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cc588-129"><dt>ExecModelClient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cc588-129"><dt>ExecModelClient.dll</dt></span></span> </dl> |



 

 
