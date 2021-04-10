---
description: Crea un contesto di dispositivo (DC) per la superficie specificata.
ms.assetid: c2eaaed6-db19-4dab-ac12-6b4e7eeb58e4
title: Funzione NtGdiDdGetDC (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdGetDC
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 4f930334f0712107d5651a22b35d6917c7977011
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126753"
---
# <a name="ntgdiddgetdc-function"></a><span data-ttu-id="375ff-103">NtGdiDdGetDC (funzione)</span><span class="sxs-lookup"><span data-stu-id="375ff-103">NtGdiDdGetDC function</span></span>

<span data-ttu-id="375ff-104">\[Questa funzione è soggetta a modifiche a ogni revisione del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="375ff-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="375ff-105">Usare invece Microsoft DirectDraw e Microsoft Direct3DAPIs; Queste API isolano le applicazioni da tali modifiche del sistema operativo e nascondono molte altre difficoltà legate all'interazione diretta con i driver di visualizzazione.\]</span><span class="sxs-lookup"><span data-stu-id="375ff-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="375ff-106">Crea un contesto di dispositivo (DC) per la superficie specificata.</span><span class="sxs-lookup"><span data-stu-id="375ff-106">Creates a device context (DC) for the specified surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="375ff-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="375ff-107">Syntax</span></span>


```C++
HDC APIENTRY NtGdiDdGetDC(
  _In_ HANDLE       hSurface,
  _In_ PALETTEENTRY *puColorTable
);
```



## <a name="parameters"></a><span data-ttu-id="375ff-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="375ff-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="375ff-109">*hSurface* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="375ff-109">*hSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="375ff-110">Handle per una superficie DirectDraw in modalità kernel restituita in precedenza da [**NtGdiDdCreateSurface**](-dxgkernel-ntgdiddcreatesurface.md) o [**NtGdiDdCreateSurfaceObject**](-dxgkernel-ntgdiddcreatesurfaceobject.md).</span><span class="sxs-lookup"><span data-stu-id="375ff-110">Handle to a kernel-mode DirectDraw surface previously returned by [**NtGdiDdCreateSurface**](-dxgkernel-ntgdiddcreatesurface.md) or [**NtGdiDdCreateSurfaceObject**](-dxgkernel-ntgdiddcreatesurfaceobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="375ff-111">*puColorTable* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="375ff-111">*puColorTable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="375ff-112">Puntatore a una tabella dei colori di override per il controller di dominio restituito.</span><span class="sxs-lookup"><span data-stu-id="375ff-112">Pointer to an override color table for the returned DC.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="375ff-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="375ff-113">Return value</span></span>

<span data-ttu-id="375ff-114">Se ha esito positivo, la funzione restituisce un **HDC** valido. in caso contrario, restituisce **null**.</span><span class="sxs-lookup"><span data-stu-id="375ff-114">If successful, this function returns a valid **HDC**; otherwise it returns **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="375ff-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="375ff-115">Remarks</span></span>

<span data-ttu-id="375ff-116">È consentito un solo controller di dominio per superficie in un determinato momento.</span><span class="sxs-lookup"><span data-stu-id="375ff-116">Only one DC is allowed per surface at any given time.</span></span> <span data-ttu-id="375ff-117">Le chiamate successive a **NtGdiDdGetDC** avranno esito negativo finché non verrà rilasciato il controller di dominio precedente.</span><span class="sxs-lookup"><span data-stu-id="375ff-117">Subsequent calls to **NtGdiDdGetDC** will fail until the previous DC is released.</span></span>

<span data-ttu-id="375ff-118">Si consiglia alle applicazioni di chiamare [IDirectDrawSurface7:: GetDC](/windows/win32/api/ddraw/nf-ddraw-idirectdrawsurface7-getdc) , che fornisce la stessa funzionalità in modo indipendente dal sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="375ff-118">Applications are advised to call [IDirectDrawSurface7::GetDC](/windows/win32/api/ddraw/nf-ddraw-idirectdrawsurface7-getdc) instead, which provides the same functionality in a manner independent of the operating system.</span></span>

## <a name="requirements"></a><span data-ttu-id="375ff-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="375ff-119">Requirements</span></span>



| <span data-ttu-id="375ff-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="375ff-120">Requirement</span></span> | <span data-ttu-id="375ff-121">Valore</span><span class="sxs-lookup"><span data-stu-id="375ff-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="375ff-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="375ff-122">Minimum supported client</span></span><br/> | <span data-ttu-id="375ff-123">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="375ff-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="375ff-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="375ff-124">Minimum supported server</span></span><br/> | <span data-ttu-id="375ff-125">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="375ff-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="375ff-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="375ff-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="375ff-127"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="375ff-127"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="375ff-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="375ff-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="375ff-129">Supporto client di livello inferiore grafica</span><span class="sxs-lookup"><span data-stu-id="375ff-129">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> <dt>

[<span data-ttu-id="375ff-130">**DdGetDC**</span><span class="sxs-lookup"><span data-stu-id="375ff-130">**DdGetDC**</span></span>](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddgetdc)
</dt> </dl>

 

 
