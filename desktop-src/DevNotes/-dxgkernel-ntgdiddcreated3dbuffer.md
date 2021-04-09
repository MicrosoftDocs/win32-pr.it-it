---
description: Utilizzato per creare un comando a livello di driver o un buffer vertex della descrizione specificata.
ms.assetid: c65403a1-5686-4c7d-80a4-6e49417c11eb
title: Funzione NtGdiDdCreateD3DBuffer (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdCreateD3DBuffer
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 2d402a70822fba094d22c82b8767ee3298b86374
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103965941"
---
# <a name="ntgdiddcreated3dbuffer-function"></a><span data-ttu-id="8471e-103">NtGdiDdCreateD3DBuffer (funzione)</span><span class="sxs-lookup"><span data-stu-id="8471e-103">NtGdiDdCreateD3DBuffer function</span></span>

<span data-ttu-id="8471e-104">\[Questa funzione è soggetta a modifiche a ogni revisione del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="8471e-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="8471e-105">Usare invece Microsoft DirectDraw e Microsoft Direct3DAPIs; Queste API isolano le applicazioni da tali modifiche del sistema operativo e nascondono molte altre difficoltà legate all'interazione diretta con i driver di visualizzazione.\]</span><span class="sxs-lookup"><span data-stu-id="8471e-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="8471e-106">Utilizzato per creare un comando a livello di driver o un buffer vertex della descrizione specificata.</span><span class="sxs-lookup"><span data-stu-id="8471e-106">Used to create a driver-level command or vertex buffer of the specified description.</span></span>

## <a name="syntax"></a><span data-ttu-id="8471e-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8471e-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdCreateD3DBuffer(
  _In_    HANDLE               hDirectDraw,
  _Inout_ HANDLE               *hSurface,
  _Inout_ DDSURFACEDESC        *puSurfaceDescription,
  _Inout_ DD_SURFACE_GLOBAL    *puSurfaceGlobalData,
  _Inout_ DD_SURFACE_LOCAL     *puSurfaceLocalData,
  _Inout_ DD_SURFACE_MORE      *puSurfaceMoreData,
  _Inout_ DD_CREATESURFACEDATA *puCreateSurfaceData,
  _Inout_ HANDLE               *puhSurface
);
```



## <a name="parameters"></a><span data-ttu-id="8471e-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="8471e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8471e-109">*hDirectDraw* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8471e-109">*hDirectDraw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8471e-110">Handle per la [**struttura \_ \_ globale di DIRECTDRAW DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_directdraw_global) che rappresenta il driver.</span><span class="sxs-lookup"><span data-stu-id="8471e-110">Handle to the [**DD\_DIRECTDRAW\_GLOBAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_directdraw_global) structure representing the driver.</span></span>

</dd> <dt>

<span data-ttu-id="8471e-111">*hSurface* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="8471e-111">*hSurface* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8471e-112">Puntatore a una matrice di handle di superficie.</span><span class="sxs-lookup"><span data-stu-id="8471e-112">Pointer to an array of surface handles.</span></span> <span data-ttu-id="8471e-113">Il chiamante può impostare questi handle sui valori di handle precedenti se le superfici vengono ricreate dopo un'opzione di modalità.</span><span class="sxs-lookup"><span data-stu-id="8471e-113">The caller can set these handles to the previous handle values if the surfaces are being re-created after a mode switch.</span></span> <span data-ttu-id="8471e-114">Questo processo è denominato "ripristino" nella documentazione di DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="8471e-114">This process is called "restoring" in the DirectDraw documentation.</span></span>

</dd> <dt>

<span data-ttu-id="8471e-115">*puSurfaceDescription* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="8471e-115">*puSurfaceDescription* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8471e-116">Puntatore a una struttura [**DDSURFACEDESC**](/previous-versions/windows/hardware/drivers/ff550339(v=vs.85)) che descrive la superficie o il buffer che deve essere creato dal driver.</span><span class="sxs-lookup"><span data-stu-id="8471e-116">Pointer to a [**DDSURFACEDESC**](/previous-versions/windows/hardware/drivers/ff550339(v=vs.85)) structure describing the surface or buffer that the driver should create.</span></span>

</dd> <dt>

<span data-ttu-id="8471e-117">*puSurfaceGlobalData* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="8471e-117">*puSurfaceGlobalData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8471e-118">Puntatore a una [**struttura \_ \_ globale della superficie DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_global) contenente dati di superficie condivisi globalmente con più superfici.</span><span class="sxs-lookup"><span data-stu-id="8471e-118">Pointer to a [**DD\_SURFACE\_GLOBAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_global) structure containing surface data that is shared globally with multiple surfaces.</span></span>

</dd> <dt>

<span data-ttu-id="8471e-119">*puSurfaceLocalData* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="8471e-119">*puSurfaceLocalData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8471e-120">Puntatore a un elenco di [**strutture \_ \_ locali della superficie DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) che descrivono gli oggetti Surface creati dal driver.</span><span class="sxs-lookup"><span data-stu-id="8471e-120">Pointer to a list of [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structures describing the surface objects created by the driver.</span></span> <span data-ttu-id="8471e-121">In questa matrice è in genere presente una sola voce.</span><span class="sxs-lookup"><span data-stu-id="8471e-121">There is usually only one entry in this array.</span></span>

</dd> <dt>

<span data-ttu-id="8471e-122">*puSurfaceMoreData* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="8471e-122">*puSurfaceMoreData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8471e-123">Puntatore a una [**\_ superficie DD \_ più**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_more) struttura che contiene dati della superficie locale aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="8471e-123">Pointer to a [**DD\_SURFACE\_MORE**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_more) structure that contains additional local surface data.</span></span>

</dd> <dt>

<span data-ttu-id="8471e-124">*puCreateSurfaceData* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="8471e-124">*puCreateSurfaceData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8471e-125">Puntatore a una struttura [**DD \_ CREATESURFACEDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_createsurfacedata) che contiene le informazioni necessarie per creare il buffer.</span><span class="sxs-lookup"><span data-stu-id="8471e-125">Pointer to a [**DD\_CREATESURFACEDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_createsurfacedata) structure that contains the information required to create the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="8471e-126">*puhSurface* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="8471e-126">*puhSurface* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8471e-127">Viene usato dall'API DirectDraw e non deve essere compilato dal driver.</span><span class="sxs-lookup"><span data-stu-id="8471e-127">Is used by the DirectDraw  API and should not be filled in by the driver.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8471e-128">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8471e-128">Return value</span></span>

<span data-ttu-id="8471e-129">**NtGdiDdCreateD3DBuffer** restituisce uno dei codici di callback seguenti.</span><span class="sxs-lookup"><span data-stu-id="8471e-129">**NtGdiDdCreateD3DBuffer** returns one of the following callback codes.</span></span>



| <span data-ttu-id="8471e-130">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="8471e-130">Return code</span></span>                                                                                              | <span data-ttu-id="8471e-131">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8471e-131">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8471e-132"><dt>**\_driver DDHAL \_ gestito**</dt></span><span class="sxs-lookup"><span data-stu-id="8471e-132"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="8471e-133">Il driver ha eseguito l'operazione e ha restituito un codice restituito valido per l'operazione.</span><span class="sxs-lookup"><span data-stu-id="8471e-133">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="8471e-134">Se il codice è DD \_ OK, DirectDraw o Direct3D procede con la funzione.</span><span class="sxs-lookup"><span data-stu-id="8471e-134">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="8471e-135">In caso contrario, DirectDraw o Direct3D restituisce il codice di errore fornito dal driver e interrompe la funzione.</span><span class="sxs-lookup"><span data-stu-id="8471e-135">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="8471e-136"><dt>**\_NOTHANDLED driver \_ DDHAL**</dt></span><span class="sxs-lookup"><span data-stu-id="8471e-136"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="8471e-137">Il driver non ha commenti sull'operazione richiesta.</span><span class="sxs-lookup"><span data-stu-id="8471e-137">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="8471e-138">Se è necessario che il driver implementi un particolare callback, DirectDraw o Direct3D segnala una condizione di errore.</span><span class="sxs-lookup"><span data-stu-id="8471e-138">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="8471e-139">In caso contrario, DirectDraw o Direct3D gestisce l'operazione come se il callback del driver non fosse stato definito eseguendo l'implementazione di DirectDraw o Direct3D indipendente dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8471e-139">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="8471e-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8471e-140">Requirements</span></span>



| <span data-ttu-id="8471e-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="8471e-141">Requirement</span></span> | <span data-ttu-id="8471e-142">Valore</span><span class="sxs-lookup"><span data-stu-id="8471e-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8471e-143">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8471e-143">Minimum supported client</span></span><br/> | <span data-ttu-id="8471e-144">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="8471e-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="8471e-145">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8471e-145">Minimum supported server</span></span><br/> | <span data-ttu-id="8471e-146">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="8471e-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="8471e-147">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8471e-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="8471e-148"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="8471e-148"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8471e-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8471e-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8471e-150">Supporto client di livello inferiore grafica</span><span class="sxs-lookup"><span data-stu-id="8471e-150">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
