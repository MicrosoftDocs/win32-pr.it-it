---
title: Metodo IVMVirtualMachineEvents OnStateChange (VPCCOMInterfaces. h)
description: Riceve una notifica che lo stato di una macchina virtuale è stato modificato. | Metodo IVMVirtualMachineEvents OnStateChange (VPCCOMInterfaces. h)
ms.assetid: 1737bb5e-078d-4ebe-9558-de083aae1baa
keywords:
- Metodo OnStateChange Virtual PC
- Metodo OnStateChange Virtual PC, interfaccia IVMVirtualMachineEvents
- Interfaccia IVMVirtualMachineEvents Virtual PC, metodo OnStateChange
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnStateChange
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7da112d8f6211882953056afef0219b9efdf9843
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353821"
---
# <a name="ivmvirtualmachineeventsonstatechange-method"></a><span data-ttu-id="6ba4e-107">Metodo IVMVirtualMachineEvents:: OnStateChange</span><span class="sxs-lookup"><span data-stu-id="6ba4e-107">IVMVirtualMachineEvents::OnStateChange method</span></span>

<span data-ttu-id="6ba4e-108">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="6ba4e-108">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="6ba4e-109">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="6ba4e-109">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="6ba4e-110">Riceve una notifica che lo stato di una macchina virtuale è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="6ba4e-110">Receives notification that a virtual machine's state has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ba4e-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6ba4e-111">Syntax</span></span>


```C++
HRESULT OnStateChange(
  [in] VMVMState virtualMachineState
);
```



## <a name="parameters"></a><span data-ttu-id="6ba4e-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="6ba4e-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ba4e-113">*virtualMachineState* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6ba4e-113">*virtualMachineState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ba4e-114">Nuovo stato della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="6ba4e-114">The new state of the virtual machine.</span></span> <span data-ttu-id="6ba4e-115">Per un elenco di valori, vedere [**VMVMState**](vmvmstate.md).</span><span class="sxs-lookup"><span data-stu-id="6ba4e-115">For a list of values, see [**VMVMState**](vmvmstate.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ba4e-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6ba4e-116">Return value</span></span>

<span data-ttu-id="6ba4e-117">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="6ba4e-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6ba4e-118">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6ba4e-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ba4e-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="6ba4e-119">Remarks</span></span>

<span data-ttu-id="6ba4e-120">Questo metodo viene chiamato quando viene modificato lo stato della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="6ba4e-120">This method is called when the state for this virtual machine changes.</span></span> <span data-ttu-id="6ba4e-121">Il programma client deve implementare questo metodo di interfaccia per ricevere una notifica dell' \_ evento vmVirtualMachineEvent StateChanged originato da [**IVMVirtualMachine**](ivmvirtualmachine.md).</span><span class="sxs-lookup"><span data-stu-id="6ba4e-121">The client program must implement this interface method to receive notification of the vmVirtualMachineEvent\_StateChanged event originating from [**IVMVirtualMachine**](ivmvirtualmachine.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6ba4e-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6ba4e-122">Requirements</span></span>



| <span data-ttu-id="6ba4e-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ba4e-123">Requirement</span></span> | <span data-ttu-id="6ba4e-124">Valore</span><span class="sxs-lookup"><span data-stu-id="6ba4e-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ba4e-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6ba4e-125">Minimum supported client</span></span><br/> | <span data-ttu-id="6ba4e-126">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="6ba4e-126">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6ba4e-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6ba4e-127">Minimum supported server</span></span><br/> | <span data-ttu-id="6ba4e-128">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="6ba4e-128">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="6ba4e-129">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="6ba4e-129">End of client support</span></span><br/>    | <span data-ttu-id="6ba4e-130">Windows 7</span><span class="sxs-lookup"><span data-stu-id="6ba4e-130">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="6ba4e-131">Prodotto</span><span class="sxs-lookup"><span data-stu-id="6ba4e-131">Product</span></span><br/>                  | <span data-ttu-id="6ba4e-132">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="6ba4e-132">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="6ba4e-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6ba4e-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="6ba4e-134"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="6ba4e-134"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="6ba4e-135">IID</span><span class="sxs-lookup"><span data-stu-id="6ba4e-135">IID</span></span><br/>                      | <span data-ttu-id="6ba4e-136">DIID \_ IVMVirtualMachineEvents è definito come 9d84f560-BB67-4961-BD12-a4da780c67e4</span><span class="sxs-lookup"><span data-stu-id="6ba4e-136">DIID\_IVMVirtualMachineEvents is defined as 9d84f560-bb67-4961-bd12-a4da780c67e4</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="6ba4e-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6ba4e-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ba4e-138">**IVMVirtualMachineEvents**</span><span class="sxs-lookup"><span data-stu-id="6ba4e-138">**IVMVirtualMachineEvents**</span></span>](ivmvirtualmachineevents.md)
</dt> </dl>

 

