---
description: Consente al driver di specificare il numero di superfici provvisorie necessarie per supportare il GUID specificato e le dimensioni, la posizione e il formato di ognuna di queste superfici.
ms.assetid: 1f3207a8-aa6a-47a3-a1d0-19166592eeca
title: Funzione NtGdiDdGetMoCompBuffInfo (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdGetMoCompBuffInfo
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 03d471e62edd061ce167e0baf2051836e9634fae
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049179"
---
# <a name="ntgdiddgetmocompbuffinfo-function"></a><span data-ttu-id="a6ca5-103">NtGdiDdGetMoCompBuffInfo (funzione)</span><span class="sxs-lookup"><span data-stu-id="a6ca5-103">NtGdiDdGetMoCompBuffInfo function</span></span>

<span data-ttu-id="a6ca5-104">\[Questa funzione è soggetta a modifiche a ogni revisione del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="a6ca5-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="a6ca5-105">Usare invece Microsoft DirectDraw e Microsoft Direct3DAPIs; Queste API isolano le applicazioni da tali modifiche del sistema operativo e nascondono molte altre difficoltà legate all'interazione diretta con i driver di visualizzazione.\]</span><span class="sxs-lookup"><span data-stu-id="a6ca5-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="a6ca5-106">Consente al driver di specificare il numero di superfici provvisorie necessarie per supportare il GUID specificato e le dimensioni, la posizione e il formato di ognuna di queste superfici.</span><span class="sxs-lookup"><span data-stu-id="a6ca5-106">Allows the driver to specify how many interim surfaces are required to support the specified GUID, and the size, location, and format of each of these surfaces.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6ca5-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a6ca5-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdGetMoCompBuffInfo(
  _In_    HANDLE                    hDirectDraw,
  _Inout_ PDD_GETMOCOMPCOMPBUFFDATA puGetBuffData
);
```



## <a name="parameters"></a><span data-ttu-id="a6ca5-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="a6ca5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6ca5-109">*hDirectDraw* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a6ca5-109">*hDirectDraw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a6ca5-110">Handle per l'oggetto DirectDraw in modalità kernel creato in precedenza.</span><span class="sxs-lookup"><span data-stu-id="a6ca5-110">Handle to previously created kernel-mode DirectDraw object.</span></span>

</dd> <dt>

<span data-ttu-id="a6ca5-111">*puGetBuffData* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="a6ca5-111">*puGetBuffData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a6ca5-112">Puntatore a una struttura [**DD \_ GETMOCOMPCOMPBUFFDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_getmocompcompbuffdata) che contiene le informazioni sul buffer compresso.</span><span class="sxs-lookup"><span data-stu-id="a6ca5-112">Pointer to a [**DD\_GETMOCOMPCOMPBUFFDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_getmocompcompbuffdata) structure that contains the compressed buffer information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6ca5-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a6ca5-113">Return value</span></span>

<span data-ttu-id="a6ca5-114">**NtGdiDdGetMoCompBuffInfo** restituisce uno dei codici di callback seguenti.</span><span class="sxs-lookup"><span data-stu-id="a6ca5-114">**NtGdiDdGetMoCompBuffInfo** returns one of the following callback codes.</span></span>



| <span data-ttu-id="a6ca5-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="a6ca5-115">Return code</span></span>                                                                                              | <span data-ttu-id="a6ca5-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a6ca5-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a6ca5-117"><dt>**\_driver DDHAL \_ gestito**</dt></span><span class="sxs-lookup"><span data-stu-id="a6ca5-117"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="a6ca5-118">Il driver ha eseguito l'operazione e ha restituito un codice restituito valido per l'operazione.</span><span class="sxs-lookup"><span data-stu-id="a6ca5-118">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="a6ca5-119">Se il codice è DD \_ OK, DirectDraw o Direct3D procede con la funzione.</span><span class="sxs-lookup"><span data-stu-id="a6ca5-119">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="a6ca5-120">In caso contrario, DirectDraw o Direct3D restituisce il codice di errore fornito dal driver e interrompe la funzione.</span><span class="sxs-lookup"><span data-stu-id="a6ca5-120">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="a6ca5-121"><dt>**\_NOTHANDLED driver \_ DDHAL**</dt></span><span class="sxs-lookup"><span data-stu-id="a6ca5-121"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="a6ca5-122">Il driver non ha commenti sull'operazione richiesta.</span><span class="sxs-lookup"><span data-stu-id="a6ca5-122">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="a6ca5-123">Se è necessario che il driver implementi un particolare callback, DirectDraw o Direct3D segnala una condizione di errore.</span><span class="sxs-lookup"><span data-stu-id="a6ca5-123">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="a6ca5-124">In caso contrario, DirectDraw o Direct3D gestisce l'operazione come se il callback del driver non fosse stato definito eseguendo l'implementazione di DirectDraw o Direct3D indipendente dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a6ca5-124">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a6ca5-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="a6ca5-125">Remarks</span></span>

<span data-ttu-id="a6ca5-126">Per ulteriori informazioni, vedere Microsoft DirectX Video Acceleration Driver Development Kit (DDK).</span><span class="sxs-lookup"><span data-stu-id="a6ca5-126">For more information, see the Microsoft DirectX Video Acceleration Driver Development Kit (DDK).</span></span>

## <a name="requirements"></a><span data-ttu-id="a6ca5-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a6ca5-127">Requirements</span></span>



| <span data-ttu-id="a6ca5-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="a6ca5-128">Requirement</span></span> | <span data-ttu-id="a6ca5-129">Valore</span><span class="sxs-lookup"><span data-stu-id="a6ca5-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a6ca5-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a6ca5-130">Minimum supported client</span></span><br/> | <span data-ttu-id="a6ca5-131">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a6ca5-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="a6ca5-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a6ca5-132">Minimum supported server</span></span><br/> | <span data-ttu-id="a6ca5-133">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a6ca5-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="a6ca5-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a6ca5-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="a6ca5-135"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="a6ca5-135"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6ca5-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a6ca5-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6ca5-137">Supporto client di livello inferiore grafica</span><span class="sxs-lookup"><span data-stu-id="a6ca5-137">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
