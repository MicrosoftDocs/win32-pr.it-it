---
title: Proprietà note IVMVirtualMachine (VPCCOMInterfaces. h)
description: Note per la macchina virtuale.
ms.assetid: 4be6842b-31b2-4619-a6ab-b728be1e2174
keywords:
- Proprietà Notes Virtual PC
- Proprietà Notes Virtual PC, interfaccia IVMVirtualMachine
- Interfaccia IVMVirtualMachine Virtual PC, proprietà Notes
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Notes
- IVMVirtualMachine.get_Notes
- IVMVirtualMachine.put_Notes
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca8fba8659a8f9546866129f21299e44006eb496
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478682"
---
# <a name="ivmvirtualmachinenotes-property"></a><span data-ttu-id="39cb7-106">Proprietà IVMVirtualMachine:: Notes</span><span class="sxs-lookup"><span data-stu-id="39cb7-106">IVMVirtualMachine::Notes property</span></span>

<span data-ttu-id="39cb7-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="39cb7-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="39cb7-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="39cb7-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="39cb7-109">Recupera e imposta le note per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="39cb7-109">Retrieves and sets the notes for the virtual machine.</span></span>

<span data-ttu-id="39cb7-110">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="39cb7-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="39cb7-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="39cb7-111">Syntax</span></span>


```C++
HRESULT put_Notes(
  [in]          BSTR virtualMachineNotes
);

HRESULT get_Notes(
  [out, retval] BSTR *virtualMachineNotes
);
```



## <a name="property-value"></a><span data-ttu-id="39cb7-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="39cb7-112">Property value</span></span>

<span data-ttu-id="39cb7-113">Specifica le note per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="39cb7-113">Specifies the notes for the virtual machine.</span></span> <span data-ttu-id="39cb7-114">La lunghezza massima della stringa è 65.536 caratteri.</span><span class="sxs-lookup"><span data-stu-id="39cb7-114">The maximum length of the string is 65,536 characters.</span></span>

<span data-ttu-id="39cb7-115">Per rimuovere eventuali note, passare una stringa vuota.</span><span class="sxs-lookup"><span data-stu-id="39cb7-115">To remove any notes, pass an empty string.</span></span>

## <a name="error-codes"></a><span data-ttu-id="39cb7-116">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="39cb7-116">Error codes</span></span>



| <span data-ttu-id="39cb7-117">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="39cb7-117">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="39cb7-118">Significato</span><span class="sxs-lookup"><span data-stu-id="39cb7-118">Meaning</span></span>                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="39cb7-119"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="39cb7-119"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="39cb7-120">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="39cb7-120">The operation was successful.</span></span><br/>                                       |
| <dl> <span data-ttu-id="39cb7-121"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="39cb7-121"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="39cb7-122">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="39cb7-122">The parameter is **NULL**.</span></span><br/>                                          |
| <dl> <span data-ttu-id="39cb7-123"><dt>E \_ </dt> <dt>0x80000003</dt> INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="39cb7-123"><dt>E\_INVALIDARG</dt> <dt>0x80000003</dt></span></span> </dl>      | <span data-ttu-id="39cb7-124">Il parametro non è valido o contiene più di 65.536 caratteri.</span><span class="sxs-lookup"><span data-stu-id="39cb7-124">The parameter is not valid or contains more than 65,536 characters.</span></span><br/> |
| <dl> <span data-ttu-id="39cb7-125"><dt>Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="39cb7-125"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="39cb7-126">La configurazione è sconosciuta.</span><span class="sxs-lookup"><span data-stu-id="39cb7-126">The configuration is unknown.</span></span><br/>                                       |
| <dl> <span data-ttu-id="39cb7-127"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="39cb7-127"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="39cb7-128">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="39cb7-128">An unexpected error has occurred.</span></span><br/>                                   |



## <a name="requirements"></a><span data-ttu-id="39cb7-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="39cb7-129">Requirements</span></span>



| <span data-ttu-id="39cb7-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="39cb7-130">Requirement</span></span> | <span data-ttu-id="39cb7-131">Valore</span><span class="sxs-lookup"><span data-stu-id="39cb7-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="39cb7-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="39cb7-132">Minimum supported client</span></span><br/> | <span data-ttu-id="39cb7-133">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="39cb7-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="39cb7-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="39cb7-134">Minimum supported server</span></span><br/> | <span data-ttu-id="39cb7-135">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="39cb7-135">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="39cb7-136">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="39cb7-136">End of client support</span></span><br/>    | <span data-ttu-id="39cb7-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="39cb7-137">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="39cb7-138">Prodotto</span><span class="sxs-lookup"><span data-stu-id="39cb7-138">Product</span></span><br/>                  | <span data-ttu-id="39cb7-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="39cb7-139">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="39cb7-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="39cb7-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="39cb7-141"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="39cb7-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="39cb7-142">IID</span><span class="sxs-lookup"><span data-stu-id="39cb7-142">IID</span></span><br/>                      | <span data-ttu-id="39cb7-143">IID \_ IVMVirtualMachine è definito come f7092aa1-33ed-4F78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="39cb7-143">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="39cb7-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="39cb7-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39cb7-145">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="39cb7-145">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

