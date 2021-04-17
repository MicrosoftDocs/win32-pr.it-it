---
title: Interfaccia IOrpcDebugNotify
description: Fornisce funzionalità di debug remoto.
ms.assetid: f91987c0-2e4b-4872-8ed6-e208a23baa49
keywords:
- Interfaccia COM IOrpcDebugNotify
- Interfaccia IOrpcDebugNotify COM, descritta
topic_type:
- apiref
api_name:
- IOrpcDebugNotify
api_location:
- N/A
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f4db08daf93997b2a7fa0ed383591cb5d111ac7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519054"
---
# <a name="iorpcdebugnotify-interface"></a><span data-ttu-id="54252-105">Interfaccia IOrpcDebugNotify</span><span class="sxs-lookup"><span data-stu-id="54252-105">IOrpcDebugNotify interface</span></span>

<span data-ttu-id="54252-106">Fornisce funzionalità di debug remoto.</span><span class="sxs-lookup"><span data-stu-id="54252-106">Provides remote debugging functionality.</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="54252-107">Quando implementare</span><span class="sxs-lookup"><span data-stu-id="54252-107">When to implement</span></span>

<span data-ttu-id="54252-108">Implementare questa interfaccia per abilitare il debug remoto tramite RPC.</span><span class="sxs-lookup"><span data-stu-id="54252-108">Implement this interface to enable remote debugging over RPC.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="54252-109">Utilizzo</span><span class="sxs-lookup"><span data-stu-id="54252-109">When to use</span></span>

<span data-ttu-id="54252-110">Questa interfaccia deve essere utilizzata per il debug remoto in-process quando le eccezioni software non devono essere utilizzate per le notifiche del debugger COM.</span><span class="sxs-lookup"><span data-stu-id="54252-110">This interface should be used for in-process remote debugging when software exceptions should not be used for the COM debugger notifications.</span></span> <span data-ttu-id="54252-111">Consente ai debugger in-process di ricevere notifiche tramite chiamate dirette usando questi metodi.</span><span class="sxs-lookup"><span data-stu-id="54252-111">It enables in-process debuggers to be notified by direct calls using these methods.</span></span>

## <a name="members"></a><span data-ttu-id="54252-112">Membri</span><span class="sxs-lookup"><span data-stu-id="54252-112">Members</span></span>

<span data-ttu-id="54252-113">L'interfaccia **IOrpcDebugNotify** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="54252-113">The **IOrpcDebugNotify** interface inherits from the [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="54252-114">**IOrpcDebugNotify** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="54252-114">**IOrpcDebugNotify** also has these types of members:</span></span>

