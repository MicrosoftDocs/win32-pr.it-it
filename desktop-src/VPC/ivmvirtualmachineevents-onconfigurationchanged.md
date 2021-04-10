---
title: Metodo IVMVirtualMachineEvents OnConfigurationChanged (VPCCOMInterfaces. h)
description: Riceve la notifica che un valore nella configurazione per questa macchina virtuale è stato modificato.
ms.assetid: 1955f23e-b318-41aa-b82e-81283be81608
keywords:
- Metodo OnConfigurationChanged Virtual PC
- Metodo OnConfigurationChanged Virtual PC, interfaccia IVMVirtualMachineEvents
- Interfaccia IVMVirtualMachineEvents Virtual PC, metodo OnConfigurationChanged
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnConfigurationChanged
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10459562da2d87b8c883217e003cd822ef923fad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963721"
---
# <a name="ivmvirtualmachineeventsonconfigurationchanged-method"></a><span data-ttu-id="93668-106">Metodo IVMVirtualMachineEvents:: OnConfigurationChanged</span><span class="sxs-lookup"><span data-stu-id="93668-106">IVMVirtualMachineEvents::OnConfigurationChanged method</span></span>

<span data-ttu-id="93668-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="93668-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="93668-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="93668-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="93668-109">Riceve la notifica che un valore nella configurazione per questa macchina virtuale è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="93668-109">Receives notification that a value in the configuration for this virtual machine has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="93668-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="93668-110">Syntax</span></span>


```C++
HRESULT OnConfigurationChanged(
  [in] BSTR    configKey,
  [in] VARIANT configData
);
```



## <a name="parameters"></a><span data-ttu-id="93668-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="93668-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93668-112">*configKey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="93668-112">*configKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93668-113">Valore all'interno della configurazione che è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="93668-113">The value inside the configuration that has changed.</span></span>

</dd> <dt>

<span data-ttu-id="93668-114">*configData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="93668-114">*configData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93668-115">Nuovo valore per la configurazione.</span><span class="sxs-lookup"><span data-stu-id="93668-115">The new value for the configuration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93668-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="93668-116">Return value</span></span>

<span data-ttu-id="93668-117">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="93668-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="93668-118">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="93668-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="93668-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="93668-119">Remarks</span></span>

<span data-ttu-id="93668-120">Questo metodo viene chiamato quando viene modificata la configurazione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="93668-120">This method is called when the configuration changes for this virtual machine.</span></span> <span data-ttu-id="93668-121">Il programma client deve implementare questo metodo di interfaccia per ricevere una notifica dell' \_ evento vmVirtualMachineEvent ConfigurationChanged originato da [**IVMVirtualMachine**](ivmvirtualmachine.md).</span><span class="sxs-lookup"><span data-stu-id="93668-121">The client program must implement this interface method to receive notification of the vmVirtualMachineEvent\_ConfigurationChanged event originating from [**IVMVirtualMachine**](ivmvirtualmachine.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="93668-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="93668-122">Requirements</span></span>



| <span data-ttu-id="93668-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="93668-123">Requirement</span></span> | <span data-ttu-id="93668-124">Valore</span><span class="sxs-lookup"><span data-stu-id="93668-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="93668-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="93668-125">Minimum supported client</span></span><br/> | <span data-ttu-id="93668-126">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="93668-126">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="93668-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="93668-127">Minimum supported server</span></span><br/> | <span data-ttu-id="93668-128">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="93668-128">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="93668-129">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="93668-129">End of client support</span></span><br/>    | <span data-ttu-id="93668-130">Windows 7</span><span class="sxs-lookup"><span data-stu-id="93668-130">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="93668-131">Prodotto</span><span class="sxs-lookup"><span data-stu-id="93668-131">Product</span></span><br/>                  | <span data-ttu-id="93668-132">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="93668-132">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="93668-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="93668-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="93668-134"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="93668-134"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="93668-135">IID</span><span class="sxs-lookup"><span data-stu-id="93668-135">IID</span></span><br/>                      | <span data-ttu-id="93668-136">DIID \_ IVMVirtualMachineEvents è definito come 9d84f560-BB67-4961-BD12-a4da780c67e4</span><span class="sxs-lookup"><span data-stu-id="93668-136">DIID\_IVMVirtualMachineEvents is defined as 9d84f560-bb67-4961-bd12-a4da780c67e4</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="93668-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="93668-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93668-138">**IVMVirtualMachineEvents**</span><span class="sxs-lookup"><span data-stu-id="93668-138">**IVMVirtualMachineEvents**</span></span>](ivmvirtualmachineevents.md)
</dt> </dl>

 

