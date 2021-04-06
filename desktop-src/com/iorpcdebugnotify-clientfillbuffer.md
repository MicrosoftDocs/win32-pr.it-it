---
title: Metodo IOrpcDebugNotify ClientFillBuffer
description: Invia i dati dal debugger client al debugger del server.
ms.assetid: d575cf34-34a2-4951-a87e-7835b2c5b7a0
keywords:
- Metodo ClientFillBuffer COM
- Metodo ClientFillBuffer COM, interfaccia IOrpcDebugNotify
- Interfaccia IOrpcDebugNotify COM, Metodo ClientFillBuffer
topic_type:
- apiref
api_name:
- IOrpcDebugNotify.ClientFillBuffer
api_location:
- N/A
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 633f4f0a8a3e135ca60468d24356a3f6e038d062
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743706"
---
# <a name="iorpcdebugnotifyclientfillbuffer-method"></a><span data-ttu-id="f5537-106">Metodo IOrpcDebugNotify:: ClientFillBuffer</span><span class="sxs-lookup"><span data-stu-id="f5537-106">IOrpcDebugNotify::ClientFillBuffer method</span></span>

<span data-ttu-id="f5537-107">Invia i dati dal debugger client al debugger del server.</span><span class="sxs-lookup"><span data-stu-id="f5537-107">Sends data from the client debugger to the server debugger.</span></span>

> [!Note]  
> <span data-ttu-id="f5537-108">Una libreria di importazione contenente la funzione **ClientFillBuffer** non è inclusa in Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="f5537-108">An import library containing the **ClientFillBuffer** function is not included in the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="f5537-109">Un'applicazione può usare le funzioni [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) e [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) per recuperare un puntatore a funzione a [**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md) da oleaut.dll e fornire questa funzione tramite l'interfaccia [**IOrpcDebugNotify**](iorpcdebugnotify.md) .</span><span class="sxs-lookup"><span data-stu-id="f5537-109">An application can use the [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) and [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) functions to retrieve a function pointer to [**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md) from oleaut.dll and provide this function via the [**IOrpcDebugNotify**](iorpcdebugnotify.md) interface.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="f5537-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f5537-110">Syntax</span></span>


```C++
void ClientFillBuffer(
   ORPC_DBG_ALL *lpOrpcDebugAll
);
```



## <a name="parameters"></a><span data-ttu-id="f5537-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="f5537-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5537-112">*lpOrpcDebugAll*</span><span class="sxs-lookup"><span data-stu-id="f5537-112">*lpOrpcDebugAll*</span></span> 
</dt> <dd>

<span data-ttu-id="f5537-113">Puntatore a una struttura [**ORPC \_ dbg \_ All**](orpc-dbg-all.md) che contiene informazioni specifiche della notifica che il sistema RPC com passa al debugger.</span><span class="sxs-lookup"><span data-stu-id="f5537-113">A pointer to a [**ORPC\_DBG\_ALL**](orpc-dbg-all.md) structure that contains notification specific information the COM RPC system passes to the debugger.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5537-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f5537-114">Return value</span></span>

<span data-ttu-id="f5537-115">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="f5537-115">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5537-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f5537-116">Requirements</span></span>



| <span data-ttu-id="f5537-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5537-117">Requirement</span></span> | <span data-ttu-id="f5537-118">Valore</span><span class="sxs-lookup"><span data-stu-id="f5537-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="f5537-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f5537-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f5537-120">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f5537-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                     |
| <span data-ttu-id="f5537-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f5537-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f5537-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f5537-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="f5537-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f5537-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="f5537-124"><dt>N/D</dt></span><span class="sxs-lookup"><span data-stu-id="f5537-124"><dt>N/A</dt></span></span> </dl> |
| <span data-ttu-id="f5537-125">IDL</span><span class="sxs-lookup"><span data-stu-id="f5537-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f5537-126"><dt>N/D</dt></span><span class="sxs-lookup"><span data-stu-id="f5537-126"><dt>N/A</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5537-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f5537-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5537-128">**DllDebugObjectRPCHook**</span><span class="sxs-lookup"><span data-stu-id="f5537-128">**DllDebugObjectRPCHook**</span></span>](dlldebugobjectrpchook.md)
</dt> <dt>

[<span data-ttu-id="f5537-129">**IOrpcDebugNotify**</span><span class="sxs-lookup"><span data-stu-id="f5537-129">**IOrpcDebugNotify**</span></span>](iorpcdebugnotify.md)
</dt> </dl>

 

