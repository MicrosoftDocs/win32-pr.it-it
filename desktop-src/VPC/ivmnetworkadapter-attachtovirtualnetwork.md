---
title: Metodo IVMNetworkAdapter AttachToVirtualNetwork (VPCCOMInterfaces. h)
description: Connette l'interfaccia di rete alla rete virtuale specificata.
ms.assetid: c743e930-c22e-4f32-b691-f7adc2485fed
keywords:
- Metodo AttachToVirtualNetwork Virtual PC
- Metodo AttachToVirtualNetwork Virtual PC, interfaccia IVMNetworkAdapter
- Interfaccia IVMNetworkAdapter Virtual PC, metodo AttachToVirtualNetwork
topic_type:
- apiref
api_name:
- IVMNetworkAdapter.AttachToVirtualNetwork
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01e7d0d9822e73ef6081a35f19ef628fd10051b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477188"
---
# <a name="ivmnetworkadapterattachtovirtualnetwork-method"></a><span data-ttu-id="2a2a4-106">Metodo IVMNetworkAdapter:: AttachToVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="2a2a4-106">IVMNetworkAdapter::AttachToVirtualNetwork method</span></span>

<span data-ttu-id="2a2a4-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="2a2a4-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="2a2a4-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="2a2a4-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="2a2a4-109">Connette l'interfaccia di rete alla rete virtuale specificata.</span><span class="sxs-lookup"><span data-stu-id="2a2a4-109">Attaches the network interface to the specified virtual network.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a2a4-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2a2a4-110">Syntax</span></span>


```C++
HRESULT AttachToVirtualNetwork(
  [in] IVMVirtualNetwork *virtualNetwork
);
```



## <a name="parameters"></a><span data-ttu-id="2a2a4-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="2a2a4-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a2a4-112">*virtualNetwork* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2a2a4-112">*virtualNetwork* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a2a4-113">Rete virtuale a cui verrà connessa la scheda di interfaccia di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="2a2a4-113">The virtual network to which this virtual NIC will be connected.</span></span> <span data-ttu-id="2a2a4-114">Vedere [**IVMVirtualNetwork**](ivmvirtualnetwork.md).</span><span class="sxs-lookup"><span data-stu-id="2a2a4-114">See [**IVMVirtualNetwork**](ivmvirtualnetwork.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a2a4-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2a2a4-115">Return value</span></span>

<span data-ttu-id="2a2a4-116">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="2a2a4-116">This method can return one of these values.</span></span>



| <span data-ttu-id="2a2a4-117">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="2a2a4-117">Return code/value</span></span>                                                                                                                                                                          | <span data-ttu-id="2a2a4-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2a2a4-118">Description</span></span>                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="2a2a4-119"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="2a2a4-119"><dt>**S\_OK**</dt></span></span> </dl>                                                                                                       | <span data-ttu-id="2a2a4-120">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="2a2a4-120">The operation was successful.</span></span><br/>                           |
| <dl> <span data-ttu-id="2a2a4-121"><dt>**E \_ PUNTATORE**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="2a2a4-121"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                  | <span data-ttu-id="2a2a4-122">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="2a2a4-122">The parameter is **NULL**.</span></span><br/>                              |
| <dl> <span data-ttu-id="2a2a4-123"><dt>**E \_**</dt> <dt>0x80000003</dt> INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="2a2a4-123"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                               | <span data-ttu-id="2a2a4-124">Il parametro non contiene una rete virtuale valida.</span><span class="sxs-lookup"><span data-stu-id="2a2a4-124">The parameter does not contain a valid virtual network.</span></span><br/> |
| <dl> <span data-ttu-id="2a2a4-125"><dt>**HRESULT \_ DA \_ Win32 ( \_ accesso errore \_ negato)**</dt> <dt>0x80070005</dt></span><span class="sxs-lookup"><span data-stu-id="2a2a4-125"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ACCESS\_DENIED)**</dt> <dt>0x80070005</dt></span></span> </dl> | <span data-ttu-id="2a2a4-126">Accesso negato alla rete virtuale richiesta.</span><span class="sxs-lookup"><span data-stu-id="2a2a4-126">Access was denied to the requested virtual network.</span></span><br/>     |
| <dl> <span data-ttu-id="2a2a4-127"><dt>**Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="2a2a4-127"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>                          | <span data-ttu-id="2a2a4-128">La macchina virtuale non è valida o non esiste più.</span><span class="sxs-lookup"><span data-stu-id="2a2a4-128">The virtual machine is invalid or no longer exists.</span></span><br/>     |
| <dl> <span data-ttu-id="2a2a4-129"><dt>**\_ \_ \_ \_ ID rete virtuale non valido E VM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2a2a4-129"><dt>**VM\_E\_INVALID\_VIRTUAL\_NETWORK\_ID**</dt></span></span> </dl>                                                                        | <span data-ttu-id="2a2a4-130">Il parametro non è una rete virtuale esistente.</span><span class="sxs-lookup"><span data-stu-id="2a2a4-130">The parameter is not an existing virtual network.</span></span><br/>       |
| <dl> <span data-ttu-id="2a2a4-131"><dt>**\_eccezione disp E \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2a2a4-131"><dt>**DISP\_E\_EXCEPTION**</dt></span></span> </dl>                                                                                          | <span data-ttu-id="2a2a4-132">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="2a2a4-132">An unexpected error has occurred.</span></span><br/>                       |



 

## <a name="requirements"></a><span data-ttu-id="2a2a4-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2a2a4-133">Requirements</span></span>



| <span data-ttu-id="2a2a4-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="2a2a4-134">Requirement</span></span> | <span data-ttu-id="2a2a4-135">Valore</span><span class="sxs-lookup"><span data-stu-id="2a2a4-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a2a4-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2a2a4-136">Minimum supported client</span></span><br/> | <span data-ttu-id="2a2a4-137">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="2a2a4-137">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2a2a4-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2a2a4-138">Minimum supported server</span></span><br/> | <span data-ttu-id="2a2a4-139">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="2a2a4-139">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="2a2a4-140">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="2a2a4-140">End of client support</span></span><br/>    | <span data-ttu-id="2a2a4-141">Windows 7</span><span class="sxs-lookup"><span data-stu-id="2a2a4-141">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="2a2a4-142">Prodotto</span><span class="sxs-lookup"><span data-stu-id="2a2a4-142">Product</span></span><br/>                  | <span data-ttu-id="2a2a4-143">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="2a2a4-143">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="2a2a4-144">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2a2a4-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="2a2a4-145"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="2a2a4-145"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="2a2a4-146">IID</span><span class="sxs-lookup"><span data-stu-id="2a2a4-146">IID</span></span><br/>                      | <span data-ttu-id="2a2a4-147">IID \_ IVMNetworkAdapter è definito come e32e4165-22b8-4DC0-8d57-850171ae207a</span><span class="sxs-lookup"><span data-stu-id="2a2a4-147">IID\_IVMNetworkAdapter is defined as e32e4165-22b8-4dc0-8d57-850171ae207a</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="2a2a4-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2a2a4-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a2a4-149">**IVMNetworkAdapter**</span><span class="sxs-lookup"><span data-stu-id="2a2a4-149">**IVMNetworkAdapter**</span></span>](ivmnetworkadapter.md)
</dt> </dl>

 

