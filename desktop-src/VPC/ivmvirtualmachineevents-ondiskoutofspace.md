---
title: Metodo IVMVirtualMachineEvents OnDiskOutOfSpace (VPCCOMInterfaces. h)
description: Riceve una notifica che indica che un disco richiesto per una macchina virtuale è insufficiente.
ms.assetid: 1c431904-fffd-4513-8670-b9723f53edf1
keywords:
- Metodo OnDiskOutOfSpace Virtual PC
- Metodo OnDiskOutOfSpace Virtual PC, interfaccia IVMVirtualMachineEvents
- Interfaccia IVMVirtualMachineEvents Virtual PC, metodo OnDiskOutOfSpace
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnDiskOutOfSpace
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ac2d5f45068dc8cd7341d0a599b2da4e5c7655a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873262"
---
# <a name="ivmvirtualmachineeventsondiskoutofspace-method"></a><span data-ttu-id="0cb7a-106">Metodo IVMVirtualMachineEvents:: OnDiskOutOfSpace</span><span class="sxs-lookup"><span data-stu-id="0cb7a-106">IVMVirtualMachineEvents::OnDiskOutOfSpace method</span></span>

<span data-ttu-id="0cb7a-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="0cb7a-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="0cb7a-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="0cb7a-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="0cb7a-109">Riceve una notifica che indica che un disco necessario per una macchina virtuale (VM) ha esaurito lo spazio disponibile.</span><span class="sxs-lookup"><span data-stu-id="0cb7a-109">Receives notification that a disk required for a virtual machine (VM) is low on free space.</span></span> <span data-ttu-id="0cb7a-110">Se lo spazio disponibile scende al di sotto di 100 MB, questo evento viene ricevuto come avviso e se lo spazio disponibile scende sotto 20 MB Questo evento viene ricevuto nuovamente come errore e la macchina virtuale verrà sospesa.</span><span class="sxs-lookup"><span data-stu-id="0cb7a-110">If free space drops below 100 MB this event is received as a warning and if free space drops below 20 MB this event is received again as an error and the VM will be paused.</span></span>

## <a name="syntax"></a><span data-ttu-id="0cb7a-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0cb7a-111">Syntax</span></span>


```C++
HRESULT OnDiskOutOfSpace(
  [in] VARIANT_BOOL criticallyLow
);
```



## <a name="parameters"></a><span data-ttu-id="0cb7a-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="0cb7a-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0cb7a-113">*criticallyLow* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0cb7a-113">*criticallyLow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0cb7a-114">Impostare su **Variant \_ true** se il disco dispone di meno di 20 MB di spazio disponibile e di **Variant \_ false** se lo spazio disponibile è superiore a 20 MB ma inferiore a 100 MB.</span><span class="sxs-lookup"><span data-stu-id="0cb7a-114">Set to **VARIANT\_TRUE** if the disk has less than 20 MB free and to **VARIANT\_FALSE** if the free space is more than 20 MB but less than 100 MB.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0cb7a-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0cb7a-115">Return value</span></span>

<span data-ttu-id="0cb7a-116">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="0cb7a-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0cb7a-117">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0cb7a-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="0cb7a-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0cb7a-118">Requirements</span></span>



| <span data-ttu-id="0cb7a-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="0cb7a-119">Requirement</span></span> | <span data-ttu-id="0cb7a-120">Valore</span><span class="sxs-lookup"><span data-stu-id="0cb7a-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="0cb7a-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0cb7a-121">Minimum supported client</span></span><br/> | <span data-ttu-id="0cb7a-122">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="0cb7a-122">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0cb7a-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0cb7a-123">Minimum supported server</span></span><br/> | <span data-ttu-id="0cb7a-124">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="0cb7a-124">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="0cb7a-125">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="0cb7a-125">End of client support</span></span><br/>    | <span data-ttu-id="0cb7a-126">Windows 7</span><span class="sxs-lookup"><span data-stu-id="0cb7a-126">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="0cb7a-127">Prodotto</span><span class="sxs-lookup"><span data-stu-id="0cb7a-127">Product</span></span><br/>                  | <span data-ttu-id="0cb7a-128">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="0cb7a-128">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="0cb7a-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0cb7a-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="0cb7a-130"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="0cb7a-130"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="0cb7a-131">IID</span><span class="sxs-lookup"><span data-stu-id="0cb7a-131">IID</span></span><br/>                      | <span data-ttu-id="0cb7a-132">DIID \_ IVMVirtualMachineEvents è definito come 9d84f560-BB67-4961-BD12-a4da780c67e4</span><span class="sxs-lookup"><span data-stu-id="0cb7a-132">DIID\_IVMVirtualMachineEvents is defined as 9d84f560-bb67-4961-bd12-a4da780c67e4</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="0cb7a-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0cb7a-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0cb7a-134">**IVMVirtualMachineEvents**</span><span class="sxs-lookup"><span data-stu-id="0cb7a-134">**IVMVirtualMachineEvents**</span></span>](ivmvirtualmachineevents.md)
</dt> </dl>

 

