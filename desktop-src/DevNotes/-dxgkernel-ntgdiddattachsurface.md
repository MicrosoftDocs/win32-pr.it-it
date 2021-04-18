---
description: Connette due rappresentazioni di superficie in modalità kernel.
ms.assetid: f1b1859f-8b62-4385-9e8a-296086446fe7
title: Funzione NtGdiDdAttachSurface (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdAttachSurface
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: a3d099e7b3a3106e0e1e4285b37d2ea205baf3d5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304568"
---
# <a name="ntgdiddattachsurface-function"></a><span data-ttu-id="6a271-103">NtGdiDdAttachSurface (funzione)</span><span class="sxs-lookup"><span data-stu-id="6a271-103">NtGdiDdAttachSurface function</span></span>

<span data-ttu-id="6a271-104">\[Questa funzione è soggetta a modifiche a ogni revisione del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="6a271-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="6a271-105">Usare invece Microsoft DirectDraw e Microsoft Direct3DAPIs; Queste API isolano le applicazioni da tali modifiche del sistema operativo e nascondono molte altre difficoltà legate all'interazione diretta con i driver di visualizzazione.\]</span><span class="sxs-lookup"><span data-stu-id="6a271-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="6a271-106">Connette due rappresentazioni di superficie in modalità kernel.</span><span class="sxs-lookup"><span data-stu-id="6a271-106">Attaches two kernel-mode surface representations.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a271-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6a271-107">Syntax</span></span>


```C++
BOOL APIENTRY NtGdiDdAttachSurface(
  _In_ HANDLE hSurfaceFrom,
  _In_ HANDLE hSurfaceTo
);
```



## <a name="parameters"></a><span data-ttu-id="6a271-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="6a271-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a271-109">*hSurfaceFrom* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6a271-109">*hSurfaceFrom* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a271-110">Handle per l'oggetto Surface in modalità kernel che sarà il punto iniziale del nuovo allegato.</span><span class="sxs-lookup"><span data-stu-id="6a271-110">Handle to kernel-mode surface object that will be the start point of the new attachment.</span></span>

</dd> <dt>

<span data-ttu-id="6a271-111">*hSurfaceTo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6a271-111">*hSurfaceTo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a271-112">Handle per l'oggetto Surface in modalità kernel che corrisponderà al punto finale del nuovo allegato.</span><span class="sxs-lookup"><span data-stu-id="6a271-112">Handle to kernel-mode surface object that will be the end point of the new attachment.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a271-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6a271-113">Return value</span></span>

<span data-ttu-id="6a271-114">**NtGdiDdAttachSurface** restituisce uno dei seguenti elementi:</span><span class="sxs-lookup"><span data-stu-id="6a271-114">**NtGdiDdAttachSurface** returns one of the following:</span></span>



| <span data-ttu-id="6a271-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="6a271-115">Return code</span></span>                                                                          | <span data-ttu-id="6a271-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6a271-116">Description</span></span>                             |
|--------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="6a271-117"><dt>**TRUE**</dt></span><span class="sxs-lookup"><span data-stu-id="6a271-117"><dt>**TRUE**</dt></span></span> </dl>  | <span data-ttu-id="6a271-118">La chiamata di funzione è riuscita.</span><span class="sxs-lookup"><span data-stu-id="6a271-118">The function call succeeded.</span></span><br/> |
| <dl> <span data-ttu-id="6a271-119"><dt>**FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="6a271-119"><dt>**FALSE**</dt></span></span> </dl> | <span data-ttu-id="6a271-120">Chiamata di funzione non riuscita.</span><span class="sxs-lookup"><span data-stu-id="6a271-120">The function call failed.</span></span><br/>    |



 

## <a name="remarks"></a><span data-ttu-id="6a271-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="6a271-121">Remarks</span></span>

<span data-ttu-id="6a271-122">Per una descrizione completa degli allegati della superficie, vedere il Software Development Kit di DirectDraw (SDK) e il kit di sviluppo di driver (DDK).</span><span class="sxs-lookup"><span data-stu-id="6a271-122">See the DirectDraw  software development kit (SDK) and Driver Development Kit (DDK) for a full description of surface attachments.</span></span>

> [!Note]  
> <span data-ttu-id="6a271-123">Come per gli altri allegati della superficie, l'allegato risultante è unidirezionale.</span><span class="sxs-lookup"><span data-stu-id="6a271-123">As with other surface attachments, the resulting attachment is one-way.</span></span> <span data-ttu-id="6a271-124">Dopo la chiamata a questa funzione, *hSurfaceTo* non verrà associato a *hSurfaceFrom*.</span><span class="sxs-lookup"><span data-stu-id="6a271-124">After this function is called, *hSurfaceTo* will not be attached to *hSurfaceFrom*.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6a271-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6a271-125">Requirements</span></span>



| <span data-ttu-id="6a271-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a271-126">Requirement</span></span> | <span data-ttu-id="6a271-127">Valore</span><span class="sxs-lookup"><span data-stu-id="6a271-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6a271-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6a271-128">Minimum supported client</span></span><br/> | <span data-ttu-id="6a271-129">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6a271-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="6a271-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6a271-130">Minimum supported server</span></span><br/> | <span data-ttu-id="6a271-131">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6a271-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="6a271-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6a271-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="6a271-133"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="6a271-133"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a271-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6a271-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a271-135">Supporto client di livello inferiore grafica</span><span class="sxs-lookup"><span data-stu-id="6a271-135">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 




