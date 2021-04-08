---
title: Proprietà IVMVirtualMachine RdpPipeName (VPCCOMInterfaces. h)
description: Recupera il nome della connessione RDP named pipe usato per video e input.
ms.assetid: 0c2d0f23-40cd-4a86-96dd-546fb3570871
keywords:
- Proprietà RdpPipeName Virtual PC
- Proprietà RdpPipeName Virtual PC, interfaccia IVMVirtualMachine
- Interfaccia IVMVirtualMachine Virtual PC, proprietà RdpPipeName
topic_type:
- apiref
api_name:
- IVMVirtualMachine.RdpPipeName
- IVMVirtualMachine.get_RdpPipeName
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86e49463c5e443a07d1fa86736047435eaf60a06
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047799"
---
# <a name="ivmvirtualmachinerdppipename-property"></a><span data-ttu-id="4cb1e-106">Proprietà IVMVirtualMachine:: RdpPipeName</span><span class="sxs-lookup"><span data-stu-id="4cb1e-106">IVMVirtualMachine::RdpPipeName property</span></span>

<span data-ttu-id="4cb1e-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="4cb1e-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="4cb1e-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="4cb1e-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="4cb1e-109">Recupera il nome della connessione RDP named pipe usato per video e input.</span><span class="sxs-lookup"><span data-stu-id="4cb1e-109">Retrieves the name of the RDP connection named pipe used for video and input.</span></span>

<span data-ttu-id="4cb1e-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="4cb1e-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="4cb1e-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4cb1e-111">Syntax</span></span>


```C++
HRESULT get_RdpPipeName(
  [out, retval] BSTR *RdpPipeName
);
```



## <a name="property-value"></a><span data-ttu-id="4cb1e-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="4cb1e-112">Property value</span></span>

<span data-ttu-id="4cb1e-113">Nome della connessione RDP named pipe usato per video e input.</span><span class="sxs-lookup"><span data-stu-id="4cb1e-113">Name of the RDP connection named pipe used for video and input.</span></span>

## <a name="error-codes"></a><span data-ttu-id="4cb1e-114">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="4cb1e-114">Error codes</span></span>

<span data-ttu-id="4cb1e-115">Se il metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="4cb1e-115">If the method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4cb1e-116">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4cb1e-116">Otherwise, it returns an **HRESULT** error code.</span></span>



| <span data-ttu-id="4cb1e-117">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="4cb1e-117">Name/value</span></span>                                                                                                                                                         | <span data-ttu-id="4cb1e-118">Significato</span><span class="sxs-lookup"><span data-stu-id="4cb1e-118">Meaning</span></span>                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <span data-ttu-id="4cb1e-119"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="4cb1e-119"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                            | <span data-ttu-id="4cb1e-120">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="4cb1e-120">The operation was successful.</span></span><br/>          |
| <dl> <span data-ttu-id="4cb1e-121"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="4cb1e-121"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>              | <span data-ttu-id="4cb1e-122">Il parametro RdpPipeName è **null**.</span><span class="sxs-lookup"><span data-stu-id="4cb1e-122">The RdpPipeName parameter is **NULL**.</span></span><br/> |
| <dl> <span data-ttu-id="4cb1e-123"><dt>Macchina virtuale \_ \_VM E \_ non \_ in esecuzione</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="4cb1e-123"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl> | <span data-ttu-id="4cb1e-124">La macchina virtuale non è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="4cb1e-124">The virtual machine is not running.</span></span><br/>    |
| <dl> <span data-ttu-id="4cb1e-125"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="4cb1e-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>      | <span data-ttu-id="4cb1e-126">Si è verificato un errore sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="4cb1e-126">An unknown error occurred.</span></span><br/>             |



## <a name="requirements"></a><span data-ttu-id="4cb1e-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4cb1e-127">Requirements</span></span>



| <span data-ttu-id="4cb1e-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="4cb1e-128">Requirement</span></span> | <span data-ttu-id="4cb1e-129">Valore</span><span class="sxs-lookup"><span data-stu-id="4cb1e-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="4cb1e-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4cb1e-130">Minimum supported client</span></span><br/> | <span data-ttu-id="4cb1e-131">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="4cb1e-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4cb1e-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4cb1e-132">Minimum supported server</span></span><br/> | <span data-ttu-id="4cb1e-133">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="4cb1e-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="4cb1e-134">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="4cb1e-134">End of client support</span></span><br/>    | <span data-ttu-id="4cb1e-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="4cb1e-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="4cb1e-136">Prodotto</span><span class="sxs-lookup"><span data-stu-id="4cb1e-136">Product</span></span><br/>                  | <span data-ttu-id="4cb1e-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="4cb1e-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="4cb1e-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4cb1e-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="4cb1e-139"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="4cb1e-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="4cb1e-140">IID</span><span class="sxs-lookup"><span data-stu-id="4cb1e-140">IID</span></span><br/>                      | <span data-ttu-id="4cb1e-141">IID \_ IVMVirtualMachine è definito come f7092aa1-33ed-4F78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="4cb1e-141">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="4cb1e-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4cb1e-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4cb1e-143">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="4cb1e-143">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

