---
description: Utilizzato dai runtime di Microsoft DirectDraw e Microsoft Direct3D per ottenere informazioni dal driver sullo stato corrente.
ms.assetid: a7697e0c-9485-4a9c-b211-67ce07dc3604
title: Funzione NtGdiD3DGetDriverState (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiD3DGetDriverState
api_type:
- HeaderDef
api_location:
- Ntgdi.h
ms.openlocfilehash: c88f2fde4d848aac5ecae3c60aef77d4c6b783cb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304465"
---
# <a name="ntgdid3dgetdriverstate-function"></a><span data-ttu-id="fe688-103">NtGdiD3DGetDriverState (funzione)</span><span class="sxs-lookup"><span data-stu-id="fe688-103">NtGdiD3DGetDriverState function</span></span>

<span data-ttu-id="fe688-104">\[Questa funzione è soggetta a modifiche a ogni revisione del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="fe688-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="fe688-105">In alternativa, usare i DirectDraw e Direct3DAPIs; Queste API isolano le applicazioni da tali modifiche del sistema operativo e nascondono molte altre difficoltà legate all'interazione diretta con i driver di visualizzazione.\]</span><span class="sxs-lookup"><span data-stu-id="fe688-105">Instead, use the DirectDraw and Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="fe688-106">Utilizzato dai runtime di Microsoft DirectDraw e Microsoft Direct3D per ottenere informazioni dal driver sullo stato corrente.</span><span class="sxs-lookup"><span data-stu-id="fe688-106">Used by both the Microsoft DirectDraw and Microsoft Direct3D runtimes to obtain information from the driver about its current state.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe688-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fe688-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiD3DGetDriverState(
  _Inout_ PDD_GETDRIVERSTATEDATA pdata
);
```



## <a name="parameters"></a><span data-ttu-id="fe688-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="fe688-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe688-109">*pData* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="fe688-109">*pdata* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="fe688-110">Puntatore a una struttura [**DD \_ GETDRIVERSTATEDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_getdriverstatedata) che descrive lo stato del driver.</span><span class="sxs-lookup"><span data-stu-id="fe688-110">Pointer to a [**DD\_GETDRIVERSTATEDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_getdriverstatedata) structure that describes the state of the driver.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe688-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fe688-111">Return value</span></span>

<span data-ttu-id="fe688-112">**NtGdiD3DGetDriverState** restituisce uno dei codici di callback seguenti.</span><span class="sxs-lookup"><span data-stu-id="fe688-112">**NtGdiD3DGetDriverState** returns one of the following callback codes.</span></span>



| <span data-ttu-id="fe688-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="fe688-113">Return code</span></span>                                                                                              | <span data-ttu-id="fe688-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fe688-114">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="fe688-115"><dt>**\_driver DDHAL \_ gestito**</dt></span><span class="sxs-lookup"><span data-stu-id="fe688-115"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="fe688-116">Il driver ha eseguito l'operazione e ha restituito un codice restituito valido per l'operazione.</span><span class="sxs-lookup"><span data-stu-id="fe688-116">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="fe688-117">Se il codice è DD \_ OK, DirectDraw o Direct3D procede con la funzione.</span><span class="sxs-lookup"><span data-stu-id="fe688-117">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="fe688-118">In caso contrario, DirectDraw o Direct3D restituisce il codice di errore fornito dal driver e interrompe la funzione.</span><span class="sxs-lookup"><span data-stu-id="fe688-118">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="fe688-119"><dt>**\_NOTHANDLED driver \_ DDHAL**</dt></span><span class="sxs-lookup"><span data-stu-id="fe688-119"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="fe688-120">Il driver non ha commenti sull'operazione richiesta.</span><span class="sxs-lookup"><span data-stu-id="fe688-120">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="fe688-121">Se è necessario che il driver implementi un particolare callback, DirectDraw o Direct3D segnala una condizione di errore.</span><span class="sxs-lookup"><span data-stu-id="fe688-121">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="fe688-122">In caso contrario, DirectDraw o Direct3D gestisce l'operazione come se il callback del driver non fosse stato definito eseguendo l'implementazione di DirectDraw o Direct3D indipendente dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fe688-122">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="fe688-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fe688-123">Requirements</span></span>



| <span data-ttu-id="fe688-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="fe688-124">Requirement</span></span> | <span data-ttu-id="fe688-125">Valore</span><span class="sxs-lookup"><span data-stu-id="fe688-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fe688-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fe688-126">Minimum supported client</span></span><br/> | <span data-ttu-id="fe688-127">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="fe688-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="fe688-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fe688-128">Minimum supported server</span></span><br/> | <span data-ttu-id="fe688-129">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="fe688-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="fe688-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fe688-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="fe688-131"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="fe688-131"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe688-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fe688-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe688-133">Supporto client di livello inferiore grafica</span><span class="sxs-lookup"><span data-stu-id="fe688-133">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
