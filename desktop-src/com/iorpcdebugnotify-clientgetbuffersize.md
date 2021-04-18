---
title: Metodo IOrpcDebugNotify ClientGetBufferSize
description: Recupera la dimensione del buffer RPC dal debugger sul lato client.
ms.assetid: 05475156-1508-4eb2-82a6-bb1701839fbd
keywords:
- Metodo ClientGetBufferSize COM
- Metodo ClientGetBufferSize COM, interfaccia IOrpcDebugNotify
- Interfaccia IOrpcDebugNotify COM, metodo ClientGetBufferSize
topic_type:
- apiref
api_name:
- IOrpcDebugNotify.ClientGetBufferSize
api_location:
- N/A
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50bd925b9c518c78ca37aa8219a00965f398c415
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302662"
---
# <a name="iorpcdebugnotifyclientgetbuffersize-method"></a><span data-ttu-id="86a92-106">Metodo IOrpcDebugNotify:: ClientGetBufferSize</span><span class="sxs-lookup"><span data-stu-id="86a92-106">IOrpcDebugNotify::ClientGetBufferSize method</span></span>

<span data-ttu-id="86a92-107">Recupera la dimensione del buffer RPC dal debugger sul lato client.</span><span class="sxs-lookup"><span data-stu-id="86a92-107">Retrieves the RPC buffer size from the client-side debugger.</span></span>

> [!Note]  
> <span data-ttu-id="86a92-108">Una libreria di importazione contenente la funzione **ClientGetBufferSize** non è inclusa in Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="86a92-108">An import library containing the **ClientGetBufferSize** function is not included in the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="86a92-109">Un'applicazione può usare le funzioni [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) e [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) per recuperare un puntatore a funzione a [**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md) da oleaut.dll e fornire questa funzione tramite l'interfaccia [**IOrpcDebugNotify**](iorpcdebugnotify.md) .</span><span class="sxs-lookup"><span data-stu-id="86a92-109">An application can use the [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) and [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) functions to retrieve a function pointer to [**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md) from oleaut.dll and provide this function via the [**IOrpcDebugNotify**](iorpcdebugnotify.md) interface.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="86a92-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="86a92-110">Syntax</span></span>


```C++
void ClientGetBufferSize(
   ORPC_DBG_ALL *lpOrpcDebugAll
);
```



## <a name="parameters"></a><span data-ttu-id="86a92-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="86a92-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86a92-112">*lpOrpcDebugAll*</span><span class="sxs-lookup"><span data-stu-id="86a92-112">*lpOrpcDebugAll*</span></span> 
</dt> <dd>

<span data-ttu-id="86a92-113">Puntatore a una struttura [**ORPC \_ dbg \_ All**](orpc-dbg-all.md) che contiene informazioni specifiche della notifica che il sistema RPC com passa al debugger.</span><span class="sxs-lookup"><span data-stu-id="86a92-113">A pointer to a [**ORPC\_DBG\_ALL**](orpc-dbg-all.md) structure that contains notification specific information the COM RPC system passes to the debugger.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86a92-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="86a92-114">Return value</span></span>

<span data-ttu-id="86a92-115">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="86a92-115">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="86a92-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="86a92-116">Requirements</span></span>



| <span data-ttu-id="86a92-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="86a92-117">Requirement</span></span> | <span data-ttu-id="86a92-118">Valore</span><span class="sxs-lookup"><span data-stu-id="86a92-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="86a92-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="86a92-119">Minimum supported client</span></span><br/> | <span data-ttu-id="86a92-120">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="86a92-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                     |
| <span data-ttu-id="86a92-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="86a92-121">Minimum supported server</span></span><br/> | <span data-ttu-id="86a92-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="86a92-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="86a92-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="86a92-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="86a92-124"><dt>N/D</dt></span><span class="sxs-lookup"><span data-stu-id="86a92-124"><dt>N/A</dt></span></span> </dl> |
| <span data-ttu-id="86a92-125">IDL</span><span class="sxs-lookup"><span data-stu-id="86a92-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="86a92-126"><dt>N/D</dt></span><span class="sxs-lookup"><span data-stu-id="86a92-126"><dt>N/A</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86a92-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="86a92-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86a92-128">**\_argomenti init \_ ORPC**</span><span class="sxs-lookup"><span data-stu-id="86a92-128">**ORPC\_INIT\_ARGS**</span></span>](orpc-init-args.md)
</dt> <dt>

[<span data-ttu-id="86a92-129">**DllDebugObjectRPCHook**</span><span class="sxs-lookup"><span data-stu-id="86a92-129">**DllDebugObjectRPCHook**</span></span>](dlldebugobjectrpchook.md)
</dt> <dt>

[<span data-ttu-id="86a92-130">**IOrpcDebugNotify**</span><span class="sxs-lookup"><span data-stu-id="86a92-130">**IOrpcDebugNotify**</span></span>](iorpcdebugnotify.md)
</dt> </dl>

 

