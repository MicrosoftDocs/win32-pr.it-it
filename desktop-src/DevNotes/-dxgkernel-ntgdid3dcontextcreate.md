---
description: Crea un contesto.
ms.assetid: f972ab40-c9e9-4d2a-88f6-4c7817d5533f
title: Funzione NtGdiD3DContextCreate (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiD3DContextCreate
api_type:
- HeaderDef
api_location:
- Ntgdi.h
ms.openlocfilehash: f59a80d3efd5e077bc1eadea66255ff5e6ea7523
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104125964"
---
# <a name="ntgdid3dcontextcreate-function"></a><span data-ttu-id="29ea1-103">NtGdiD3DContextCreate (funzione)</span><span class="sxs-lookup"><span data-stu-id="29ea1-103">NtGdiD3DContextCreate function</span></span>

<span data-ttu-id="29ea1-104">\[Questa funzione è soggetta a modifiche a ogni revisione del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="29ea1-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="29ea1-105">Usare invece Microsoft DirectDraw e Microsoft Direct3DAPIs; Queste API isolano le applicazioni da tali modifiche del sistema operativo e nascondono molte altre difficoltà legate all'interazione diretta con i driver di visualizzazione.\]</span><span class="sxs-lookup"><span data-stu-id="29ea1-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="29ea1-106">Crea un contesto.</span><span class="sxs-lookup"><span data-stu-id="29ea1-106">Creates a context.</span></span>

## <a name="syntax"></a><span data-ttu-id="29ea1-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="29ea1-107">Syntax</span></span>


```C++
BOOL APIENTRY NtGdiD3DContextCreate(
  _In_    HANDLE                  hDirectDrawLocal,
  _In_    HANDLE                  hSurfColor,
  _In_    HANDLE                  hSurfZ,
  _Inout_ D3DNTHAL_CONTEXTCREATEI *pdcci
);
```



## <a name="parameters"></a><span data-ttu-id="29ea1-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="29ea1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29ea1-109">*hDirectDrawLocal* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="29ea1-109">*hDirectDrawLocal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29ea1-110">Handle per un oggetto DirectDraw in modalità kernel, creato in precedenza con [**NtGdiDdCreateDirectDrawObject**](-dxgkernel-ntgdiddcreatedirectdrawobject.md), che rappresenta il dispositivo in cui deve essere creato il contesto Direct3D.</span><span class="sxs-lookup"><span data-stu-id="29ea1-110">Handle to a kernel-mode DirectDraw object, previously created with [**NtGdiDdCreateDirectDrawObject**](-dxgkernel-ntgdiddcreatedirectdrawobject.md), representing the device on which the Direct3D context is to be created.</span></span>

</dd> <dt>

<span data-ttu-id="29ea1-111">*hSurfColor* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="29ea1-111">*hSurfColor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29ea1-112">Handle per una [**struttura \_ \_ locale della superficie DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) che descrive la superficie DirectDraw da utilizzare come destinazione del rendering.</span><span class="sxs-lookup"><span data-stu-id="29ea1-112">Handle to a [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structure that describes the DirectDraw surface to be used as the rendering target.</span></span>

</dd> <dt>

<span data-ttu-id="29ea1-113">*hSurfZ* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="29ea1-113">*hSurfZ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29ea1-114">Handle per una [**struttura \_ \_ locale della superficie DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) che descrive la superficie di DirectDraw da utilizzare come buffer di profondità.</span><span class="sxs-lookup"><span data-stu-id="29ea1-114">Handle to a [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structure that describes the DirectDraw surface to be used as a depth buffer.</span></span> <span data-ttu-id="29ea1-115">Se questo membro è **null**, non è necessario eseguire alcun buffer di profondità.</span><span class="sxs-lookup"><span data-stu-id="29ea1-115">If this member is **NULL**, no depth buffering is to be performed.</span></span>

</dd> <dt>

<span data-ttu-id="29ea1-116">*pdcci* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="29ea1-116">*pdcci* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="29ea1-117">Puntatore a una struttura [**D3DNTHAL \_ CONTEXTCREATEDATA**](/windows-hardware/drivers/ddi/) che contiene le informazioni necessarie per creare un contesto e i dati che devono essere archiviati dal driver nel nuovo contesto.</span><span class="sxs-lookup"><span data-stu-id="29ea1-117">Pointer to a [**D3DNTHAL\_CONTEXTCREATEDATA**](/windows-hardware/drivers/ddi/) structure that contains the information required to create a context and the data that the driver should store in the new context.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29ea1-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="29ea1-118">Return value</span></span>

<span data-ttu-id="29ea1-119">**NtGdiD3DContextCreate** restituisce uno dei codici di callback seguenti.</span><span class="sxs-lookup"><span data-stu-id="29ea1-119">**NtGdiD3DContextCreate** returns one of the following callback codes.</span></span>



| <span data-ttu-id="29ea1-120">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="29ea1-120">Return code</span></span>                                                                                              | <span data-ttu-id="29ea1-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="29ea1-121">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="29ea1-122"><dt>**\_driver DDHAL \_ gestito**</dt></span><span class="sxs-lookup"><span data-stu-id="29ea1-122"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="29ea1-123">Il driver ha eseguito l'operazione e ha restituito un codice restituito valido per l'operazione.</span><span class="sxs-lookup"><span data-stu-id="29ea1-123">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="29ea1-124">Se il codice è DD \_ OK, DirectDraw o Direct3D procede con la funzione.</span><span class="sxs-lookup"><span data-stu-id="29ea1-124">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="29ea1-125">In caso contrario, DirectDraw o Direct3D restituisce il codice di errore fornito dal driver e interrompe la funzione.</span><span class="sxs-lookup"><span data-stu-id="29ea1-125">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="29ea1-126"><dt>**\_NOTHANDLED driver \_ DDHAL**</dt></span><span class="sxs-lookup"><span data-stu-id="29ea1-126"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="29ea1-127">Il driver non ha commenti sull'operazione richiesta.</span><span class="sxs-lookup"><span data-stu-id="29ea1-127">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="29ea1-128">Se è necessario che il driver implementi un particolare callback, DirectDraw o Direct3D segnala una condizione di errore.</span><span class="sxs-lookup"><span data-stu-id="29ea1-128">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="29ea1-129">In caso contrario, DirectDraw o Direct3D gestisce l'operazione come se il callback del driver non fosse stato definito eseguendo l'implementazione di DirectDraw o Direct3D indipendente dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="29ea1-129">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="29ea1-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="29ea1-130">Requirements</span></span>



| <span data-ttu-id="29ea1-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="29ea1-131">Requirement</span></span> | <span data-ttu-id="29ea1-132">Valore</span><span class="sxs-lookup"><span data-stu-id="29ea1-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="29ea1-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="29ea1-133">Minimum supported client</span></span><br/> | <span data-ttu-id="29ea1-134">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="29ea1-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="29ea1-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="29ea1-135">Minimum supported server</span></span><br/> | <span data-ttu-id="29ea1-136">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="29ea1-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="29ea1-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="29ea1-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="29ea1-138"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="29ea1-138"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29ea1-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="29ea1-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29ea1-140">Supporto client di livello inferiore grafica</span><span class="sxs-lookup"><span data-stu-id="29ea1-140">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
