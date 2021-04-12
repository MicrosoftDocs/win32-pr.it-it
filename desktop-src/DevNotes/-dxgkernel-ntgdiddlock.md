---
description: Blocca un'area specificata di memoria della superficie e fornisce un puntatore valido a un blocco di memoria associato a una superficie.
ms.assetid: 02810576-73d8-431d-ab41-3244dcff311f
title: Funzione NtGdiDdLock (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdLock
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 3ddf40ae992b6b463886396ba026ec08293bb027
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104482908"
---
# <a name="ntgdiddlock-function"></a><span data-ttu-id="28dec-103">NtGdiDdLock (funzione)</span><span class="sxs-lookup"><span data-stu-id="28dec-103">NtGdiDdLock function</span></span>

<span data-ttu-id="28dec-104">\[Questa funzione è soggetta a modifiche a ogni revisione del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="28dec-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="28dec-105">Usare invece Microsoft DirectDraw e Microsoft Direct3DAPIs; Queste API isolano le applicazioni da tali modifiche del sistema operativo e nascondono molte altre difficoltà legate all'interazione diretta con i driver di visualizzazione.\]</span><span class="sxs-lookup"><span data-stu-id="28dec-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="28dec-106">Blocca un'area specificata di memoria della superficie e fornisce un puntatore valido a un blocco di memoria associato a una superficie.</span><span class="sxs-lookup"><span data-stu-id="28dec-106">Locks a specified area of surface memory and provides a valid pointer to a block of memory associated with a surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="28dec-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="28dec-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdLock(
  _In_    HANDLE       hSurface,
  _Inout_ PDD_LOCKDATA puLockData,
  _In_    HDC          hdcClip
);
```



## <a name="parameters"></a><span data-ttu-id="28dec-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="28dec-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28dec-109">*hSurface* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="28dec-109">*hSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28dec-110">Handle per una [**struttura \_ \_ locale della superficie DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) che descrive la superficie associata all'area di memoria da bloccare.</span><span class="sxs-lookup"><span data-stu-id="28dec-110">Handle to a [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structure that describes the surface associated with the memory region to be locked down.</span></span>

</dd> <dt>

<span data-ttu-id="28dec-111">*puLockData* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="28dec-111">*puLockData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="28dec-112">Puntatore a una struttura [**DD \_ LOCKDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_lockdata) che contiene le informazioni necessarie per eseguire il blocco.</span><span class="sxs-lookup"><span data-stu-id="28dec-112">Pointer to a [**DD\_LOCKDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_lockdata) structure that contains the information required to perform the lockdown.</span></span>

</dd> <dt>

<span data-ttu-id="28dec-113">*hdcClip* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="28dec-113">*hdcClip* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28dec-114">Riservato.</span><span class="sxs-lookup"><span data-stu-id="28dec-114">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28dec-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="28dec-115">Return value</span></span>

<span data-ttu-id="28dec-116">**NtGdiDdLock** restituisce uno dei codici di callback seguenti.</span><span class="sxs-lookup"><span data-stu-id="28dec-116">**NtGdiDdLock** returns one of the following callback codes.</span></span>



| <span data-ttu-id="28dec-117">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="28dec-117">Return code</span></span>                                                                                              | <span data-ttu-id="28dec-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="28dec-118">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="28dec-119"><dt>**\_driver DDHAL \_ gestito**</dt></span><span class="sxs-lookup"><span data-stu-id="28dec-119"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="28dec-120">Il driver ha eseguito l'operazione e ha restituito un codice restituito valido per l'operazione.</span><span class="sxs-lookup"><span data-stu-id="28dec-120">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="28dec-121">Se il codice è DD \_ OK, DirectDraw o Direct3D procede con la funzione.</span><span class="sxs-lookup"><span data-stu-id="28dec-121">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="28dec-122">In caso contrario, DirectDraw o Direct3D restituisce il codice di errore fornito dal driver e interrompe la funzione.</span><span class="sxs-lookup"><span data-stu-id="28dec-122">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="28dec-123"><dt>**\_NOTHANDLED driver \_ DDHAL**</dt></span><span class="sxs-lookup"><span data-stu-id="28dec-123"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="28dec-124">Il driver non ha commenti sull'operazione richiesta.</span><span class="sxs-lookup"><span data-stu-id="28dec-124">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="28dec-125">Se è necessario che il driver implementi un particolare callback, DirectDraw o Direct3D segnala una condizione di errore.</span><span class="sxs-lookup"><span data-stu-id="28dec-125">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="28dec-126">In caso contrario, DirectDraw o Direct3D gestisce l'operazione come se il callback del driver non fosse stato definito eseguendo l'implementazione di DirectDraw o Direct3D indipendente dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="28dec-126">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="28dec-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="28dec-127">Requirements</span></span>



| <span data-ttu-id="28dec-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="28dec-128">Requirement</span></span> | <span data-ttu-id="28dec-129">Valore</span><span class="sxs-lookup"><span data-stu-id="28dec-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="28dec-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="28dec-130">Minimum supported client</span></span><br/> | <span data-ttu-id="28dec-131">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="28dec-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="28dec-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="28dec-132">Minimum supported server</span></span><br/> | <span data-ttu-id="28dec-133">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="28dec-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="28dec-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="28dec-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="28dec-135"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="28dec-135"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28dec-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="28dec-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28dec-137">Supporto client di livello inferiore grafica</span><span class="sxs-lookup"><span data-stu-id="28dec-137">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
