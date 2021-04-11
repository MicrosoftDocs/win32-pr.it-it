---
description: Notifica al driver che un decodificatore software inizierà a usare la compensazione di movimento con il GUID specificato.
ms.assetid: c9a55428-7fe6-45dd-987a-d9ab8ae8a1cb
title: Funzione NtGdiDdCreateMoComp (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdCreateMoComp
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: f1705b5bf7ac5eddd1ac39e14f3b91b7fd3728cd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126633"
---
# <a name="ntgdiddcreatemocomp-function"></a><span data-ttu-id="b4a5a-103">NtGdiDdCreateMoComp (funzione)</span><span class="sxs-lookup"><span data-stu-id="b4a5a-103">NtGdiDdCreateMoComp function</span></span>

<span data-ttu-id="b4a5a-104">\[Questa funzione è soggetta a modifiche a ogni revisione del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="b4a5a-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="b4a5a-105">Usare invece Microsoft DirectDraw e Microsoft Direct3DAPIs; Queste API isolano le applicazioni da tali modifiche del sistema operativo e nascondono molte altre difficoltà legate all'interazione diretta con i driver di visualizzazione.\]</span><span class="sxs-lookup"><span data-stu-id="b4a5a-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="b4a5a-106">Notifica al driver che un decodificatore software inizierà a usare la compensazione di movimento con il GUID specificato.</span><span class="sxs-lookup"><span data-stu-id="b4a5a-106">Notifies the driver that a software decoder will start using motion compensation with the specified GUID.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4a5a-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b4a5a-107">Syntax</span></span>


```C++
HANDLE APIENTRY NtGdiDdCreateMoComp(
  _In_    HANDLE               hDirectDraw,
  _Inout_ PDD_CREATEMOCOMPDATA puCreateMoCompData
);
```



## <a name="parameters"></a><span data-ttu-id="b4a5a-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="b4a5a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4a5a-109">*hDirectDraw* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b4a5a-109">*hDirectDraw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4a5a-110">Handle per un oggetto in modalità kernel DirectDraw creato in precedenza per il dispositivo in cui deve essere utilizzata la compensazione del movimento.</span><span class="sxs-lookup"><span data-stu-id="b4a5a-110">Handle to a previously created DirectDraw kernel-mode object for the device on which motion compensation is to be used.</span></span>

</dd> <dt>

<span data-ttu-id="b4a5a-111">*puCreateMoCompData* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="b4a5a-111">*puCreateMoCompData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b4a5a-112">Puntatore a una struttura [**DD \_ CREATEMOCOMPDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_createmocompdata) che contiene le informazioni necessarie per iniziare a utilizzare la compensazione di movimento.</span><span class="sxs-lookup"><span data-stu-id="b4a5a-112">Pointer to a [**DD\_CREATEMOCOMPDATA**](/windows/win32/api/ddrawint/ns-ddrawint-dd_createmocompdata) structure that contains the information required to begin using motion compensation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4a5a-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b4a5a-113">Return value</span></span>

<span data-ttu-id="b4a5a-114">**NtGdiDdCreateMoComp** restituisce uno dei codici di callback seguenti.</span><span class="sxs-lookup"><span data-stu-id="b4a5a-114">**NtGdiDdCreateMoComp** returns one of the following callback codes.</span></span>



| <span data-ttu-id="b4a5a-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="b4a5a-115">Return code</span></span>                                                                                              | <span data-ttu-id="b4a5a-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b4a5a-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b4a5a-117"><dt>**\_driver DDHAL \_ gestito**</dt></span><span class="sxs-lookup"><span data-stu-id="b4a5a-117"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="b4a5a-118">Il driver ha eseguito l'operazione e ha restituito un codice restituito valido per l'operazione.</span><span class="sxs-lookup"><span data-stu-id="b4a5a-118">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="b4a5a-119">Se il codice è DD \_ OK, DirectDraw o Direct3D procede con la funzione.</span><span class="sxs-lookup"><span data-stu-id="b4a5a-119">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="b4a5a-120">In caso contrario, DirectDraw o Direct3D restituisce il codice di errore fornito dal driver e interrompe la funzione.</span><span class="sxs-lookup"><span data-stu-id="b4a5a-120">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="b4a5a-121"><dt>**\_NOTHANDLED driver \_ DDHAL**</dt></span><span class="sxs-lookup"><span data-stu-id="b4a5a-121"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="b4a5a-122">Il driver non ha commenti sull'operazione richiesta.</span><span class="sxs-lookup"><span data-stu-id="b4a5a-122">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="b4a5a-123">Se è necessario che il driver implementi un particolare callback, DirectDraw o Direct3D segnala una condizione di errore.</span><span class="sxs-lookup"><span data-stu-id="b4a5a-123">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="b4a5a-124">In caso contrario, DirectDraw o Direct3D gestisce l'operazione come se il callback del driver non fosse stato definito eseguendo l'implementazione di DirectDraw o Direct3D indipendente dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b4a5a-124">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b4a5a-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="b4a5a-125">Remarks</span></span>

<span data-ttu-id="b4a5a-126">Per ulteriori informazioni, vedere Microsoft DirectX Video Acceleration Driver Development Kit (DDK).</span><span class="sxs-lookup"><span data-stu-id="b4a5a-126">For more information, see the Microsoft DirectX Video Acceleration Driver Development Kit (DDK).</span></span>

## <a name="requirements"></a><span data-ttu-id="b4a5a-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b4a5a-127">Requirements</span></span>



| <span data-ttu-id="b4a5a-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="b4a5a-128">Requirement</span></span> | <span data-ttu-id="b4a5a-129">Valore</span><span class="sxs-lookup"><span data-stu-id="b4a5a-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b4a5a-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b4a5a-130">Minimum supported client</span></span><br/> | <span data-ttu-id="b4a5a-131">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b4a5a-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="b4a5a-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b4a5a-132">Minimum supported server</span></span><br/> | <span data-ttu-id="b4a5a-133">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b4a5a-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="b4a5a-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b4a5a-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="b4a5a-135"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="b4a5a-135"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4a5a-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b4a5a-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4a5a-137">Supporto client di livello inferiore grafica</span><span class="sxs-lookup"><span data-stu-id="b4a5a-137">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
