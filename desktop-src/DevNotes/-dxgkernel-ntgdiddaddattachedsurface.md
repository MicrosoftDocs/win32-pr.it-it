---
description: Connette una superficie a un'altra superficie.
ms.assetid: c4ef9e96-c498-4175-a2cd-22e0f88fd86e
title: Funzione NtGdiDdAddAttachedSurface (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdAddAttachedSurface
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: d6e87d3a077c1381eeaa306e594daec0f5b855d1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877454"
---
# <a name="ntgdiddaddattachedsurface-function"></a><span data-ttu-id="d9b9c-103">NtGdiDdAddAttachedSurface (funzione)</span><span class="sxs-lookup"><span data-stu-id="d9b9c-103">NtGdiDdAddAttachedSurface function</span></span>

<span data-ttu-id="d9b9c-104">\[Questa funzione è soggetta a modifiche a ogni revisione del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="d9b9c-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="d9b9c-105">Usare invece Microsoft DirectDraw e Microsoft Direct3DAPIs; Queste API isolano le applicazioni da tali modifiche del sistema operativo e nascondono molte altre difficoltà legate all'interazione diretta con i driver di visualizzazione.\]</span><span class="sxs-lookup"><span data-stu-id="d9b9c-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="d9b9c-106">Connette una superficie a un'altra superficie.</span><span class="sxs-lookup"><span data-stu-id="d9b9c-106">Attaches a surface to another surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9b9c-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d9b9c-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdAddAttachedSurface(
  _In_    HANDLE                     hSurface,
  _In_    HANDLE                     hSurfaceAttached,
  _Inout_ PDD_ADDATTACHEDSURFACEDATA puAddAttachedSurfaceData
);
```



## <a name="parameters"></a><span data-ttu-id="d9b9c-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="d9b9c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9b9c-109">*hSurface* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d9b9c-109">*hSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9b9c-110">Handle per una [**struttura \_ \_ locale della superficie DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) che rappresenta la superficie a cui viene collegata un'altra superficie.</span><span class="sxs-lookup"><span data-stu-id="d9b9c-110">Handle to a [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structure that represents the surface to which another surface is being attached.</span></span>

</dd> <dt>

<span data-ttu-id="d9b9c-111">*hSurfaceAttached* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d9b9c-111">*hSurfaceAttached* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9b9c-112">Handle per una [**struttura \_ \_ locale della superficie DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) che rappresenta la superficie da collegare.</span><span class="sxs-lookup"><span data-stu-id="d9b9c-112">Handle to a [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structure that represents the surface to be attached.</span></span>

</dd> <dt>

<span data-ttu-id="d9b9c-113">*puAddAttachedSurfaceData* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="d9b9c-113">*puAddAttachedSurfaceData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d9b9c-114">Puntatore a una struttura [**DD \_ ADDATTACHEDSURFACEDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_addattachedsurfacedata) che contiene le informazioni necessarie per l'esecuzione dell'allegato da parte del driver.</span><span class="sxs-lookup"><span data-stu-id="d9b9c-114">Pointer to a [**DD\_ADDATTACHEDSURFACEDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_addattachedsurfacedata) structure that contains information required for the driver to perform the attachment.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9b9c-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d9b9c-115">Return value</span></span>

<span data-ttu-id="d9b9c-116">**NtGdiDdAddAttachedSurface** restituisce uno dei codici di callback seguenti.</span><span class="sxs-lookup"><span data-stu-id="d9b9c-116">**NtGdiDdAddAttachedSurface** returns one of the following callback codes.</span></span>



| <span data-ttu-id="d9b9c-117">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="d9b9c-117">Return code</span></span>                                                                                              | <span data-ttu-id="d9b9c-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d9b9c-118">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d9b9c-119"><dt>**\_driver DDHAL \_ gestito**</dt></span><span class="sxs-lookup"><span data-stu-id="d9b9c-119"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="d9b9c-120">Il driver ha eseguito l'operazione e ha restituito un codice restituito valido per l'operazione.</span><span class="sxs-lookup"><span data-stu-id="d9b9c-120">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="d9b9c-121">Se il codice è DD \_ OK, DirectDraw o Direct3D procede con la funzione.</span><span class="sxs-lookup"><span data-stu-id="d9b9c-121">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="d9b9c-122">In caso contrario, DirectDraw o Direct3D restituisce il codice di errore fornito dal driver e interrompe la funzione.</span><span class="sxs-lookup"><span data-stu-id="d9b9c-122">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="d9b9c-123"><dt>**\_NOTHANDLED driver \_ DDHAL**</dt></span><span class="sxs-lookup"><span data-stu-id="d9b9c-123"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="d9b9c-124">Il driver non ha commenti sull'operazione richiesta.</span><span class="sxs-lookup"><span data-stu-id="d9b9c-124">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="d9b9c-125">Se è necessario che il driver implementi un particolare callback, DirectDraw o Direct3D segnala una condizione di errore.</span><span class="sxs-lookup"><span data-stu-id="d9b9c-125">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="d9b9c-126">In caso contrario, DirectDraw o Direct3D gestisce l'operazione come se il callback del driver non fosse stato definito eseguendo l'implementazione di DirectDraw o Direct3D indipendente dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d9b9c-126">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="d9b9c-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d9b9c-127">Requirements</span></span>



| <span data-ttu-id="d9b9c-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="d9b9c-128">Requirement</span></span> | <span data-ttu-id="d9b9c-129">Valore</span><span class="sxs-lookup"><span data-stu-id="d9b9c-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d9b9c-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d9b9c-130">Minimum supported client</span></span><br/> | <span data-ttu-id="d9b9c-131">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d9b9c-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="d9b9c-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d9b9c-132">Minimum supported server</span></span><br/> | <span data-ttu-id="d9b9c-133">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d9b9c-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="d9b9c-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d9b9c-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="d9b9c-135"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="d9b9c-135"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9b9c-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d9b9c-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9b9c-137">Supporto client di livello inferiore grafica</span><span class="sxs-lookup"><span data-stu-id="d9b9c-137">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
