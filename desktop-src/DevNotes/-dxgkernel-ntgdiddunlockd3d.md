---
description: Utilizzato per rilasciare un blocco mantenuto su un'area specificata della memoria del buffer.
ms.assetid: ec06829b-2b3a-45db-9ecd-d4c7cf67b8ae
title: Funzione NtGdiDdUnlockD3D (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdUnlockD3D
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 207f647cadc81a797d71a607fdfd6f73ea38f475
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104125919"
---
# <a name="ntgdiddunlockd3d-function"></a><span data-ttu-id="ef122-103">NtGdiDdUnlockD3D (funzione)</span><span class="sxs-lookup"><span data-stu-id="ef122-103">NtGdiDdUnlockD3D function</span></span>

<span data-ttu-id="ef122-104">\[Questa funzione è soggetta a modifiche a ogni revisione del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="ef122-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="ef122-105">Usare invece Microsoft DirectDraw e Microsoft Direct3DAPIs; Queste API isolano le applicazioni da tali modifiche del sistema operativo e nascondono molte altre difficoltà legate all'interazione diretta con i driver di visualizzazione.\]</span><span class="sxs-lookup"><span data-stu-id="ef122-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="ef122-106">Utilizzato per rilasciare un blocco mantenuto su un'area specificata della memoria del buffer.</span><span class="sxs-lookup"><span data-stu-id="ef122-106">Used to release a lock held on a specified area of buffer memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef122-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ef122-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdUnlockD3D(
  _In_    HANDLE         hSurface,
  _Inout_ PDD_UNLOCKDATA puUnlockData
);
```



## <a name="parameters"></a><span data-ttu-id="ef122-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="ef122-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef122-109">*hSurface* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ef122-109">*hSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef122-110">Puntatore a una [**struttura \_ \_ locale della superficie DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) che descrive la superficie da sbloccare.</span><span class="sxs-lookup"><span data-stu-id="ef122-110">Pointer to a [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structure that describes the surface to be unlocked.</span></span>

</dd> <dt>

<span data-ttu-id="ef122-111">*puUnlockData* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="ef122-111">*puUnlockData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ef122-112">Puntatore a una struttura [**DD \_ UNLOCKDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_unlockdata) che contiene le informazioni necessarie per eseguire il rilascio del blocco.</span><span class="sxs-lookup"><span data-stu-id="ef122-112">Pointer to a [**DD\_UNLOCKDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_unlockdata) structure that contains the information required to perform the lock release.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef122-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ef122-113">Return value</span></span>

<span data-ttu-id="ef122-114">**NtGdiDdUnlockD3D** restituisce uno dei codici di callback seguenti.</span><span class="sxs-lookup"><span data-stu-id="ef122-114">**NtGdiDdUnlockD3D** returns one of the following callback codes.</span></span>



| <span data-ttu-id="ef122-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="ef122-115">Return code</span></span>                                                                                              | <span data-ttu-id="ef122-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ef122-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ef122-117"><dt>**\_driver DDHAL \_ gestito**</dt></span><span class="sxs-lookup"><span data-stu-id="ef122-117"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="ef122-118">Il driver ha eseguito l'operazione e ha restituito un codice restituito valido per l'operazione.</span><span class="sxs-lookup"><span data-stu-id="ef122-118">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="ef122-119">Se il codice è DD \_ OK, DirectDraw o Direct3D procede con la funzione.</span><span class="sxs-lookup"><span data-stu-id="ef122-119">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="ef122-120">In caso contrario, DirectDraw o Direct3D restituisce il codice di errore fornito dal driver e interrompe la funzione.</span><span class="sxs-lookup"><span data-stu-id="ef122-120">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="ef122-121"><dt>**\_NOTHANDLED driver \_ DDHAL**</dt></span><span class="sxs-lookup"><span data-stu-id="ef122-121"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="ef122-122">Il driver non ha commenti sull'operazione richiesta.</span><span class="sxs-lookup"><span data-stu-id="ef122-122">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="ef122-123">Se è necessario che il driver implementi un particolare callback, DirectDraw o Direct3D segnala una condizione di errore.</span><span class="sxs-lookup"><span data-stu-id="ef122-123">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="ef122-124">In caso contrario, DirectDraw o Direct3D gestisce l'operazione come se il callback del driver non fosse stato definito eseguendo l'implementazione di DirectDraw o Direct3D indipendente dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ef122-124">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="ef122-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ef122-125">Requirements</span></span>



| <span data-ttu-id="ef122-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="ef122-126">Requirement</span></span> | <span data-ttu-id="ef122-127">Valore</span><span class="sxs-lookup"><span data-stu-id="ef122-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ef122-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ef122-128">Minimum supported client</span></span><br/> | <span data-ttu-id="ef122-129">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ef122-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="ef122-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ef122-130">Minimum supported server</span></span><br/> | <span data-ttu-id="ef122-131">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ef122-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="ef122-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ef122-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="ef122-133"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="ef122-133"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef122-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ef122-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef122-135">Supporto client di livello inferiore grafica</span><span class="sxs-lookup"><span data-stu-id="ef122-135">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
