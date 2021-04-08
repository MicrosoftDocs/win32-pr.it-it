---
description: Causa l'intercambio della memoria della superficie associata alla destinazione e alle superfici correnti.
ms.assetid: 2c557393-079e-48e5-b3a6-1157265d88e3
title: Funzione NtGdiDdFlip (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdFlip
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 1fd2d6f84f602fd07cc29a0efeae28209cb970a5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877741"
---
# <a name="ntgdiddflip-function"></a><span data-ttu-id="a3b37-103">NtGdiDdFlip (funzione)</span><span class="sxs-lookup"><span data-stu-id="a3b37-103">NtGdiDdFlip function</span></span>

<span data-ttu-id="a3b37-104">\[Questa funzione è soggetta a modifiche a ogni revisione del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="a3b37-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="a3b37-105">Usare invece Microsoft DirectDraw e Microsoft Direct3DAPIs; Queste API isolano le applicazioni da tali modifiche del sistema operativo e nascondono molte altre difficoltà legate all'interazione diretta con i driver di visualizzazione.\]</span><span class="sxs-lookup"><span data-stu-id="a3b37-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="a3b37-106">Causa l'intercambio della memoria della superficie associata alla destinazione e alle superfici correnti.</span><span class="sxs-lookup"><span data-stu-id="a3b37-106">Causes the surface memory associated with the target and current surfaces to be interchanged.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3b37-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a3b37-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdFlip(
  _In_    HANDLE       hSurfaceCurrent,
  _In_    HANDLE       hSurfaceTarget,
  _In_    HANDLE       hSurfaceCurrentLeft,
  _In_    HANDLE       hSurfaceTargetLeft,
  _Inout_ PDD_FLIPDATA puFlipData
);
```



## <a name="parameters"></a><span data-ttu-id="a3b37-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="a3b37-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3b37-109">*hSurfaceCurrent* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a3b37-109">*hSurfaceCurrent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3b37-110">Handle per la [struttura \_ \_ locale della superficie DD](https://msdn.microsoft.com/library/ms793861.aspx) che descrive la superficie corrente.</span><span class="sxs-lookup"><span data-stu-id="a3b37-110">Handle to the [DD\_SURFACE\_LOCAL](https://msdn.microsoft.com/library/ms793861.aspx) structure describing the current surface.</span></span>

</dd> <dt>

<span data-ttu-id="a3b37-111">*hSurfaceTarget* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a3b37-111">*hSurfaceTarget* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3b37-112">Handle per la [struttura \_ \_ locale della superficie DD](https://msdn.microsoft.com/library/ms793861.aspx) che descrive la superficie di destinazione, ovvero l'area in cui il driver deve essere invertito.</span><span class="sxs-lookup"><span data-stu-id="a3b37-112">Handle to the [DD\_SURFACE\_LOCAL](https://msdn.microsoft.com/library/ms793861.aspx) structure describing the target surface; that is, the surface to which the driver should flip.</span></span>

</dd> <dt>

<span data-ttu-id="a3b37-113">*hSurfaceCurrentLeft* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a3b37-113">*hSurfaceCurrentLeft* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3b37-114">Handle per la [struttura \_ \_ locale della superficie DD](https://msdn.microsoft.com/library/ms793861.aspx) che descrive la superficie di sinistra corrente.</span><span class="sxs-lookup"><span data-stu-id="a3b37-114">Handle to the [DD\_SURFACE\_LOCAL](https://msdn.microsoft.com/library/ms793861.aspx) structure describing the current left surface.</span></span>

</dd> <dt>

<span data-ttu-id="a3b37-115">*hSurfaceTargetLeft* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a3b37-115">*hSurfaceTargetLeft* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a3b37-116">Handle per la [struttura \_ \_ locale della superficie DD](https://msdn.microsoft.com/library/ms793861.aspx) che descrive la superficie di destinazione sinistra in cui eseguire il capovolgimento.</span><span class="sxs-lookup"><span data-stu-id="a3b37-116">Handle to the [DD\_SURFACE\_LOCAL](https://msdn.microsoft.com/library/ms793861.aspx) structure describing the left target surface to flip to.</span></span>

</dd> <dt>

<span data-ttu-id="a3b37-117">*puFlipData* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="a3b37-117">*puFlipData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a3b37-118">Puntatore a una struttura [DD \_ FLIPDATA](https://msdn.microsoft.com/library/ms794213.aspx) che contiene le informazioni necessarie per eseguire il capovolgimento.</span><span class="sxs-lookup"><span data-stu-id="a3b37-118">Pointer to a [DD\_FLIPDATA](https://msdn.microsoft.com/library/ms794213.aspx) structure that contains the information required to perform the flip.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3b37-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a3b37-119">Return value</span></span>

<span data-ttu-id="a3b37-120">**NtGdiDdFlip** restituisce uno dei codici di callback seguenti.</span><span class="sxs-lookup"><span data-stu-id="a3b37-120">**NtGdiDdFlip** returns one of the following callback codes.</span></span>



| <span data-ttu-id="a3b37-121">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="a3b37-121">Return code</span></span>                                                                                              | <span data-ttu-id="a3b37-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a3b37-122">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a3b37-123"><dt>**\_driver DDHAL \_ gestito**</dt></span><span class="sxs-lookup"><span data-stu-id="a3b37-123"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="a3b37-124">Il driver ha eseguito l'operazione e ha restituito un codice restituito valido per l'operazione.</span><span class="sxs-lookup"><span data-stu-id="a3b37-124">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="a3b37-125">Se il codice è DD \_ OK, DirectDraw o Direct3D procede con la funzione.</span><span class="sxs-lookup"><span data-stu-id="a3b37-125">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="a3b37-126">In caso contrario, DirectDraw o Direct3D restituisce il codice di errore fornito dal driver e interrompe la funzione.</span><span class="sxs-lookup"><span data-stu-id="a3b37-126">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="a3b37-127"><dt>**\_NOTHANDLED driver \_ DDHAL**</dt></span><span class="sxs-lookup"><span data-stu-id="a3b37-127"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="a3b37-128">Il driver non ha commenti sull'operazione richiesta.</span><span class="sxs-lookup"><span data-stu-id="a3b37-128">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="a3b37-129">Se è necessario che il driver implementi un particolare callback, DirectDraw o Direct3D segnala una condizione di errore.</span><span class="sxs-lookup"><span data-stu-id="a3b37-129">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="a3b37-130">In caso contrario, DirectDraw o Direct3D gestisce l'operazione come se il callback del driver non fosse stato definito eseguendo l'implementazione di DirectDraw o Direct3D indipendente dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a3b37-130">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="a3b37-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a3b37-131">Requirements</span></span>



| <span data-ttu-id="a3b37-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="a3b37-132">Requirement</span></span> | <span data-ttu-id="a3b37-133">Valore</span><span class="sxs-lookup"><span data-stu-id="a3b37-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a3b37-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a3b37-134">Minimum supported client</span></span><br/> | <span data-ttu-id="a3b37-135">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a3b37-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="a3b37-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a3b37-136">Minimum supported server</span></span><br/> | <span data-ttu-id="a3b37-137">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a3b37-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="a3b37-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a3b37-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="a3b37-139"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="a3b37-139"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a3b37-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a3b37-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3b37-141">Supporto client di livello inferiore grafica</span><span class="sxs-lookup"><span data-stu-id="a3b37-141">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 




