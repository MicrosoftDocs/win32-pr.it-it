---
description: "Funzione NtGdiDdAddAttachedSurface: collega una superficie a un'altra superficie."
ms.assetid: c4ef9e96-c498-4175-a2cd-22e0f88fd86e
title: Funzione NtGdiDdAddAttachedSurface (Ntgdi.h)
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
ms.openlocfilehash: dacaa07a586a88c808d8da07b8233002e8ae5055
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085789"
---
# <a name="ntgdiddaddattachedsurface-function"></a><span data-ttu-id="24b67-103">Funzione NtGdiDdAddAttachedSurface</span><span class="sxs-lookup"><span data-stu-id="24b67-103">NtGdiDdAddAttachedSurface function</span></span>

<span data-ttu-id="24b67-104">\[Questa funzione è soggetta a modifiche con ogni revisione del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="24b67-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="24b67-105">Usare invece Microsoft DirectDraw e Microsoft Direct3DAPIs. Queste API isolano le applicazioni da tali modifiche del sistema operativo e nascondono molte altre difficoltà nell'interazione diretta con i driver di visualizzazione.\]</span><span class="sxs-lookup"><span data-stu-id="24b67-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="24b67-106">Collega una superficie a un'altra superficie.</span><span class="sxs-lookup"><span data-stu-id="24b67-106">Attaches a surface to another surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="24b67-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="24b67-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdAddAttachedSurface(
  _In_    HANDLE                     hSurface,
  _In_    HANDLE                     hSurfaceAttached,
  _Inout_ PDD_ADDATTACHEDSURFACEDATA puAddAttachedSurfaceData
);
```



## <a name="parameters"></a><span data-ttu-id="24b67-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="24b67-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24b67-109">*hSurface* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="24b67-109">*hSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24b67-110">Handle a una [**struttura DD \_ SURFACE \_ LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) che rappresenta la superficie a cui è collegata un'altra superficie.</span><span class="sxs-lookup"><span data-stu-id="24b67-110">Handle to a [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structure that represents the surface to which another surface is being attached.</span></span>

</dd> <dt>

<span data-ttu-id="24b67-111">*hSurfaceAttached* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="24b67-111">*hSurfaceAttached* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24b67-112">Handle a una [**struttura DD \_ SURFACE \_ LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) che rappresenta la superficie da collegare.</span><span class="sxs-lookup"><span data-stu-id="24b67-112">Handle to a [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structure that represents the surface to be attached.</span></span>

</dd> <dt>

<span data-ttu-id="24b67-113">*puAddAttachedSurfaceData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="24b67-113">*puAddAttachedSurfaceData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="24b67-114">Puntatore a [**una struttura \_ ADDATTACHEDSURFACEDATA DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_addattachedsurfacedata) che contiene le informazioni necessarie al driver per eseguire l'allegato.</span><span class="sxs-lookup"><span data-stu-id="24b67-114">Pointer to a [**DD\_ADDATTACHEDSURFACEDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_addattachedsurfacedata) structure that contains information required for the driver to perform the attachment.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24b67-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="24b67-115">Return value</span></span>

<span data-ttu-id="24b67-116">**NtGdiDdAddAttachedSurface** restituisce uno dei codici di callback seguenti.</span><span class="sxs-lookup"><span data-stu-id="24b67-116">**NtGdiDdAddAttachedSurface** returns one of the following callback codes.</span></span>



| <span data-ttu-id="24b67-117">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="24b67-117">Return code</span></span>                                                                                              | <span data-ttu-id="24b67-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="24b67-118">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="24b67-119"><dt>**DRIVER DDHAL \_ \_ GESTITO**</dt></span><span class="sxs-lookup"><span data-stu-id="24b67-119"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="24b67-120">Il driver ha eseguito l'operazione e ha restituito un codice restituito valido per tale operazione.</span><span class="sxs-lookup"><span data-stu-id="24b67-120">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="24b67-121">Se questo codice è DD \_ OK, DirectDraw o Direct3D procede con la funzione .</span><span class="sxs-lookup"><span data-stu-id="24b67-121">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="24b67-122">In caso contrario, DirectDraw o Direct3D restituisce il codice di errore fornito dal driver e interrompe la funzione.</span><span class="sxs-lookup"><span data-stu-id="24b67-122">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="24b67-123"><dt>**DRIVER DDHAL \_ \_ NON GESTITO**</dt></span><span class="sxs-lookup"><span data-stu-id="24b67-123"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="24b67-124">Il driver non ha commenti sull'operazione richiesta.</span><span class="sxs-lookup"><span data-stu-id="24b67-124">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="24b67-125">Se è necessario che il driver abbia implementato un callback specifico, DirectDraw o Direct3D segnala una condizione di errore.</span><span class="sxs-lookup"><span data-stu-id="24b67-125">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="24b67-126">In caso contrario, DirectDraw o Direct3D gestisce l'operazione come se il callback del driver non fosse stato definito eseguendo l'implementazione indipendente dal dispositivo DirectDraw o Direct3D.</span><span class="sxs-lookup"><span data-stu-id="24b67-126">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="24b67-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="24b67-127">Requirements</span></span>



| <span data-ttu-id="24b67-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="24b67-128">Requirement</span></span> | <span data-ttu-id="24b67-129">Valore</span><span class="sxs-lookup"><span data-stu-id="24b67-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="24b67-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="24b67-130">Minimum supported client</span></span><br/> | <span data-ttu-id="24b67-131">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="24b67-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="24b67-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="24b67-132">Minimum supported server</span></span><br/> | <span data-ttu-id="24b67-133">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="24b67-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="24b67-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="24b67-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="24b67-135"><dt>Ntgdi.h</dt></span><span class="sxs-lookup"><span data-stu-id="24b67-135"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24b67-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="24b67-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24b67-137">Supporto client di basso livello per grafica</span><span class="sxs-lookup"><span data-stu-id="24b67-137">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
