---
description: Consente al driver di segnalare che alloca internamente la memoria di visualizzazione per eseguire la compensazione del movimento.
ms.assetid: cf2878ae-7eff-4214-bb9e-e8b608831108
title: Funzione NtGdiDdGetInternalMoCompInfo (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdGetInternalMoCompInfo
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: a9ddbb7843c7a1142ac6cd9906ef1ed3265e5d11
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877730"
---
# <a name="ntgdiddgetinternalmocompinfo-function"></a><span data-ttu-id="ca757-103">NtGdiDdGetInternalMoCompInfo (funzione)</span><span class="sxs-lookup"><span data-stu-id="ca757-103">NtGdiDdGetInternalMoCompInfo function</span></span>

<span data-ttu-id="ca757-104">\[Questa funzione è soggetta a modifiche a ogni revisione del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="ca757-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="ca757-105">Usare invece Microsoft DirectDraw e Microsoft Direct3DAPIs; Queste API isolano le applicazioni da tali modifiche del sistema operativo e nascondono molte altre difficoltà legate all'interazione diretta con i driver di visualizzazione.\]</span><span class="sxs-lookup"><span data-stu-id="ca757-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="ca757-106">Consente al driver di segnalare che alloca internamente la memoria di visualizzazione per eseguire la compensazione del movimento.</span><span class="sxs-lookup"><span data-stu-id="ca757-106">Allows the driver to report that it internally allocates display memory to perform motion compensation.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca757-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ca757-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdGetInternalMoCompInfo(
  _In_    HANDLE                    hDirectDraw,
  _Inout_ PDD_GETINTERNALMOCOMPDATA puGetInternalData
);
```



## <a name="parameters"></a><span data-ttu-id="ca757-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="ca757-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca757-109">*hDirectDraw* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ca757-109">*hDirectDraw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca757-110">Handle per l'oggetto DirectDraw in modalità kernel creato in precedenza.</span><span class="sxs-lookup"><span data-stu-id="ca757-110">Handle to previously created kernel-mode DirectDraw object.</span></span>

</dd> <dt>

<span data-ttu-id="ca757-111">*puGetInternalData* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="ca757-111">*puGetInternalData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ca757-112">Puntatore a una struttura [**DD \_ GETINTERNALMOCOMPDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_getinternalmocompdata) che contiene i requisiti di memoria interni.</span><span class="sxs-lookup"><span data-stu-id="ca757-112">Pointer to a [**DD\_GETINTERNALMOCOMPDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_getinternalmocompdata) structure that contains the internal memory requirements.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca757-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ca757-113">Return value</span></span>

<span data-ttu-id="ca757-114">**NtGdiDdGetInternalMoCompInfo** restituisce uno dei codici di callback seguenti.</span><span class="sxs-lookup"><span data-stu-id="ca757-114">**NtGdiDdGetInternalMoCompInfo** returns one of the following callback codes.</span></span>



| <span data-ttu-id="ca757-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="ca757-115">Return code</span></span>                                                                                              | <span data-ttu-id="ca757-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ca757-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ca757-117"><dt>**\_driver DDHAL \_ gestito**</dt></span><span class="sxs-lookup"><span data-stu-id="ca757-117"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="ca757-118">Il driver ha eseguito l'operazione e ha restituito un codice restituito valido per l'operazione.</span><span class="sxs-lookup"><span data-stu-id="ca757-118">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="ca757-119">Se il codice è DD \_ OK, DirectDraw o Direct3D procede con la funzione.</span><span class="sxs-lookup"><span data-stu-id="ca757-119">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="ca757-120">In caso contrario, DirectDraw o Direct3D restituisce il codice di errore fornito dal driver e interrompe la funzione.</span><span class="sxs-lookup"><span data-stu-id="ca757-120">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="ca757-121"><dt>**\_NOTHANDLED driver \_ DDHAL**</dt></span><span class="sxs-lookup"><span data-stu-id="ca757-121"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="ca757-122">Il driver non ha commenti sull'operazione richiesta.</span><span class="sxs-lookup"><span data-stu-id="ca757-122">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="ca757-123">Se è necessario che il driver implementi un particolare callback, DirectDraw o Direct3D segnala una condizione di errore.</span><span class="sxs-lookup"><span data-stu-id="ca757-123">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="ca757-124">In caso contrario, DirectDraw o Direct3D gestisce l'operazione come se il callback del driver non fosse stato definito eseguendo l'implementazione di DirectDraw o Direct3D indipendente dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ca757-124">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ca757-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="ca757-125">Remarks</span></span>

<span data-ttu-id="ca757-126">Per ulteriori informazioni, vedere Microsoft DirectX Video Acceleration Driver Development Kit (DDK).</span><span class="sxs-lookup"><span data-stu-id="ca757-126">For more information, see the Microsoft DirectX Video Acceleration Driver Development Kit (DDK).</span></span>

## <a name="requirements"></a><span data-ttu-id="ca757-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ca757-127">Requirements</span></span>



| <span data-ttu-id="ca757-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="ca757-128">Requirement</span></span> | <span data-ttu-id="ca757-129">Valore</span><span class="sxs-lookup"><span data-stu-id="ca757-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ca757-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ca757-130">Minimum supported client</span></span><br/> | <span data-ttu-id="ca757-131">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ca757-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="ca757-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ca757-132">Minimum supported server</span></span><br/> | <span data-ttu-id="ca757-133">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ca757-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="ca757-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ca757-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="ca757-135"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="ca757-135"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca757-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ca757-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca757-137">Supporto client di livello inferiore grafica</span><span class="sxs-lookup"><span data-stu-id="ca757-137">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
