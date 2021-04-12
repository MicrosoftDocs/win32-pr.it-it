---
title: Metodo IVMVirtualMachineEvents OnAdditionsUninstalled (VPCCOMInterfaces. h)
description: Riceve una notifica di disinstallazione dei componenti di integrazione in una macchina virtuale.
ms.assetid: bbbc01b6-adb1-491e-a5b0-ff463dca7dfd
keywords:
- Metodo OnAdditionsUninstalled Virtual PC
- Metodo OnAdditionsUninstalled Virtual PC, interfaccia IVMVirtualMachineEvents
- Interfaccia IVMVirtualMachineEvents Virtual PC, metodo OnAdditionsUninstalled
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnAdditionsUninstalled
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 514a88249ad34d51965df75feab6f129bd9fa5a2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104118906"
---
# <a name="ivmvirtualmachineeventsonadditionsuninstalled-method"></a><span data-ttu-id="d9da9-106">Metodo IVMVirtualMachineEvents:: OnAdditionsUninstalled</span><span class="sxs-lookup"><span data-stu-id="d9da9-106">IVMVirtualMachineEvents::OnAdditionsUninstalled method</span></span>

<span data-ttu-id="d9da9-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="d9da9-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="d9da9-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="d9da9-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="d9da9-109">Riceve una notifica di disinstallazione dei componenti di integrazione in una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="d9da9-109">Receives notification that integration components are uninstalled in a virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9da9-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d9da9-110">Syntax</span></span>


```C++
HRESULT OnAdditionsUninstalled();
```



## <a name="parameters"></a><span data-ttu-id="d9da9-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="d9da9-111">Parameters</span></span>

<span data-ttu-id="d9da9-112">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="d9da9-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d9da9-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d9da9-113">Return value</span></span>

<span data-ttu-id="d9da9-114">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="d9da9-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d9da9-115">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d9da9-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9da9-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d9da9-116">Requirements</span></span>



| <span data-ttu-id="d9da9-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="d9da9-117">Requirement</span></span> | <span data-ttu-id="d9da9-118">Valore</span><span class="sxs-lookup"><span data-stu-id="d9da9-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9da9-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d9da9-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d9da9-120">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="d9da9-120">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d9da9-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d9da9-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d9da9-122">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="d9da9-122">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="d9da9-123">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="d9da9-123">End of client support</span></span><br/>    | <span data-ttu-id="d9da9-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d9da9-124">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="d9da9-125">Prodotto</span><span class="sxs-lookup"><span data-stu-id="d9da9-125">Product</span></span><br/>                  | <span data-ttu-id="d9da9-126">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="d9da9-126">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="d9da9-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d9da9-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="d9da9-128"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="d9da9-128"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="d9da9-129">IID</span><span class="sxs-lookup"><span data-stu-id="d9da9-129">IID</span></span><br/>                      | <span data-ttu-id="d9da9-130">DIID \_ IVMVirtualMachineEvents è definito come 9d84f560-BB67-4961-BD12-a4da780c67e4</span><span class="sxs-lookup"><span data-stu-id="d9da9-130">DIID\_IVMVirtualMachineEvents is defined as 9d84f560-bb67-4961-bd12-a4da780c67e4</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="d9da9-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d9da9-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9da9-132">**IVMVirtualMachineEvents**</span><span class="sxs-lookup"><span data-stu-id="d9da9-132">**IVMVirtualMachineEvents**</span></span>](ivmvirtualmachineevents.md)
</dt> </dl>

 

