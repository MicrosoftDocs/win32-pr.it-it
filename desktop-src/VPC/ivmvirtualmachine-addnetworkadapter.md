---
title: Metodo IVMVirtualMachine AddNetworkAdapter (VPCCOMInterfaces. h)
description: Aggiunge un'interfaccia di rete alla macchina virtuale.
ms.assetid: 1fa39d2c-4a5a-42cb-afa4-520bf19b8cc8
keywords:
- Metodo AddNetworkAdapter Virtual PC
- Metodo AddNetworkAdapter Virtual PC, interfaccia IVMVirtualMachine
- Interfaccia IVMVirtualMachine Virtual PC, metodo AddNetworkAdapter
topic_type:
- apiref
api_name:
- IVMVirtualMachine.AddNetworkAdapter
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8d24351e5f5a32aff08e755329ac12baaaaf546
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302095"
---
# <a name="ivmvirtualmachineaddnetworkadapter-method"></a><span data-ttu-id="2f7ab-106">Metodo IVMVirtualMachine:: AddNetworkAdapter</span><span class="sxs-lookup"><span data-stu-id="2f7ab-106">IVMVirtualMachine::AddNetworkAdapter method</span></span>

<span data-ttu-id="2f7ab-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="2f7ab-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="2f7ab-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="2f7ab-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="2f7ab-109">Aggiunge un'interfaccia di rete alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="2f7ab-109">Adds a network interface to the virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f7ab-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2f7ab-110">Syntax</span></span>


```C++
HRESULT AddNetworkAdapter(
  [out, retval] IVMNetworkAdapter **networkAdapter
);
```



## <a name="parameters"></a><span data-ttu-id="2f7ab-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="2f7ab-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f7ab-112">*NetworkAdapter* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="2f7ab-112">*networkAdapter* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="2f7ab-113">Oggetto [**IVMNetworkAdapter**](ivmnetworkadapter.md) .</span><span class="sxs-lookup"><span data-stu-id="2f7ab-113">An [**IVMNetworkAdapter**](ivmnetworkadapter.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f7ab-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2f7ab-114">Return value</span></span>

<span data-ttu-id="2f7ab-115">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="2f7ab-115">This method can return one of these values.</span></span>



| <span data-ttu-id="2f7ab-116">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="2f7ab-116">Return code/value</span></span>                                                                                                                                                            | <span data-ttu-id="2f7ab-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2f7ab-117">Description</span></span>                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="2f7ab-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="2f7ab-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                  | <span data-ttu-id="2f7ab-119">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="2f7ab-119">The operation was successful.</span></span><br/>                        |
| <dl> <span data-ttu-id="2f7ab-120"><dt>**E \_ PUNTATORE**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="2f7ab-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                    | <span data-ttu-id="2f7ab-121">Il parametro *NetworkAdapter* è **null**.</span><span class="sxs-lookup"><span data-stu-id="2f7ab-121">The *networkAdapter* parameter is **NULL**.</span></span><br/>          |
| <dl> <span data-ttu-id="2f7ab-122"><dt>**Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="2f7ab-122"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>            | <span data-ttu-id="2f7ab-123">La configurazione è sconosciuta.</span><span class="sxs-lookup"><span data-stu-id="2f7ab-123">The configuration is unknown.</span></span><br/>                        |
| <dl> <span data-ttu-id="2f7ab-124"><dt>**Macchina virtuale \_ 0xA0040301 \_ \_ \_ valore non valido E pref**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="2f7ab-124"><dt>**VM\_E\_PREF\_ILLEGAL\_VALUE**</dt> <dt>0xA0040301</dt></span></span> </dl>   | <span data-ttu-id="2f7ab-125">Non è possibile aggiungere più di quattro schede di rete (4).</span><span class="sxs-lookup"><span data-stu-id="2f7ab-125">No more than four (4) network adapters can be added.</span></span><br/> |
| <dl> <span data-ttu-id="2f7ab-126"><dt>**Macchina virtuale \_ \_Macchina virtuale di e \_ in esecuzione \_ o \_ salvata**</dt> <dt>0xA004020B</dt></span><span class="sxs-lookup"><span data-stu-id="2f7ab-126"><dt>**VM\_E\_VM\_RUNNING\_OR\_SAVED**</dt> <dt>0xA004020B</dt></span></span> </dl> | <span data-ttu-id="2f7ab-127">Lo stato della macchina virtuale è in esecuzione o salvato.</span><span class="sxs-lookup"><span data-stu-id="2f7ab-127">The virtual machine is in a running or saved state.</span></span><br/>  |
| <dl> <span data-ttu-id="2f7ab-128"><dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="2f7ab-128"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>            | <span data-ttu-id="2f7ab-129">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="2f7ab-129">An unexpected error has occurred.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="2f7ab-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="2f7ab-130">Remarks</span></span>

<span data-ttu-id="2f7ab-131">È possibile aggiungere solo una nuova interfaccia di rete a una macchina virtuale arrestata.</span><span class="sxs-lookup"><span data-stu-id="2f7ab-131">You can only add a new network interface to a stopped virtual machine.</span></span> <span data-ttu-id="2f7ab-132">La scheda di rete appena creata non è connessa a una rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="2f7ab-132">The newly created network adapter is not connected to a virtual network.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f7ab-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2f7ab-133">Requirements</span></span>



| <span data-ttu-id="2f7ab-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f7ab-134">Requirement</span></span> | <span data-ttu-id="2f7ab-135">Valore</span><span class="sxs-lookup"><span data-stu-id="2f7ab-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f7ab-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2f7ab-136">Minimum supported client</span></span><br/> | <span data-ttu-id="2f7ab-137">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="2f7ab-137">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2f7ab-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2f7ab-138">Minimum supported server</span></span><br/> | <span data-ttu-id="2f7ab-139">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="2f7ab-139">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="2f7ab-140">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="2f7ab-140">End of client support</span></span><br/>    | <span data-ttu-id="2f7ab-141">Windows 7</span><span class="sxs-lookup"><span data-stu-id="2f7ab-141">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="2f7ab-142">Prodotto</span><span class="sxs-lookup"><span data-stu-id="2f7ab-142">Product</span></span><br/>                  | <span data-ttu-id="2f7ab-143">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="2f7ab-143">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="2f7ab-144">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2f7ab-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f7ab-145"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f7ab-145"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="2f7ab-146">IID</span><span class="sxs-lookup"><span data-stu-id="2f7ab-146">IID</span></span><br/>                      | <span data-ttu-id="2f7ab-147">IID \_ IVMVirtualMachine è definito come f7092aa1-33ed-4F78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="2f7ab-147">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="2f7ab-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2f7ab-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f7ab-149">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="2f7ab-149">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

