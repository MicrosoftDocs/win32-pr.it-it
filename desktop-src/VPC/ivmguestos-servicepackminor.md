---
title: Proprietà IVMGuestOS ServicePackMinor (VPCCOMInterfaces. h)
description: La versione secondaria della Service Pack del sistema operativo guest in esecuzione nella macchina virtuale.
ms.assetid: f1413b5a-6a74-42a6-9671-b00b7c8912fa
keywords:
- Proprietà ServicePackMinor Virtual PC
- Proprietà ServicePackMinor Virtual PC, interfaccia IVMGuestOS
- Interfaccia IVMGuestOS Virtual PC, proprietà ServicePackMinor
topic_type:
- apiref
api_name:
- IVMGuestOS.ServicePackMinor
- IVMGuestOS.get_ServicePackMinor
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22e7a94c5ed8de42cc2455160424246e899014cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477194"
---
# <a name="ivmguestosservicepackminor-property"></a><span data-ttu-id="4b27e-106">Proprietà IVMGuestOS:: ServicePackMinor</span><span class="sxs-lookup"><span data-stu-id="4b27e-106">IVMGuestOS::ServicePackMinor property</span></span>

<span data-ttu-id="4b27e-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="4b27e-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="4b27e-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="4b27e-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="4b27e-109">La versione secondaria della Service Pack del sistema operativo guest in esecuzione nella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="4b27e-109">The minor version of the service pack of the guest operating system running in the virtual machine.</span></span>

<span data-ttu-id="4b27e-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="4b27e-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b27e-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4b27e-111">Syntax</span></span>


```C++
HRESULT get_ServicePackMinor(
  [out, retval] BSTR *servicePackMinor
);
```



## <a name="property-value"></a><span data-ttu-id="4b27e-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="4b27e-112">Property value</span></span>

<span data-ttu-id="4b27e-113">Il numero di versione secondario del Service Pack più recente installato.</span><span class="sxs-lookup"><span data-stu-id="4b27e-113">The minor version number of the latest Service Pack installed.</span></span>

## <a name="error-codes"></a><span data-ttu-id="4b27e-114">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="4b27e-114">Error codes</span></span>



| <span data-ttu-id="4b27e-115">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="4b27e-115">Name/value</span></span>                                                                                                                                                                       | <span data-ttu-id="4b27e-116">Significato</span><span class="sxs-lookup"><span data-stu-id="4b27e-116">Meaning</span></span>                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="4b27e-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="4b27e-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="4b27e-118">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="4b27e-118">The operation was successful.</span></span><br/>                        |
| <dl> <span data-ttu-id="4b27e-119"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="4b27e-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                            | <span data-ttu-id="4b27e-120">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="4b27e-120">The parameter is **NULL**.</span></span><br/>                           |
| <dl> <span data-ttu-id="4b27e-121"><dt>Macchina virtuale \_ \_VM E \_ non \_ in esecuzione</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="4b27e-121"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="4b27e-122">La macchina virtuale non è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="4b27e-122">The VM is not running.</span></span><br/>                               |
| <dl> <span data-ttu-id="4b27e-123"><dt>Macchina virtuale \_ E \_ funzionalità aggiuntive \_ \_ non \_ disponibili</dt> <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="4b27e-123"><dt>VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="4b27e-124">I componenti di integrazione non sono installati in questa macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="4b27e-124">Integration components are not installed in this VM.</span></span><br/> |
| <dl> <span data-ttu-id="4b27e-125"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="4b27e-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="4b27e-126">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="4b27e-126">An unexpected error has occurred.</span></span><br/>                    |



## <a name="requirements"></a><span data-ttu-id="4b27e-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4b27e-127">Requirements</span></span>



| <span data-ttu-id="4b27e-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="4b27e-128">Requirement</span></span> | <span data-ttu-id="4b27e-129">Valore</span><span class="sxs-lookup"><span data-stu-id="4b27e-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b27e-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4b27e-130">Minimum supported client</span></span><br/> | <span data-ttu-id="4b27e-131">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="4b27e-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4b27e-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4b27e-132">Minimum supported server</span></span><br/> | <span data-ttu-id="4b27e-133">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="4b27e-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="4b27e-134">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="4b27e-134">End of client support</span></span><br/>    | <span data-ttu-id="4b27e-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="4b27e-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="4b27e-136">Prodotto</span><span class="sxs-lookup"><span data-stu-id="4b27e-136">Product</span></span><br/>                  | <span data-ttu-id="4b27e-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="4b27e-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="4b27e-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4b27e-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="4b27e-139"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="4b27e-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="4b27e-140">IID</span><span class="sxs-lookup"><span data-stu-id="4b27e-140">IID</span></span><br/>                      | <span data-ttu-id="4b27e-141">IID \_ IVMGuestOS è definito come 99fea0db-4880-499a-B6D8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="4b27e-141">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="4b27e-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4b27e-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b27e-143">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="4b27e-143">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

