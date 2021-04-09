---
description: Notifica al driver che questo oggetto compensazione movimento non verrà più utilizzato. Il driver deve ora eseguire tutte le operazioni di pulizia necessarie.
ms.assetid: 1d86a564-efe1-4971-99ec-2c9a6aa59c89
title: Funzione NtGdiDdDestroyMoComp (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdDestroyMoComp
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: b7bc5915fe43bd4d48495b2b1beda8ee38f05fe9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877558"
---
# <a name="ntgdidddestroymocomp-function"></a><span data-ttu-id="89635-104">NtGdiDdDestroyMoComp (funzione)</span><span class="sxs-lookup"><span data-stu-id="89635-104">NtGdiDdDestroyMoComp function</span></span>

<span data-ttu-id="89635-105">\[Questa funzione è soggetta a modifiche a ogni revisione del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="89635-105">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="89635-106">Usare invece Microsoft DirectDraw e Microsoft Direct3DAPIs; Queste API isolano le applicazioni da tali modifiche del sistema operativo e nascondono molte altre difficoltà legate all'interazione diretta con i driver di visualizzazione.\]</span><span class="sxs-lookup"><span data-stu-id="89635-106">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="89635-107">Notifica al driver che questo oggetto compensazione movimento non verrà più utilizzato.</span><span class="sxs-lookup"><span data-stu-id="89635-107">Notifies the driver that this motion compensation object will no longer be used.</span></span> <span data-ttu-id="89635-108">Il driver deve ora eseguire tutte le operazioni di pulizia necessarie.</span><span class="sxs-lookup"><span data-stu-id="89635-108">The driver now needs to perform any necessary cleanup.</span></span>

## <a name="syntax"></a><span data-ttu-id="89635-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="89635-109">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdDestroyMoComp(
  _In_    HANDLE                hMoComp,
  _Inout_ PDD_DESTROYMOCOMPDATA puBeginFrameData
);
```



## <a name="parameters"></a><span data-ttu-id="89635-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="89635-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89635-111">*hMoComp* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="89635-111">*hMoComp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89635-112">Handle per una [**struttura \_ \_ locale DD MOTIONCOMP**](/windows/win32/api/ddrawint/ns-ddrawint-dd_motioncomp_local) che contiene una descrizione dell'oggetto compensazione movimento da eliminare definitivamente.</span><span class="sxs-lookup"><span data-stu-id="89635-112">Handle to a [**DD\_MOTIONCOMP\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_motioncomp_local) structure that contains a description of the motion compensation object to be destroyed.</span></span>

</dd> <dt>

<span data-ttu-id="89635-113">*puBeginFrameData* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="89635-113">*puBeginFrameData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="89635-114">Puntatore a una struttura [**DD \_ DESTROYMOCOMPDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_destroymocompdata) che contiene le informazioni necessarie per completare la compensazione del movimento.</span><span class="sxs-lookup"><span data-stu-id="89635-114">Pointer to a [**DD\_DESTROYMOCOMPDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_destroymocompdata) structure that contains the information needed to finish motion compensation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89635-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="89635-115">Return value</span></span>

<span data-ttu-id="89635-116">**NtGdiDdDestroyMoComp** restituisce uno dei codici di callback seguenti.</span><span class="sxs-lookup"><span data-stu-id="89635-116">**NtGdiDdDestroyMoComp** returns one of the following callback codes.</span></span>



| <span data-ttu-id="89635-117">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="89635-117">Return code</span></span>                                                                                              | <span data-ttu-id="89635-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="89635-118">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="89635-119"><dt>**\_driver DDHAL \_ gestito**</dt></span><span class="sxs-lookup"><span data-stu-id="89635-119"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="89635-120">Il driver ha eseguito l'operazione e ha restituito un codice restituito valido per l'operazione.</span><span class="sxs-lookup"><span data-stu-id="89635-120">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="89635-121">Se il codice è DD \_ OK, DirectDraw o Direct3D procede con la funzione.</span><span class="sxs-lookup"><span data-stu-id="89635-121">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="89635-122">In caso contrario, DirectDraw o Direct3D restituisce il codice di errore fornito dal driver e interrompe la funzione.</span><span class="sxs-lookup"><span data-stu-id="89635-122">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="89635-123"><dt>**\_NOTHANDLED driver \_ DDHAL**</dt></span><span class="sxs-lookup"><span data-stu-id="89635-123"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="89635-124">Il driver non ha commenti sull'operazione richiesta.</span><span class="sxs-lookup"><span data-stu-id="89635-124">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="89635-125">Se è necessario che il driver implementi un particolare callback, DirectDraw o Direct3D segnala una condizione di errore.</span><span class="sxs-lookup"><span data-stu-id="89635-125">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="89635-126">In caso contrario, DirectDraw o Direct3D gestisce l'operazione come se il callback del driver non fosse stato definito eseguendo l'implementazione di DirectDraw o Direct3D indipendente dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="89635-126">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="89635-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="89635-127">Remarks</span></span>

<span data-ttu-id="89635-128">Per ulteriori informazioni, vedere Microsoft DirectX Video Acceleration Driver Development Kit (DDK).</span><span class="sxs-lookup"><span data-stu-id="89635-128">For more information, see the Microsoft DirectX Video Acceleration Driver Development Kit (DDK).</span></span>

## <a name="requirements"></a><span data-ttu-id="89635-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="89635-129">Requirements</span></span>



| <span data-ttu-id="89635-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="89635-130">Requirement</span></span> | <span data-ttu-id="89635-131">Valore</span><span class="sxs-lookup"><span data-stu-id="89635-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="89635-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="89635-132">Minimum supported client</span></span><br/> | <span data-ttu-id="89635-133">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="89635-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="89635-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="89635-134">Minimum supported server</span></span><br/> | <span data-ttu-id="89635-135">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="89635-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="89635-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="89635-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="89635-137"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="89635-137"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89635-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="89635-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89635-139">Supporto client di livello inferiore grafica</span><span class="sxs-lookup"><span data-stu-id="89635-139">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
