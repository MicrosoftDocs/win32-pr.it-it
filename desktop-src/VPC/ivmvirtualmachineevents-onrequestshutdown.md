---
title: Metodo IVMVirtualMachineEvents OnRequestShutdown (VPCCOMInterfaces. h)
description: Riceve la notifica che è stata effettuata una richiesta di arresto.
ms.assetid: e04131fd-5ca7-4392-9725-ba62b905324a
keywords:
- Metodo OnRequestShutdown Virtual PC
- Metodo OnRequestShutdown Virtual PC, interfaccia IVMVirtualMachineEvents
- Interfaccia IVMVirtualMachineEvents Virtual PC, metodo OnRequestShutdown
topic_type:
- apiref
api_name:
- IVMVirtualMachineEvents.OnRequestShutdown
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94dce60a7dfdb5ed5dce714e8b8eafcbd9558b95
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477404"
---
# <a name="ivmvirtualmachineeventsonrequestshutdown-method"></a><span data-ttu-id="17e4f-106">Metodo IVMVirtualMachineEvents:: OnRequestShutdown</span><span class="sxs-lookup"><span data-stu-id="17e4f-106">IVMVirtualMachineEvents::OnRequestShutdown method</span></span>

<span data-ttu-id="17e4f-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="17e4f-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="17e4f-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="17e4f-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="17e4f-109">Riceve la notifica che è stata effettuata una richiesta di arresto.</span><span class="sxs-lookup"><span data-stu-id="17e4f-109">Receives notification that a shutdown request has been made.</span></span>

## <a name="syntax"></a><span data-ttu-id="17e4f-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="17e4f-110">Syntax</span></span>


```C++
HRESULT OnRequestShutdown();
```



## <a name="parameters"></a><span data-ttu-id="17e4f-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="17e4f-111">Parameters</span></span>

<span data-ttu-id="17e4f-112">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="17e4f-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="17e4f-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="17e4f-113">Return value</span></span>

<span data-ttu-id="17e4f-114">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="17e4f-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="17e4f-115">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="17e4f-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="17e4f-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="17e4f-116">Remarks</span></span>

<span data-ttu-id="17e4f-117">Questo metodo viene chiamato ogni volta che la sessione della macchina virtuale sta per essere arrestata.</span><span class="sxs-lookup"><span data-stu-id="17e4f-117">This method is called whenever the virtual machine session is about to shut down.</span></span> <span data-ttu-id="17e4f-118">Il programma client deve implementare questo metodo di interfaccia per ricevere una notifica dell'evento **vmVirtualMachineEvent \_ RequestShutdown** originato da [**IVMVirtualMachine**](ivmvirtualmachine.md).</span><span class="sxs-lookup"><span data-stu-id="17e4f-118">The client program must implement this interface method to receive notification of the **vmVirtualMachineEvent\_RequestShutdown** event originating from [**IVMVirtualMachine**](ivmvirtualmachine.md).</span></span>

<span data-ttu-id="17e4f-119">Questa notifica degli eventi viene inviata solo quando la sessione delle macchine virtuali sta per essere arrestata.</span><span class="sxs-lookup"><span data-stu-id="17e4f-119">This event notification is sent only when the virtual machines session is about to shut down.</span></span> <span data-ttu-id="17e4f-120">Le routine di arresto del sistema operativo, ad esempio [**IVMGuestOS:: Shutdown**](ivmguestos-shutdown.md), non generano direttamente questo evento, a meno che non tenti anche di eseguire un'alimentazione software dell'hardware virtuale.</span><span class="sxs-lookup"><span data-stu-id="17e4f-120">Operating system shutdown routines, such as [**IVMGuestOS::Shutdown**](ivmguestos-shutdown.md), do not fire this event directly unless they also attempt to perform a software power off of the virtual hardware.</span></span>

## <a name="requirements"></a><span data-ttu-id="17e4f-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="17e4f-121">Requirements</span></span>



| <span data-ttu-id="17e4f-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="17e4f-122">Requirement</span></span> | <span data-ttu-id="17e4f-123">Valore</span><span class="sxs-lookup"><span data-stu-id="17e4f-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="17e4f-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="17e4f-124">Minimum supported client</span></span><br/> | <span data-ttu-id="17e4f-125">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="17e4f-125">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="17e4f-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="17e4f-126">Minimum supported server</span></span><br/> | <span data-ttu-id="17e4f-127">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="17e4f-127">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="17e4f-128">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="17e4f-128">End of client support</span></span><br/>    | <span data-ttu-id="17e4f-129">Windows 7</span><span class="sxs-lookup"><span data-stu-id="17e4f-129">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="17e4f-130">Prodotto</span><span class="sxs-lookup"><span data-stu-id="17e4f-130">Product</span></span><br/>                  | <span data-ttu-id="17e4f-131">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="17e4f-131">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="17e4f-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="17e4f-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="17e4f-133"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="17e4f-133"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="17e4f-134">IID</span><span class="sxs-lookup"><span data-stu-id="17e4f-134">IID</span></span><br/>                      | <span data-ttu-id="17e4f-135">DIID \_ IVMVirtualMachineEvents è definito come 9d84f560-BB67-4961-BD12-a4da780c67e4</span><span class="sxs-lookup"><span data-stu-id="17e4f-135">DIID\_IVMVirtualMachineEvents is defined as 9d84f560-bb67-4961-bd12-a4da780c67e4</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="17e4f-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="17e4f-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17e4f-137">**IVMVirtualMachineEvents**</span><span class="sxs-lookup"><span data-stu-id="17e4f-137">**IVMVirtualMachineEvents**</span></span>](ivmvirtualmachineevents.md)
</dt> </dl>

 

