---
description: Controlla la luminosità e i controlli di luminosità di una superficie di sovrapposizione.
ms.assetid: 2f617c89-5505-4d84-be7d-473b216c0571
title: Funzione NtGdiDdColorControl (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdColorControl
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 45ed8683a892b07fa63fbe79b657669e647126cd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104125955"
---
# <a name="ntgdiddcolorcontrol-function"></a><span data-ttu-id="56ec6-103">NtGdiDdColorControl (funzione)</span><span class="sxs-lookup"><span data-stu-id="56ec6-103">NtGdiDdColorControl function</span></span>

<span data-ttu-id="56ec6-104">\[Questa funzione è soggetta a modifiche a ogni revisione del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="56ec6-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="56ec6-105">Usare invece Microsoft DirectDraw e Microsoft Direct3DAPIs; Queste API isolano le applicazioni da tali modifiche del sistema operativo e nascondono molte altre difficoltà legate all'interazione diretta con i driver di visualizzazione.\]</span><span class="sxs-lookup"><span data-stu-id="56ec6-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="56ec6-106">Controlla la luminosità e i controlli di luminosità di una superficie di sovrapposizione.</span><span class="sxs-lookup"><span data-stu-id="56ec6-106">Controls the luminance and brightness controls of an overlay surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="56ec6-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="56ec6-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdColorControl(
  _In_    HANDLE               hSurface,
  _Inout_ PDD_COLORCONTROLDATA puColorControlData
);
```



## <a name="parameters"></a><span data-ttu-id="56ec6-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="56ec6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56ec6-109">*hSurface* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="56ec6-109">*hSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="56ec6-110">Handle per la [**struttura \_ \_ locale della superficie DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) che rappresenta la superficie della sovrimpressione.</span><span class="sxs-lookup"><span data-stu-id="56ec6-110">Handle to the [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structure representing the overlay surface.</span></span>

</dd> <dt>

<span data-ttu-id="56ec6-111">*puColorControlData* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="56ec6-111">*puColorControlData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="56ec6-112">Puntatore a una struttura [**DD \_ COLORCONTROLDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_colorcontroldata) che contiene le informazioni sul controllo del colore per una superficie di sovrapposizione specificata.</span><span class="sxs-lookup"><span data-stu-id="56ec6-112">Pointer to a [**DD\_COLORCONTROLDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_colorcontroldata) structure that contains the color control information for a specified overlay surface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56ec6-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="56ec6-113">Return value</span></span>

<span data-ttu-id="56ec6-114">**NtGdiDdColorControl** restituisce uno dei codici di callback seguenti.</span><span class="sxs-lookup"><span data-stu-id="56ec6-114">**NtGdiDdColorControl** returns one of the following callback codes.</span></span>



| <span data-ttu-id="56ec6-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="56ec6-115">Return code</span></span>                                                                                              | <span data-ttu-id="56ec6-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="56ec6-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="56ec6-117"><dt>**\_driver DDHAL \_ gestito**</dt></span><span class="sxs-lookup"><span data-stu-id="56ec6-117"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="56ec6-118">Il driver ha eseguito l'operazione e ha restituito un codice restituito valido per l'operazione.</span><span class="sxs-lookup"><span data-stu-id="56ec6-118">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="56ec6-119">Se il codice è DD \_ OK, DirectDraw o Direct3D procede con la funzione.</span><span class="sxs-lookup"><span data-stu-id="56ec6-119">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="56ec6-120">In caso contrario, DirectDraw o Direct3D restituisce il codice di errore fornito dal driver e interrompe la funzione.</span><span class="sxs-lookup"><span data-stu-id="56ec6-120">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="56ec6-121"><dt>**\_NOTHANDLED driver \_ DDHAL**</dt></span><span class="sxs-lookup"><span data-stu-id="56ec6-121"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="56ec6-122">Il driver non ha commenti sull'operazione richiesta.</span><span class="sxs-lookup"><span data-stu-id="56ec6-122">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="56ec6-123">Se è necessario che il driver implementi un particolare callback, DirectDraw o Direct3D segnala una condizione di errore.</span><span class="sxs-lookup"><span data-stu-id="56ec6-123">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="56ec6-124">In caso contrario, DirectDraw o Direct3D gestisce l'operazione come se il callback del driver non fosse stato definito eseguendo l'implementazione di DirectDraw o Direct3D indipendente dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="56ec6-124">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="56ec6-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="56ec6-125">Requirements</span></span>



| <span data-ttu-id="56ec6-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="56ec6-126">Requirement</span></span> | <span data-ttu-id="56ec6-127">Valore</span><span class="sxs-lookup"><span data-stu-id="56ec6-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="56ec6-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="56ec6-128">Minimum supported client</span></span><br/> | <span data-ttu-id="56ec6-129">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="56ec6-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="56ec6-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="56ec6-130">Minimum supported server</span></span><br/> | <span data-ttu-id="56ec6-131">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="56ec6-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="56ec6-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="56ec6-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="56ec6-133"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="56ec6-133"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56ec6-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="56ec6-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56ec6-135">Supporto client di livello inferiore grafica</span><span class="sxs-lookup"><span data-stu-id="56ec6-135">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
