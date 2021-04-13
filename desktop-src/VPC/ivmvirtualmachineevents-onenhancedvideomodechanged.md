---
title: Metodo IVMVirtualMachineEvents OnEnhancedVideoModeChanged (VPCCOMInterfaces. h)
description: Riceve una notifica della modifica del supporto di una macchina virtuale per la modalità video avanzata.
ms.assetid: be22a859-4687-4647-9f53-f79ae8ad52a5
keywords:
- Metodo OnEnhancedVideoModeChanged Virtual PC
- Metodo OnEnhancedVideoModeChanged Virtual PC, interfaccia IVMVirtualMachineEvents
- Interfaccia IVMVirtualMachineEvents Virtual PC, metodo OnEnhancedVideoModeChanged
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnEnhancedVideoModeChanged
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29bbc67fe298c1a47d853072d8c58ab5b3ce1988
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475028"
---
# <a name="ivmvirtualmachineeventsonenhancedvideomodechanged-method"></a><span data-ttu-id="5f079-106">Metodo IVMVirtualMachineEvents:: OnEnhancedVideoModeChanged</span><span class="sxs-lookup"><span data-stu-id="5f079-106">IVMVirtualMachineEvents::OnEnhancedVideoModeChanged method</span></span>

<span data-ttu-id="5f079-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="5f079-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="5f079-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="5f079-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="5f079-109">Riceve una notifica della modifica del supporto di una macchina virtuale per la modalità video avanzata.</span><span class="sxs-lookup"><span data-stu-id="5f079-109">Receives notification that a virtual machine's support for enhanced video mode has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f079-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5f079-110">Syntax</span></span>


```C++
HRESULT OnEnhancedVideoModeChanged(
  [in] VARIANT_BOOL enhancedVideoMode
);
```



## <a name="parameters"></a><span data-ttu-id="5f079-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="5f079-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f079-112">*enhancedVideoMode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5f079-112">*enhancedVideoMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f079-113">Indica se è disponibile la modalità video avanzata.</span><span class="sxs-lookup"><span data-stu-id="5f079-113">Indicates whether enhanced video mode is available.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f079-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5f079-114">Return value</span></span>

<span data-ttu-id="5f079-115">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="5f079-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5f079-116">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5f079-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f079-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5f079-117">Requirements</span></span>



| <span data-ttu-id="5f079-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f079-118">Requirement</span></span> | <span data-ttu-id="5f079-119">Valore</span><span class="sxs-lookup"><span data-stu-id="5f079-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f079-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5f079-120">Minimum supported client</span></span><br/> | <span data-ttu-id="5f079-121">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="5f079-121">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5f079-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5f079-122">Minimum supported server</span></span><br/> | <span data-ttu-id="5f079-123">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="5f079-123">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="5f079-124">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="5f079-124">End of client support</span></span><br/>    | <span data-ttu-id="5f079-125">Windows 7</span><span class="sxs-lookup"><span data-stu-id="5f079-125">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="5f079-126">Prodotto</span><span class="sxs-lookup"><span data-stu-id="5f079-126">Product</span></span><br/>                  | <span data-ttu-id="5f079-127">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="5f079-127">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="5f079-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5f079-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="5f079-129"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="5f079-129"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="5f079-130">IID</span><span class="sxs-lookup"><span data-stu-id="5f079-130">IID</span></span><br/>                      | <span data-ttu-id="5f079-131">DIID \_ IVMVirtualMachineEvents è definito come 9d84f560-BB67-4961-BD12-a4da780c67e4</span><span class="sxs-lookup"><span data-stu-id="5f079-131">DIID\_IVMVirtualMachineEvents is defined as 9d84f560-bb67-4961-bd12-a4da780c67e4</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="5f079-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5f079-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f079-133">**IVMVirtualMachineEvents**</span><span class="sxs-lookup"><span data-stu-id="5f079-133">**IVMVirtualMachineEvents**</span></span>](ivmvirtualmachineevents.md)
</dt> </dl>

 

