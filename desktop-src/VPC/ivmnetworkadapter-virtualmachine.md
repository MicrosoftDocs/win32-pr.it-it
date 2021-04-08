---
title: Proprietà IVMNetworkAdapter VirtualMachine (VPCCOMInterfaces. h)
description: Recupera la macchina virtuale associata a questa interfaccia di rete.
ms.assetid: a3519041-0081-44e7-aa76-760d59ca8587
keywords:
- Proprietà VirtualMachine Virtual PC
- Proprietà VirtualMachine Virtual PC, interfaccia IVMNetworkAdapter
- Interfaccia IVMNetworkAdapter Virtual PC, proprietà VirtualMachine
topic_type:
- apiref
api_name:
- IVMNetworkAdapter.VirtualMachine
- IVMNetworkAdapter.get_VirtualMachine
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea50e43bdcffcd16f668ef596a0f9db9d9bccfe2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047803"
---
# <a name="ivmnetworkadaptervirtualmachine-property"></a><span data-ttu-id="67604-106">Proprietà IVMNetworkAdapter:: VirtualMachine</span><span class="sxs-lookup"><span data-stu-id="67604-106">IVMNetworkAdapter::VirtualMachine property</span></span>

<span data-ttu-id="67604-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="67604-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="67604-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="67604-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="67604-109">Recupera la macchina virtuale associata a questa interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="67604-109">Retrieves the virtual machine associated with this network interface.</span></span>

<span data-ttu-id="67604-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="67604-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="67604-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="67604-111">Syntax</span></span>


```C++
HRESULT get_VirtualMachine(
  [out, retval] IVMVirtualMachine **virtualMachine
);
```



## <a name="property-value"></a><span data-ttu-id="67604-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="67604-112">Property value</span></span>

<span data-ttu-id="67604-113">Interfaccia [**IVMVirtualMachine**](ivmvirtualmachine.md) che rappresenta la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="67604-113">An [**IVMVirtualMachine**](ivmvirtualmachine.md) interface that represents the virtual machine.</span></span>

## <a name="error-codes"></a><span data-ttu-id="67604-114">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="67604-114">Error codes</span></span>



| <span data-ttu-id="67604-115">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="67604-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="67604-116">Significato</span><span class="sxs-lookup"><span data-stu-id="67604-116">Meaning</span></span>                                         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="67604-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="67604-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="67604-118">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="67604-118">The operation was successful.</span></span><br/>        |
| <dl> <span data-ttu-id="67604-119"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="67604-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="67604-120">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="67604-120">The parameter is **NULL**.</span></span><br/>           |
| <dl> <span data-ttu-id="67604-121"><dt>Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="67604-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="67604-122">Impossibile trovare la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="67604-122">The virtual machine cannot be found.</span></span><br/> |
| <dl> <span data-ttu-id="67604-123"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="67604-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="67604-124">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="67604-124">An unexpected error has occurred.</span></span><br/>    |



## <a name="requirements"></a><span data-ttu-id="67604-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="67604-125">Requirements</span></span>



| <span data-ttu-id="67604-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="67604-126">Requirement</span></span> | <span data-ttu-id="67604-127">Valore</span><span class="sxs-lookup"><span data-stu-id="67604-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="67604-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="67604-128">Minimum supported client</span></span><br/> | <span data-ttu-id="67604-129">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="67604-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="67604-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="67604-130">Minimum supported server</span></span><br/> | <span data-ttu-id="67604-131">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="67604-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="67604-132">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="67604-132">End of client support</span></span><br/>    | <span data-ttu-id="67604-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="67604-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="67604-134">Prodotto</span><span class="sxs-lookup"><span data-stu-id="67604-134">Product</span></span><br/>                  | <span data-ttu-id="67604-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="67604-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="67604-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="67604-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="67604-137"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="67604-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="67604-138">IID</span><span class="sxs-lookup"><span data-stu-id="67604-138">IID</span></span><br/>                      | <span data-ttu-id="67604-139">IID \_ IVMNetworkAdapter è definito come e32e4165-22b8-4DC0-8d57-850171ae207a</span><span class="sxs-lookup"><span data-stu-id="67604-139">IID\_IVMNetworkAdapter is defined as e32e4165-22b8-4dc0-8d57-850171ae207a</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="67604-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="67604-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67604-141">**IVMNetworkAdapter**</span><span class="sxs-lookup"><span data-stu-id="67604-141">**IVMNetworkAdapter**</span></span>](ivmnetworkadapter.md)
</dt> </dl>

 

