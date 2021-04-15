---
title: Proprietà ComputerName di IVMGuestOS (VPCCOMInterfaces. h)
description: Nome del computer del sistema operativo guest in esecuzione nella macchina virtuale.
ms.assetid: b35fa1a1-e105-43e6-9a2f-a5c7e71772cf
keywords:
- ComputerName proprietà PC virtuale
- Proprietà ComputerName Virtual PC, interfaccia IVMGuestOS
- Interfaccia IVMGuestOS Virtual PC, proprietà ComputerName
topic_type:
- apiref
api_name:
- IVMGuestOS.ComputerName
- IVMGuestOS.get_ComputerName
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75b266c238809284b340095dd25390d6e5f3d2b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479006"
---
# <a name="ivmguestoscomputername-property"></a><span data-ttu-id="84a84-106">Proprietà IVMGuestOS:: ComputerName</span><span class="sxs-lookup"><span data-stu-id="84a84-106">IVMGuestOS::ComputerName property</span></span>

<span data-ttu-id="84a84-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="84a84-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="84a84-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="84a84-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="84a84-109">Recupera il nome computer del sistema operativo guest in esecuzione nella macchina virtuale (VM).</span><span class="sxs-lookup"><span data-stu-id="84a84-109">Retrieves the computer name of the guest operating system running in the virtual machine (VM).</span></span>

<span data-ttu-id="84a84-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="84a84-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="84a84-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="84a84-111">Syntax</span></span>


```C++
HRESULT get_ComputerName(
  [out, retval] BSTR *guestComputerName
);
```



## <a name="property-value"></a><span data-ttu-id="84a84-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="84a84-112">Property value</span></span>

<span data-ttu-id="84a84-113">Nome del computer del sistema operativo guest.</span><span class="sxs-lookup"><span data-stu-id="84a84-113">The computer name of the guest operating system.</span></span>

## <a name="error-codes"></a><span data-ttu-id="84a84-114">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="84a84-114">Error codes</span></span>



| <span data-ttu-id="84a84-115">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="84a84-115">Name/value</span></span>                                                                                                                                                                       | <span data-ttu-id="84a84-116">Significato</span><span class="sxs-lookup"><span data-stu-id="84a84-116">Meaning</span></span>                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="84a84-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="84a84-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="84a84-118">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="84a84-118">The operation was successful.</span></span><br/>                        |
| <dl> <span data-ttu-id="84a84-119"><dt>E \_ </dt> <dt>0x80000003</dt> INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="84a84-119"><dt>E\_INVALIDARG</dt> <dt>0x80000003</dt></span></span> </dl>                         | <span data-ttu-id="84a84-120">Il parametro non è valido o non è specificato.</span><span class="sxs-lookup"><span data-stu-id="84a84-120">The parameter is not valid or not specified.</span></span><br/>         |
| <dl> <span data-ttu-id="84a84-121"><dt>Macchina virtuale \_ \_VM E \_ non \_ in esecuzione</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="84a84-121"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="84a84-122">La macchina virtuale non è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="84a84-122">The VM is not running.</span></span><br/>                               |
| <dl> <span data-ttu-id="84a84-123"><dt>Macchina virtuale \_ E \_ funzionalità aggiuntive \_ \_ non \_ disponibili</dt> <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="84a84-123"><dt>VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="84a84-124">I componenti di integrazione non sono installati in questa macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="84a84-124">Integration components are not installed in this VM.</span></span><br/> |
| <dl> <span data-ttu-id="84a84-125"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="84a84-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="84a84-126">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="84a84-126">An unexpected error has occurred.</span></span><br/>                    |



## <a name="requirements"></a><span data-ttu-id="84a84-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="84a84-127">Requirements</span></span>



| <span data-ttu-id="84a84-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="84a84-128">Requirement</span></span> | <span data-ttu-id="84a84-129">Valore</span><span class="sxs-lookup"><span data-stu-id="84a84-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="84a84-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="84a84-130">Minimum supported client</span></span><br/> | <span data-ttu-id="84a84-131">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="84a84-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="84a84-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="84a84-132">Minimum supported server</span></span><br/> | <span data-ttu-id="84a84-133">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="84a84-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="84a84-134">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="84a84-134">End of client support</span></span><br/>    | <span data-ttu-id="84a84-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="84a84-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="84a84-136">Prodotto</span><span class="sxs-lookup"><span data-stu-id="84a84-136">Product</span></span><br/>                  | <span data-ttu-id="84a84-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="84a84-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="84a84-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="84a84-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="84a84-139"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="84a84-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="84a84-140">IID</span><span class="sxs-lookup"><span data-stu-id="84a84-140">IID</span></span><br/>                      | <span data-ttu-id="84a84-141">IID \_ IVMGuestOS è definito come 99fea0db-4880-499a-B6D8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="84a84-141">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="84a84-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="84a84-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84a84-143">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="84a84-143">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

