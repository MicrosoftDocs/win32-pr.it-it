---
description: Elimina un oggetto Surface Microsoft DirectDraw in modalità kernel allocato in precedenza, creato con il membro dwCaps della struttura DDSCAPS impostata su DDSCAPS \_ EXECUTEBUFFER.
ms.assetid: c737b706-25be-49b8-8d8c-35f48aea2889
title: Funzione NtGdiDdDestroyD3DBuffer (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdDestroyD3DBuffer
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: e88394e8cc3d13e1d117a1e53eab1190b1290ca4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103747719"
---
# <a name="ntgdidddestroyd3dbuffer-function"></a><span data-ttu-id="d465d-103">NtGdiDdDestroyD3DBuffer (funzione)</span><span class="sxs-lookup"><span data-stu-id="d465d-103">NtGdiDdDestroyD3DBuffer function</span></span>

<span data-ttu-id="d465d-104">\[Questa funzione è soggetta a modifiche a ogni revisione del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="d465d-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="d465d-105">Usare invece il DirectDraw e Microsoft Direct3DAPIs; Queste API isolano le applicazioni da tali modifiche del sistema operativo e nascondono molte altre difficoltà legate all'interazione diretta con i driver di visualizzazione.\]</span><span class="sxs-lookup"><span data-stu-id="d465d-105">Instead, use the DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="d465d-106">Elimina un oggetto Surface Microsoft DirectDraw in modalità kernel allocato in precedenza, creato con il membro **dwCaps** della struttura [**DDSCAPS**](/previous-versions/windows/hardware/drivers/ff550286(v=vs.85)) impostata su ddsCaps \_ EXECUTEBUFFER.</span><span class="sxs-lookup"><span data-stu-id="d465d-106">Destroys a previously allocated kernel-mode Microsoft DirectDraw surface object that was created with the **dwCaps** member of the [**DDSCAPS**](/previous-versions/windows/hardware/drivers/ff550286(v=vs.85)) structure set to DDSCAPS\_EXECUTEBUFFER.</span></span>

## <a name="syntax"></a><span data-ttu-id="d465d-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d465d-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdDestroyD3DBuffer(
  _In_ HANDLE hSurface
);
```



## <a name="parameters"></a><span data-ttu-id="d465d-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="d465d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d465d-109">*hSurface* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d465d-109">*hSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d465d-110">Handle per una struttura [**DD \_ DESTROYSURFACEDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_destroysurfacedata) che contiene le informazioni necessarie per eliminare un comando Direct3D o un vertex buffer.</span><span class="sxs-lookup"><span data-stu-id="d465d-110">Handle to a [**DD\_DESTROYSURFACEDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_destroysurfacedata) structure that contains the information needed to destroy a Direct3D command or vertex buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d465d-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d465d-111">Return value</span></span>

<span data-ttu-id="d465d-112">**NtGdiDdDestroyD3DBuffer** restituisce uno dei codici di callback seguenti.</span><span class="sxs-lookup"><span data-stu-id="d465d-112">**NtGdiDdDestroyD3DBuffer** returns one of the following callback codes.</span></span>



| <span data-ttu-id="d465d-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="d465d-113">Return code</span></span>                                                                                              | <span data-ttu-id="d465d-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d465d-114">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d465d-115"><dt>**\_driver DDHAL \_ gestito**</dt></span><span class="sxs-lookup"><span data-stu-id="d465d-115"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="d465d-116">Il driver ha eseguito l'operazione e ha restituito un codice restituito valido per l'operazione.</span><span class="sxs-lookup"><span data-stu-id="d465d-116">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="d465d-117">Se il codice è DD \_ OK, DirectDraw o Direct3D procede con la funzione.</span><span class="sxs-lookup"><span data-stu-id="d465d-117">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="d465d-118">In caso contrario, DirectDraw o Direct3D restituisce il codice di errore fornito dal driver e interrompe la funzione.</span><span class="sxs-lookup"><span data-stu-id="d465d-118">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="d465d-119"><dt>**\_NOTHANDLED driver \_ DDHAL**</dt></span><span class="sxs-lookup"><span data-stu-id="d465d-119"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="d465d-120">Il driver non ha commenti sull'operazione richiesta.</span><span class="sxs-lookup"><span data-stu-id="d465d-120">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="d465d-121">Se è necessario che il driver implementi un particolare callback, DirectDraw o Direct3D segnala una condizione di errore.</span><span class="sxs-lookup"><span data-stu-id="d465d-121">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="d465d-122">In caso contrario, DirectDraw o Direct3D gestisce l'operazione come se il callback del driver non fosse stato definito eseguendo l'implementazione di DirectDraw o Direct3D indipendente dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d465d-122">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="d465d-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d465d-123">Requirements</span></span>



| <span data-ttu-id="d465d-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="d465d-124">Requirement</span></span> | <span data-ttu-id="d465d-125">Valore</span><span class="sxs-lookup"><span data-stu-id="d465d-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d465d-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d465d-126">Minimum supported client</span></span><br/> | <span data-ttu-id="d465d-127">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d465d-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="d465d-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d465d-128">Minimum supported server</span></span><br/> | <span data-ttu-id="d465d-129">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d465d-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="d465d-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d465d-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="d465d-131"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="d465d-131"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d465d-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d465d-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d465d-133">Supporto client di livello inferiore grafica</span><span class="sxs-lookup"><span data-stu-id="d465d-133">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
