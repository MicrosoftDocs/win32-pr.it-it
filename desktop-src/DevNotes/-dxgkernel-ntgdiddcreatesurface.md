---
description: "Funzione NtGdiDdCreateSurface: collega una superficie a un'altra superficie."
ms.assetid: 4fd757c7-9e32-4737-b666-3226f6cf29fa
title: Funzione NtGdiDdCreateSurface (Ntgdi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdCreateSurface
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: bf8e13cff80ddea4e102c045c174565e7e835274
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085779"
---
# <a name="ntgdiddcreatesurface-function"></a><span data-ttu-id="051a9-103">Funzione NtGdiDdCreateSurface</span><span class="sxs-lookup"><span data-stu-id="051a9-103">NtGdiDdCreateSurface function</span></span>

<span data-ttu-id="051a9-104">\[Questa funzione è soggetta a modifiche con ogni revisione del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="051a9-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="051a9-105">Usare invece Microsoft DirectDraw e Microsoft Direct3DAPIs. Queste API isolano le applicazioni da tali modifiche del sistema operativo e nascondono molte altre difficoltà nell'interazione diretta con i driver di visualizzazione.\]</span><span class="sxs-lookup"><span data-stu-id="051a9-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="051a9-106">Collega una superficie a un'altra superficie.</span><span class="sxs-lookup"><span data-stu-id="051a9-106">Attaches a surface to another surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="051a9-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="051a9-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdCreateSurface(
  _In_    HANDLE               hDirectDraw,
  _In_    HANDLE               *hSurface,
  _Inout_ DDSURFACEDESC        *puSurfaceDescription,
  _Inout_ DD_SURFACE_GLOBAL    *puSurfaceGlobalData,
  _Inout_ DD_SURFACE_LOCAL     *puSurfaceLocalData,
  _Inout_ DD_SURFACE_MORE      *puSurfaceMoreData,
  _Inout_ DD_CREATESURFACEDATA *puCreateSurfaceData,
  _Out_   HANDLE               *puhSurface
);
```



## <a name="parameters"></a><span data-ttu-id="051a9-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="051a9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="051a9-109">*hDirectDraw* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="051a9-109">*hDirectDraw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="051a9-110">Handle per la [**struttura \_ DD DIRECTDRAW \_ GLOBAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_directdraw_global) che rappresenta il driver.</span><span class="sxs-lookup"><span data-stu-id="051a9-110">Handle to the [**DD\_DIRECTDRAW\_GLOBAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_directdraw_global) structure representing the driver.</span></span>

</dd> <dt>

<span data-ttu-id="051a9-111">*hSurface* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="051a9-111">*hSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="051a9-112">Handle precedente alla stessa superficie.</span><span class="sxs-lookup"><span data-stu-id="051a9-112">Previous handle to the same surface.</span></span> <span data-ttu-id="051a9-113">Usato se la superficie viene ri-creata dopo un cambio di modalità.</span><span class="sxs-lookup"><span data-stu-id="051a9-113">Used if the surface is being re-created after a mode switch.</span></span>

</dd> <dt>

<span data-ttu-id="051a9-114">*puSurfaceDescription* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="051a9-114">*puSurfaceDescription* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="051a9-115">Puntatore alla [**struttura DDSURFACEDESC**](/previous-versions/windows/hardware/drivers/ff550339(v=vs.85)) che descrive la superficie o il buffer che il driver deve creare.</span><span class="sxs-lookup"><span data-stu-id="051a9-115">Pointer to the [**DDSURFACEDESC**](/previous-versions/windows/hardware/drivers/ff550339(v=vs.85)) structure describing the surface or buffer that the driver should create.</span></span>

</dd> <dt>

<span data-ttu-id="051a9-116">*puSurfaceGlobalData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="051a9-116">*puSurfaceGlobalData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="051a9-117">Puntatore alla [**struttura DD \_ SURFACE \_ GLOBAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_global) contenente i dati di superficie condivisi a livello globale con più superfici.</span><span class="sxs-lookup"><span data-stu-id="051a9-117">Pointer to the [**DD\_SURFACE\_GLOBAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_global) structure containing surface data that is shared globally with multiple surfaces.</span></span>

</dd> <dt>

<span data-ttu-id="051a9-118">*puSurfaceLocalData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="051a9-118">*puSurfaceLocalData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="051a9-119">Puntatore a un elenco [**di strutture \_ SURFACE \_ LOCAL DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) che descrivono gli oggetti superficie creati dal driver.</span><span class="sxs-lookup"><span data-stu-id="051a9-119">Pointer to a list of [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structures describing the surface objects created by the driver.</span></span>

</dd> <dt>

<span data-ttu-id="051a9-120">*puSurfaceMoreData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="051a9-120">*puSurfaceMoreData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="051a9-121">Puntatore a una [**struttura DD \_ SURFACE \_ MORE**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_more) che contiene dati aggiuntivi sulla superficie locale.</span><span class="sxs-lookup"><span data-stu-id="051a9-121">Pointer to a [**DD\_SURFACE\_MORE**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_more) structure that contains additional local surface data.</span></span>

</dd> <dt>

<span data-ttu-id="051a9-122">*puCreateSurfaceData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="051a9-122">*puCreateSurfaceData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="051a9-123">Puntatore a [**una struttura \_ CREATESURFACEDATA DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_createsurfacedata) che contiene le informazioni necessarie per creare una superficie.</span><span class="sxs-lookup"><span data-stu-id="051a9-123">Pointer to a [**DD\_CREATESURFACEDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_createsurfacedata) structure that contains the information required to create a surface.</span></span>

</dd> <dt>

<span data-ttu-id="051a9-124">*puhSurface* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="051a9-124">*puhSurface* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="051a9-125">Viene usato dall'API DirectDraw e non deve essere compilato dal driver.</span><span class="sxs-lookup"><span data-stu-id="051a9-125">Is used by the DirectDraw  API and should not be filled in by the driver.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="051a9-126">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="051a9-126">Return value</span></span>

<span data-ttu-id="051a9-127">**NtGdiDdCreateSurface** restituisce uno dei codici di callback seguenti.</span><span class="sxs-lookup"><span data-stu-id="051a9-127">**NtGdiDdCreateSurface** returns one of the following callback codes.</span></span>



| <span data-ttu-id="051a9-128">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="051a9-128">Return code</span></span>                                                                                              | <span data-ttu-id="051a9-129">Descrizione</span><span class="sxs-lookup"><span data-stu-id="051a9-129">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="051a9-130"><dt>**DRIVER DDHAL \_ \_ GESTITO**</dt></span><span class="sxs-lookup"><span data-stu-id="051a9-130"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="051a9-131">Il driver ha eseguito l'operazione e ha restituito un codice restituito valido per tale operazione.</span><span class="sxs-lookup"><span data-stu-id="051a9-131">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="051a9-132">Se questo codice è DD \_ OK, DirectDraw o Direct3D procede con la funzione .</span><span class="sxs-lookup"><span data-stu-id="051a9-132">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="051a9-133">In caso contrario, DirectDraw o Direct3D restituisce il codice di errore fornito dal driver e interrompe la funzione.</span><span class="sxs-lookup"><span data-stu-id="051a9-133">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="051a9-134"><dt>**DRIVER DDHAL \_ \_ NON GESTITO**</dt></span><span class="sxs-lookup"><span data-stu-id="051a9-134"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="051a9-135">Il driver non ha alcun commento sull'operazione richiesta.</span><span class="sxs-lookup"><span data-stu-id="051a9-135">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="051a9-136">Se è necessario che il driver abbia implementato un callback specifico, DirectDraw o Direct3D segnala una condizione di errore.</span><span class="sxs-lookup"><span data-stu-id="051a9-136">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="051a9-137">In caso contrario, DirectDraw o Direct3D gestisce l'operazione come se il callback del driver non fosse stato definito eseguendo l'implementazione DirectDraw o Direct3D indipendente dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="051a9-137">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="051a9-138">Commenti</span><span class="sxs-lookup"><span data-stu-id="051a9-138">Remarks</span></span>

<span data-ttu-id="051a9-139">È consigliabile che l'applicazione [chiami IDirectDraw7::CreateSurface](/windows/win32/api/ddraw/nf-ddraw-idirectdraw7-createsurface) anziché usare questa funzione.</span><span class="sxs-lookup"><span data-stu-id="051a9-139">It is recommended that your application call [IDirectDraw7::CreateSurface](/windows/win32/api/ddraw/nf-ddraw-idirectdraw7-createsurface) instead of using this function.</span></span>

<span data-ttu-id="051a9-140">Quando si crea una catena di superfici collegate, ad esempio una catena di scambio o una catena o mipmap, è prima necessario chiamare [**NtGdiDdCreateSurfaceObject**](-dxgkernel-ntgdiddcreatesurfaceobject.md) per ogni superficie.</span><span class="sxs-lookup"><span data-stu-id="051a9-140">When creating a chain of attached surfaces, such as a swap chain or chain or mipmaps, [**NtGdiDdCreateSurfaceObject**](-dxgkernel-ntgdiddcreatesurfaceobject.md) should be called for each surface first.</span></span> <span data-ttu-id="051a9-141">Chiamare quindi [**NtGdiDdAttachSurface per**](-dxgkernel-ntgdiddattachsurface.md) collegarli.</span><span class="sxs-lookup"><span data-stu-id="051a9-141">Then call [**NtGdiDdAttachSurface**](-dxgkernel-ntgdiddattachsurface.md) to attach them.</span></span> <span data-ttu-id="051a9-142">Chiamare infine **NtGdiDdCreateSurface solo** per la prima superficie della catena.</span><span class="sxs-lookup"><span data-stu-id="051a9-142">Finally, call **NtGdiDdCreateSurface** for the first surface in the chain only.</span></span> <span data-ttu-id="051a9-143">In questo caso, *hSurface* è l'handle restituito da **NtGdiDdCreateSurfaceObject** per la prima superficie della catena.</span><span class="sxs-lookup"><span data-stu-id="051a9-143">In this case, *hSurface* would be the handle returned by **NtGdiDdCreateSurfaceObject** for the first surface in the chain.</span></span>

<span data-ttu-id="051a9-144">**NtGdiDdCreateSurface** deve essere chiamato solo per creare superfici nella memoria video locale e non locale.</span><span class="sxs-lookup"><span data-stu-id="051a9-144">**NtGdiDdCreateSurface** should only be called to create surfaces in local and non-local video memory.</span></span> <span data-ttu-id="051a9-145">Non deve mai essere chiamato per creare superfici di memoria di sistema.</span><span class="sxs-lookup"><span data-stu-id="051a9-145">It should never be called to create system memory surfaces.</span></span> <span data-ttu-id="051a9-146">Per creare superfici di memoria di sistema, usare [**NtGdiDdCreateSurfaceObject.**](-dxgkernel-ntgdiddcreatesurfaceobject.md)</span><span class="sxs-lookup"><span data-stu-id="051a9-146">To create system memory surfaces, use [**NtGdiDdCreateSurfaceObject**](-dxgkernel-ntgdiddcreatesurfaceobject.md) instead.</span></span>

## <a name="requirements"></a><span data-ttu-id="051a9-147">Requisiti</span><span class="sxs-lookup"><span data-stu-id="051a9-147">Requirements</span></span>



| <span data-ttu-id="051a9-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="051a9-148">Requirement</span></span> | <span data-ttu-id="051a9-149">Valore</span><span class="sxs-lookup"><span data-stu-id="051a9-149">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="051a9-150">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="051a9-150">Minimum supported client</span></span><br/> | <span data-ttu-id="051a9-151">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="051a9-151">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="051a9-152">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="051a9-152">Minimum supported server</span></span><br/> | <span data-ttu-id="051a9-153">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="051a9-153">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="051a9-154">Intestazione</span><span class="sxs-lookup"><span data-stu-id="051a9-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="051a9-155"><dt>Ntgdi.h</dt></span><span class="sxs-lookup"><span data-stu-id="051a9-155"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="051a9-156">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="051a9-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="051a9-157">Supporto client di basso livello per grafica</span><span class="sxs-lookup"><span data-stu-id="051a9-157">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
