---
title: Metodo IVMVirtualPCEvents OnEventLogged (VPCCOMInterfaces. h)
description: Riceve la notifica che Windows Virtual PC registra un evento.
ms.assetid: 89439e8e-e9bf-409e-a129-525b9feb8fdd
keywords:
- Metodo OnEventLogged Virtual PC
- Metodo OnEventLogged Virtual PC, interfaccia IVMVirtualPCEvents
- Interfaccia IVMVirtualPCEvents Virtual PC, metodo OnEventLogged
topic_type:
- apiref
api_name:
- IVMVirtualPCEvents.OnEventLogged
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 196d480383f488c9c0885e95857c8d1a053d5887
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518004"
---
# <a name="ivmvirtualpceventsoneventlogged-method"></a><span data-ttu-id="76c8c-106">Metodo IVMVirtualPCEvents:: OnEventLogged</span><span class="sxs-lookup"><span data-stu-id="76c8c-106">IVMVirtualPCEvents::OnEventLogged method</span></span>

<span data-ttu-id="76c8c-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="76c8c-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="76c8c-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="76c8c-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="76c8c-109">Riceve la notifica che Windows Virtual PC registra un evento.</span><span class="sxs-lookup"><span data-stu-id="76c8c-109">Receives notification that Windows Virtual PC logs an event.</span></span>

## <a name="syntax"></a><span data-ttu-id="76c8c-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="76c8c-110">Syntax</span></span>


```C++
HRESULT OnEventLogged(
  [in] long logMessageID
);
```



## <a name="parameters"></a><span data-ttu-id="76c8c-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="76c8c-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76c8c-112">*logMessageID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="76c8c-112">*logMessageID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76c8c-113">Identificatore del messaggio del registro eventi registrato.</span><span class="sxs-lookup"><span data-stu-id="76c8c-113">The message identifier of the event log message that was logged.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76c8c-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="76c8c-114">Return value</span></span>

<span data-ttu-id="76c8c-115">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="76c8c-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="76c8c-116">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="76c8c-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="76c8c-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="76c8c-117">Remarks</span></span>

<span data-ttu-id="76c8c-118">Questo metodo viene chiamato quando Windows Virtual PC registra un messaggio nel registro eventi di Windows.</span><span class="sxs-lookup"><span data-stu-id="76c8c-118">This method is called when Windows Virtual PC logs a message to the Windows event log.</span></span> <span data-ttu-id="76c8c-119">Il programma client deve implementare questo metodo di interfaccia per ricevere una notifica dell'evento **vmVirtualPCEvent \_ EventLogged** originato da [**IVMVirtualPC**](ivmvirtualpc.md).</span><span class="sxs-lookup"><span data-stu-id="76c8c-119">The client program must implement this interface method to receive notification of the **vmVirtualPCEvent\_EventLogged** event originating from [**IVMVirtualPC**](ivmvirtualpc.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="76c8c-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="76c8c-120">Requirements</span></span>



| <span data-ttu-id="76c8c-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="76c8c-121">Requirement</span></span> | <span data-ttu-id="76c8c-122">Valore</span><span class="sxs-lookup"><span data-stu-id="76c8c-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="76c8c-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="76c8c-123">Minimum supported client</span></span><br/> | <span data-ttu-id="76c8c-124">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="76c8c-124">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="76c8c-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="76c8c-125">Minimum supported server</span></span><br/> | <span data-ttu-id="76c8c-126">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="76c8c-126">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="76c8c-127">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="76c8c-127">End of client support</span></span><br/>    | <span data-ttu-id="76c8c-128">Windows 7</span><span class="sxs-lookup"><span data-stu-id="76c8c-128">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="76c8c-129">Prodotto</span><span class="sxs-lookup"><span data-stu-id="76c8c-129">Product</span></span><br/>                  | <span data-ttu-id="76c8c-130">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="76c8c-130">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="76c8c-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="76c8c-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="76c8c-132"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="76c8c-132"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="76c8c-133">IID</span><span class="sxs-lookup"><span data-stu-id="76c8c-133">IID</span></span><br/>                      | <span data-ttu-id="76c8c-134">DIID \_ IVMVirtualPCEvents è definito come efed1ef1-3c09-41f7-a9c2-7e29fa286c9d</span><span class="sxs-lookup"><span data-stu-id="76c8c-134">DIID\_IVMVirtualPCEvents is defined as efed1ef1-3c09-41f7-a9c2-7e29fa286c9d</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="76c8c-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="76c8c-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76c8c-136">**IVMVirtualPCEvents**</span><span class="sxs-lookup"><span data-stu-id="76c8c-136">**IVMVirtualPCEvents**</span></span>](ivmvirtualpcevents.md)
</dt> </dl>

 

