---
title: Metodo IOrpcDebugNotify ServerNotify
description: Informa il server di una richiesta del debugger in ingresso dal client.
ms.assetid: 6c868b9e-f25b-4d27-80ff-697d0c005b8d
keywords:
- Metodo ServerNotify COM
- Metodo ServerNotify COM, interfaccia IOrpcDebugNotify
- Interfaccia IOrpcDebugNotify COM, metodo ServerNotify
topic_type:
- apiref
api_name:
- IOrpcDebugNotify.ServerNotify
api_location:
- N/A
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d6dab7cf68b305e83212045851a88e1cdecdde9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964901"
---
# <a name="iorpcdebugnotifyservernotify-method"></a><span data-ttu-id="d0605-106">Metodo IOrpcDebugNotify:: ServerNotify</span><span class="sxs-lookup"><span data-stu-id="d0605-106">IOrpcDebugNotify::ServerNotify method</span></span>

<span data-ttu-id="d0605-107">Informa il server di una richiesta del debugger in ingresso dal client.</span><span class="sxs-lookup"><span data-stu-id="d0605-107">Informs the server of an incoming debugger request from the client.</span></span>

> [!Note]  
> <span data-ttu-id="d0605-108">Una libreria di importazione contenente la funzione **ServerNotify** non è inclusa in Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="d0605-108">An import library containing the **ServerNotify** function is not included in the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="d0605-109">Un'applicazione può usare le funzioni [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) e [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) per recuperare un puntatore a funzione a [**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md) da oleaut.dll e fornire questa funzione tramite l'interfaccia [**IOrpcDebugNotify**](iorpcdebugnotify.md) .</span><span class="sxs-lookup"><span data-stu-id="d0605-109">An application can use the [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) and [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) functions to retrieve a function pointer to [**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md) from oleaut.dll and provide this function via the [**IOrpcDebugNotify**](iorpcdebugnotify.md) interface.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="d0605-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d0605-110">Syntax</span></span>


```C++
void ServerNotify(
   ORPC_DBG_ALL *lpOrpcDebugAll
);
```



## <a name="parameters"></a><span data-ttu-id="d0605-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="d0605-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0605-112">*lpOrpcDebugAll*</span><span class="sxs-lookup"><span data-stu-id="d0605-112">*lpOrpcDebugAll*</span></span> 
</dt> <dd>

<span data-ttu-id="d0605-113">Puntatore a una struttura [**ORPC \_ dbg \_ All**](orpc-dbg-all.md) che contiene informazioni specifiche della notifica che il sistema RPC com passa al debugger.</span><span class="sxs-lookup"><span data-stu-id="d0605-113">A pointer to a [**ORPC\_DBG\_ALL**](orpc-dbg-all.md) structure that contains notification specific information the COM RPC system passes to the debugger.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0605-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d0605-114">Return value</span></span>

<span data-ttu-id="d0605-115">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="d0605-115">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0605-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d0605-116">Requirements</span></span>



| <span data-ttu-id="d0605-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0605-117">Requirement</span></span> | <span data-ttu-id="d0605-118">Valore</span><span class="sxs-lookup"><span data-stu-id="d0605-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="d0605-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d0605-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d0605-120">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d0605-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                     |
| <span data-ttu-id="d0605-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d0605-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d0605-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d0605-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="d0605-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d0605-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="d0605-124"><dt>N/D</dt></span><span class="sxs-lookup"><span data-stu-id="d0605-124"><dt>N/A</dt></span></span> </dl> |
| <span data-ttu-id="d0605-125">IDL</span><span class="sxs-lookup"><span data-stu-id="d0605-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d0605-126"><dt>N/D</dt></span><span class="sxs-lookup"><span data-stu-id="d0605-126"><dt>N/A</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0605-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d0605-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0605-128">**\_argomenti init \_ ORPC**</span><span class="sxs-lookup"><span data-stu-id="d0605-128">**ORPC\_INIT\_ARGS**</span></span>](orpc-init-args.md)
</dt> <dt>

[<span data-ttu-id="d0605-129">**DllDebugObjectRPCHook**</span><span class="sxs-lookup"><span data-stu-id="d0605-129">**DllDebugObjectRPCHook**</span></span>](dlldebugobjectrpchook.md)
</dt> <dt>

[<span data-ttu-id="d0605-130">**IOrpcDebugNotify**</span><span class="sxs-lookup"><span data-stu-id="d0605-130">**IOrpcDebugNotify**</span></span>](iorpcdebugnotify.md)
</dt> </dl>

 

