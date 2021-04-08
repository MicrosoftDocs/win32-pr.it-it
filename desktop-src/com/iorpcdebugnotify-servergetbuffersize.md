---
title: Metodo IOrpcDebugNotify ServerGetBufferSize
description: Recupera la dimensione del buffer RPC dal debugger lato server.
ms.assetid: 1e9ef194-c85b-4f6d-8b89-1f7ee6941189
keywords:
- Metodo ServerGetBufferSize COM
- Metodo ServerGetBufferSize COM, interfaccia IOrpcDebugNotify
- Interfaccia IOrpcDebugNotify COM, metodo ServerGetBufferSize
topic_type:
- apiref
api_name:
- IOrpcDebugNotify.ServerGetBufferSize
api_location:
- N/A
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d461670cc65f5cfcb433a52529e724a1c54bede
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964951"
---
# <a name="iorpcdebugnotifyservergetbuffersize-method"></a><span data-ttu-id="724d0-106">Metodo IOrpcDebugNotify:: ServerGetBufferSize</span><span class="sxs-lookup"><span data-stu-id="724d0-106">IOrpcDebugNotify::ServerGetBufferSize method</span></span>

<span data-ttu-id="724d0-107">Recupera la dimensione del buffer RPC dal debugger lato server.</span><span class="sxs-lookup"><span data-stu-id="724d0-107">Retrieves the RPC buffer size from the server-side debugger.</span></span>

> [!Note]  
> <span data-ttu-id="724d0-108">Una libreria di importazione contenente la funzione **ServerGetBufferSize** non è inclusa in Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="724d0-108">An import library containing the **ServerGetBufferSize** function is not included in the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="724d0-109">Un'applicazione può usare le funzioni [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) e [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) per recuperare un puntatore a funzione a [**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md) da oleaut.dll e fornire questa funzione tramite l'interfaccia [**IOrpcDebugNotify**](iorpcdebugnotify.md) .</span><span class="sxs-lookup"><span data-stu-id="724d0-109">An application can use the [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) and [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) functions to retrieve a function pointer to [**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md) from oleaut.dll and provide this function via the [**IOrpcDebugNotify**](iorpcdebugnotify.md) interface.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="724d0-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="724d0-110">Syntax</span></span>


```C++
void ServerGetBufferSize(
   ORPC_DBG_ALL *lpOrpcDebugAll
);
```



## <a name="parameters"></a><span data-ttu-id="724d0-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="724d0-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="724d0-112">*lpOrpcDebugAll*</span><span class="sxs-lookup"><span data-stu-id="724d0-112">*lpOrpcDebugAll*</span></span> 
</dt> <dd>

<span data-ttu-id="724d0-113">Puntatore a una struttura [**ORPC \_ dbg \_ All**](orpc-dbg-all.md) che contiene informazioni specifiche della notifica che il sistema RPC com passa al debugger.</span><span class="sxs-lookup"><span data-stu-id="724d0-113">A pointer to a [**ORPC\_DBG\_ALL**](orpc-dbg-all.md) structure that contains notification specific information the COM RPC system passes to the debugger.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="724d0-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="724d0-114">Return value</span></span>

<span data-ttu-id="724d0-115">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="724d0-115">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="724d0-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="724d0-116">Requirements</span></span>



| <span data-ttu-id="724d0-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="724d0-117">Requirement</span></span> | <span data-ttu-id="724d0-118">Valore</span><span class="sxs-lookup"><span data-stu-id="724d0-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="724d0-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="724d0-119">Minimum supported client</span></span><br/> | <span data-ttu-id="724d0-120">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="724d0-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                     |
| <span data-ttu-id="724d0-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="724d0-121">Minimum supported server</span></span><br/> | <span data-ttu-id="724d0-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="724d0-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="724d0-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="724d0-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="724d0-124"><dt>N/D</dt></span><span class="sxs-lookup"><span data-stu-id="724d0-124"><dt>N/A</dt></span></span> </dl> |
| <span data-ttu-id="724d0-125">IDL</span><span class="sxs-lookup"><span data-stu-id="724d0-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="724d0-126"><dt>N/D</dt></span><span class="sxs-lookup"><span data-stu-id="724d0-126"><dt>N/A</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="724d0-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="724d0-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="724d0-128">**\_argomenti init \_ ORPC**</span><span class="sxs-lookup"><span data-stu-id="724d0-128">**ORPC\_INIT\_ARGS**</span></span>](orpc-init-args.md)
</dt> <dt>

[<span data-ttu-id="724d0-129">**DllDebugObjectRPCHook**</span><span class="sxs-lookup"><span data-stu-id="724d0-129">**DllDebugObjectRPCHook**</span></span>](dlldebugobjectrpchook.md)
</dt> <dt>

[<span data-ttu-id="724d0-130">**IOrpcDebugNotify**</span><span class="sxs-lookup"><span data-stu-id="724d0-130">**IOrpcDebugNotify**</span></span>](iorpcdebugnotify.md)
</dt> </dl>

 

