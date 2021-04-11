---
description: Notifica al driver quando Microsoft DirectDraw esegue il capovolgimento da o verso una superficie di Windows Graphics Device Interface (GDI).
ms.assetid: e79be33a-24bc-477b-bc67-395fff74309c
title: Funzione NtGdiDdFlipToGDISurface (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdFlipToGDISurface
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 7e233bddf72c79507eab1fcefbf3de66460d228e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126756"
---
# <a name="ntgdiddfliptogdisurface-function"></a><span data-ttu-id="87a64-103">NtGdiDdFlipToGDISurface (funzione)</span><span class="sxs-lookup"><span data-stu-id="87a64-103">NtGdiDdFlipToGDISurface function</span></span>

<span data-ttu-id="87a64-104">\[Questa funzione è soggetta a modifiche a ogni revisione del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="87a64-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="87a64-105">Usare invece il DirectDraw e Microsoft Direct3DAPIs; Queste API isolano le applicazioni da tali modifiche del sistema operativo e nascondono molte altre difficoltà legate all'interazione diretta con i driver di visualizzazione.\]</span><span class="sxs-lookup"><span data-stu-id="87a64-105">Instead, use the DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="87a64-106">Notifica al driver quando Microsoft DirectDraw esegue il capovolgimento da o verso una superficie di Windows Graphics Device Interface (GDI).</span><span class="sxs-lookup"><span data-stu-id="87a64-106">Notifies the driver when Microsoft DirectDraw is flipping to or from a Windows Graphics Device Interface (GDI) surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="87a64-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="87a64-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdFlipToGDISurface(
  _In_    HANDLE                   hDirectDraw,
  _Inout_ PDD_FLIPTOGDISURFACEDATA puFlipToGDISurfaceData
);
```



## <a name="parameters"></a><span data-ttu-id="87a64-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="87a64-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87a64-109">*hDirectDraw* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="87a64-109">*hDirectDraw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87a64-110">Handle per l'oggetto DirectDraw in modalità kernel creato in precedenza.</span><span class="sxs-lookup"><span data-stu-id="87a64-110">Handle to previously created kernel-mode DirectDraw object.</span></span>

</dd> <dt>

<span data-ttu-id="87a64-111">*puFlipToGDISurfaceData* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="87a64-111">*puFlipToGDISurfaceData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="87a64-112">Puntatore a una struttura [DD \_ FLIPTOGDISURFACEDATA](https://msdn.microsoft.com/library/ms793922.aspx) che contiene le informazioni di notifica.</span><span class="sxs-lookup"><span data-stu-id="87a64-112">Pointer to a [DD\_FLIPTOGDISURFACEDATA](https://msdn.microsoft.com/library/ms793922.aspx) structure that contains the notification information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87a64-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="87a64-113">Return value</span></span>

<span data-ttu-id="87a64-114">**NtGdiDdFlipToGDISurface** restituisce uno dei codici di callback seguenti.</span><span class="sxs-lookup"><span data-stu-id="87a64-114">**NtGdiDdFlipToGDISurface** returns one of the following callback codes.</span></span>



| <span data-ttu-id="87a64-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="87a64-115">Return code</span></span>                                                                                              | <span data-ttu-id="87a64-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="87a64-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="87a64-117"><dt>**\_driver DDHAL \_ gestito**</dt></span><span class="sxs-lookup"><span data-stu-id="87a64-117"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="87a64-118">Il driver ha eseguito l'operazione e ha restituito un codice restituito valido per l'operazione.</span><span class="sxs-lookup"><span data-stu-id="87a64-118">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="87a64-119">Se il codice è DD \_ OK, DirectDraw o Direct3D procede con la funzione.</span><span class="sxs-lookup"><span data-stu-id="87a64-119">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="87a64-120">In caso contrario, DirectDraw o Direct3D restituisce il codice di errore fornito dal driver e interrompe la funzione.</span><span class="sxs-lookup"><span data-stu-id="87a64-120">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="87a64-121"><dt>**\_NOTHANDLED driver \_ DDHAL**</dt></span><span class="sxs-lookup"><span data-stu-id="87a64-121"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="87a64-122">Il driver non ha commenti sull'operazione richiesta.</span><span class="sxs-lookup"><span data-stu-id="87a64-122">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="87a64-123">Se è necessario che il driver implementi un particolare callback, DirectDraw o Direct3D segnala una condizione di errore.</span><span class="sxs-lookup"><span data-stu-id="87a64-123">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="87a64-124">In caso contrario, DirectDraw o Direct3D gestisce l'operazione come se il callback del driver non fosse stato definito eseguendo l'implementazione di DirectDraw o Direct3D indipendente dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="87a64-124">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="87a64-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="87a64-125">Requirements</span></span>



| <span data-ttu-id="87a64-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="87a64-126">Requirement</span></span> | <span data-ttu-id="87a64-127">Valore</span><span class="sxs-lookup"><span data-stu-id="87a64-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="87a64-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="87a64-128">Minimum supported client</span></span><br/> | <span data-ttu-id="87a64-129">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="87a64-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="87a64-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="87a64-130">Minimum supported server</span></span><br/> | <span data-ttu-id="87a64-131">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="87a64-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="87a64-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="87a64-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="87a64-133"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="87a64-133"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87a64-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="87a64-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87a64-135">Supporto client di livello inferiore grafica</span><span class="sxs-lookup"><span data-stu-id="87a64-135">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 




