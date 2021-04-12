---
title: Metodo IVMVirtualMachineEvents OnAdditionsAvailable (VPCCOMInterfaces. h)
description: Riceve la notifica che i componenti di integrazione sono disponibili in una macchina virtuale.
ms.assetid: c940104b-4d34-47c2-bf48-9024a7f86c46
keywords:
- Metodo OnAdditionsAvailable Virtual PC
- Metodo OnAdditionsAvailable Virtual PC, interfaccia IVMVirtualMachineEvents
- Interfaccia IVMVirtualMachineEvents Virtual PC, metodo OnAdditionsAvailable
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnAdditionsAvailable
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 193b44f533079bc957cbb8b297409641814b6e21
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478671"
---
# <a name="ivmvirtualmachineeventsonadditionsavailable-method"></a><span data-ttu-id="5647a-106">Metodo IVMVirtualMachineEvents:: OnAdditionsAvailable</span><span class="sxs-lookup"><span data-stu-id="5647a-106">IVMVirtualMachineEvents::OnAdditionsAvailable method</span></span>

<span data-ttu-id="5647a-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="5647a-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="5647a-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="5647a-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="5647a-109">Riceve la notifica che i componenti di integrazione sono disponibili in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="5647a-109">Receives notification that integration components are available in a virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="5647a-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5647a-110">Syntax</span></span>


```C++
HRESULT OnAdditionsAvailable();
```



## <a name="parameters"></a><span data-ttu-id="5647a-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="5647a-111">Parameters</span></span>

<span data-ttu-id="5647a-112">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="5647a-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5647a-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5647a-113">Return value</span></span>

<span data-ttu-id="5647a-114">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="5647a-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5647a-115">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5647a-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="5647a-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5647a-116">Requirements</span></span>



| <span data-ttu-id="5647a-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="5647a-117">Requirement</span></span> | <span data-ttu-id="5647a-118">Valore</span><span class="sxs-lookup"><span data-stu-id="5647a-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="5647a-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5647a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="5647a-120">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="5647a-120">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5647a-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5647a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="5647a-122">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="5647a-122">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="5647a-123">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="5647a-123">End of client support</span></span><br/>    | <span data-ttu-id="5647a-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="5647a-124">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="5647a-125">Prodotto</span><span class="sxs-lookup"><span data-stu-id="5647a-125">Product</span></span><br/>                  | <span data-ttu-id="5647a-126">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="5647a-126">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="5647a-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5647a-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="5647a-128"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="5647a-128"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="5647a-129">IID</span><span class="sxs-lookup"><span data-stu-id="5647a-129">IID</span></span><br/>                      | <span data-ttu-id="5647a-130">DIID \_ IVMVirtualMachineEvents è definito come 9d84f560-BB67-4961-BD12-a4da780c67e4</span><span class="sxs-lookup"><span data-stu-id="5647a-130">DIID\_IVMVirtualMachineEvents is defined as 9d84f560-bb67-4961-bd12-a4da780c67e4</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="5647a-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5647a-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5647a-132">**IVMVirtualMachineEvents**</span><span class="sxs-lookup"><span data-stu-id="5647a-132">**IVMVirtualMachineEvents**</span></span>](ivmvirtualmachineevents.md)
</dt> </dl>

 

