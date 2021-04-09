---
title: Metodo IVMVirtualMachineEvents OnHeartbeatStopped (VPCCOMInterfaces. h)
description: Riceve una notifica di arresto dell'heartbeat di una macchina virtuale.
ms.assetid: 58fc81a8-747c-47f9-98ec-38482694f533
keywords:
- Metodo OnHeartbeatStopped Virtual PC
- Metodo OnHeartbeatStopped Virtual PC, interfaccia IVMVirtualMachineEvents
- Interfaccia IVMVirtualMachineEvents Virtual PC, metodo OnHeartbeatStopped
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnHeartbeatStopped
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ade783d2d182439d5c500dcc114c74c8278ba6c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964703"
---
# <a name="ivmvirtualmachineeventsonheartbeatstopped-method"></a><span data-ttu-id="d3a13-106">Metodo IVMVirtualMachineEvents:: OnHeartbeatStopped</span><span class="sxs-lookup"><span data-stu-id="d3a13-106">IVMVirtualMachineEvents::OnHeartbeatStopped method</span></span>

<span data-ttu-id="d3a13-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="d3a13-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="d3a13-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="d3a13-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="d3a13-109">Riceve una notifica di arresto dell'heartbeat di una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="d3a13-109">Receives notification that a virtual machine's heartbeat has stopped.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3a13-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d3a13-110">Syntax</span></span>


```C++
HRESULT OnHeartbeatStopped();
```



## <a name="parameters"></a><span data-ttu-id="d3a13-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="d3a13-111">Parameters</span></span>

<span data-ttu-id="d3a13-112">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="d3a13-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d3a13-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d3a13-113">Return value</span></span>

<span data-ttu-id="d3a13-114">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="d3a13-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d3a13-115">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d3a13-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d3a13-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="d3a13-116">Remarks</span></span>

<span data-ttu-id="d3a13-117">Questo metodo viene chiamato quando il sistema operativo guest per questa macchina virtuale si è arrestato in modo improvviso.</span><span class="sxs-lookup"><span data-stu-id="d3a13-117">This method is called when the guest operating system for this virtual machine has stopped abruptly.</span></span> <span data-ttu-id="d3a13-118">Il programma client deve implementare questo metodo di interfaccia per ricevere una notifica dell' \_ evento vmVirtualMachineEvent HeartbeatStopped originato da [**IVMVirtualMachine**](ivmvirtualmachine.md).</span><span class="sxs-lookup"><span data-stu-id="d3a13-118">The client program must implement this interface method to receive notification of the vmVirtualMachineEvent\_HeartbeatStopped event originating from [**IVMVirtualMachine**](ivmvirtualmachine.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d3a13-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d3a13-119">Requirements</span></span>



| <span data-ttu-id="d3a13-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="d3a13-120">Requirement</span></span> | <span data-ttu-id="d3a13-121">Valore</span><span class="sxs-lookup"><span data-stu-id="d3a13-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3a13-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d3a13-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d3a13-123">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="d3a13-123">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d3a13-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d3a13-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d3a13-125">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="d3a13-125">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="d3a13-126">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="d3a13-126">End of client support</span></span><br/>    | <span data-ttu-id="d3a13-127">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d3a13-127">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="d3a13-128">Prodotto</span><span class="sxs-lookup"><span data-stu-id="d3a13-128">Product</span></span><br/>                  | <span data-ttu-id="d3a13-129">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="d3a13-129">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="d3a13-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d3a13-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="d3a13-131"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="d3a13-131"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="d3a13-132">IID</span><span class="sxs-lookup"><span data-stu-id="d3a13-132">IID</span></span><br/>                      | <span data-ttu-id="d3a13-133">DIID \_ IVMVirtualMachineEvents è definito come 9d84f560-BB67-4961-BD12-a4da780c67e4</span><span class="sxs-lookup"><span data-stu-id="d3a13-133">DIID\_IVMVirtualMachineEvents is defined as 9d84f560-bb67-4961-bd12-a4da780c67e4</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="d3a13-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d3a13-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3a13-135">**IVMVirtualMachineEvents**</span><span class="sxs-lookup"><span data-stu-id="d3a13-135">**IVMVirtualMachineEvents**</span></span>](ivmvirtualmachineevents.md)
</dt> </dl>

 

