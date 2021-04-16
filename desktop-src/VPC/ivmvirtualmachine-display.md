---
title: Proprietà di visualizzazione IVMVirtualMachine (VPCCOMInterfaces. h)
description: Recupera la visualizzazione video per la macchina virtuale.
ms.assetid: ca5a433d-4613-4b6d-9de7-d9c6a2038e38
keywords:
- Visualizza proprietà PC virtuale
- Visualizza proprietà PC virtuale, interfaccia IVMVirtualMachine
- Interfaccia IVMVirtualMachine Virtual PC, proprietà di visualizzazione
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Display
- IVMVirtualMachine.get_Display
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 175150ba76074918d497efd2c9f65a53af46b8bb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477405"
---
# <a name="ivmvirtualmachinedisplay-property"></a><span data-ttu-id="7c5e6-106">IVMVirtualMachine::D proprietà di riproduzione</span><span class="sxs-lookup"><span data-stu-id="7c5e6-106">IVMVirtualMachine::Display property</span></span>

<span data-ttu-id="7c5e6-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="7c5e6-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="7c5e6-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="7c5e6-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="7c5e6-109">Recupera la visualizzazione video per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7c5e6-109">Retrieves the video display for the virtual machine.</span></span>

<span data-ttu-id="7c5e6-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="7c5e6-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c5e6-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7c5e6-111">Syntax</span></span>


```C++
HRESULT get_Display(
  [out, retval] IVMDisplay **display
);
```



## <a name="property-value"></a><span data-ttu-id="7c5e6-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="7c5e6-112">Property value</span></span>

<span data-ttu-id="7c5e6-113">Oggetto [**IVMDisplay**](ivmdisplay.md) .</span><span class="sxs-lookup"><span data-stu-id="7c5e6-113">The [**IVMDisplay**](ivmdisplay.md) object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="7c5e6-114">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="7c5e6-114">Error codes</span></span>



| <span data-ttu-id="7c5e6-115">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="7c5e6-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="7c5e6-116">Significato</span><span class="sxs-lookup"><span data-stu-id="7c5e6-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="7c5e6-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="7c5e6-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="7c5e6-118">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="7c5e6-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="7c5e6-119"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="7c5e6-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="7c5e6-120">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="7c5e6-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="7c5e6-121"><dt>Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="7c5e6-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="7c5e6-122">La configurazione è sconosciuta.</span><span class="sxs-lookup"><span data-stu-id="7c5e6-122">The configuration is unknown.</span></span><br/>     |
| <dl> <span data-ttu-id="7c5e6-123"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="7c5e6-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="7c5e6-124">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="7c5e6-124">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="7c5e6-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7c5e6-125">Requirements</span></span>



| <span data-ttu-id="7c5e6-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c5e6-126">Requirement</span></span> | <span data-ttu-id="7c5e6-127">Valore</span><span class="sxs-lookup"><span data-stu-id="7c5e6-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c5e6-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7c5e6-128">Minimum supported client</span></span><br/> | <span data-ttu-id="7c5e6-129">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="7c5e6-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7c5e6-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7c5e6-130">Minimum supported server</span></span><br/> | <span data-ttu-id="7c5e6-131">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="7c5e6-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="7c5e6-132">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="7c5e6-132">End of client support</span></span><br/>    | <span data-ttu-id="7c5e6-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="7c5e6-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="7c5e6-134">Prodotto</span><span class="sxs-lookup"><span data-stu-id="7c5e6-134">Product</span></span><br/>                  | <span data-ttu-id="7c5e6-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="7c5e6-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="7c5e6-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7c5e6-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c5e6-137"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c5e6-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="7c5e6-138">IID</span><span class="sxs-lookup"><span data-stu-id="7c5e6-138">IID</span></span><br/>                      | <span data-ttu-id="7c5e6-139">IID \_ IVMVirtualMachine è definito come f7092aa1-33ed-4F78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="7c5e6-139">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="7c5e6-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7c5e6-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c5e6-141">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="7c5e6-141">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

