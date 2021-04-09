---
title: Metodo OnReset IVMVirtualMachineEvents (VPCCOMInterfaces. h)
description: Riceve la notifica che una macchina virtuale è stata reimpostata.
ms.assetid: 10a66aea-9a8f-4663-8eb6-cc35f361e43f
keywords:
- Metodo OnReset Virtual PC
- Metodo OnReset Virtual PC, interfaccia IVMVirtualMachineEvents
- Interfaccia IVMVirtualMachineEvents Virtual PC, Metodo OnReset
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnReset
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6345d0e925777fbecf42247b3e3064b9f993c7c9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963719"
---
# <a name="ivmvirtualmachineeventsonreset-method"></a><span data-ttu-id="a6879-106">Metodo IVMVirtualMachineEvents:: OnReset</span><span class="sxs-lookup"><span data-stu-id="a6879-106">IVMVirtualMachineEvents::OnReset method</span></span>

<span data-ttu-id="a6879-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="a6879-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="a6879-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="a6879-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="a6879-109">Riceve la notifica che una macchina virtuale è stata reimpostata.</span><span class="sxs-lookup"><span data-stu-id="a6879-109">Receives notification that a virtual machine has been reset.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6879-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a6879-110">Syntax</span></span>


```C++
HRESULT OnReset();
```



## <a name="parameters"></a><span data-ttu-id="a6879-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="a6879-111">Parameters</span></span>

<span data-ttu-id="a6879-112">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="a6879-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a6879-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a6879-113">Return value</span></span>

<span data-ttu-id="a6879-114">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="a6879-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a6879-115">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a6879-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a6879-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="a6879-116">Remarks</span></span>

<span data-ttu-id="a6879-117">Questo metodo viene chiamato quando la macchina virtuale è stata reimpostata.</span><span class="sxs-lookup"><span data-stu-id="a6879-117">This method is called when the virtual machine has been reset.</span></span> <span data-ttu-id="a6879-118">Il programma client deve implementare questo metodo di interfaccia per ricevere una notifica dell' \_ evento di reimpostazione vmVirtualMachineEvent originato da [**IVMVirtualMachine**](ivmvirtualmachine.md).</span><span class="sxs-lookup"><span data-stu-id="a6879-118">The client program must implement this interface method to receive notification of the vmVirtualMachineEvent\_Reset event originating from [**IVMVirtualMachine**](ivmvirtualmachine.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a6879-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a6879-119">Requirements</span></span>



| <span data-ttu-id="a6879-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="a6879-120">Requirement</span></span> | <span data-ttu-id="a6879-121">Valore</span><span class="sxs-lookup"><span data-stu-id="a6879-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6879-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a6879-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a6879-123">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="a6879-123">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a6879-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a6879-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a6879-125">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="a6879-125">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="a6879-126">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="a6879-126">End of client support</span></span><br/>    | <span data-ttu-id="a6879-127">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a6879-127">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="a6879-128">Prodotto</span><span class="sxs-lookup"><span data-stu-id="a6879-128">Product</span></span><br/>                  | <span data-ttu-id="a6879-129">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="a6879-129">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="a6879-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a6879-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="a6879-131"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="a6879-131"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="a6879-132">IID</span><span class="sxs-lookup"><span data-stu-id="a6879-132">IID</span></span><br/>                      | <span data-ttu-id="a6879-133">DIID \_ IVMVirtualMachineEvents è definito come 9d84f560-BB67-4961-BD12-a4da780c67e4</span><span class="sxs-lookup"><span data-stu-id="a6879-133">DIID\_IVMVirtualMachineEvents is defined as 9d84f560-bb67-4961-bd12-a4da780c67e4</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="a6879-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a6879-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6879-135">**IVMVirtualMachineEvents**</span><span class="sxs-lookup"><span data-stu-id="a6879-135">**IVMVirtualMachineEvents**</span></span>](ivmvirtualmachineevents.md)
</dt> </dl>

 

