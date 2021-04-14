---
title: Proprietà IVMVirtualMachine ProcessorSpeed (VPCCOMInterfaces. h)
description: Velocità del processore, in megahertz (MHz) o gigahertz (GHz).
ms.assetid: 465157a9-08ad-4636-b7c6-a188ff21e131
keywords:
- Proprietà ProcessorSpeed Virtual PC
- Proprietà ProcessorSpeed Virtual PC, interfaccia IVMVirtualMachine
- Interfaccia IVMVirtualMachine Virtual PC, proprietà ProcessorSpeed
topic_type:
- apiref
api_name:
- IVMVirtualMachine.ProcessorSpeed
- IVMVirtualMachine.get_ProcessorSpeed
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebaeb6f17e867d7618241b099b765ff450a2a4e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478676"
---
# <a name="ivmvirtualmachineprocessorspeed-property"></a><span data-ttu-id="46d0d-106">IVMVirtualMachine::P proprietà rocessorSpeed</span><span class="sxs-lookup"><span data-stu-id="46d0d-106">IVMVirtualMachine::ProcessorSpeed property</span></span>

<span data-ttu-id="46d0d-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="46d0d-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="46d0d-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="46d0d-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="46d0d-109">Recupera la velocità del processore, in megahertz (MHz) o gigahertz (GHz).</span><span class="sxs-lookup"><span data-stu-id="46d0d-109">Retrieves the speed of the processor, in megahertz (MHz) or gigahertz (GHz).</span></span>

<span data-ttu-id="46d0d-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="46d0d-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="46d0d-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="46d0d-111">Syntax</span></span>


```C++
HRESULT get_ProcessorSpeed(
  [out, retval] long *processorSpeed
);
```



## <a name="property-value"></a><span data-ttu-id="46d0d-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="46d0d-112">Property value</span></span>

<span data-ttu-id="46d0d-113">Velocità, in megahertz o gigahertz.</span><span class="sxs-lookup"><span data-stu-id="46d0d-113">The speed, in megahertz or gigahertz.</span></span>

## <a name="error-codes"></a><span data-ttu-id="46d0d-114">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="46d0d-114">Error codes</span></span>



| <span data-ttu-id="46d0d-115">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="46d0d-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="46d0d-116">Significato</span><span class="sxs-lookup"><span data-stu-id="46d0d-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="46d0d-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="46d0d-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="46d0d-118">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="46d0d-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="46d0d-119"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="46d0d-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="46d0d-120">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="46d0d-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="46d0d-121"><dt>Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="46d0d-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="46d0d-122">La configurazione è sconosciuta.</span><span class="sxs-lookup"><span data-stu-id="46d0d-122">The configuration is unknown.</span></span><br/>     |
| <dl> <span data-ttu-id="46d0d-123"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="46d0d-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="46d0d-124">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="46d0d-124">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="46d0d-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="46d0d-125">Requirements</span></span>



| <span data-ttu-id="46d0d-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="46d0d-126">Requirement</span></span> | <span data-ttu-id="46d0d-127">Valore</span><span class="sxs-lookup"><span data-stu-id="46d0d-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="46d0d-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="46d0d-128">Minimum supported client</span></span><br/> | <span data-ttu-id="46d0d-129">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="46d0d-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="46d0d-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="46d0d-130">Minimum supported server</span></span><br/> | <span data-ttu-id="46d0d-131">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="46d0d-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="46d0d-132">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="46d0d-132">End of client support</span></span><br/>    | <span data-ttu-id="46d0d-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="46d0d-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="46d0d-134">Prodotto</span><span class="sxs-lookup"><span data-stu-id="46d0d-134">Product</span></span><br/>                  | <span data-ttu-id="46d0d-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="46d0d-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="46d0d-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="46d0d-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="46d0d-137"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="46d0d-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="46d0d-138">IID</span><span class="sxs-lookup"><span data-stu-id="46d0d-138">IID</span></span><br/>                      | <span data-ttu-id="46d0d-139">IID \_ IVMVirtualMachine è definito come f7092aa1-33ed-4F78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="46d0d-139">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="46d0d-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="46d0d-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46d0d-141">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="46d0d-141">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

