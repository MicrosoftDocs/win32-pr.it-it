---
description: Esegue una query sulla quantità di memoria libera nell'heap del managed memory del driver.
ms.assetid: d7f8792b-a515-4e70-9474-6a3474b6612b
title: Funzione NtGdiD3DContextDestroyAll (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiD3DContextDestroyAll
api_type:
- HeaderDef
api_location:
- Ntgdi.h
ms.openlocfilehash: 8bb42c902555568ebe7a26656cd188e9c8e40213
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877561"
---
# <a name="ntgdid3dcontextdestroyall-function"></a><span data-ttu-id="9656f-103">NtGdiD3DContextDestroyAll (funzione)</span><span class="sxs-lookup"><span data-stu-id="9656f-103">NtGdiD3DContextDestroyAll function</span></span>

<span data-ttu-id="9656f-104">\[Questa funzione è soggetta a modifiche a ogni revisione del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="9656f-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="9656f-105">Usare invece Microsoft DirectDraw e Microsoft Direct3DAPIs; Queste API isolano le applicazioni da tali modifiche del sistema operativo e nascondono molte altre difficoltà legate all'interazione diretta con i driver di visualizzazione.\]</span><span class="sxs-lookup"><span data-stu-id="9656f-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="9656f-106">Esegue una query sulla quantità di memoria libera nell'heap del managed memory del driver.</span><span class="sxs-lookup"><span data-stu-id="9656f-106">Queries the amount of free memory in the driver-managed memory heap.</span></span>

## <a name="syntax"></a><span data-ttu-id="9656f-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9656f-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiD3DContextDestroyAll(void);
```



## <a name="parameters"></a><span data-ttu-id="9656f-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="9656f-108">Parameters</span></span>

<span data-ttu-id="9656f-109">Questa funzione non ha parametri.</span><span class="sxs-lookup"><span data-stu-id="9656f-109">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9656f-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9656f-110">Return value</span></span>

<span data-ttu-id="9656f-111">**NtGdiD3DContextDestroyAll** restituisce uno dei codici di callback seguenti.</span><span class="sxs-lookup"><span data-stu-id="9656f-111">**NtGdiD3DContextDestroyAll** returns one of the following callback codes.</span></span>



| <span data-ttu-id="9656f-112">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="9656f-112">Return code</span></span>                                                                                              | <span data-ttu-id="9656f-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9656f-113">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9656f-114"><dt>**\_driver DDHAL \_ gestito**</dt></span><span class="sxs-lookup"><span data-stu-id="9656f-114"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="9656f-115">Il driver ha eseguito l'operazione e ha restituito un codice restituito valido per l'operazione.</span><span class="sxs-lookup"><span data-stu-id="9656f-115">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="9656f-116">Se il codice è DD \_ OK, DirectDraw o Direct3D procede con la funzione.</span><span class="sxs-lookup"><span data-stu-id="9656f-116">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="9656f-117">In caso contrario, DirectDraw o Direct3D restituisce il codice di errore fornito dal driver e interrompe la funzione.</span><span class="sxs-lookup"><span data-stu-id="9656f-117">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="9656f-118"><dt>**\_NOTHANDLED driver \_ DDHAL**</dt></span><span class="sxs-lookup"><span data-stu-id="9656f-118"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="9656f-119">Il driver non ha commenti sull'operazione richiesta.</span><span class="sxs-lookup"><span data-stu-id="9656f-119">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="9656f-120">Se è necessario che il driver implementi un particolare callback, DirectDraw o Direct3D segnala una condizione di errore.</span><span class="sxs-lookup"><span data-stu-id="9656f-120">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="9656f-121">In caso contrario, DirectDraw o Direct3D gestisce l'operazione come se il callback del driver non fosse stato definito eseguendo l'implementazione di DirectDraw o Direct3D indipendente dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9656f-121">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="9656f-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9656f-122">Requirements</span></span>



| <span data-ttu-id="9656f-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="9656f-123">Requirement</span></span> | <span data-ttu-id="9656f-124">Valore</span><span class="sxs-lookup"><span data-stu-id="9656f-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9656f-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9656f-125">Minimum supported client</span></span><br/> | <span data-ttu-id="9656f-126">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="9656f-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="9656f-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9656f-127">Minimum supported server</span></span><br/> | <span data-ttu-id="9656f-128">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="9656f-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="9656f-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9656f-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="9656f-130"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="9656f-130"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9656f-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9656f-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9656f-132">Supporto client di livello inferiore grafica</span><span class="sxs-lookup"><span data-stu-id="9656f-132">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 




