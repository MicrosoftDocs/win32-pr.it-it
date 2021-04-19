---
description: Restituisce l'handle dell'API Microsoft DirectX in modalità kernel da usare nelle chiamate successive ai punti di ingresso in modalità kernel che controllano il meccanismo dell'API DirectX.
ms.assetid: c95cb188-305f-4b60-be55-0511b57f0597
title: Funzione NtGdiDdGetDxHandle (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdGetDxHandle
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: f1b304216c518765be73d9f3a3e63d39ec4b37fb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304846"
---
# <a name="ntgdiddgetdxhandle-function"></a><span data-ttu-id="03c29-103">NtGdiDdGetDxHandle (funzione)</span><span class="sxs-lookup"><span data-stu-id="03c29-103">NtGdiDdGetDxHandle function</span></span>

<span data-ttu-id="03c29-104">\[Questa funzione è soggetta a modifiche a ogni revisione del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="03c29-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="03c29-105">Usare invece Microsoft DirectDraw e Microsoft Direct3DAPIs; Queste API isolano le applicazioni da tali modifiche del sistema operativo e nascondono molte altre difficoltà legate all'interazione diretta con i driver di visualizzazione.\]</span><span class="sxs-lookup"><span data-stu-id="03c29-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="03c29-106">Restituisce l'handle dell'API Microsoft DirectX in modalità kernel da usare nelle chiamate successive ai punti di ingresso in modalità kernel che controllano il meccanismo dell'API DirectX.</span><span class="sxs-lookup"><span data-stu-id="03c29-106">Returns the kernel-mode Microsoft DirectX  API handle to use in subsequent calls to the kernel-mode entry points that control the DirectX  API mechanism.</span></span>

## <a name="syntax"></a><span data-ttu-id="03c29-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="03c29-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdGetDxHandle(
  _In_ HANDLE hDirectDraw,
  _In_ HANDLE hSurface,
  _In_ BOOL   bRelease
);
```



## <a name="parameters"></a><span data-ttu-id="03c29-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="03c29-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03c29-109">*hDirectDraw* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="03c29-109">*hDirectDraw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03c29-110">Handle per l'oggetto DirectDraw proprietario della superficie.</span><span class="sxs-lookup"><span data-stu-id="03c29-110">Handle to DirectDraw object owning the surface.</span></span> <span data-ttu-id="03c29-111">Questo parametro è facoltativo e può essere impostato su **null**.</span><span class="sxs-lookup"><span data-stu-id="03c29-111">This parameter is optional and may be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="03c29-112">*hSurface* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="03c29-112">*hSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03c29-113">Handle per la superficie per cui restituire un handle dell'API DirectX in modalità kernel.</span><span class="sxs-lookup"><span data-stu-id="03c29-113">Handle to surface for which to return a kernel-mode DirectX API handle.</span></span> <span data-ttu-id="03c29-114">Questo parametro è facoltativo e può essere impostato su **null**.</span><span class="sxs-lookup"><span data-stu-id="03c29-114">This parameter is optional and may be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="03c29-115">*bRelease* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="03c29-115">*bRelease* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03c29-116">Impostare su **true** se l'interfaccia della modalità kernel dell'API DirectX deve essere rilasciata.</span><span class="sxs-lookup"><span data-stu-id="03c29-116">Set to **TRUE** if the DirectX API kernel mode interface should be released.</span></span> <span data-ttu-id="03c29-117">In caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="03c29-117">Otherwise, **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="03c29-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="03c29-118">Return value</span></span>

<span data-ttu-id="03c29-119">Handle di API DirectX usato nei successivi punti di ingresso del kernel basati sull'API DirectX.</span><span class="sxs-lookup"><span data-stu-id="03c29-119">A DirectX API handle used in subsequent DirectX API-oriented kernel entry points.</span></span>

## <a name="remarks"></a><span data-ttu-id="03c29-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="03c29-120">Remarks</span></span>

<span data-ttu-id="03c29-121">Se vengono specificati sia *hDirectDraw* che *hSurface* , *hSurface* viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="03c29-121">If both *hDirectDraw* and *hSurface* are specified, *hSurface* is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="03c29-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="03c29-122">Requirements</span></span>



| <span data-ttu-id="03c29-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="03c29-123">Requirement</span></span> | <span data-ttu-id="03c29-124">Valore</span><span class="sxs-lookup"><span data-stu-id="03c29-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="03c29-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="03c29-125">Minimum supported client</span></span><br/> | <span data-ttu-id="03c29-126">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="03c29-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="03c29-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="03c29-127">Minimum supported server</span></span><br/> | <span data-ttu-id="03c29-128">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="03c29-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="03c29-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="03c29-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="03c29-130"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="03c29-130"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03c29-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="03c29-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03c29-132">Supporto client di livello inferiore grafica</span><span class="sxs-lookup"><span data-stu-id="03c29-132">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 