-   [<span data-ttu-id="54252-115">Metodi</span><span class="sxs-lookup"><span data-stu-id="54252-115">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="54252-116">Metodi</span><span class="sxs-lookup"><span data-stu-id="54252-116">Methods</span></span>

<span data-ttu-id="54252-117">L'interfaccia **IOrpcDebugNotify** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="54252-117">The **IOrpcDebugNotify** interface has these methods.</span></span>



| <span data-ttu-id="54252-118">Metodo</span><span class="sxs-lookup"><span data-stu-id="54252-118">Method</span></span>                                                              | <span data-ttu-id="54252-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="54252-119">Description</span></span>                                                                    |
|:--------------------------------------------------------------------|:-------------------------------------------------------------------------------|
| [<span data-ttu-id="54252-120">**ClientFillBuffer**</span><span class="sxs-lookup"><span data-stu-id="54252-120">**ClientFillBuffer**</span></span>](iorpcdebugnotify-clientfillbuffer.md)       | <span data-ttu-id="54252-121">Invia i dati dal debugger client al debugger del server.</span><span class="sxs-lookup"><span data-stu-id="54252-121">Sends data from the client debugger to the server debugger.</span></span><br/>         |
| [<span data-ttu-id="54252-122">**ClientGetBufferSize**</span><span class="sxs-lookup"><span data-stu-id="54252-122">**ClientGetBufferSize**</span></span>](iorpcdebugnotify-clientgetbuffersize.md) | <span data-ttu-id="54252-123">Recupera la dimensione del buffer RPC dal debugger sul lato client.</span><span class="sxs-lookup"><span data-stu-id="54252-123">Retrieves the RPC buffer size from the client-side debugger.</span></span><br/>        |
| [<span data-ttu-id="54252-124">**ClientNotify**</span><span class="sxs-lookup"><span data-stu-id="54252-124">**ClientNotify**</span></span>](iorpcdebugnotify-clientnotify.md)               | <span data-ttu-id="54252-125">Informa il client di una richiesta del debugger in uscita al server.</span><span class="sxs-lookup"><span data-stu-id="54252-125">Informs the client of an outgoing debugger request to the server.</span></span><br/>   |
| [<span data-ttu-id="54252-126">**ServerFillBuffer**</span><span class="sxs-lookup"><span data-stu-id="54252-126">**ServerFillBuffer**</span></span>](iorpcdebugnotify-serverfillbuffer.md)       | <span data-ttu-id="54252-127">Invia i dati dal debugger del server al debugger client.</span><span class="sxs-lookup"><span data-stu-id="54252-127">Sends data from the server debugger to the client debugger.</span></span><br/>         |
| [<span data-ttu-id="54252-128">**ServerGetBufferSize**</span><span class="sxs-lookup"><span data-stu-id="54252-128">**ServerGetBufferSize**</span></span>](iorpcdebugnotify-servergetbuffersize.md) | <span data-ttu-id="54252-129">Recupera la dimensione del buffer RPC dal debugger lato server.</span><span class="sxs-lookup"><span data-stu-id="54252-129">Retrieves the RPC buffer size from the server-side debugger.</span></span><br/>        |
| [<span data-ttu-id="54252-130">**ServerNotify**</span><span class="sxs-lookup"><span data-stu-id="54252-130">**ServerNotify**</span></span>](iorpcdebugnotify-servernotify.md)               | <span data-ttu-id="54252-131">Informa il server di una richiesta del debugger in ingresso dal client.</span><span class="sxs-lookup"><span data-stu-id="54252-131">Informs the server of an incoming debugger request from the client.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="54252-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="54252-132">Remarks</span></span>

<span data-ttu-id="54252-133">Una libreria di importazione contenente l'interfaccia **IOrpcDebugNotify** non è inclusa nel Software Development Kit (SDK) di Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="54252-133">An import library containing the **IOrpcDebugNotify** interface is not included in the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="54252-134">Un'applicazione può usare le funzioni [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) e [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) per recuperare un puntatore a funzione a [**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md) da oleaut.dll e fornire questi metodi tramite l'interfaccia **IOrpcDebugNotify** .</span><span class="sxs-lookup"><span data-stu-id="54252-134">An application can use the [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) and [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) functions to retrieve a function pointer to [**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md) from oleaut.dll and provide these methods via the **IOrpcDebugNotify** interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="54252-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="54252-135">Requirements</span></span>



| <span data-ttu-id="54252-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="54252-136">Requirement</span></span> | <span data-ttu-id="54252-137">Valore</span><span class="sxs-lookup"><span data-stu-id="54252-137">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="54252-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="54252-138">Minimum supported client</span></span><br/> | <span data-ttu-id="54252-139">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="54252-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                     |
| <span data-ttu-id="54252-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="54252-140">Minimum supported server</span></span><br/> | <span data-ttu-id="54252-141">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="54252-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="54252-142">Intestazione</span><span class="sxs-lookup"><span data-stu-id="54252-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="54252-143"><dt>N/D</dt></span><span class="sxs-lookup"><span data-stu-id="54252-143"><dt>N/A</dt></span></span> </dl> |
| <span data-ttu-id="54252-144">IDL</span><span class="sxs-lookup"><span data-stu-id="54252-144">IDL</span></span><br/>                      | <dl> <span data-ttu-id="54252-145"><dt>N/D</dt></span><span class="sxs-lookup"><span data-stu-id="54252-145"><dt>N/A</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54252-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="54252-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54252-147">**IUnknown**</span><span class="sxs-lookup"><span data-stu-id="54252-147">**IUnknown**</span></span>](/windows/desktop/api/Unknwn/nn-unknwn-iunknown)
</dt> <dt>

[<span data-ttu-id="54252-148">**ORPC \_ dbg \_ All**</span><span class="sxs-lookup"><span data-stu-id="54252-148">**ORPC\_DBG\_ALL**</span></span>](orpc-dbg-all.md)
</dt> <dt>

[<span data-ttu-id="54252-149">**\_buffer dbg \_ ORPC**</span><span class="sxs-lookup"><span data-stu-id="54252-149">**ORPC\_DBG\_BUFFER**</span></span>](orpc-dbg-buffer.md)
</dt> <dt>

[<span data-ttu-id="54252-150">**\_argomenti init \_ ORPC**</span><span class="sxs-lookup"><span data-stu-id="54252-150">**ORPC\_INIT\_ARGS**</span></span>](orpc-init-args.md)
</dt> <dt>

[<span data-ttu-id="54252-151">**DllDebugObjectRPCHook**</span><span class="sxs-lookup"><span data-stu-id="54252-151">**DllDebugObjectRPCHook**</span></span>](dlldebugobjectrpchook.md)
</dt> </dl>

 

