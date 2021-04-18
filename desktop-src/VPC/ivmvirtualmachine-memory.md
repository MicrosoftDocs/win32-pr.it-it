---
title: Proprietà Memory IVMVirtualMachine (VPCCOMInterfaces. h)
description: Quantità di memoria fisica della macchina virtuale, in megabyte.
ms.assetid: 1a1d4cc7-a537-49f0-981f-0b72eca9013e
keywords:
- Proprietà memoria Virtual PC
- Proprietà Memory Virtual PC, interfaccia IVMVirtualMachine
- Interfaccia IVMVirtualMachine Virtual PC, proprietà Memory
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Memory
- IVMVirtualMachine.get_Memory
- IVMVirtualMachine.put_Memory
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b73251b58639e0311e33120cd4bb0e778a017b9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106300925"
---
# <a name="ivmvirtualmachinememory-property"></a><span data-ttu-id="02e9e-106">Proprietà IVMVirtualMachine:: memory</span><span class="sxs-lookup"><span data-stu-id="02e9e-106">IVMVirtualMachine::Memory property</span></span>

<span data-ttu-id="02e9e-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="02e9e-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="02e9e-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="02e9e-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="02e9e-109">Recupera e imposta la quantità di memoria fisica nella macchina virtuale, in megabyte.</span><span class="sxs-lookup"><span data-stu-id="02e9e-109">Retrieves and sets the amount of physical memory in the virtual machine, in megabytes.</span></span>

<span data-ttu-id="02e9e-110">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="02e9e-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="02e9e-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="02e9e-111">Syntax</span></span>


```C++
HRESULT put_Memory(
  [in]          long megabytesOfMemory
);

HRESULT get_Memory(
  [out, retval] long *megabytesOfMemory
);
```



## <a name="property-value"></a><span data-ttu-id="02e9e-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="02e9e-112">Property value</span></span>

<span data-ttu-id="02e9e-113">Specifica la quantità di memoria fisica, in megabyte.</span><span class="sxs-lookup"><span data-stu-id="02e9e-113">Specifies the amount of physical memory, in megabytes.</span></span>

## <a name="error-codes"></a><span data-ttu-id="02e9e-114">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="02e9e-114">Error codes</span></span>



| <span data-ttu-id="02e9e-115">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="02e9e-115">Name/value</span></span>                                                                                                                                                         | <span data-ttu-id="02e9e-116">Significato</span><span class="sxs-lookup"><span data-stu-id="02e9e-116">Meaning</span></span>                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <span data-ttu-id="02e9e-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="02e9e-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                            | <span data-ttu-id="02e9e-118">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="02e9e-118">The operation was successful.</span></span><br/>                  |
| <dl> <span data-ttu-id="02e9e-119"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="02e9e-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>              | <span data-ttu-id="02e9e-120">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="02e9e-120">The parameter is **NULL**.</span></span><br/>                     |
| <dl> <span data-ttu-id="02e9e-121"><dt>E \_ </dt> <dt>0x80000003</dt> INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="02e9e-121"><dt>E\_INVALIDARG</dt> <dt>0x80000003</dt></span></span> </dl>           | <span data-ttu-id="02e9e-122">Il parametro non è valido o non è compreso nell'intervallo.</span><span class="sxs-lookup"><span data-stu-id="02e9e-122">The parameter is not valid or is out of range.</span></span><br/> |
| <dl> <span data-ttu-id="02e9e-123"><dt>Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="02e9e-123"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>      | <span data-ttu-id="02e9e-124">La configurazione è sconosciuta.</span><span class="sxs-lookup"><span data-stu-id="02e9e-124">The configuration is unknown.</span></span><br/>                  |
| <dl> <span data-ttu-id="02e9e-125"><dt>Macchina virtuale \_ E \_ pref \_ non \_ trovato</dt> <dt>0xA0040300</dt></span><span class="sxs-lookup"><span data-stu-id="02e9e-125"><dt>VM\_E\_PREF\_NOT\_FOUND</dt> <dt>0xA0040300</dt></span></span> </dl> | <span data-ttu-id="02e9e-126">La preferenza non è stata trovata.</span><span class="sxs-lookup"><span data-stu-id="02e9e-126">The preference was not found.</span></span><br/>                  |
| <dl> <span data-ttu-id="02e9e-127"><dt>Macchina virtuale \_ 0xA0040302 \_ virtuale E pref \_ VM \_ attiva</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="02e9e-127"><dt>VM\_E\_PREF\_VM\_ACTIVE</dt> <dt>0xA0040302</dt></span></span> </dl> | <span data-ttu-id="02e9e-128">La macchina virtuale è in esecuzione o salvata.</span><span class="sxs-lookup"><span data-stu-id="02e9e-128">The virtual machine is running or saved.</span></span><br/>       |
| <dl> <span data-ttu-id="02e9e-129"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="02e9e-129"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>      | <span data-ttu-id="02e9e-130">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="02e9e-130">An unexpected error has occurred.</span></span><br/>              |



## <a name="remarks"></a><span data-ttu-id="02e9e-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="02e9e-131">Remarks</span></span>

<span data-ttu-id="02e9e-132">La quantità di memoria fisica in una macchina virtuale deve essere almeno 4 MB.</span><span class="sxs-lookup"><span data-stu-id="02e9e-132">The amount of physical memory in a virtual machine must be at least 4 MB.</span></span> <span data-ttu-id="02e9e-133">Il limite superiore per la memoria dipende dalla configurazione host, ma può contenere al massimo 3.712 MB.</span><span class="sxs-lookup"><span data-stu-id="02e9e-133">The upper limit on memory depends on the host configuration, but can be at most 3,712 MB.</span></span>

## <a name="requirements"></a><span data-ttu-id="02e9e-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="02e9e-134">Requirements</span></span>



| <span data-ttu-id="02e9e-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="02e9e-135">Requirement</span></span> | <span data-ttu-id="02e9e-136">Valore</span><span class="sxs-lookup"><span data-stu-id="02e9e-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="02e9e-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="02e9e-137">Minimum supported client</span></span><br/> | <span data-ttu-id="02e9e-138">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="02e9e-138">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="02e9e-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="02e9e-139">Minimum supported server</span></span><br/> | <span data-ttu-id="02e9e-140">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="02e9e-140">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="02e9e-141">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="02e9e-141">End of client support</span></span><br/>    | <span data-ttu-id="02e9e-142">Windows 7</span><span class="sxs-lookup"><span data-stu-id="02e9e-142">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="02e9e-143">Prodotto</span><span class="sxs-lookup"><span data-stu-id="02e9e-143">Product</span></span><br/>                  | <span data-ttu-id="02e9e-144">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="02e9e-144">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="02e9e-145">Intestazione</span><span class="sxs-lookup"><span data-stu-id="02e9e-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="02e9e-146"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="02e9e-146"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="02e9e-147">IID</span><span class="sxs-lookup"><span data-stu-id="02e9e-147">IID</span></span><br/>                      | <span data-ttu-id="02e9e-148">IID \_ IVMVirtualMachine è definito come f7092aa1-33ed-4F78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="02e9e-148">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="02e9e-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="02e9e-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02e9e-150">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="02e9e-150">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

