---
description: Esegue una query sullo stato blit della superficie specificata.
ms.assetid: 0221bdc6-2146-4f4d-afb5-d1f701446d5e
title: Funzione NtGdiDdGetBltStatus (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdGetBltStatus
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 381de7f8c360f222a004786834fa36e92f1220d9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304847"
---
# <a name="ntgdiddgetbltstatus-function"></a><span data-ttu-id="71008-103">NtGdiDdGetBltStatus (funzione)</span><span class="sxs-lookup"><span data-stu-id="71008-103">NtGdiDdGetBltStatus function</span></span>

<span data-ttu-id="71008-104">\[Questa funzione è soggetta a modifiche a ogni revisione del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="71008-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="71008-105">Usare invece Microsoft DirectDraw e Microsoft Direct3DAPIs; Queste API isolano le applicazioni da tali modifiche del sistema operativo e nascondono molte altre difficoltà legate all'interazione diretta con i driver di visualizzazione.\]</span><span class="sxs-lookup"><span data-stu-id="71008-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="71008-106">Esegue una query sullo stato blit della superficie specificata.</span><span class="sxs-lookup"><span data-stu-id="71008-106">Queries the blit status of the specified surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="71008-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="71008-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdGetBltStatus(
  _In_    HANDLE               hSurface,
  _Inout_ PDD_GETBLTSTATUSDATA puGetBltStatusData
);
```



## <a name="parameters"></a><span data-ttu-id="71008-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="71008-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71008-109">*hSurface* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="71008-109">*hSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71008-110">Handle per una [struttura \_ \_ locale della superficie DD](https://msdn.microsoft.com/library/ms793861.aspx) che rappresenta l'area di cui viene eseguita la query sullo stato blit.</span><span class="sxs-lookup"><span data-stu-id="71008-110">Handle to a [DD\_SURFACE\_LOCAL](https://msdn.microsoft.com/library/ms793861.aspx) structure representing the surface whose blit status is being queried.</span></span>

</dd> <dt>

<span data-ttu-id="71008-111">*puGetBltStatusData* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="71008-111">*puGetBltStatusData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="71008-112">Puntatore a una struttura [DD \_ GETBLTSTATUSDATA](https://msdn.microsoft.com/library/ms794243.aspx) che contiene le informazioni necessarie per eseguire la query sullo stato blit.</span><span class="sxs-lookup"><span data-stu-id="71008-112">Pointer to a [DD\_GETBLTSTATUSDATA](https://msdn.microsoft.com/library/ms794243.aspx) structure that contains the information required to perform the blit status query.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71008-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="71008-113">Return value</span></span>

<span data-ttu-id="71008-114">**NtGdiDdGetBltStatus** restituisce uno dei codici di callback seguenti.</span><span class="sxs-lookup"><span data-stu-id="71008-114">**NtGdiDdGetBltStatus** returns one of the following callback codes.</span></span>



| <span data-ttu-id="71008-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="71008-115">Return code</span></span>                                                                                              | <span data-ttu-id="71008-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="71008-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="71008-117"><dt>**\_driver DDHAL \_ gestito**</dt></span><span class="sxs-lookup"><span data-stu-id="71008-117"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="71008-118">Il driver ha eseguito l'operazione e ha restituito un codice restituito valido per l'operazione.</span><span class="sxs-lookup"><span data-stu-id="71008-118">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="71008-119">Se il codice è DD \_ OK, DirectDraw o Direct3D procede con la funzione.</span><span class="sxs-lookup"><span data-stu-id="71008-119">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="71008-120">In caso contrario, DirectDraw o Direct3D restituisce il codice di errore fornito dal driver e interrompe la funzione.</span><span class="sxs-lookup"><span data-stu-id="71008-120">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="71008-121"><dt>**\_NOTHANDLED driver \_ DDHAL**</dt></span><span class="sxs-lookup"><span data-stu-id="71008-121"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="71008-122">Il driver non ha commenti sull'operazione richiesta.</span><span class="sxs-lookup"><span data-stu-id="71008-122">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="71008-123">Se è necessario che il driver implementi un particolare callback, DirectDraw o Direct3D segnala una condizione di errore.</span><span class="sxs-lookup"><span data-stu-id="71008-123">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="71008-124">In caso contrario, DirectDraw o Direct3D gestisce l'operazione come se il callback del driver non fosse stato definito eseguendo l'implementazione di DirectDraw o Direct3D indipendente dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="71008-124">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="71008-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="71008-125">Requirements</span></span>



| <span data-ttu-id="71008-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="71008-126">Requirement</span></span> | <span data-ttu-id="71008-127">Valore</span><span class="sxs-lookup"><span data-stu-id="71008-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="71008-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="71008-128">Minimum supported client</span></span><br/> | <span data-ttu-id="71008-129">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="71008-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="71008-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="71008-130">Minimum supported server</span></span><br/> | <span data-ttu-id="71008-131">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="71008-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="71008-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="71008-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="71008-133"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="71008-133"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71008-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="71008-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71008-135">Supporto client di livello inferiore grafica</span><span class="sxs-lookup"><span data-stu-id="71008-135">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 




