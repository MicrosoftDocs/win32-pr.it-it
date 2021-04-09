---
description: Elimina definitivamente un oggetto Surface Microsoft DirectDraw in modalità kernel allocato in precedenza.
ms.assetid: 65419fce-9e82-4621-9906-832144888a3b
title: Funzione NtGdiDdDestroySurface (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdDestroySurface
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 54799aa90007370439b2be8c8cf8c1f584360a5d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049183"
---
# <a name="ntgdidddestroysurface-function"></a><span data-ttu-id="e8489-103">NtGdiDdDestroySurface (funzione)</span><span class="sxs-lookup"><span data-stu-id="e8489-103">NtGdiDdDestroySurface function</span></span>

<span data-ttu-id="e8489-104">\[Questa funzione è soggetta a modifiche a ogni revisione del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="e8489-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="e8489-105">Usare invece il DirectDraw e Microsoft Direct3DAPIs; Queste API isolano le applicazioni da tali modifiche del sistema operativo e nascondono molte altre difficoltà legate all'interazione diretta con i driver di visualizzazione.\]</span><span class="sxs-lookup"><span data-stu-id="e8489-105">Instead, use the DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="e8489-106">Elimina definitivamente un oggetto Surface Microsoft DirectDraw in modalità kernel allocato in precedenza.</span><span class="sxs-lookup"><span data-stu-id="e8489-106">Destroys a previously allocated kernel-mode Microsoft DirectDraw surface object.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8489-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e8489-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdDestroySurface(
  _In_ HANDLE hSurface,
  _In_ BOOL   bRealDestroy
);
```



## <a name="parameters"></a><span data-ttu-id="e8489-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="e8489-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8489-109">*hSurface* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e8489-109">*hSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8489-110">Handle per l'oggetto Surface precedentemente allocato in modalità kernel.</span><span class="sxs-lookup"><span data-stu-id="e8489-110">Handle to previously allocated kernel-mode surface object.</span></span>

</dd> <dt>

<span data-ttu-id="e8489-111">*bRealDestroy* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e8489-111">*bRealDestroy* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8489-112">Specifica la modalità di eliminazione della superficie.</span><span class="sxs-lookup"><span data-stu-id="e8489-112">Specifies how to destroy the surface.</span></span> <span data-ttu-id="e8489-113">Può essere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="e8489-113">Can be one of the following values.</span></span>

<dt>



 <span data-ttu-id="e8489-114">TRUE</span><span class="sxs-lookup"><span data-stu-id="e8489-114">(TRUE)</span></span>


</dt> <dd>

<span data-ttu-id="e8489-115">Elimina la superficie e la memoria video disponibile.</span><span class="sxs-lookup"><span data-stu-id="e8489-115">Destroy the surface and free video memory.</span></span>

</dd> <dt>



 <span data-ttu-id="e8489-116">FALSE</span><span class="sxs-lookup"><span data-stu-id="e8489-116">(FALSE)</span></span>


</dt> <dd>

<span data-ttu-id="e8489-117">Liberare la memoria del video, ma lasciare la superficie in uno stato non inizializzato.</span><span class="sxs-lookup"><span data-stu-id="e8489-117">Free the video memory but leave the surface in an uninitialized state.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8489-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e8489-118">Return value</span></span>

<span data-ttu-id="e8489-119">**NtGdiDdDestroySurface** restituisce uno dei codici di callback seguenti.</span><span class="sxs-lookup"><span data-stu-id="e8489-119">**NtGdiDdDestroySurface** returns one of the following callback codes.</span></span>



| <span data-ttu-id="e8489-120">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="e8489-120">Return code</span></span>                                                                                              | <span data-ttu-id="e8489-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e8489-121">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e8489-122"><dt>**\_driver DDHAL \_ gestito**</dt></span><span class="sxs-lookup"><span data-stu-id="e8489-122"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="e8489-123">Il driver ha eseguito l'operazione e ha restituito un codice restituito valido per l'operazione.</span><span class="sxs-lookup"><span data-stu-id="e8489-123">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="e8489-124">Se il codice è DD \_ OK, DirectDraw o Direct3D procede con la funzione.</span><span class="sxs-lookup"><span data-stu-id="e8489-124">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="e8489-125">In caso contrario, DirectDraw o Direct3D restituisce il codice di errore fornito dal driver e interrompe la funzione.</span><span class="sxs-lookup"><span data-stu-id="e8489-125">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="e8489-126"><dt>**\_NOTHANDLED driver \_ DDHAL**</dt></span><span class="sxs-lookup"><span data-stu-id="e8489-126"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="e8489-127">Il driver non ha commenti sull'operazione richiesta.</span><span class="sxs-lookup"><span data-stu-id="e8489-127">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="e8489-128">Se è necessario che il driver implementi un particolare callback, DirectDraw o Direct3D segnala una condizione di errore.</span><span class="sxs-lookup"><span data-stu-id="e8489-128">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="e8489-129">In caso contrario, DirectDraw o Direct3D gestisce l'operazione come se il callback del driver non fosse stato definito eseguendo l'implementazione di DirectDraw o Direct3D indipendente dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e8489-129">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e8489-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="e8489-130">Remarks</span></span>

<span data-ttu-id="e8489-131">È consigliabile che le applicazioni usino le API DirectDraw e Direct3D per creare ed eliminare definitivamente le superfici anziché questa funzione.</span><span class="sxs-lookup"><span data-stu-id="e8489-131">It is recommended that applications use the DirectDraw and Direct3D APIs to create and destroy surfaces instead of this function.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8489-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e8489-132">Requirements</span></span>



| <span data-ttu-id="e8489-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8489-133">Requirement</span></span> | <span data-ttu-id="e8489-134">Valore</span><span class="sxs-lookup"><span data-stu-id="e8489-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e8489-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e8489-135">Minimum supported client</span></span><br/> | <span data-ttu-id="e8489-136">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e8489-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="e8489-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e8489-137">Minimum supported server</span></span><br/> | <span data-ttu-id="e8489-138">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e8489-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="e8489-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e8489-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="e8489-140"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="e8489-140"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8489-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e8489-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8489-142">Supporto client di livello inferiore grafica</span><span class="sxs-lookup"><span data-stu-id="e8489-142">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 




