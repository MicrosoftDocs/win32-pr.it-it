---
description: Crea una superficie Microsoft Direct3D da una superficie Microsoft DirectDraw e vi associa un valore di handle richiesto.
ms.assetid: 7b1ce714-a56e-4508-8160-af8c1748c5f7
title: Funzione NtGdiDdCreateSurfaceEx (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdCreateSurfaceEx
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 8aad613762773e466fb83eadf689b7703a8c4198
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104125940"
---
# <a name="ntgdiddcreatesurfaceex-function"></a><span data-ttu-id="e75ea-103">NtGdiDdCreateSurfaceEx (funzione)</span><span class="sxs-lookup"><span data-stu-id="e75ea-103">NtGdiDdCreateSurfaceEx function</span></span>

<span data-ttu-id="e75ea-104">\[Questa funzione è soggetta a modifiche a ogni revisione del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="e75ea-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="e75ea-105">In alternativa, usare i DirectDraw e Direct3DAPIs; Queste API isolano le applicazioni da tali modifiche del sistema operativo e nascondono molte altre difficoltà legate all'interazione diretta con i driver di visualizzazione.\]</span><span class="sxs-lookup"><span data-stu-id="e75ea-105">Instead, use the DirectDraw and Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="e75ea-106">Crea una superficie Microsoft Direct3D da una superficie Microsoft DirectDraw e vi associa un valore di handle richiesto.</span><span class="sxs-lookup"><span data-stu-id="e75ea-106">Creates a Microsoft Direct3D surface from a Microsoft DirectDraw surface and associates a requested handle value to it.</span></span>

## <a name="syntax"></a><span data-ttu-id="e75ea-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e75ea-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdCreateSurfaceEx(
  _In_ HANDLE hDirectDraw,
  _In_ HANDLE hSurface,
  _In_ DWORD  dwSurfaceHandle
);
```



## <a name="parameters"></a><span data-ttu-id="e75ea-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="e75ea-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e75ea-109">*hDirectDraw* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e75ea-109">*hDirectDraw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e75ea-110">Handle per l'oggetto DirectDraw creato dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e75ea-110">Handle to the DirectDraw object created by the application.</span></span>

</dd> <dt>

<span data-ttu-id="e75ea-111">*hSurface* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e75ea-111">*hSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e75ea-112">Handle per la superficie DirectDraw da creare per Direct3D.</span><span class="sxs-lookup"><span data-stu-id="e75ea-112">Handle to the DirectDraw surface to be created for Direct3D.</span></span> <span data-ttu-id="e75ea-113">Questi handle sono univoci all'interno di ogni struttura [**\_ \_ locale di DIRECTDRAW GG**](/windows/win32/api/ddrawint/ns-ddrawint-dd_directdraw_local) diversa.</span><span class="sxs-lookup"><span data-stu-id="e75ea-113">These handles are unique within each different [**DD\_DIRECTDRAW\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_directdraw_local) structure.</span></span>

</dd> <dt>

<span data-ttu-id="e75ea-114">*dwSurfaceHandle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e75ea-114">*dwSurfaceHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e75ea-115">Handle per una struttura [**DD \_ CREATESURFACEEXDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_createsurfaceexdata) che contiene le informazioni necessarie per la creazione della superficie da parte del driver.</span><span class="sxs-lookup"><span data-stu-id="e75ea-115">Handle to a [**DD\_CREATESURFACEEXDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_createsurfaceexdata) structure that contains the information required for the driver to create the surface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e75ea-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e75ea-116">Return value</span></span>

<span data-ttu-id="e75ea-117">**NtGdiDdCreateSurfaceEx** restituisce uno dei codici di callback seguenti.</span><span class="sxs-lookup"><span data-stu-id="e75ea-117">**NtGdiDdCreateSurfaceEx** returns one of the following callback codes.</span></span>



| <span data-ttu-id="e75ea-118">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="e75ea-118">Return code</span></span>                                                                                              | <span data-ttu-id="e75ea-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e75ea-119">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e75ea-120"><dt>**\_driver DDHAL \_ gestito**</dt></span><span class="sxs-lookup"><span data-stu-id="e75ea-120"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="e75ea-121">Il driver ha eseguito l'operazione e ha restituito un codice restituito valido per l'operazione.</span><span class="sxs-lookup"><span data-stu-id="e75ea-121">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="e75ea-122">Se il codice è DD \_ OK, DirectDraw o Direct3D procede con la funzione.</span><span class="sxs-lookup"><span data-stu-id="e75ea-122">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="e75ea-123">In caso contrario, DirectDraw o Direct3D restituisce il codice di errore fornito dal driver e interrompe la funzione.</span><span class="sxs-lookup"><span data-stu-id="e75ea-123">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="e75ea-124"><dt>**\_NOTHANDLED driver \_ DDHAL**</dt></span><span class="sxs-lookup"><span data-stu-id="e75ea-124"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="e75ea-125">Il driver non ha commenti sull'operazione richiesta.</span><span class="sxs-lookup"><span data-stu-id="e75ea-125">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="e75ea-126">Se è necessario che il driver implementi un particolare callback, DirectDraw o Direct3D segnala una condizione di errore.</span><span class="sxs-lookup"><span data-stu-id="e75ea-126">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="e75ea-127">In caso contrario, DirectDraw o Direct3D gestisce l'operazione come se il callback del driver non fosse stato definito eseguendo l'implementazione di DirectDraw o Direct3D indipendente dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e75ea-127">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="e75ea-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e75ea-128">Requirements</span></span>



| <span data-ttu-id="e75ea-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="e75ea-129">Requirement</span></span> | <span data-ttu-id="e75ea-130">Valore</span><span class="sxs-lookup"><span data-stu-id="e75ea-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e75ea-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e75ea-131">Minimum supported client</span></span><br/> | <span data-ttu-id="e75ea-132">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e75ea-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="e75ea-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e75ea-133">Minimum supported server</span></span><br/> | <span data-ttu-id="e75ea-134">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e75ea-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="e75ea-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e75ea-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="e75ea-136"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="e75ea-136"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e75ea-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e75ea-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e75ea-138">Supporto client di livello inferiore grafica</span><span class="sxs-lookup"><span data-stu-id="e75ea-138">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
