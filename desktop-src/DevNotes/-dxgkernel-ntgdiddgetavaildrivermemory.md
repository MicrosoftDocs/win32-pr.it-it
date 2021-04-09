---
description: Esegue una query sulla quantità di memoria libera in tutti gli heap di memoria video.
ms.assetid: 6718e8da-0da0-42e3-a02b-6884b141fe24
title: Funzione NtGdiDdGetAvailDriverMemory (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdGetAvailDriverMemory
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: c6ec322665b84b3ddad14b7032b8e49245377d40
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049180"
---
# <a name="ntgdiddgetavaildrivermemory-function"></a><span data-ttu-id="b792a-103">NtGdiDdGetAvailDriverMemory (funzione)</span><span class="sxs-lookup"><span data-stu-id="b792a-103">NtGdiDdGetAvailDriverMemory function</span></span>

<span data-ttu-id="b792a-104">\[Questa funzione è soggetta a modifiche a ogni revisione del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="b792a-104">\[This function is subject to change with each operating system revision.</span></span> <span data-ttu-id="b792a-105">Usare invece Microsoft DirectDraw e Microsoft Direct3DAPIs; Queste API isolano le applicazioni da tali modifiche del sistema operativo e nascondono molte altre difficoltà legate all'interazione diretta con i driver di visualizzazione.\]</span><span class="sxs-lookup"><span data-stu-id="b792a-105">Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.\]</span></span>

<span data-ttu-id="b792a-106">Esegue una query sulla quantità di memoria libera in tutti gli heap di memoria video.</span><span class="sxs-lookup"><span data-stu-id="b792a-106">Queries the amount of free memory in all video memory heaps.</span></span>

## <a name="syntax"></a><span data-ttu-id="b792a-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b792a-107">Syntax</span></span>


```C++
DWORD APIENTRY NtGdiDdGetAvailDriverMemory(
  _In_    HANDLE                       hDirectDraw,
  _Inout_ PDD_GETAVAILDRIVERMEMORYDATA puGetAvailDriverMemoryData
);
```



## <a name="parameters"></a><span data-ttu-id="b792a-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="b792a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b792a-109">*hDirectDraw* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b792a-109">*hDirectDraw* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b792a-110">Handle per l'oggetto DirectDraw in modalità kernel creato in precedenza.</span><span class="sxs-lookup"><span data-stu-id="b792a-110">Handle to previously created kernel-mode DirectDraw object.</span></span>

</dd> <dt>

<span data-ttu-id="b792a-111">*puGetAvailDriverMemoryData* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="b792a-111">*puGetAvailDriverMemoryData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b792a-112">Puntatore a una struttura [DD \_ GETAVAILDRIVERMEMORYDATA](https://msdn.microsoft.com/library/ms794088.aspx) che contiene le informazioni necessarie per eseguire la query.</span><span class="sxs-lookup"><span data-stu-id="b792a-112">Pointer to a [DD\_GETAVAILDRIVERMEMORYDATA](https://msdn.microsoft.com/library/ms794088.aspx) structure that contains the information required to perform the query.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b792a-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b792a-113">Return value</span></span>

<span data-ttu-id="b792a-114">**NtGdiDdGetAvailDriverMemory** restituisce uno dei codici di callback seguenti.</span><span class="sxs-lookup"><span data-stu-id="b792a-114">**NtGdiDdGetAvailDriverMemory** returns one of the following callback codes.</span></span>



| <span data-ttu-id="b792a-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="b792a-115">Return code</span></span>                                                                                              | <span data-ttu-id="b792a-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b792a-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b792a-117"><dt>**\_driver DDHAL \_ gestito**</dt></span><span class="sxs-lookup"><span data-stu-id="b792a-117"><dt>**DDHAL\_DRIVER\_HANDLED**</dt></span></span> </dl>    | <span data-ttu-id="b792a-118">Il driver ha eseguito l'operazione e ha restituito un codice restituito valido per l'operazione.</span><span class="sxs-lookup"><span data-stu-id="b792a-118">The driver has performed the operation and returned a valid return code for that operation.</span></span> <span data-ttu-id="b792a-119">Se il codice è DD \_ OK, DirectDraw o Direct3D procede con la funzione.</span><span class="sxs-lookup"><span data-stu-id="b792a-119">If this code is DD\_OK, DirectDraw or Direct3D proceeds with the function.</span></span> <span data-ttu-id="b792a-120">In caso contrario, DirectDraw o Direct3D restituisce il codice di errore fornito dal driver e interrompe la funzione.</span><span class="sxs-lookup"><span data-stu-id="b792a-120">Otherwise, DirectDraw or Direct3D returns the error code provided by the driver and aborts the function.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="b792a-121"><dt>**\_NOTHANDLED driver \_ DDHAL**</dt></span><span class="sxs-lookup"><span data-stu-id="b792a-121"><dt>**DDHAL\_DRIVER\_NOTHANDLED**</dt></span></span> </dl> | <span data-ttu-id="b792a-122">Il driver non ha commenti sull'operazione richiesta.</span><span class="sxs-lookup"><span data-stu-id="b792a-122">The driver has no comment on the requested operation.</span></span> <span data-ttu-id="b792a-123">Se è necessario che il driver implementi un particolare callback, DirectDraw o Direct3D segnala una condizione di errore.</span><span class="sxs-lookup"><span data-stu-id="b792a-123">If the driver is required to have implemented a particular callback, DirectDraw or Direct3D reports an error condition.</span></span> <span data-ttu-id="b792a-124">In caso contrario, DirectDraw o Direct3D gestisce l'operazione come se il callback del driver non fosse stato definito eseguendo l'implementazione di DirectDraw o Direct3D indipendente dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b792a-124">Otherwise, DirectDraw or Direct3D handles the operation as if the driver callback had not been defined by executing the DirectDraw or Direct3D device-independent implementation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="b792a-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b792a-125">Requirements</span></span>



| <span data-ttu-id="b792a-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="b792a-126">Requirement</span></span> | <span data-ttu-id="b792a-127">Valore</span><span class="sxs-lookup"><span data-stu-id="b792a-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b792a-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b792a-128">Minimum supported client</span></span><br/> | <span data-ttu-id="b792a-129">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b792a-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="b792a-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b792a-130">Minimum supported server</span></span><br/> | <span data-ttu-id="b792a-131">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b792a-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="b792a-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b792a-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="b792a-133"><dt>Ntgdi. h</dt></span><span class="sxs-lookup"><span data-stu-id="b792a-133"><dt>Ntgdi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b792a-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b792a-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b792a-135">Supporto client di livello inferiore grafica</span><span class="sxs-lookup"><span data-stu-id="b792a-135">Graphics Low Level Client Support</span></span>](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 




