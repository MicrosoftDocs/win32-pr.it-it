---
description: Rimuove un allegato, creato con NtGdiDdAttachSurface, tra due oggetti Surface in modalità kernel.
ms.assetid: 28037b42-a00c-4063-93ee-5d71761a95d8
title: Funzione NtGdiDdUnattachSurface (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdUnattachSurface
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 4513020a40c9b704e0b84e1a8b1c582be95db78f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103965938"
---
# <a name="ntgdiddunattachsurface-function"></a><span data-ttu-id="06b29-103">NtGdiDdUnattachSurface (funzione)</span><span class="sxs-lookup"><span data-stu-id="06b29-103">NtGdiDdUnattachSurface function</span></span>

<span data-ttu-id="06b29-104">\[Questa funzione è soggetta a modifiche a ogni revisione del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="06b29-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="06b29-105">Usare invece Microsoft DirectDraw e Microsoft Direct3DAPIs; Queste API isolano le applicazioni da tali modifiche del sistema operativo e nascondono molte altre difficoltà legate all'interazione diretta con i driver di visualizzazione.\]</span><span class="sxs-lookup"><span data-stu-id="06b29-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="06b29-106">Rimuove un allegato, creato con [**NtGdiDdAttachSurface**](-dxgkernel-ntgdiddattachsurface.md), tra due oggetti Surface in modalità kernel.</span><span class="sxs-lookup"><span data-stu-id="06b29-106">Removes an attachment, created with [**NtGdiDdAttachSurface**](-dxgkernel-ntgdiddattachsurface.md), between two kernel-mode surface objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="06b29-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="06b29-107">Syntax</span></span>


```C++
VOID APIENTRY NtGdiDdUnattachSurface(
  _In_ HANDLE hSurface,
  _In_ HANDLE hSurfaceAttached
);
```



## <a name="parameters"></a><span data-ttu-id="06b29-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="06b29-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06b29-109">*hSurface* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="06b29-109">*hSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06b29-110">Oggetto Surface in modalità kernel passato come parametro hSurfaceFrom a [**NtGdiDdAttachSurface**](-dxgkernel-ntgdiddattachsurface.md).</span><span class="sxs-lookup"><span data-stu-id="06b29-110">The kernel-mode surface object that was passed as the hSurfaceFrom parameter to [**NtGdiDdAttachSurface**](-dxgkernel-ntgdiddattachsurface.md).</span></span>

</dd> <dt>

<span data-ttu-id="06b29-111">*hSurfaceAttached* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="06b29-111">*hSurfaceAttached* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06b29-112">Oggetto Surface in modalità kernel passato come parametro hSurfaceTo a [ **NtGdiDdAttachSurface**](-dxgkernel-ntgdiddattachsurface.md)</span><span class="sxs-lookup"><span data-stu-id="06b29-112">The kernel-mode surface object that was passed as the hSurfaceTo parameter to [**NtGdiDdAttachSurface**](-dxgkernel-ntgdiddattachsurface.md)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06b29-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="06b29-113">Return value</span></span>

<span data-ttu-id="06b29-114">**NtGdiDdUnattachSurface** restituisce uno dei codici di callback seguenti.</span><span class="sxs-lookup"><span data-stu-id="06b29-114">**NtGdiDdUnattachSurface** returns one of the following callback codes.</span></span>



| <span data-ttu-id="06b29-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="06b29-115">Return code</span></span>                                                                                              | <span data-ttu-id="06b29-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="06b29-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="06b29-117"><dt>**\_driver DDHAL \_ gestito**</dt></span><span class="sxs-lookup"><span data-stu-id="06b29-117"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="06b29-118">Il driver ha eseguito l'operazione e ha restituito un codice restituito valido per l'operazione.</span><span class="sxs-lookup"><span data-stu-id="06b29-118">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="06b29-119">Se il codice è DD \_ OK, DirectDraw o Direct3D procede con la funzione.</span><span class="sxs-lookup"><span data-stu-id="06b29-119">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="06b29-120">In caso contrario, DirectDraw o Direct3D restituisce il codice di errore fornito dal driver e interrompe la funzione.</span><span class="sxs-lookup"><span data-stu-id="06b29-120">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="06b29-121"><dt>**\_NOTHANDLED driver \_ DDHAL**</dt></span><span class="sxs-lookup"><span data-stu-id="06b29-121"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="06b29-122">Il driver non ha commenti sull'operazione richiesta.</span><span class="sxs-lookup"><span data-stu-id="06b29-122">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="06b29-123">Se è necessario che il driver implementi un particolare callback, DirectDraw o Direct3D segnala una condizione di errore.</span><span class="sxs-lookup"><span data-stu-id="06b29-123">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="06b29-124">In caso contrario, DirectDraw o Direct3D gestisce l'operazione come se il callback del driver non fosse stato definito eseguendo l'implementazione di DirectDraw o Direct3D indipendente dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="06b29-124">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="06b29-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="06b29-125">Remarks</span></span>

<span data-ttu-id="06b29-126">È consigliabile che le applicazioni usino l'API DirectDraw, che gestisce gli allegati della superficie in modo più di livello superiore.</span><span class="sxs-lookup"><span data-stu-id="06b29-126">It is recommended that applications use the DirectDraw  API, which handles surface attachments in a higher-level manner.</span></span>

<span data-ttu-id="06b29-127">Non è necessario chiamare questa funzione perché il kernel eliminerà automaticamente tutti gli allegati quando viene chiamato [**NtGdiDdDestroySurface**](-dxgkernel-ntgdidddestroysurface.md) .</span><span class="sxs-lookup"><span data-stu-id="06b29-127">It is not necessary to call this function because the kernel will automatically destroy all attachments when [**NtGdiDdDestroySurface**](-dxgkernel-ntgdidddestroysurface.md) is called.</span></span>

## <a name="requirements"></a><span data-ttu-id="06b29-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="06b29-128">Requirements</span></span>



| <span data-ttu-id="06b29-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="06b29-129">Requirement</span></span> | <span data-ttu-id="06b29-130">Valore</span><span class="sxs-lookup"><span data-stu-id="06b29-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="06b29-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="06b29-131">Minimum supported client</span></span><br/> | <span data-ttu-id="06b29-132">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="06b29-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="06b29-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="06b29-133">Minimum supported server</span></span><br/> | <span data-ttu-id="06b29-134">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="06b29-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="06b29-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="06b29-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="06b29-136"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="06b29-136"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06b29-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="06b29-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06b29-138">Supporto client di livello inferiore grafica</span><span class="sxs-lookup"><span data-stu-id="06b29-138">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 




