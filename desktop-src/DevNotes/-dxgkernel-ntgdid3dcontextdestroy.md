---
description: Elimina il contesto specificato.
ms.assetid: ac113178-bdb6-4601-940d-6b00b339904d
title: Funzione NtGdiD3DContextDestroy (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiD3DContextDestroy
api_type:
- HeaderDef
api_location:
- Ntgdi.h
ms.openlocfilehash: 19799c3895072011dd104deec18664d1ffc52b9d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523634"
---
# <a name="ntgdid3dcontextdestroy-function"></a><span data-ttu-id="d9ecc-103">NtGdiD3DContextDestroy (funzione)</span><span class="sxs-lookup"><span data-stu-id="d9ecc-103">NtGdiD3DContextDestroy function</span></span>

<span data-ttu-id="d9ecc-104">\[Questa funzione è soggetta a modifiche a ogni revisione del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="d9ecc-105">Usare invece Microsoft DirectDraw e Microsoft Direct3DAPIs; Queste API isolano le applicazioni da tali modifiche del sistema operativo e nascondono molte altre difficoltà legate all'interazione diretta con i driver di visualizzazione.\]</span><span class="sxs-lookup"><span data-stu-id="d9ecc-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="d9ecc-106">Elimina il contesto specificato.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-106">Deletes the specified context.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9ecc-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d9ecc-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiD3DContextDestroy(
  _In_ LPD3DNTHAL_CONTEXTDESTROYDATA pContextDestroyData
);
```



## <a name="parameters"></a><span data-ttu-id="d9ecc-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="d9ecc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9ecc-109">*pContextDestroyData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d9ecc-109">*pContextDestroyData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9ecc-110">Puntatore a una [**struttura \_ CONTEXTDESTROYDATA di D3DNTHAL**](/windows-hardware/drivers/ddi/) contenente le informazioni necessarie per l'eliminazione del contesto da parte del driver.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-110">Pointer to a [**D3DNTHAL\_CONTEXTDESTROYDATA**](/windows-hardware/drivers/ddi/) structure that contains the information required for the driver to destroy the context.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9ecc-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d9ecc-111">Return value</span></span>

<span data-ttu-id="d9ecc-112">**NtGdiD3DContextDestroy** restituisce uno dei codici di callback seguenti.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-112">**NtGdiD3DContextDestroy** returns one of the following callback codes.</span></span>



| <span data-ttu-id="d9ecc-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="d9ecc-113">Return code</span></span>                                                                                              | <span data-ttu-id="d9ecc-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d9ecc-114">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d9ecc-115"><dt>**\_driver DDHAL \_ gestito**</dt></span><span class="sxs-lookup"><span data-stu-id="d9ecc-115"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="d9ecc-116">Il driver ha eseguito l'operazione e ha restituito un codice restituito valido per l'operazione.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-116">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="d9ecc-117">Se il codice è DD \_ OK, DirectDraw o Direct3D procede con la funzione.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-117">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="d9ecc-118">In caso contrario, DirectDraw o Direct3D restituisce il codice di errore fornito dal driver e interrompe la funzione.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-118">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="d9ecc-119"><dt>**\_NOTHANDLED driver \_ DDHAL**</dt></span><span class="sxs-lookup"><span data-stu-id="d9ecc-119"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="d9ecc-120">Il driver non ha commenti sull'operazione richiesta.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-120">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="d9ecc-121">Se è necessario che il driver implementi un particolare callback, DirectDraw o Direct3D segnala una condizione di errore.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-121">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="d9ecc-122">In caso contrario, DirectDraw o Direct3D gestisce l'operazione come se il callback del driver non fosse stato definito eseguendo l'implementazione di DirectDraw o Direct3D indipendente dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d9ecc-122">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="d9ecc-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d9ecc-123">Requirements</span></span>



| <span data-ttu-id="d9ecc-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="d9ecc-124">Requirement</span></span> | <span data-ttu-id="d9ecc-125">Valore</span><span class="sxs-lookup"><span data-stu-id="d9ecc-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d9ecc-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d9ecc-126">Minimum supported client</span></span><br/> | <span data-ttu-id="d9ecc-127">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d9ecc-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="d9ecc-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d9ecc-128">Minimum supported server</span></span><br/> | <span data-ttu-id="d9ecc-129">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d9ecc-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="d9ecc-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d9ecc-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="d9ecc-131"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="d9ecc-131"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9ecc-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d9ecc-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9ecc-133">Supporto client di livello inferiore grafica</span><span class="sxs-lookup"><span data-stu-id="d9ecc-133">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
