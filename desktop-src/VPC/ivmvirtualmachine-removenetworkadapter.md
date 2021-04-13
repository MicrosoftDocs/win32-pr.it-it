---
title: Metodo IVMVirtualMachine RemoveNetworkAdapter (VPCCOMInterfaces. h)
description: Rimuove un'interfaccia di rete dalla macchina virtuale.
ms.assetid: 25a5b172-55b8-4cbe-98aa-630148cf6b6d
keywords:
- Metodo RemoveNetworkAdapter Virtual PC
- Metodo RemoveNetworkAdapter Virtual PC, interfaccia IVMVirtualMachine
- Interfaccia IVMVirtualMachine Virtual PC, metodo RemoveNetworkAdapter
topic_type:
- apiref
api_name:
- IVMVirtualMachine.RemoveNetworkAdapter
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27424f7a3dc5445f56d960393aa12345fcf5f1cc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478347"
---
# <a name="ivmvirtualmachineremovenetworkadapter-method"></a><span data-ttu-id="49002-106">Metodo IVMVirtualMachine:: RemoveNetworkAdapter</span><span class="sxs-lookup"><span data-stu-id="49002-106">IVMVirtualMachine::RemoveNetworkAdapter method</span></span>

<span data-ttu-id="49002-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="49002-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="49002-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="49002-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="49002-109">Rimuove un'interfaccia di rete dalla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="49002-109">Removes a network interface from the virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="49002-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="49002-110">Syntax</span></span>


```C++
HRESULT RemoveNetworkAdapter(
  [in] IVMNetworkAdapter *networkAdapter
);
```



## <a name="parameters"></a><span data-ttu-id="49002-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="49002-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49002-112">*NetworkAdapter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="49002-112">*networkAdapter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49002-113">Oggetto [**IVMNetworkAdapter**](ivmnetworkadapter.md) che rappresenta la scheda di rete da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="49002-113">An [**IVMNetworkAdapter**](ivmnetworkadapter.md) object that represents the network adapter to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49002-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="49002-114">Return value</span></span>

<span data-ttu-id="49002-115">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="49002-115">This method can return one of these values.</span></span>



| <span data-ttu-id="49002-116">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="49002-116">Return code/value</span></span>                                                                                                                                                            | <span data-ttu-id="49002-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="49002-117">Description</span></span>                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <span data-ttu-id="49002-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="49002-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                  | <span data-ttu-id="49002-119">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="49002-119">The operation was successful.</span></span><br/>                       |
| <dl> <span data-ttu-id="49002-120"><dt>**E \_ PUNTATORE**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="49002-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                    | <span data-ttu-id="49002-121">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="49002-121">The parameter is **NULL**.</span></span><br/>                          |
| <dl> <span data-ttu-id="49002-122"><dt>**Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="49002-122"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>            | <span data-ttu-id="49002-123">La configurazione è sconosciuta.</span><span class="sxs-lookup"><span data-stu-id="49002-123">The configuration is unknown.</span></span><br/>                       |
| <dl> <span data-ttu-id="49002-124"><dt>**Macchina virtuale \_ \_Macchina virtuale di e \_ in esecuzione \_ o \_ salvata**</dt> <dt>0xA004020B</dt></span><span class="sxs-lookup"><span data-stu-id="49002-124"><dt>**VM\_E\_VM\_RUNNING\_OR\_SAVED**</dt> <dt>0xA004020B</dt></span></span> </dl> | <span data-ttu-id="49002-125">Lo stato della macchina virtuale è in esecuzione o salvato.</span><span class="sxs-lookup"><span data-stu-id="49002-125">The virtual machine is in a running or saved state.</span></span><br/> |
| <dl> <span data-ttu-id="49002-126"><dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="49002-126"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>            | <span data-ttu-id="49002-127">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="49002-127">An unexpected error has occurred.</span></span><br/>                   |



 

## <a name="remarks"></a><span data-ttu-id="49002-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="49002-128">Remarks</span></span>

<span data-ttu-id="49002-129">È possibile rimuovere solo un'interfaccia di rete esistente da una macchina virtuale arrestata.</span><span class="sxs-lookup"><span data-stu-id="49002-129">You can only remove an existing network interface from a virtual machine that is stopped.</span></span>

## <a name="requirements"></a><span data-ttu-id="49002-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="49002-130">Requirements</span></span>



| <span data-ttu-id="49002-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="49002-131">Requirement</span></span> | <span data-ttu-id="49002-132">Valore</span><span class="sxs-lookup"><span data-stu-id="49002-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="49002-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="49002-133">Minimum supported client</span></span><br/> | <span data-ttu-id="49002-134">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="49002-134">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="49002-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="49002-135">Minimum supported server</span></span><br/> | <span data-ttu-id="49002-136">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="49002-136">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="49002-137">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="49002-137">End of client support</span></span><br/>    | <span data-ttu-id="49002-138">Windows 7</span><span class="sxs-lookup"><span data-stu-id="49002-138">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="49002-139">Prodotto</span><span class="sxs-lookup"><span data-stu-id="49002-139">Product</span></span><br/>                  | <span data-ttu-id="49002-140">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="49002-140">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="49002-141">Intestazione</span><span class="sxs-lookup"><span data-stu-id="49002-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="49002-142"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="49002-142"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="49002-143">IID</span><span class="sxs-lookup"><span data-stu-id="49002-143">IID</span></span><br/>                      | <span data-ttu-id="49002-144">IID \_ IVMVirtualMachine è definito come f7092aa1-33ed-4F78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="49002-144">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="49002-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="49002-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49002-146">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="49002-146">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

