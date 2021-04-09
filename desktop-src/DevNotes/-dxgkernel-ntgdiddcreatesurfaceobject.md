---
description: Crea un oggetto Surface in modalità kernel che rappresenta l'oggetto Surface della modalità utente a cui fa riferimento puSurfaceLocal.
ms.assetid: 1b2886a8-279b-4bec-9fb8-b88a68ded25b
title: Funzione NtGdiDdCreateSurfaceObject (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdCreateSurfaceObject
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 5aef9a70897f5a8a46f9c966242d8842c54f9946
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049107"
---
# <a name="ntgdiddcreatesurfaceobject-function"></a><span data-ttu-id="27fcc-103">NtGdiDdCreateSurfaceObject (funzione)</span><span class="sxs-lookup"><span data-stu-id="27fcc-103">NtGdiDdCreateSurfaceObject function</span></span>

<span data-ttu-id="27fcc-104">\[Questa funzione è soggetta a modifiche a ogni revisione del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="27fcc-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="27fcc-105">Usare invece Microsoft DirectDraw e Microsoft Direct3DAPIs; Queste API isolano le applicazioni da tali modifiche del sistema operativo e nascondono molte altre difficoltà legate all'interazione diretta con i driver di visualizzazione.\]</span><span class="sxs-lookup"><span data-stu-id="27fcc-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="27fcc-106">Crea un oggetto Surface in modalità kernel che rappresenta l'oggetto Surface della modalità utente a cui fa riferimento *puSurfaceLocal*.</span><span class="sxs-lookup"><span data-stu-id="27fcc-106">Creates a kernel-mode surface object that represents the user-mode surface object referenced by *puSurfaceLocal*.</span></span>

## <a name="syntax"></a><span data-ttu-id="27fcc-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="27fcc-107">Syntax</span></span>


```C++
HANDLE APIENTRY NtGdiDdCreateSurfaceObject(
  _In_ HANDLE             hDirectDrawLocal,
  _In_ HANDLE             hSurface,
  _In_ PDD_SURFACE_LOCAL  puSurfaceLocal,
  _In_ PDD_SURFACE_MORE   puSurfaceMore,
  _In_ PDD_SURFACE_GLOBAL puSurfaceGlobal,
  _In_ BOOL               bComplete
);
```



## <a name="parameters"></a><span data-ttu-id="27fcc-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="27fcc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27fcc-109">*hDirectDrawLocal* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="27fcc-109">*hDirectDrawLocal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27fcc-110">Handle per l'oggetto DirectDraw in modalità kernel.</span><span class="sxs-lookup"><span data-stu-id="27fcc-110">Handle to the kernel-mode DirectDraw object.</span></span>

</dd> <dt>

<span data-ttu-id="27fcc-111">*hSurface* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="27fcc-111">*hSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27fcc-112">Handle precedente alla stessa superficie.</span><span class="sxs-lookup"><span data-stu-id="27fcc-112">Previous handle to the same surface.</span></span> <span data-ttu-id="27fcc-113">Utilizzato se la superficie viene ricreata dopo un'opzione di modalità.</span><span class="sxs-lookup"><span data-stu-id="27fcc-113">Used if the surface is being re-created after a mode switch.</span></span>

</dd> <dt>

<span data-ttu-id="27fcc-114">*puSurfaceLocal* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="27fcc-114">*puSurfaceLocal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27fcc-115">Puntatore alla struttura [**\_ \_ locale della superficie DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) che rappresenta l'oggetto superficie in modalità utente di DirectDraw a cui associare la memoria allocata.</span><span class="sxs-lookup"><span data-stu-id="27fcc-115">Pointer to the [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structure that represents the DirectDraw user-mode surface object with which to associate the allocated memory.</span></span> <span data-ttu-id="27fcc-116">Per informazioni dettagliate, vedere la documentazione di DDK.</span><span class="sxs-lookup"><span data-stu-id="27fcc-116">See the DDK documentation for details.</span></span>

</dd> <dt>

<span data-ttu-id="27fcc-117">*puSurfaceMore* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="27fcc-117">*puSurfaceMore* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27fcc-118">Puntatore alla [**superficie DD \_ \_ più**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_more) struttura che contiene dati locali aggiuntivi per ogni singolo oggetto Surface.</span><span class="sxs-lookup"><span data-stu-id="27fcc-118">Pointer to the [**DD\_SURFACE\_MORE**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_more) structure that contains additional local data for each individual surface object.</span></span> <span data-ttu-id="27fcc-119">Per informazioni dettagliate, vedere la documentazione di DDK.</span><span class="sxs-lookup"><span data-stu-id="27fcc-119">See the DDK documentation for details.</span></span>

</dd> <dt>

<span data-ttu-id="27fcc-120">*puSurfaceGlobal* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="27fcc-120">*puSurfaceGlobal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27fcc-121">Puntatore alla struttura [**\_ \_ globale della superficie DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_global) che contiene i dati di superficie condivisi a livello globale con più superfici.</span><span class="sxs-lookup"><span data-stu-id="27fcc-121">Pointer to the [**DD\_SURFACE\_GLOBAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_global) structure that contains surface data shared globally with multiple surfaces.</span></span> <span data-ttu-id="27fcc-122">Per informazioni dettagliate, vedere la documentazione di DDK.</span><span class="sxs-lookup"><span data-stu-id="27fcc-122">See the DDK documentation for details.</span></span>

</dd> <dt>

<span data-ttu-id="27fcc-123">*bComplete* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="27fcc-123">*bComplete* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27fcc-124">Flag di completamento oggetto in modalità kernel.</span><span class="sxs-lookup"><span data-stu-id="27fcc-124">Kernel-mode object completion flag.</span></span> <span data-ttu-id="27fcc-125">Può essere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="27fcc-125">Can be one of the following values.</span></span>

<dt>



 <span data-ttu-id="27fcc-126">TRUE</span><span class="sxs-lookup"><span data-stu-id="27fcc-126">(TRUE)</span></span>


</dt> <dd>

<span data-ttu-id="27fcc-127">Completa tutte le operazioni di elaborazione relative alla rappresentazione in modalità kernel.</span><span class="sxs-lookup"><span data-stu-id="27fcc-127">Complete all processing concerning the kernel-mode representation.</span></span>

</dd> <dt>



 <span data-ttu-id="27fcc-128">FALSE</span><span class="sxs-lookup"><span data-stu-id="27fcc-128">(FALSE)</span></span>


</dt> <dd>

<span data-ttu-id="27fcc-129">Creare l'oggetto, ma non impostare dati interni come il puntatore di memoria.</span><span class="sxs-lookup"><span data-stu-id="27fcc-129">Create the object, but do not set up internal data such as the memory pointer.</span></span> <span data-ttu-id="27fcc-130">Gli oggetti creati usando **false** possono essere collegati usando [**NtGdiDdAttachSurface**](-dxgkernel-ntgdiddattachsurface.md) e vengono completati da una chiamata a [**NtGdiDdCreateSurface**](-dxgkernel-ntgdiddcreatesurface.md).</span><span class="sxs-lookup"><span data-stu-id="27fcc-130">Objects created using **FALSE** can be attached using [**NtGdiDdAttachSurface**](-dxgkernel-ntgdiddattachsurface.md) and are completed by a call to [**NtGdiDdCreateSurface**](-dxgkernel-ntgdiddcreatesurface.md).</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27fcc-131">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="27fcc-131">Return value</span></span>

<span data-ttu-id="27fcc-132">Se ha esito positivo, questa funzione restituisce un handle alla rappresentazione di superficie in modalità kernel; in caso contrario, restituisce **null**.</span><span class="sxs-lookup"><span data-stu-id="27fcc-132">If successful, this function returns a handle to the kernel-mode surface representation; otherwise it returns **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="27fcc-133">Commenti</span><span class="sxs-lookup"><span data-stu-id="27fcc-133">Remarks</span></span>

<span data-ttu-id="27fcc-134">Per creare e gestire oggetti dispositivo di grafica, è consigliabile usare le API DirectDraw e [Direct3D](../direct3d10/d3d10-graphics-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="27fcc-134">Applications are advised to use the DirectDraw and [Direct3D](../direct3d10/d3d10-graphics-reference.md) APIs to create and manage graphics device objects.</span></span> <span data-ttu-id="27fcc-135">Questi costrutti astraggono il processo di creazione del dispositivo in modo semplificato e indipendente dal sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="27fcc-135">These constructs abstract the device creation process in a simplified and operating-system-independent way.</span></span>

## <a name="requirements"></a><span data-ttu-id="27fcc-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="27fcc-136">Requirements</span></span>



| <span data-ttu-id="27fcc-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="27fcc-137">Requirement</span></span> | <span data-ttu-id="27fcc-138">Valore</span><span class="sxs-lookup"><span data-stu-id="27fcc-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="27fcc-139">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="27fcc-139">Minimum supported client</span></span><br/> | <span data-ttu-id="27fcc-140">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="27fcc-140">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="27fcc-141">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="27fcc-141">Minimum supported server</span></span><br/> | <span data-ttu-id="27fcc-142">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="27fcc-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="27fcc-143">Intestazione</span><span class="sxs-lookup"><span data-stu-id="27fcc-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="27fcc-144"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="27fcc-144"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27fcc-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="27fcc-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27fcc-146">Supporto client di livello inferiore grafica</span><span class="sxs-lookup"><span data-stu-id="27fcc-146">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> <dt>

[<span data-ttu-id="27fcc-147">**DdCreateSurfaceObject**</span><span class="sxs-lookup"><span data-stu-id="27fcc-147">**DdCreateSurfaceObject**</span></span>](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddcreatesurfaceobject)
</dt> <dt>

[<span data-ttu-id="27fcc-148">**NtGdiDdDeleteSurfaceObject**</span><span class="sxs-lookup"><span data-stu-id="27fcc-148">**NtGdiDdDeleteSurfaceObject**</span></span>](-dxgkernel-ntgdidddeletesurfaceobject.md)
</dt> <dt>

[<span data-ttu-id="27fcc-149">**NtGdiDdAttachSurface**</span><span class="sxs-lookup"><span data-stu-id="27fcc-149">**NtGdiDdAttachSurface**</span></span>](-dxgkernel-ntgdiddattachsurface.md)
</dt> <dt>

[<span data-ttu-id="27fcc-150">**NtGdiDdCreateSurface**</span><span class="sxs-lookup"><span data-stu-id="27fcc-150">**NtGdiDdCreateSurface**</span></span>](-dxgkernel-ntgdiddcreatesurface.md)
</dt> </dl>

 

 
