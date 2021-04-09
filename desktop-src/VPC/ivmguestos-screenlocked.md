---
title: Proprietà IVMGuestOS ScreenLocked (VPCCOMInterfaces. h)
description: Indica se lo schermo del sistema operativo guest è bloccato.
ms.assetid: 5ce2e0ad-b98c-4aa7-99b5-0fc85026a121
keywords:
- Proprietà ScreenLocked Virtual PC
- Proprietà ScreenLocked Virtual PC, interfaccia IVMGuestOS
- Interfaccia IVMGuestOS Virtual PC, proprietà ScreenLocked
topic_type:
- apiref
api_name:
- IVMGuestOS.ScreenLocked
- IVMGuestOS.get_ScreenLocked
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa1f14bf0a61f06e9f36b44d02881cf7edc1f793
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048464"
---
# <a name="ivmguestosscreenlocked-property"></a><span data-ttu-id="9cc2a-106">Proprietà IVMGuestOS:: ScreenLocked</span><span class="sxs-lookup"><span data-stu-id="9cc2a-106">IVMGuestOS::ScreenLocked property</span></span>

<span data-ttu-id="9cc2a-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="9cc2a-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="9cc2a-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="9cc2a-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="9cc2a-109">Indica se lo schermo del sistema operativo guest è bloccato.</span><span class="sxs-lookup"><span data-stu-id="9cc2a-109">Indicates whether the screen in the guest operating system is locked.</span></span>

<span data-ttu-id="9cc2a-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="9cc2a-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="9cc2a-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9cc2a-111">Syntax</span></span>


```C++
HRESULT get_ScreenLocked(
  [out, retval] VARIANT_BOOL *guestScreenLocked
);
```



## <a name="property-value"></a><span data-ttu-id="9cc2a-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="9cc2a-112">Property value</span></span>

<span data-ttu-id="9cc2a-113">**Variante \_ TRUE** se la schermata è bloccata nel sistema operativo guest, **Variant \_ false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="9cc2a-113">**VARIANT\_TRUE** if screen is locked in guest operating system, **VARIANT\_FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="9cc2a-114">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="9cc2a-114">Error codes</span></span>



| <span data-ttu-id="9cc2a-115">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="9cc2a-115">Name/value</span></span>                                                                                                                                                                       | <span data-ttu-id="9cc2a-116">Significato</span><span class="sxs-lookup"><span data-stu-id="9cc2a-116">Meaning</span></span>                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9cc2a-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="9cc2a-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="9cc2a-118">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="9cc2a-118">The operation was successful.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="9cc2a-119"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="9cc2a-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                            | <span data-ttu-id="9cc2a-120">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="9cc2a-120">The parameter is **NULL**.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="9cc2a-121"><dt>Macchina virtuale \_ \_VM E \_ non \_ in esecuzione</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="9cc2a-121"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="9cc2a-122">Per questa operazione è necessario che la macchina virtuale (VM) sia in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="9cc2a-122">The virtual machine (VM) must be running for this operation.</span></span><br/>                     |
| <dl> <span data-ttu-id="9cc2a-123"><dt>Macchina virtuale \_ E \_ funzionalità aggiuntive \_ \_ non \_ disponibili</dt> <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="9cc2a-123"><dt>VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="9cc2a-124">La funzionalità componenti di integrazione non è abilitata nel sistema operativo guest.</span><span class="sxs-lookup"><span data-stu-id="9cc2a-124">The integration components feature is not enabled in the guest operating system.</span></span><br/> |
| <dl> <span data-ttu-id="9cc2a-125"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="9cc2a-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="9cc2a-126">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="9cc2a-126">An unexpected error has occurred.</span></span><br/>                                                |



## <a name="requirements"></a><span data-ttu-id="9cc2a-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9cc2a-127">Requirements</span></span>



| <span data-ttu-id="9cc2a-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="9cc2a-128">Requirement</span></span> | <span data-ttu-id="9cc2a-129">Valore</span><span class="sxs-lookup"><span data-stu-id="9cc2a-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="9cc2a-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9cc2a-130">Minimum supported client</span></span><br/> | <span data-ttu-id="9cc2a-131">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="9cc2a-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9cc2a-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9cc2a-132">Minimum supported server</span></span><br/> | <span data-ttu-id="9cc2a-133">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="9cc2a-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="9cc2a-134">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="9cc2a-134">End of client support</span></span><br/>    | <span data-ttu-id="9cc2a-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="9cc2a-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="9cc2a-136">Prodotto</span><span class="sxs-lookup"><span data-stu-id="9cc2a-136">Product</span></span><br/>                  | <span data-ttu-id="9cc2a-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="9cc2a-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="9cc2a-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9cc2a-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="9cc2a-139"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="9cc2a-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="9cc2a-140">IID</span><span class="sxs-lookup"><span data-stu-id="9cc2a-140">IID</span></span><br/>                      | <span data-ttu-id="9cc2a-141">IID \_ IVMGuestOS è definito come 99fea0db-4880-499a-B6D8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="9cc2a-141">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="9cc2a-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9cc2a-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9cc2a-143">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="9cc2a-143">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

