---
title: Metodo IVMVirtualPCEvents OnVMStateChange (VPCCOMInterfaces. h)
description: Riceve una notifica che lo stato di una macchina virtuale è stato modificato. | Metodo IVMVirtualPCEvents OnVMStateChange (VPCCOMInterfaces. h)
ms.assetid: a79afe14-9b7d-4528-ad38-e9b5ad068561
keywords:
- Metodo OnVMStateChange Virtual PC
- Metodo OnVMStateChange Virtual PC, interfaccia IVMVirtualPCEvents
- Interfaccia IVMVirtualPCEvents Virtual PC, metodo OnVMStateChange
topic_type:
- apiref
api_name:
- IVMVirtualPCEvents.OnVMStateChange
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2d0a8bd9a362c558c307fb4719c95a9ba8cbf4a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321540"
---
# <a name="ivmvirtualpceventsonvmstatechange-method"></a><span data-ttu-id="d200a-107">Metodo IVMVirtualPCEvents:: OnVMStateChange</span><span class="sxs-lookup"><span data-stu-id="d200a-107">IVMVirtualPCEvents::OnVMStateChange method</span></span>

<span data-ttu-id="d200a-108">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="d200a-108">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="d200a-109">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="d200a-109">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="d200a-110">Riceve una notifica che lo stato di una macchina virtuale è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="d200a-110">Receives notification that a virtual machine's state has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="d200a-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d200a-111">Syntax</span></span>


```C++
HRESULT OnVMStateChange(
  [in] BSTR      virtualMachineConfig,
  [in] VMVMState virtualMachineState
);
```



## <a name="parameters"></a><span data-ttu-id="d200a-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="d200a-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d200a-113">*virtualMachineConfig* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d200a-113">*virtualMachineConfig* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d200a-114">Nome della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="d200a-114">The name of the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="d200a-115">*virtualMachineState* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d200a-115">*virtualMachineState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d200a-116">Nuovo stato della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="d200a-116">The new state of the virtual machine.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d200a-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d200a-117">Return value</span></span>

<span data-ttu-id="d200a-118">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="d200a-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d200a-119">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d200a-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d200a-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="d200a-120">Remarks</span></span>

<span data-ttu-id="d200a-121">Il programma client deve implementare questo metodo di interfaccia per ricevere una notifica dell'evento **vmVirtualPCEvent \_ VMStateChanged** originato da [**IVMVirtualPC**](ivmvirtualpc.md).</span><span class="sxs-lookup"><span data-stu-id="d200a-121">The client program must implement this interface method to receive notification of the **vmVirtualPCEvent\_VMStateChanged** event originating from [**IVMVirtualPC**](ivmvirtualpc.md).</span></span> <span data-ttu-id="d200a-122">Per monitorare una macchina virtuale specifica, usare il metodo [**IVMVirtualMachineEvents:: OnStateChange**](ivmvirtualmachineevents-onstatechange.md) .</span><span class="sxs-lookup"><span data-stu-id="d200a-122">To monitor a specific virtual machine, use the [**IVMVirtualMachineEvents::OnStateChange**](ivmvirtualmachineevents-onstatechange.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="d200a-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d200a-123">Requirements</span></span>



| <span data-ttu-id="d200a-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="d200a-124">Requirement</span></span> | <span data-ttu-id="d200a-125">Valore</span><span class="sxs-lookup"><span data-stu-id="d200a-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d200a-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d200a-126">Minimum supported client</span></span><br/> | <span data-ttu-id="d200a-127">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="d200a-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d200a-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d200a-128">Minimum supported server</span></span><br/> | <span data-ttu-id="d200a-129">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="d200a-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="d200a-130">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="d200a-130">End of client support</span></span><br/>    | <span data-ttu-id="d200a-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d200a-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="d200a-132">Prodotto</span><span class="sxs-lookup"><span data-stu-id="d200a-132">Product</span></span><br/>                  | <span data-ttu-id="d200a-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="d200a-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="d200a-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d200a-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="d200a-135"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="d200a-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="d200a-136">IID</span><span class="sxs-lookup"><span data-stu-id="d200a-136">IID</span></span><br/>                      | <span data-ttu-id="d200a-137">DIID \_ IVMVirtualPCEvents è definito come efed1ef1-3c09-41f7-a9c2-7e29fa286c9d</span><span class="sxs-lookup"><span data-stu-id="d200a-137">DIID\_IVMVirtualPCEvents is defined as efed1ef1-3c09-41f7-a9c2-7e29fa286c9d</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="d200a-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d200a-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d200a-139">**IVMVirtualPCEvents**</span><span class="sxs-lookup"><span data-stu-id="d200a-139">**IVMVirtualPCEvents**</span></span>](ivmvirtualpcevents.md)
</dt> </dl>

 

