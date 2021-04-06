---
title: Proprietà tempo di IVMVirtualPC (VPCCOMInterfaces. h)
description: Recupera il numero di secondi in cui l'applicazione Virtual PC Windows è stata eseguita.
ms.assetid: 3007a961-2e8c-4674-aab6-4424d0d73eca
keywords:
- Tempo di proprietà del PC virtuale
- Proprietà tempo di esecuzione Virtual PC, interfaccia IVMVirtualPC
- Interfaccia IVMVirtualPC Virtual PC, proprietà tempo di esecuzione
topic_type:
- apiref
api_name:
- IVMVirtualPC.UpTime
- IVMVirtualPC.get_UpTime
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fab07128380a097677e0ad8acca5208e5cef11da
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743439"
---
# <a name="ivmvirtualpcuptime-property"></a><span data-ttu-id="d8caa-106">Proprietà IVMVirtualPC:: uptime</span><span class="sxs-lookup"><span data-stu-id="d8caa-106">IVMVirtualPC::UpTime property</span></span>

<span data-ttu-id="d8caa-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="d8caa-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="d8caa-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="d8caa-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="d8caa-109">Recupera il numero di secondi in cui l'applicazione Virtual PC Windows è stata eseguita.</span><span class="sxs-lookup"><span data-stu-id="d8caa-109">Retrieves the number of seconds the Windows Virtual PC application has been running.</span></span>

<span data-ttu-id="d8caa-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="d8caa-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8caa-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d8caa-111">Syntax</span></span>


```C++
HRESULT get_UpTime(
  [out, retval] long *secondsAlive
);
```



## <a name="property-value"></a><span data-ttu-id="d8caa-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="d8caa-112">Property value</span></span>

<span data-ttu-id="d8caa-113">Il numero di secondi in cui l'applicazione Virtual PC Windows è stata eseguita.</span><span class="sxs-lookup"><span data-stu-id="d8caa-113">The number of seconds that the Windows Virtual PC application has been running.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d8caa-114">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="d8caa-114">Error codes</span></span>



| <span data-ttu-id="d8caa-115">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="d8caa-115">Name/value</span></span>                                                                                                                                                                           | <span data-ttu-id="d8caa-116">Significato</span><span class="sxs-lookup"><span data-stu-id="d8caa-116">Meaning</span></span>                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d8caa-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="d8caa-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="d8caa-118">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="d8caa-118">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="d8caa-119"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="d8caa-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="d8caa-120">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="d8caa-120">The parameter is **NULL**.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="d8caa-121"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="d8caa-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                        | <span data-ttu-id="d8caa-122">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="d8caa-122">An unexpected error has occurred.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="d8caa-123"><dt>Macchina virtuale \_ E \_ \_ virtualizzazione hardware \_ disabilitato</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="d8caa-123"><dt>VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="d8caa-124">Il processore non supporta le estensioni di virtualizzazione accelerata hardware (HAV).</span><span class="sxs-lookup"><span data-stu-id="d8caa-124">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="d8caa-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d8caa-125">Requirements</span></span>



| <span data-ttu-id="d8caa-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="d8caa-126">Requirement</span></span> | <span data-ttu-id="d8caa-127">Valore</span><span class="sxs-lookup"><span data-stu-id="d8caa-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8caa-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d8caa-128">Minimum supported client</span></span><br/> | <span data-ttu-id="d8caa-129">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="d8caa-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d8caa-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d8caa-130">Minimum supported server</span></span><br/> | <span data-ttu-id="d8caa-131">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="d8caa-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="d8caa-132">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="d8caa-132">End of client support</span></span><br/>    | <span data-ttu-id="d8caa-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d8caa-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="d8caa-134">Prodotto</span><span class="sxs-lookup"><span data-stu-id="d8caa-134">Product</span></span><br/>                  | <span data-ttu-id="d8caa-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="d8caa-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="d8caa-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d8caa-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="d8caa-137"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="d8caa-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="d8caa-138">IID</span><span class="sxs-lookup"><span data-stu-id="d8caa-138">IID</span></span><br/>                      | <span data-ttu-id="d8caa-139">IID \_ IVMVirtualPC è definito come 236ba0d9-A24A-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="d8caa-139">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="d8caa-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d8caa-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8caa-141">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="d8caa-141">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

