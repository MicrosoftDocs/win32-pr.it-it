---
title: Proprietà Accountant di IVMVirtualMachine (VPCCOMInterfaces. h)
description: Recupera un contabile per questa macchina virtuale.
ms.assetid: 5e512b83-8630-46ee-b521-c8a8193727f5
keywords:
- Proprietà del contabile Virtual PC
- Proprietà Accountant Virtual PC, interfaccia IVMVirtualMachine
- Interfaccia IVMVirtualMachine Virtual PC, proprietà Accountant
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Accountant
- IVMVirtualMachine.get_Accountant
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af1212de041b1d4c5bda59b9b12ab1d715be67cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121347"
---
# <a name="ivmvirtualmachineaccountant-property"></a><span data-ttu-id="05a5a-106">Proprietà IVMVirtualMachine:: Accountant</span><span class="sxs-lookup"><span data-stu-id="05a5a-106">IVMVirtualMachine::Accountant property</span></span>

<span data-ttu-id="05a5a-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="05a5a-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="05a5a-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="05a5a-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="05a5a-109">Recupera un contabile per questa macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="05a5a-109">Retrieves an accountant for this virtual machine.</span></span>

<span data-ttu-id="05a5a-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="05a5a-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="05a5a-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="05a5a-111">Syntax</span></span>


```C++
HRESULT get_Accountant(
  [out, retval] IVMAccountant **accountant
);
```



## <a name="property-value"></a><span data-ttu-id="05a5a-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="05a5a-112">Property value</span></span>

<span data-ttu-id="05a5a-113">Oggetto [**IVMAccountant**](ivmaccountant.md) .</span><span class="sxs-lookup"><span data-stu-id="05a5a-113">The [**IVMAccountant**](ivmaccountant.md) object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="05a5a-114">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="05a5a-114">Error codes</span></span>



| <span data-ttu-id="05a5a-115">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="05a5a-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="05a5a-116">Significato</span><span class="sxs-lookup"><span data-stu-id="05a5a-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="05a5a-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="05a5a-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="05a5a-118">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="05a5a-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="05a5a-119"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="05a5a-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="05a5a-120">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="05a5a-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="05a5a-121"><dt>Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="05a5a-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="05a5a-122">La configurazione è sconosciuta.</span><span class="sxs-lookup"><span data-stu-id="05a5a-122">The configuration is unknown.</span></span><br/>     |
| <dl> <span data-ttu-id="05a5a-123"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="05a5a-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="05a5a-124">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="05a5a-124">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="05a5a-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="05a5a-125">Requirements</span></span>



| <span data-ttu-id="05a5a-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="05a5a-126">Requirement</span></span> | <span data-ttu-id="05a5a-127">Valore</span><span class="sxs-lookup"><span data-stu-id="05a5a-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="05a5a-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="05a5a-128">Minimum supported client</span></span><br/> | <span data-ttu-id="05a5a-129">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="05a5a-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="05a5a-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="05a5a-130">Minimum supported server</span></span><br/> | <span data-ttu-id="05a5a-131">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="05a5a-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="05a5a-132">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="05a5a-132">End of client support</span></span><br/>    | <span data-ttu-id="05a5a-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="05a5a-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="05a5a-134">Prodotto</span><span class="sxs-lookup"><span data-stu-id="05a5a-134">Product</span></span><br/>                  | <span data-ttu-id="05a5a-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="05a5a-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="05a5a-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="05a5a-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="05a5a-137"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="05a5a-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="05a5a-138">IID</span><span class="sxs-lookup"><span data-stu-id="05a5a-138">IID</span></span><br/>                      | <span data-ttu-id="05a5a-139">IID \_ IVMVirtualMachine è definito come f7092aa1-33ed-4F78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="05a5a-139">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="05a5a-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="05a5a-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05a5a-141">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="05a5a-141">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

