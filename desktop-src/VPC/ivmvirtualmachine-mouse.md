---
title: Proprietà mouse IVMVirtualMachine (VPCCOMInterfaces. h)
description: Recupera il dispositivo mouse per la macchina virtuale.
ms.assetid: 917bbcc1-615d-4fd7-87e1-62abf2ece539
keywords:
- Proprietà del mouse Virtual PC
- Proprietà del mouse Virtual PC, interfaccia IVMVirtualMachine
- Interfaccia IVMVirtualMachine Virtual PC, proprietà mouse
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Mouse
- IVMVirtualMachine.get_Mouse
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 111d511f4e7948a83a968b154721bf81dbfe53b4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302552"
---
# <a name="ivmvirtualmachinemouse-property"></a><span data-ttu-id="d7edf-106">Proprietà IVMVirtualMachine:: mouse</span><span class="sxs-lookup"><span data-stu-id="d7edf-106">IVMVirtualMachine::Mouse property</span></span>

<span data-ttu-id="d7edf-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="d7edf-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="d7edf-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="d7edf-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="d7edf-109">Recupera il dispositivo mouse per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="d7edf-109">Retrieves the mouse device for the virtual machine.</span></span>

<span data-ttu-id="d7edf-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="d7edf-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7edf-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d7edf-111">Syntax</span></span>


```C++
HRESULT get_Mouse(
  [out, retval] IVMMouse **mouse
);
```



## <a name="property-value"></a><span data-ttu-id="d7edf-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="d7edf-112">Property value</span></span>

<span data-ttu-id="d7edf-113">Oggetto [**IVMMouse**](ivmmouse.md) .</span><span class="sxs-lookup"><span data-stu-id="d7edf-113">An [**IVMMouse**](ivmmouse.md) object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d7edf-114">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="d7edf-114">Error codes</span></span>



| <span data-ttu-id="d7edf-115">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="d7edf-115">Name/value</span></span>                                                                                                                                                         | <span data-ttu-id="d7edf-116">Significato</span><span class="sxs-lookup"><span data-stu-id="d7edf-116">Meaning</span></span>                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="d7edf-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="d7edf-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                            | <span data-ttu-id="d7edf-118">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="d7edf-118">The operation was successful.</span></span><br/>       |
| <dl> <span data-ttu-id="d7edf-119"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="d7edf-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>              | <span data-ttu-id="d7edf-120">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="d7edf-120">The parameter is **NULL**.</span></span><br/>          |
| <dl> <span data-ttu-id="d7edf-121"><dt>Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="d7edf-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>      | <span data-ttu-id="d7edf-122">La configurazione è sconosciuta.</span><span class="sxs-lookup"><span data-stu-id="d7edf-122">The configuration is unknown.</span></span><br/>       |
| <dl> <span data-ttu-id="d7edf-123"><dt>Macchina virtuale \_ \_VM E \_ non \_ in esecuzione</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="d7edf-123"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl> | <span data-ttu-id="d7edf-124">La macchina virtuale non è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="d7edf-124">The virtual machine is not running.</span></span><br/> |
| <dl> <span data-ttu-id="d7edf-125"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="d7edf-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>      | <span data-ttu-id="d7edf-126">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="d7edf-126">An unexpected error has occurred.</span></span><br/>   |



## <a name="requirements"></a><span data-ttu-id="d7edf-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d7edf-127">Requirements</span></span>



| <span data-ttu-id="d7edf-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7edf-128">Requirement</span></span> | <span data-ttu-id="d7edf-129">Valore</span><span class="sxs-lookup"><span data-stu-id="d7edf-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7edf-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d7edf-130">Minimum supported client</span></span><br/> | <span data-ttu-id="d7edf-131">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="d7edf-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d7edf-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d7edf-132">Minimum supported server</span></span><br/> | <span data-ttu-id="d7edf-133">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="d7edf-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="d7edf-134">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="d7edf-134">End of client support</span></span><br/>    | <span data-ttu-id="d7edf-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d7edf-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="d7edf-136">Prodotto</span><span class="sxs-lookup"><span data-stu-id="d7edf-136">Product</span></span><br/>                  | <span data-ttu-id="d7edf-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="d7edf-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="d7edf-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d7edf-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7edf-139"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7edf-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="d7edf-140">IID</span><span class="sxs-lookup"><span data-stu-id="d7edf-140">IID</span></span><br/>                      | <span data-ttu-id="d7edf-141">IID \_ IVMVirtualMachine è definito come f7092aa1-33ed-4F78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="d7edf-141">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="d7edf-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d7edf-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7edf-143">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="d7edf-143">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

