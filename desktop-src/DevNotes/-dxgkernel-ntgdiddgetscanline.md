---
description: Restituisce il numero della linea di analisi fisica corrente.
ms.assetid: 159d5ea0-25b8-4c2d-9cd4-cf4ee0ca0561
title: Funzione NtGdiDdGetScanLine (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdGetScanLine
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 814063208e8115c5ba2a7fe427e21223ac478f57
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304754"
---
# <a name="ntgdiddgetscanline-function"></a><span data-ttu-id="0eacc-103">NtGdiDdGetScanLine (funzione)</span><span class="sxs-lookup"><span data-stu-id="0eacc-103">NtGdiDdGetScanLine function</span></span>

<span data-ttu-id="0eacc-104">\[Questa funzione è soggetta a modifiche a ogni revisione del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="0eacc-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="0eacc-105">Usare invece Microsoft DirectDraw e Microsoft Direct3DAPIs; Queste API isolano le applicazioni da tali modifiche del sistema operativo e nascondono molte altre difficoltà legate all'interazione diretta con i driver di visualizzazione.\]</span><span class="sxs-lookup"><span data-stu-id="0eacc-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="0eacc-106">Restituisce il numero della linea di analisi fisica corrente.</span><span class="sxs-lookup"><span data-stu-id="0eacc-106">Returns the number of the current physical scan line.</span></span>

## <a name="syntax"></a><span data-ttu-id="0eacc-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0eacc-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdGetScanLine(
  _In_    HANDLE              hDirectDraw,
  _Inout_ PDD_GETSCANLINEDATA puGetScanLineData
);
```



## <a name="parameters"></a><span data-ttu-id="0eacc-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="0eacc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0eacc-109">*hDirectDraw* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0eacc-109">*hDirectDraw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0eacc-110">Handle per una [**struttura \_ \_ globale di DIRECTDRAW DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_directdraw_global) che rappresenta il driver.</span><span class="sxs-lookup"><span data-stu-id="0eacc-110">Handle to a [**DD\_DIRECTDRAW\_GLOBAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_directdraw_global) structure that represents the driver.</span></span>

</dd> <dt>

<span data-ttu-id="0eacc-111">*puGetScanLineData* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="0eacc-111">*puGetScanLineData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="0eacc-112">Puntatore a una [**struttura \_ GETSCANLINEDATA DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_getscanlinedata) in cui il driver restituisce il numero della riga di analisi corrente.</span><span class="sxs-lookup"><span data-stu-id="0eacc-112">Pointer to a [**DD\_GETSCANLINEDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_getscanlinedata) structure in which the driver returns the number of the current scan line.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0eacc-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0eacc-113">Return value</span></span>

<span data-ttu-id="0eacc-114">**NtGdiDdGetScanLine** restituisce uno dei codici di callback seguenti.</span><span class="sxs-lookup"><span data-stu-id="0eacc-114">**NtGdiDdGetScanLine** returns one of the following callback codes.</span></span>



| <span data-ttu-id="0eacc-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="0eacc-115">Return code</span></span>                                                                                              | <span data-ttu-id="0eacc-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0eacc-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0eacc-117"><dt>**\_driver DDHAL \_ gestito**</dt></span><span class="sxs-lookup"><span data-stu-id="0eacc-117"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="0eacc-118">Il driver ha eseguito l'operazione e ha restituito un codice restituito valido per l'operazione.</span><span class="sxs-lookup"><span data-stu-id="0eacc-118">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="0eacc-119">Se il codice è DD \_ OK, DirectDraw o Direct3D procede con la funzione.</span><span class="sxs-lookup"><span data-stu-id="0eacc-119">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="0eacc-120">In caso contrario, DirectDraw o Direct3D restituisce il codice di errore fornito dal driver e interrompe la funzione.</span><span class="sxs-lookup"><span data-stu-id="0eacc-120">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="0eacc-121"><dt>**\_NOTHANDLED driver \_ DDHAL**</dt></span><span class="sxs-lookup"><span data-stu-id="0eacc-121"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="0eacc-122">Il driver non ha commenti sull'operazione richiesta.</span><span class="sxs-lookup"><span data-stu-id="0eacc-122">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="0eacc-123">Se è necessario che il driver implementi un particolare callback, DirectDraw o Direct3D segnala una condizione di errore.</span><span class="sxs-lookup"><span data-stu-id="0eacc-123">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="0eacc-124">In caso contrario, DirectDraw o Direct3D gestisce l'operazione come se il callback del driver non fosse stato definito eseguendo l'implementazione di DirectDraw o Direct3D indipendente dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0eacc-124">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="0eacc-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0eacc-125">Requirements</span></span>



| <span data-ttu-id="0eacc-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="0eacc-126">Requirement</span></span> | <span data-ttu-id="0eacc-127">Valore</span><span class="sxs-lookup"><span data-stu-id="0eacc-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0eacc-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0eacc-128">Minimum supported client</span></span><br/> | <span data-ttu-id="0eacc-129">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="0eacc-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="0eacc-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0eacc-130">Minimum supported server</span></span><br/> | <span data-ttu-id="0eacc-131">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="0eacc-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="0eacc-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0eacc-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="0eacc-133"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="0eacc-133"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0eacc-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0eacc-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0eacc-135">Supporto client di livello inferiore grafica</span><span class="sxs-lookup"><span data-stu-id="0eacc-135">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
