---
title: Proprietà IVMAccountant CPUUtilizationHistory (VPCCOMInterfaces. h)
description: Recupera l'utilizzo di CPU recente della macchina virtuale, come una matrice di valori percentuali.
ms.assetid: f6b92b25-9455-4061-8db0-3e42f9f7391d
keywords:
- Proprietà CPUUtilizationHistory Virtual PC
- Proprietà CPUUtilizationHistory Virtual PC, interfaccia IVMAccountant
- Interfaccia IVMAccountant Virtual PC, proprietà CPUUtilizationHistory
topic_type:
- apiref
api_name:
- IVMAccountant.CPUUtilizationHistory
- IVMAccountant.get_CPUUtilizationHistory
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfa7e91a83be7ab4c09a0b779a729745e80e1e74
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479019"
---
# <a name="ivmaccountantcpuutilizationhistory-property"></a><span data-ttu-id="7a7ee-106">Proprietà IVMAccountant:: CPUUtilizationHistory</span><span class="sxs-lookup"><span data-stu-id="7a7ee-106">IVMAccountant::CPUUtilizationHistory property</span></span>

<span data-ttu-id="7a7ee-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="7a7ee-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="7a7ee-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="7a7ee-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="7a7ee-109">Recupera l'utilizzo di CPU recente della macchina virtuale, come una matrice di valori percentuali.</span><span class="sxs-lookup"><span data-stu-id="7a7ee-109">Retrieves the recent CPU utilization of this virtual machine (as an array of percentage values).</span></span>

<span data-ttu-id="7a7ee-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="7a7ee-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a7ee-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7a7ee-111">Syntax</span></span>


```C++
HRESULT get_CPUUtilizationHistory(
  [out, retval] VARIANT *percentageUtilization
);
```



## <a name="property-value"></a><span data-ttu-id="7a7ee-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="7a7ee-112">Property value</span></span>

<span data-ttu-id="7a7ee-113">Uso della CPU recente della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7a7ee-113">The recent CPU use of this virtual machine.</span></span> <span data-ttu-id="7a7ee-114">Questi dati vengono restituiti come una matrice di 60 elementi che rappresentano la percentuale di utilizzo della CPU in ogni secondo nel minuto precedente.</span><span class="sxs-lookup"><span data-stu-id="7a7ee-114">This data is returned as an array of 60 elements that represent the percentage of CPU use at each second over the past minute.</span></span> <span data-ttu-id="7a7ee-115">Il tipo Variant è VT \_ array \| VT \_ Ui1.</span><span class="sxs-lookup"><span data-stu-id="7a7ee-115">Variant type is VT\_ARRAY\|VT\_UI1.</span></span>

## <a name="error-codes"></a><span data-ttu-id="7a7ee-116">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="7a7ee-116">Error codes</span></span>



| <span data-ttu-id="7a7ee-117">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="7a7ee-117">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="7a7ee-118">Significato</span><span class="sxs-lookup"><span data-stu-id="7a7ee-118">Meaning</span></span>                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7a7ee-119"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="7a7ee-119"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="7a7ee-120">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="7a7ee-120">The operation was successful.</span></span><br/>                                           |
| <dl> <span data-ttu-id="7a7ee-121"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="7a7ee-121"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="7a7ee-122">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="7a7ee-122">The parameter is **NULL**.</span></span><br/>                                              |
| <dl> <span data-ttu-id="7a7ee-123"><dt>S \_ FALSE</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="7a7ee-123"><dt>S\_FALSE</dt> <dt>1</dt></span></span> </dl>                    | <span data-ttu-id="7a7ee-124">La macchina virtuale non è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="7a7ee-124">The virtual machine is not running.</span></span> <span data-ttu-id="7a7ee-125">Tutti gli elementi della matrice 60 vengono impostati su 0.</span><span class="sxs-lookup"><span data-stu-id="7a7ee-125">All 60 array elements are set to 0.</span></span><br/> |
| <dl> <span data-ttu-id="7a7ee-126"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="7a7ee-126"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="7a7ee-127">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="7a7ee-127">An unexpected error has occurred.</span></span><br/>                                       |



## <a name="requirements"></a><span data-ttu-id="7a7ee-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7a7ee-128">Requirements</span></span>



| <span data-ttu-id="7a7ee-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="7a7ee-129">Requirement</span></span> | <span data-ttu-id="7a7ee-130">Valore</span><span class="sxs-lookup"><span data-stu-id="7a7ee-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a7ee-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7a7ee-131">Minimum supported client</span></span><br/> | <span data-ttu-id="7a7ee-132">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="7a7ee-132">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7a7ee-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7a7ee-133">Minimum supported server</span></span><br/> | <span data-ttu-id="7a7ee-134">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="7a7ee-134">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="7a7ee-135">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="7a7ee-135">End of client support</span></span><br/>    | <span data-ttu-id="7a7ee-136">Windows 7</span><span class="sxs-lookup"><span data-stu-id="7a7ee-136">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="7a7ee-137">Prodotto</span><span class="sxs-lookup"><span data-stu-id="7a7ee-137">Product</span></span><br/>                  | <span data-ttu-id="7a7ee-138">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="7a7ee-138">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="7a7ee-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7a7ee-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="7a7ee-140"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="7a7ee-140"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="7a7ee-141">IID</span><span class="sxs-lookup"><span data-stu-id="7a7ee-141">IID</span></span><br/>                      | <span data-ttu-id="7a7ee-142">IID \_ IVMAccountant è definito come 6376c067-7f57-4D63-b754-06e2e4f51d73</span><span class="sxs-lookup"><span data-stu-id="7a7ee-142">IID\_IVMAccountant is defined as 6376c067-7f57-4d63-b754-06e2e4f51d73</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="7a7ee-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7a7ee-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a7ee-144">**IVMAccountant**</span><span class="sxs-lookup"><span data-stu-id="7a7ee-144">**IVMAccountant**</span></span>](ivmaccountant.md)
</dt> </dl>

 

