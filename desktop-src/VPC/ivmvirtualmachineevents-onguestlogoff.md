---
title: Metodo IVMVirtualMachineEvents OnGuestLogoff (VPCCOMInterfaces. h)
description: Riceve la notifica che un utente si è disconnesso dal sistema operativo guest.
ms.assetid: 3771ba28-eea9-4c8b-9224-231b00d2f2f5
keywords:
- Metodo OnGuestLogoff Virtual PC
- Metodo OnGuestLogoff Virtual PC, interfaccia IVMVirtualMachineEvents
- Interfaccia IVMVirtualMachineEvents Virtual PC, metodo OnGuestLogoff
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnGuestLogoff
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ce5100c3901b3de32a769b6bae0e16fcffe26a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963720"
---
# <a name="ivmvirtualmachineeventsonguestlogoff-method"></a><span data-ttu-id="5453c-106">Metodo IVMVirtualMachineEvents:: OnGuestLogoff</span><span class="sxs-lookup"><span data-stu-id="5453c-106">IVMVirtualMachineEvents::OnGuestLogoff method</span></span>

<span data-ttu-id="5453c-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="5453c-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="5453c-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="5453c-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="5453c-109">Riceve la notifica che un utente si è disconnesso dal sistema operativo guest.</span><span class="sxs-lookup"><span data-stu-id="5453c-109">Receives notification that a user has logged off from the guest operating system.</span></span>

## <a name="syntax"></a><span data-ttu-id="5453c-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5453c-110">Syntax</span></span>


```C++
HRESULT OnGuestLogoff(
  [in] VMLogoffType logoffType
);
```



## <a name="parameters"></a><span data-ttu-id="5453c-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="5453c-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5453c-112">*logoffType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5453c-112">*logoffType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5453c-113">Valore dell'enumerazione [**VMLogoffType**](vmlogofftype.md) che descrive il tipo di disconnessione.</span><span class="sxs-lookup"><span data-stu-id="5453c-113">Value from the [**VMLogoffType**](vmlogofftype.md) enumeration that describes the type of logoff.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5453c-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5453c-114">Return value</span></span>

<span data-ttu-id="5453c-115">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="5453c-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5453c-116">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5453c-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="5453c-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5453c-117">Requirements</span></span>



| <span data-ttu-id="5453c-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="5453c-118">Requirement</span></span> | <span data-ttu-id="5453c-119">Valore</span><span class="sxs-lookup"><span data-stu-id="5453c-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="5453c-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5453c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="5453c-121">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="5453c-121">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5453c-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5453c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="5453c-123">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="5453c-123">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="5453c-124">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="5453c-124">End of client support</span></span><br/>    | <span data-ttu-id="5453c-125">Windows 7</span><span class="sxs-lookup"><span data-stu-id="5453c-125">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="5453c-126">Prodotto</span><span class="sxs-lookup"><span data-stu-id="5453c-126">Product</span></span><br/>                  | <span data-ttu-id="5453c-127">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="5453c-127">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="5453c-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5453c-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="5453c-129"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="5453c-129"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="5453c-130">IID</span><span class="sxs-lookup"><span data-stu-id="5453c-130">IID</span></span><br/>                      | <span data-ttu-id="5453c-131">DIID \_ IVMVirtualMachineEvents è definito come 9d84f560-BB67-4961-BD12-a4da780c67e4</span><span class="sxs-lookup"><span data-stu-id="5453c-131">DIID\_IVMVirtualMachineEvents is defined as 9d84f560-bb67-4961-bd12-a4da780c67e4</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="5453c-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5453c-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5453c-133">**IVMVirtualMachineEvents**</span><span class="sxs-lookup"><span data-stu-id="5453c-133">**IVMVirtualMachineEvents**</span></span>](ivmvirtualmachineevents.md)
</dt> <dt>

[<span data-ttu-id="5453c-134">**VMLogoffType**</span><span class="sxs-lookup"><span data-stu-id="5453c-134">**VMLogoffType**</span></span>](vmlogofftype.md)
</dt> </dl>

 

