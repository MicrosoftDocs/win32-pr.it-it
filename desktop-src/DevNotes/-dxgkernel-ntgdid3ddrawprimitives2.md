---
description: Esegue il rendering delle primitive e restituisce lo stato di rendering aggiornato.
ms.assetid: ef28ee62-a7ad-406c-a892-ffee14123d16
title: Funzione NtGdiD3DDrawPrimitives2 (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiD3DDrawPrimitives2
api_type:
- HeaderDef
api_location:
- Ntgdi.h
ms.openlocfilehash: ebde2fd5adf3b0892606d0ebbc1c7d5f6b55d9cd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049127"
---
# <a name="ntgdid3ddrawprimitives2-function"></a><span data-ttu-id="1127c-103">NtGdiD3DDrawPrimitives2 (funzione)</span><span class="sxs-lookup"><span data-stu-id="1127c-103">NtGdiD3DDrawPrimitives2 function</span></span>

<span data-ttu-id="1127c-104">\[Questa funzione è soggetta a modifiche a ogni revisione del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="1127c-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="1127c-105">Usare invece Microsoft DirectDraw e Microsoft Direct3DAPIs; Queste API isolano le applicazioni da tali modifiche del sistema operativo e nascondono molte altre difficoltà legate all'interazione diretta con i driver di visualizzazione.\]</span><span class="sxs-lookup"><span data-stu-id="1127c-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="1127c-106">Esegue il rendering delle primitive e restituisce lo stato di rendering aggiornato.</span><span class="sxs-lookup"><span data-stu-id="1127c-106">Renders primitives and returns the updated render state.</span></span>

## <a name="syntax"></a><span data-ttu-id="1127c-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1127c-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiD3DDrawPrimitives2(
  _In_    HANDLE                         hCmdBuf,
  _In_    HANDLE                         hVBuf,
  _Inout_ LPD3DNTHAL_DRAWPRIMITIVES2DATA pded,
  _Inout_ FLATPTR                        *pfpVidMemCmd,
  _Inout_ DWORD                          *pdwSizeCmd,
  _Inout_ FLATPTR                        *pfpVidMemVtx,
  _Inout_ DWORD                          *pdwSizeVtx
);
```



## <a name="parameters"></a><span data-ttu-id="1127c-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="1127c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1127c-109">*hCmdBuf* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1127c-109">*hCmdBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1127c-110">Handle per la [**struttura \_ \_ locale della superficie DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) che identifica la superficie DirectDraw contenente i dati del comando.</span><span class="sxs-lookup"><span data-stu-id="1127c-110">Handle to the [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structure that identifies the DirectDraw surface containing the command data.</span></span>

</dd> <dt>

<span data-ttu-id="1127c-111">*hVBuf* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1127c-111">*hVBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1127c-112">Handle per la [**struttura \_ \_ locale della superficie DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) che identifica la superficie DirectDraw contenente i dati del vertice.</span><span class="sxs-lookup"><span data-stu-id="1127c-112">Handle to the [**DD\_SURFACE\_LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) structure that identifies the DirectDraw surface containing the vertex data.</span></span>

</dd> <dt>

<span data-ttu-id="1127c-113">*pded* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="1127c-113">*pded* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1127c-114">Puntatore a una [**struttura \_ DRAWPRIMITIVES2DATA di D3DNTHAL**](/windows-hardware/drivers/ddi/) contenente le informazioni necessarie per il rendering di una o più primitive da parte del driver.</span><span class="sxs-lookup"><span data-stu-id="1127c-114">Pointer to a [**D3DNTHAL\_DRAWPRIMITIVES2DATA**](/windows-hardware/drivers/ddi/) structure that contains the information required for the driver to render one or more primitives.</span></span>

</dd> <dt>

<span data-ttu-id="1127c-115">*pfpVidMemCmd* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="1127c-115">*pfpVidMemCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1127c-116">Nuovo puntatore alla memoria video se il driver ha invertito il buffer dei comandi.</span><span class="sxs-lookup"><span data-stu-id="1127c-116">New pointer to video memory if the driver swapped the command buffer.</span></span>

</dd> <dt>

<span data-ttu-id="1127c-117">*pdwSizeCmd* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="1127c-117">*pdwSizeCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1127c-118">Specifica il numero minimo di byte in base ai quali il driver deve aumentare il buffer dei comandi di swapping.</span><span class="sxs-lookup"><span data-stu-id="1127c-118">Specifies the minimum number of bytes that the driver must increase the swap command buffer by.</span></span>

</dd> <dt>

<span data-ttu-id="1127c-119">*pfpVidMemVtx* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="1127c-119">*pfpVidMemVtx* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1127c-120">Nuovo puntatore alla memoria video se il driver ha invertito il buffer del vertice.</span><span class="sxs-lookup"><span data-stu-id="1127c-120">New pointer to video memory if the driver swapped the vertex buffer.</span></span>

</dd> <dt>

<span data-ttu-id="1127c-121">*pdwSizeVtx* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="1127c-121">*pdwSizeVtx* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1127c-122">Specifica il numero minimo di byte che il driver deve allocare per il buffer dei vertici di swapping.</span><span class="sxs-lookup"><span data-stu-id="1127c-122">Specifies the minimum number of bytes that the driver must allocate for the swap vertex buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1127c-123">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1127c-123">Return value</span></span>

<span data-ttu-id="1127c-124">**NtGdiD3DDrawPrimitives2** restituisce uno dei codici di callback seguenti.</span><span class="sxs-lookup"><span data-stu-id="1127c-124">**NtGdiD3DDrawPrimitives2** returns one of the following callback codes.</span></span>



| <span data-ttu-id="1127c-125">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="1127c-125">Return code</span></span>                                                                                              | <span data-ttu-id="1127c-126">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1127c-126">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1127c-127"><dt>**\_driver DDHAL \_ gestito**</dt></span><span class="sxs-lookup"><span data-stu-id="1127c-127"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="1127c-128">Il driver ha eseguito l'operazione e ha restituito un codice restituito valido per l'operazione.</span><span class="sxs-lookup"><span data-stu-id="1127c-128">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="1127c-129">Se il codice è DD \_ OK, DirectDraw o Direct3D procede con la funzione.</span><span class="sxs-lookup"><span data-stu-id="1127c-129">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="1127c-130">In caso contrario, DirectDraw o Direct3D restituisce il codice di errore fornito dal driver e interrompe la funzione.</span><span class="sxs-lookup"><span data-stu-id="1127c-130">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="1127c-131"><dt>**\_NOTHANDLED driver \_ DDHAL**</dt></span><span class="sxs-lookup"><span data-stu-id="1127c-131"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="1127c-132">Il driver non ha commenti sull'operazione richiesta.</span><span class="sxs-lookup"><span data-stu-id="1127c-132">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="1127c-133">Se è necessario che il driver implementi un particolare callback, DirectDraw o Direct3D segnala una condizione di errore.</span><span class="sxs-lookup"><span data-stu-id="1127c-133">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="1127c-134">In caso contrario, DirectDraw o Direct3D gestisce l'operazione come se il callback del driver non fosse stato definito eseguendo l'implementazione di DirectDraw o Direct3D indipendente dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1127c-134">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="1127c-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1127c-135">Requirements</span></span>



| <span data-ttu-id="1127c-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="1127c-136">Requirement</span></span> | <span data-ttu-id="1127c-137">Valore</span><span class="sxs-lookup"><span data-stu-id="1127c-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1127c-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1127c-138">Minimum supported client</span></span><br/> | <span data-ttu-id="1127c-139">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="1127c-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="1127c-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1127c-140">Minimum supported server</span></span><br/> | <span data-ttu-id="1127c-141">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="1127c-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="1127c-142">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1127c-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="1127c-143"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="1127c-143"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1127c-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1127c-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1127c-145">Supporto client di livello inferiore grafica</span><span class="sxs-lookup"><span data-stu-id="1127c-145">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
