---
title: Metodo IVMVirtualMachineEvents OnTripleFault (VPCCOMInterfaces. h)
description: Riceve una notifica che una macchina virtuale presenta tre errori.
ms.assetid: a17b1a05-3058-48ba-a196-7e9563f3e1c0
keywords:
- Metodo OnTripleFault Virtual PC
- Metodo OnTripleFault Virtual PC, interfaccia IVMVirtualMachineEvents
- Interfaccia IVMVirtualMachineEvents Virtual PC, metodo OnTripleFault
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnTripleFault
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48d635b9009ecadecb7aed4a921a9c609ef69505
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518562"
---
# <a name="ivmvirtualmachineeventsontriplefault-method"></a><span data-ttu-id="3594a-106">Metodo IVMVirtualMachineEvents:: OnTripleFault</span><span class="sxs-lookup"><span data-stu-id="3594a-106">IVMVirtualMachineEvents::OnTripleFault method</span></span>

<span data-ttu-id="3594a-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="3594a-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="3594a-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="3594a-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="3594a-109">Riceve una notifica che una macchina virtuale presenta tre errori.</span><span class="sxs-lookup"><span data-stu-id="3594a-109">Receives notification that a virtual machine has triple-faulted.</span></span>

## <a name="syntax"></a><span data-ttu-id="3594a-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3594a-110">Syntax</span></span>


```C++
HRESULT OnTripleFault();
```



## <a name="parameters"></a><span data-ttu-id="3594a-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="3594a-111">Parameters</span></span>

<span data-ttu-id="3594a-112">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="3594a-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3594a-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3594a-113">Return value</span></span>

<span data-ttu-id="3594a-114">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="3594a-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3594a-115">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3594a-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="3594a-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="3594a-116">Remarks</span></span>

<span data-ttu-id="3594a-117">Questo metodo viene chiamato quando una macchina virtuale presenta tre errori.</span><span class="sxs-lookup"><span data-stu-id="3594a-117">This method is called when a virtual machine has triple-faulted.</span></span> <span data-ttu-id="3594a-118">Il programma client deve implementare questo metodo di interfaccia per ricevere una notifica dell' \_ evento vmVirtualMachineEvent TripleFault originato da [**IVMVirtualMachine**](ivmvirtualmachine.md).</span><span class="sxs-lookup"><span data-stu-id="3594a-118">The client program must implement this interface method to receive notification of the vmVirtualMachineEvent\_TripleFault event originating from [**IVMVirtualMachine**](ivmvirtualmachine.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3594a-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3594a-119">Requirements</span></span>



| <span data-ttu-id="3594a-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="3594a-120">Requirement</span></span> | <span data-ttu-id="3594a-121">Valore</span><span class="sxs-lookup"><span data-stu-id="3594a-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="3594a-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3594a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="3594a-123">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="3594a-123">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3594a-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3594a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="3594a-125">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="3594a-125">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="3594a-126">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="3594a-126">End of client support</span></span><br/>    | <span data-ttu-id="3594a-127">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3594a-127">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="3594a-128">Prodotto</span><span class="sxs-lookup"><span data-stu-id="3594a-128">Product</span></span><br/>                  | <span data-ttu-id="3594a-129">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="3594a-129">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="3594a-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3594a-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="3594a-131"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="3594a-131"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="3594a-132">IID</span><span class="sxs-lookup"><span data-stu-id="3594a-132">IID</span></span><br/>                      | <span data-ttu-id="3594a-133">DIID \_ IVMVirtualMachineEvents è definito come 9d84f560-BB67-4961-BD12-a4da780c67e4</span><span class="sxs-lookup"><span data-stu-id="3594a-133">DIID\_IVMVirtualMachineEvents is defined as 9d84f560-bb67-4961-bd12-a4da780c67e4</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="3594a-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3594a-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3594a-135">**IVMVirtualMachineEvents**</span><span class="sxs-lookup"><span data-stu-id="3594a-135">**IVMVirtualMachineEvents**</span></span>](ivmvirtualmachineevents.md)
</dt> </dl>

 

