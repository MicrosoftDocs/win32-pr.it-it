---
description: Imposta la posizione per una sovrimpressione.
ms.assetid: dd495118-9ceb-4100-a7ec-794659bb4461
title: Funzione NtGdiDdSetOverlayPosition (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdSetOverlayPosition
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 73882e20fd7065d208835c2005d102b1312e8ce1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049105"
---
# <a name="ntgdiddsetoverlayposition-function"></a><span data-ttu-id="4fb24-103">NtGdiDdSetOverlayPosition (funzione)</span><span class="sxs-lookup"><span data-stu-id="4fb24-103">NtGdiDdSetOverlayPosition function</span></span>

<span data-ttu-id="4fb24-104">\[Questa funzione è soggetta a modifiche a ogni revisione del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="4fb24-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="4fb24-105">Usare invece Microsoft DirectDraw e Microsoft Direct3DAPIs; Queste API isolano le applicazioni da tali modifiche del sistema operativo e nascondono molte altre difficoltà legate all'interazione diretta con i driver di visualizzazione.\]</span><span class="sxs-lookup"><span data-stu-id="4fb24-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="4fb24-106">Imposta la posizione per una sovrimpressione.</span><span class="sxs-lookup"><span data-stu-id="4fb24-106">Sets the position for an overlay.</span></span>

## <a name="syntax"></a><span data-ttu-id="4fb24-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4fb24-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdSetOverlayPosition(
  _In_    HANDLE                     hSurfaceSource,
  _In_    HANDLE                     hSurfaceDestination,
  _Inout_ PDD_SETOVERLAYPOSITIONDATA puSetOverlayPositionData
);
```



## <a name="parameters"></a><span data-ttu-id="4fb24-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="4fb24-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4fb24-109">*hSurfaceSource* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4fb24-109">*hSurfaceSource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4fb24-110">Handle per una [**struttura \_ \_ locale della superficie DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) che rappresenta la superficie della sovrimpressione DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="4fb24-110">Handle to a [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structure that represents the DirectDraw overlay surface.</span></span>

</dd> <dt>

<span data-ttu-id="4fb24-111">*hSurfaceDestination* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4fb24-111">*hSurfaceDestination* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4fb24-112">Puntatore a una [**struttura \_ \_ locale della superficie DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) che rappresenta la superficie sovrapposta.</span><span class="sxs-lookup"><span data-stu-id="4fb24-112">Pointer to a [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structure representing the surface that is being overlaid.</span></span>

</dd> <dt>

<span data-ttu-id="4fb24-113">*puSetOverlayPositionData* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="4fb24-113">*puSetOverlayPositionData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="4fb24-114">Puntatore a una struttura [**DD \_ SETOVERLAYPOSITIONDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_setoverlaypositiondata) che contiene le informazioni necessarie per impostare la posizione della sovrimpressione.</span><span class="sxs-lookup"><span data-stu-id="4fb24-114">Pointer to a [**DD\_SETOVERLAYPOSITIONDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_setoverlaypositiondata) structure that contains the information required to set the overlay position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4fb24-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4fb24-115">Return value</span></span>

<span data-ttu-id="4fb24-116">**NtGdiDdSetOverlayPosition** restituisce uno dei codici di callback seguenti.</span><span class="sxs-lookup"><span data-stu-id="4fb24-116">**NtGdiDdSetOverlayPosition** returns one of the following callback codes.</span></span>



| <span data-ttu-id="4fb24-117">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="4fb24-117">Return code</span></span>                                                                                              | <span data-ttu-id="4fb24-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4fb24-118">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4fb24-119"><dt>**\_driver DDHAL \_ gestito**</dt></span><span class="sxs-lookup"><span data-stu-id="4fb24-119"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="4fb24-120">Il driver ha eseguito l'operazione e ha restituito un codice restituito valido per l'operazione.</span><span class="sxs-lookup"><span data-stu-id="4fb24-120">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="4fb24-121">Se il codice è DD \_ OK, DirectDraw o Direct3D procede con la funzione.</span><span class="sxs-lookup"><span data-stu-id="4fb24-121">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="4fb24-122">In caso contrario, DirectDraw o Direct3D restituisce il codice di errore fornito dal driver e interrompe la funzione.</span><span class="sxs-lookup"><span data-stu-id="4fb24-122">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="4fb24-123"><dt>**\_NOTHANDLED driver \_ DDHAL**</dt></span><span class="sxs-lookup"><span data-stu-id="4fb24-123"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="4fb24-124">Il driver non ha commenti sull'operazione richiesta.</span><span class="sxs-lookup"><span data-stu-id="4fb24-124">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="4fb24-125">Se è necessario che il driver implementi un particolare callback, DirectDraw o Direct3D segnala una condizione di errore.</span><span class="sxs-lookup"><span data-stu-id="4fb24-125">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="4fb24-126">In caso contrario, DirectDraw o Direct3D gestisce l'operazione come se il callback del driver non fosse stato definito eseguendo l'implementazione di DirectDraw o Direct3D indipendente dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4fb24-126">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="4fb24-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4fb24-127">Requirements</span></span>



| <span data-ttu-id="4fb24-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="4fb24-128">Requirement</span></span> | <span data-ttu-id="4fb24-129">Valore</span><span class="sxs-lookup"><span data-stu-id="4fb24-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4fb24-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4fb24-130">Minimum supported client</span></span><br/> | <span data-ttu-id="4fb24-131">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="4fb24-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="4fb24-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4fb24-132">Minimum supported server</span></span><br/> | <span data-ttu-id="4fb24-133">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="4fb24-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="4fb24-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4fb24-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="4fb24-135"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="4fb24-135"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4fb24-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4fb24-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4fb24-137">Supporto client di livello inferiore grafica</span><span class="sxs-lookup"><span data-stu-id="4fb24-137">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
