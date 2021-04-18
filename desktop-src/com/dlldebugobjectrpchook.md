---
title: DllDebugObjectRPCHook (funzione)
description: Esportato da DLL COM per consentire il debug remoto.
ms.assetid: a0f8bf12-0889-452d-84d0-255c5c143bc1
keywords:
- DllDebugObjectRPCHook funzione COM
topic_type:
- apiref
api_name:
- DllDebugObjectRPCHook
api_location:
- ole32.dll
- API-MS-Win-Core-Com-private-l1-1-0.dll
- ComBase.dll
- API-MS-Win-Core-COM-Private-l1-1-1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62fffe6cc2d9ca650442d0a1c3fea2048fc6c84b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302591"
---
# <a name="dlldebugobjectrpchook-function"></a><span data-ttu-id="00a87-104">DllDebugObjectRPCHook (funzione)</span><span class="sxs-lookup"><span data-stu-id="00a87-104">DllDebugObjectRPCHook function</span></span>

<span data-ttu-id="00a87-105">Esportato da DLL COM per consentire il debug remoto.</span><span class="sxs-lookup"><span data-stu-id="00a87-105">Exported by COM DLLs to enable remote debugging.</span></span>

## <a name="syntax"></a><span data-ttu-id="00a87-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="00a87-106">Syntax</span></span>


```C++
BOOL WINAPI DllDebugObjectRPCHook(
   BOOL             fTrace,
   LPORPC_INIT_ARGS lpOrpcInitArgs
);
```



## <a name="parameters"></a><span data-ttu-id="00a87-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="00a87-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00a87-108">*fTrace*</span><span class="sxs-lookup"><span data-stu-id="00a87-108">*fTrace*</span></span> 
</dt> <dd>

<span data-ttu-id="00a87-109">Se **true**, il debug remoto è abilitato.</span><span class="sxs-lookup"><span data-stu-id="00a87-109">If **TRUE**, remote debugging is enabled.</span></span> <span data-ttu-id="00a87-110">Se **false**, il debug remoto non è abilitato.</span><span class="sxs-lookup"><span data-stu-id="00a87-110">If **FALSE**, remote debugging is not enabled.</span></span>

</dd> <dt>

<span data-ttu-id="00a87-111">*lpOrpcInitArgs*</span><span class="sxs-lookup"><span data-stu-id="00a87-111">*lpOrpcInitArgs*</span></span> 
</dt> <dd>

<span data-ttu-id="00a87-112">Puntatore a una struttura [**ORPC \_ init \_ arguments**](orpc-init-args.md) .</span><span class="sxs-lookup"><span data-stu-id="00a87-112">A pointer to an [**ORPC\_INIT\_ARGS**](orpc-init-args.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00a87-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="00a87-113">Return value</span></span>

<span data-ttu-id="00a87-114">**True** se ha esito positivo, **false** in caso contrario</span><span class="sxs-lookup"><span data-stu-id="00a87-114">**TRUE** if successful, **FALSE** otherwise</span></span>

## <a name="requirements"></a><span data-ttu-id="00a87-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="00a87-115">Requirements</span></span>



| <span data-ttu-id="00a87-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="00a87-116">Requirement</span></span> | <span data-ttu-id="00a87-117">Valore</span><span class="sxs-lookup"><span data-stu-id="00a87-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="00a87-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="00a87-118">Minimum supported client</span></span><br/> | <span data-ttu-id="00a87-119">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="00a87-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="00a87-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="00a87-120">Minimum supported server</span></span><br/> | <span data-ttu-id="00a87-121">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="00a87-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="00a87-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="00a87-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="00a87-123"><dt>N/D</dt></span><span class="sxs-lookup"><span data-stu-id="00a87-123"><dt>N/A</dt></span></span> </dl>       |
| <span data-ttu-id="00a87-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="00a87-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="00a87-125"><dt>Ole32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="00a87-125"><dt>Ole32.lib</dt></span></span> </dl> |
| <span data-ttu-id="00a87-126">DLL</span><span class="sxs-lookup"><span data-stu-id="00a87-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="00a87-127"><dt>Ole32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="00a87-127"><dt>Ole32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00a87-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="00a87-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00a87-129">**ORPC \_ dbg \_ All**</span><span class="sxs-lookup"><span data-stu-id="00a87-129">**ORPC\_DBG\_ALL**</span></span>](orpc-dbg-all.md)
</dt> <dt>

[<span data-ttu-id="00a87-130">**\_buffer dbg \_ ORPC**</span><span class="sxs-lookup"><span data-stu-id="00a87-130">**ORPC\_DBG\_BUFFER**</span></span>](orpc-dbg-buffer.md)
</dt> <dt>

[<span data-ttu-id="00a87-131">**\_argomenti init \_ ORPC**</span><span class="sxs-lookup"><span data-stu-id="00a87-131">**ORPC\_INIT\_ARGS**</span></span>](orpc-init-args.md)
</dt> <dt>

[<span data-ttu-id="00a87-132">**IOrpcDebugNotify**</span><span class="sxs-lookup"><span data-stu-id="00a87-132">**IOrpcDebugNotify**</span></span>](iorpcdebugnotify.md)
</dt> </dl>

 

 





