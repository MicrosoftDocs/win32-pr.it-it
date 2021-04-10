---
title: Proprietà tempo di IVMAccountant (VPCCOMInterfaces. h)
description: Recupera il numero di secondi di esecuzione della macchina virtuale.
ms.assetid: 0c62d51b-fdf1-43f6-81d8-a5f0538c510f
keywords:
- Tempo di proprietà del PC virtuale
- Proprietà tempo di esecuzione Virtual PC, interfaccia IVMAccountant
- Interfaccia IVMAccountant Virtual PC, proprietà tempo di esecuzione
topic_type:
- apiref
api_name:
- IVMAccountant.UpTime
- IVMAccountant.get_UpTime
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c496aa9c32d402dcc8e84bad5410ec7774d2a80a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119970"
---
# <a name="ivmaccountantuptime-property"></a><span data-ttu-id="5f66c-106">Proprietà IVMAccountant:: uptime</span><span class="sxs-lookup"><span data-stu-id="5f66c-106">IVMAccountant::UpTime property</span></span>

<span data-ttu-id="5f66c-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="5f66c-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="5f66c-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="5f66c-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="5f66c-109">Recupera il numero di secondi di esecuzione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="5f66c-109">Retrieves the number of seconds that the virtual machine has been running.</span></span>

<span data-ttu-id="5f66c-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="5f66c-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f66c-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5f66c-111">Syntax</span></span>


```C++
HRESULT get_UpTime(
  [out, retval] long *secondsAlive
);
```



## <a name="property-value"></a><span data-ttu-id="5f66c-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="5f66c-112">Property value</span></span>

<span data-ttu-id="5f66c-113">numero di secondi.</span><span class="sxs-lookup"><span data-stu-id="5f66c-113">The number of seconds.</span></span>

## <a name="error-codes"></a><span data-ttu-id="5f66c-114">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="5f66c-114">Error codes</span></span>



| <span data-ttu-id="5f66c-115">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="5f66c-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="5f66c-116">Significato</span><span class="sxs-lookup"><span data-stu-id="5f66c-116">Meaning</span></span>                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="5f66c-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="5f66c-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="5f66c-118">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="5f66c-118">The operation was successful.</span></span><br/>       |
| <dl> <span data-ttu-id="5f66c-119"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="5f66c-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="5f66c-120">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="5f66c-120">The parameter is **NULL**.</span></span><br/>          |
| <dl> <span data-ttu-id="5f66c-121"><dt>S \_ FALSE</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="5f66c-121"><dt>S\_FALSE</dt> <dt>1</dt></span></span> </dl>                    | <span data-ttu-id="5f66c-122">La macchina virtuale non è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="5f66c-122">The virtual machine is not running.</span></span><br/> |
| <dl> <span data-ttu-id="5f66c-123"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="5f66c-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="5f66c-124">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="5f66c-124">An unexpected error has occurred.</span></span><br/>   |



## <a name="requirements"></a><span data-ttu-id="5f66c-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5f66c-125">Requirements</span></span>



| <span data-ttu-id="5f66c-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f66c-126">Requirement</span></span> | <span data-ttu-id="5f66c-127">Valore</span><span class="sxs-lookup"><span data-stu-id="5f66c-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f66c-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5f66c-128">Minimum supported client</span></span><br/> | <span data-ttu-id="5f66c-129">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="5f66c-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5f66c-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5f66c-130">Minimum supported server</span></span><br/> | <span data-ttu-id="5f66c-131">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="5f66c-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="5f66c-132">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="5f66c-132">End of client support</span></span><br/>    | <span data-ttu-id="5f66c-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="5f66c-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="5f66c-134">Prodotto</span><span class="sxs-lookup"><span data-stu-id="5f66c-134">Product</span></span><br/>                  | <span data-ttu-id="5f66c-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="5f66c-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="5f66c-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5f66c-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="5f66c-137"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="5f66c-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="5f66c-138">IID</span><span class="sxs-lookup"><span data-stu-id="5f66c-138">IID</span></span><br/>                      | <span data-ttu-id="5f66c-139">IID \_ IVMAccountant è definito come 6376c067-7f57-4D63-b754-06e2e4f51d73</span><span class="sxs-lookup"><span data-stu-id="5f66c-139">IID\_IVMAccountant is defined as 6376c067-7f57-4d63-b754-06e2e4f51d73</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="5f66c-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5f66c-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f66c-141">**IVMAccountant**</span><span class="sxs-lookup"><span data-stu-id="5f66c-141">**IVMAccountant**</span></span>](ivmaccountant.md)
</dt> </dl>

 

