---
title: Metodo IVMVirtualMachine DiscardUndoDisks (VPCCOMInterfaces. h)
description: Elimina i file modifiche disco virtuali.
ms.assetid: 5c3a4b3f-ea58-498c-b7cf-54f028fa061c
keywords:
- Metodo DiscardUndoDisks Virtual PC
- Metodo DiscardUndoDisks Virtual PC, interfaccia IVMVirtualMachine
- Interfaccia IVMVirtualMachine Virtual PC, metodo DiscardUndoDisks
topic_type:
- apiref
api_name:
- IVMVirtualMachine.DiscardUndoDisks
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d548b69a6cfebc383a0233f01ef19ad14d051474
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477044"
---
# <a name="ivmvirtualmachinediscardundodisks-method"></a><span data-ttu-id="93674-106">IVMVirtualMachine::D Metodo iscardUndoDisks</span><span class="sxs-lookup"><span data-stu-id="93674-106">IVMVirtualMachine::DiscardUndoDisks method</span></span>

<span data-ttu-id="93674-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="93674-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="93674-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="93674-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="93674-109">Elimina i file modifiche disco virtuali.</span><span class="sxs-lookup"><span data-stu-id="93674-109">Discards the virtual undo disks.</span></span>

## <a name="syntax"></a><span data-ttu-id="93674-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="93674-110">Syntax</span></span>


```C++
HRESULT DiscardUndoDisks();
```



## <a name="parameters"></a><span data-ttu-id="93674-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="93674-111">Parameters</span></span>

<span data-ttu-id="93674-112">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="93674-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="93674-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="93674-113">Return value</span></span>

<span data-ttu-id="93674-114">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="93674-114">This method can return one of these values.</span></span>



| <span data-ttu-id="93674-115">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="93674-115">Return code/value</span></span>                                                                                                                                                            | <span data-ttu-id="93674-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="93674-116">Description</span></span>                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="93674-117"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="93674-117"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                  | <span data-ttu-id="93674-118">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="93674-118">The operation was successful.</span></span><br/>                                                                        |
| <dl> <span data-ttu-id="93674-119"><dt>**Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="93674-119"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>            | <span data-ttu-id="93674-120">La configurazione è sconosciuta.</span><span class="sxs-lookup"><span data-stu-id="93674-120">The configuration is unknown.</span></span><br/>                                                                        |
| <dl> <span data-ttu-id="93674-121"><dt>**Macchina virtuale \_ \_Macchina virtuale di e \_ in esecuzione \_ o \_ salvata**</dt> <dt>0xA004020B</dt></span><span class="sxs-lookup"><span data-stu-id="93674-121"><dt>**VM\_E\_VM\_RUNNING\_OR\_SAVED**</dt> <dt>0xA004020B</dt></span></span> </dl> | <span data-ttu-id="93674-122">I dischi di annullamento virtuali non possono essere rimossi mentre la macchina virtuale è in esecuzione o in uno stato salvato.</span><span class="sxs-lookup"><span data-stu-id="93674-122">The virtual undo disks cannot be discarded while the virtual machine is running or in a saved state.</span></span><br/> |
| <dl> <span data-ttu-id="93674-123"><dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="93674-123"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>            | <span data-ttu-id="93674-124">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="93674-124">An unexpected error has occurred.</span></span><br/>                                                                    |



 

## <a name="requirements"></a><span data-ttu-id="93674-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="93674-125">Requirements</span></span>



| <span data-ttu-id="93674-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="93674-126">Requirement</span></span> | <span data-ttu-id="93674-127">Valore</span><span class="sxs-lookup"><span data-stu-id="93674-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="93674-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="93674-128">Minimum supported client</span></span><br/> | <span data-ttu-id="93674-129">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="93674-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="93674-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="93674-130">Minimum supported server</span></span><br/> | <span data-ttu-id="93674-131">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="93674-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="93674-132">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="93674-132">End of client support</span></span><br/>    | <span data-ttu-id="93674-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="93674-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="93674-134">Prodotto</span><span class="sxs-lookup"><span data-stu-id="93674-134">Product</span></span><br/>                  | <span data-ttu-id="93674-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="93674-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="93674-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="93674-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="93674-137"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="93674-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="93674-138">IID</span><span class="sxs-lookup"><span data-stu-id="93674-138">IID</span></span><br/>                      | <span data-ttu-id="93674-139">IID \_ IVMVirtualMachine è definito come f7092aa1-33ed-4F78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="93674-139">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="93674-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="93674-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93674-141">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="93674-141">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

