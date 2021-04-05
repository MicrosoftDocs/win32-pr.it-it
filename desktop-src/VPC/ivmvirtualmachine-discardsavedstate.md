---
title: Metodo IVMVirtualMachine DiscardSavedState (VPCCOMInterfaces. h)
description: Elimina le informazioni sullo stato salvato per una macchina virtuale salvata.
ms.assetid: 546d6ea9-bfa3-487d-a333-399986bdf9a1
keywords:
- Metodo DiscardSavedState Virtual PC
- Metodo DiscardSavedState Virtual PC, interfaccia IVMVirtualMachine
- Interfaccia IVMVirtualMachine Virtual PC, metodo DiscardSavedState
topic_type:
- apiref
api_name:
- IVMVirtualMachine.DiscardSavedState
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ce5c9cc0b07af2cc8c995d0c368d7747fa1475a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048493"
---
# <a name="ivmvirtualmachinediscardsavedstate-method"></a><span data-ttu-id="a32f9-106">IVMVirtualMachine::D Metodo iscardSavedState</span><span class="sxs-lookup"><span data-stu-id="a32f9-106">IVMVirtualMachine::DiscardSavedState method</span></span>

<span data-ttu-id="a32f9-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="a32f9-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="a32f9-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="a32f9-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="a32f9-109">Elimina le informazioni sullo stato salvato per una macchina virtuale salvata.</span><span class="sxs-lookup"><span data-stu-id="a32f9-109">Discards any saved state information for a saved virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="a32f9-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a32f9-110">Syntax</span></span>


```C++
HRESULT DiscardSavedState();
```



## <a name="parameters"></a><span data-ttu-id="a32f9-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="a32f9-111">Parameters</span></span>

<span data-ttu-id="a32f9-112">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="a32f9-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a32f9-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a32f9-113">Return value</span></span>

<span data-ttu-id="a32f9-114">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="a32f9-114">This method can return one of these values.</span></span>



| <span data-ttu-id="a32f9-115">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="a32f9-115">Return code/value</span></span>                                                                                                                                                           | <span data-ttu-id="a32f9-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a32f9-116">Description</span></span>                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a32f9-117"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="a32f9-117"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                 | <span data-ttu-id="a32f9-118">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="a32f9-118">The operation was successful.</span></span><br/>                               |
| <dl> <span data-ttu-id="a32f9-119"><dt>**Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="a32f9-119"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>           | <span data-ttu-id="a32f9-120">La configurazione è sconosciuta.</span><span class="sxs-lookup"><span data-stu-id="a32f9-120">The configuration is unknown.</span></span><br/>                               |
| <dl> <span data-ttu-id="a32f9-121"><dt>**Macchina virtuale \_ E \_ macchina virtuale \_ che esegue**</dt> <dt>0xA0040500</dt></span><span class="sxs-lookup"><span data-stu-id="a32f9-121"><dt>**VM\_E\_VM\_RUNNING**</dt> <dt>0xA0040500</dt></span></span> </dl>           | <span data-ttu-id="a32f9-122">La macchina virtuale è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="a32f9-122">The virtual machine is running.</span></span><br/>                             |
| <dl> <span data-ttu-id="a32f9-123"><dt>**Macchina virtuale \_ E \_ VM \_ senza \_ \_ stato salvato**</dt> <dt>0xA00400501</dt></span><span class="sxs-lookup"><span data-stu-id="a32f9-123"><dt>**VM\_E\_VM\_NO\_SAVED\_STATE**</dt> <dt>0xA00400501</dt></span></span> </dl> | <span data-ttu-id="a32f9-124">La macchina virtuale non è in esecuzione, ma non ha uno stato salvato.</span><span class="sxs-lookup"><span data-stu-id="a32f9-124">The virtual machine is not running, but has no saved state.</span></span><br/> |
| <dl> <span data-ttu-id="a32f9-125"><dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="a32f9-125"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>           | <span data-ttu-id="a32f9-126">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="a32f9-126">An unexpected error has occurred.</span></span><br/>                           |



 

## <a name="requirements"></a><span data-ttu-id="a32f9-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a32f9-127">Requirements</span></span>



| <span data-ttu-id="a32f9-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="a32f9-128">Requirement</span></span> | <span data-ttu-id="a32f9-129">Valore</span><span class="sxs-lookup"><span data-stu-id="a32f9-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a32f9-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a32f9-130">Minimum supported client</span></span><br/> | <span data-ttu-id="a32f9-131">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="a32f9-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a32f9-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a32f9-132">Minimum supported server</span></span><br/> | <span data-ttu-id="a32f9-133">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="a32f9-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="a32f9-134">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="a32f9-134">End of client support</span></span><br/>    | <span data-ttu-id="a32f9-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a32f9-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="a32f9-136">Prodotto</span><span class="sxs-lookup"><span data-stu-id="a32f9-136">Product</span></span><br/>                  | <span data-ttu-id="a32f9-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="a32f9-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="a32f9-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a32f9-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="a32f9-139"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="a32f9-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="a32f9-140">IID</span><span class="sxs-lookup"><span data-stu-id="a32f9-140">IID</span></span><br/>                      | <span data-ttu-id="a32f9-141">IID \_ IVMVirtualMachine è definito come f7092aa1-33ed-4F78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="a32f9-141">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="a32f9-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a32f9-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a32f9-143">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="a32f9-143">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

