---
description: Riposiziona o modifica gli attributi visivi di una superficie di sovrapposizione.
ms.assetid: 6d39166c-0efc-450d-adf4-9f4dfdf7c57f
title: Funzione NtGdiDdUpdateOverlay (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdUpdateOverlay
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: bbe610c27d83061bda0996ce9acc082efa95e3a7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103965937"
---
# <a name="ntgdiddupdateoverlay-function"></a><span data-ttu-id="5177b-103">NtGdiDdUpdateOverlay (funzione)</span><span class="sxs-lookup"><span data-stu-id="5177b-103">NtGdiDdUpdateOverlay function</span></span>

<span data-ttu-id="5177b-104">\[Questa funzione è soggetta a modifiche a ogni revisione del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="5177b-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="5177b-105">Usare invece Microsoft DirectDraw e Microsoft Direct3DAPIs; Queste API isolano le applicazioni da tali modifiche del sistema operativo e nascondono molte altre difficoltà legate all'interazione diretta con i driver di visualizzazione.\]</span><span class="sxs-lookup"><span data-stu-id="5177b-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="5177b-106">Riposiziona o modifica gli attributi visivi di una superficie di sovrapposizione.</span><span class="sxs-lookup"><span data-stu-id="5177b-106">Repositions or modifies the visual attributes of an overlay surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="5177b-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5177b-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdUpdateOverlay(
  _In_    HANDLE                hSurfaceDestination,
  _In_    HANDLE                hSurfaceSource,
  _Inout_ PDD_UPDATEOVERLAYDATA puUpdateOverlayData
);
```



## <a name="parameters"></a><span data-ttu-id="5177b-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="5177b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5177b-109">*hSurfaceDestination* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5177b-109">*hSurfaceDestination* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5177b-110">Handle per l'oggetto DirectDraw in modalità kernel creato in precedenza.</span><span class="sxs-lookup"><span data-stu-id="5177b-110">Handle to previously created kernel-mode DirectDraw object.</span></span>

</dd> <dt>

<span data-ttu-id="5177b-111">*hSurfaceSource* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5177b-111">*hSurfaceSource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5177b-112">Handle per una [**struttura \_ \_ locale della superficie DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) che descrive la superficie della sovrimpressione.</span><span class="sxs-lookup"><span data-stu-id="5177b-112">Handle to a [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structure that describes the overlay surface.</span></span>

</dd> <dt>

<span data-ttu-id="5177b-113">*puUpdateOverlayData* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="5177b-113">*puUpdateOverlayData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="5177b-114">Puntatore a una struttura [**DD \_ UPDATEOVERLAYDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_updateoverlaydata) che contiene le informazioni necessarie per aggiornare la sovrimpressione.</span><span class="sxs-lookup"><span data-stu-id="5177b-114">Pointer to a [**DD\_UPDATEOVERLAYDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_updateoverlaydata) structure that contains the information required to update the overlay.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5177b-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5177b-115">Return value</span></span>

<span data-ttu-id="5177b-116">**NtGdiDdUpdateOverlay** restituisce uno dei codici di callback seguenti.</span><span class="sxs-lookup"><span data-stu-id="5177b-116">**NtGdiDdUpdateOverlay** returns one of the following callback codes.</span></span>



| <span data-ttu-id="5177b-117">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="5177b-117">Return code</span></span>                                                                                              | <span data-ttu-id="5177b-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5177b-118">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5177b-119"><dt>**\_driver DDHAL \_ gestito**</dt></span><span class="sxs-lookup"><span data-stu-id="5177b-119"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="5177b-120">Il driver ha eseguito l'operazione e ha restituito un codice restituito valido per l'operazione.</span><span class="sxs-lookup"><span data-stu-id="5177b-120">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="5177b-121">Se il codice è DD \_ OK, DirectDraw o Direct3D procede con la funzione.</span><span class="sxs-lookup"><span data-stu-id="5177b-121">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="5177b-122">In caso contrario, DirectDraw o Direct3D restituisce il codice di errore fornito dal driver e interrompe la funzione.</span><span class="sxs-lookup"><span data-stu-id="5177b-122">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="5177b-123"><dt>**\_NOTHANDLED driver \_ DDHAL**</dt></span><span class="sxs-lookup"><span data-stu-id="5177b-123"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="5177b-124">Il driver non ha commenti sull'operazione richiesta.</span><span class="sxs-lookup"><span data-stu-id="5177b-124">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="5177b-125">Se è necessario che il driver implementi un particolare callback, DirectDraw o Direct3D segnala una condizione di errore.</span><span class="sxs-lookup"><span data-stu-id="5177b-125">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="5177b-126">In caso contrario, DirectDraw o Direct3D gestisce l'operazione come se il callback del driver non fosse stato definito eseguendo l'implementazione di DirectDraw o Direct3D indipendente dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5177b-126">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="5177b-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5177b-127">Requirements</span></span>



| <span data-ttu-id="5177b-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="5177b-128">Requirement</span></span> | <span data-ttu-id="5177b-129">Valore</span><span class="sxs-lookup"><span data-stu-id="5177b-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5177b-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5177b-130">Minimum supported client</span></span><br/> | <span data-ttu-id="5177b-131">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5177b-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="5177b-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5177b-132">Minimum supported server</span></span><br/> | <span data-ttu-id="5177b-133">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5177b-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="5177b-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5177b-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="5177b-135"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="5177b-135"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5177b-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5177b-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5177b-137">Supporto client di livello inferiore grafica</span><span class="sxs-lookup"><span data-stu-id="5177b-137">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
