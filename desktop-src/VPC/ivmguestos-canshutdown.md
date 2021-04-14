---
title: Proprietà IVMGuestOS CanShutdown (VPCCOMInterfaces. h)
description: Indica se il sistema operativo guest può essere arrestato in modo corretto.
ms.assetid: 239cba43-9494-4efd-a4c8-0bb47f476b81
keywords:
- Proprietà CanShutdown Virtual PC
- Proprietà CanShutdown Virtual PC, interfaccia IVMGuestOS
- Interfaccia IVMGuestOS Virtual PC, proprietà CanShutdown
topic_type:
- apiref
api_name:
- IVMGuestOS.CanShutdown
- IVMGuestOS.get_CanShutdown
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f76e652b7a172da6f5a438f72b09443a13dcce2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341243"
---
# <a name="ivmguestoscanshutdown-property"></a><span data-ttu-id="1ce79-106">Proprietà IVMGuestOS:: CanShutdown</span><span class="sxs-lookup"><span data-stu-id="1ce79-106">IVMGuestOS::CanShutdown property</span></span>

<span data-ttu-id="1ce79-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="1ce79-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="1ce79-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="1ce79-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="1ce79-109">Indica se il sistema operativo guest può essere arrestato in modo corretto (richiede componenti di integrazione).</span><span class="sxs-lookup"><span data-stu-id="1ce79-109">Indicates whether the guest operating system can be cleanly shut down (requires Integration Components).</span></span>

<span data-ttu-id="1ce79-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="1ce79-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ce79-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1ce79-111">Syntax</span></span>


```C++
HRESULT get_CanShutdown(
  [out, retval] VARIANT_BOOL *canShutdown
);
```



## <a name="property-value"></a><span data-ttu-id="1ce79-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="1ce79-112">Property value</span></span>

<span data-ttu-id="1ce79-113">**Variante \_ TRUE** se il sistema operativo supporta l'operazione di arresto e la **variante \_ false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="1ce79-113">**VARIANT\_TRUE** if the operating system supports the shutdown operation and **VARIANT\_FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="1ce79-114">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="1ce79-114">Error codes</span></span>



| <span data-ttu-id="1ce79-115">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="1ce79-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="1ce79-116">Significato</span><span class="sxs-lookup"><span data-stu-id="1ce79-116">Meaning</span></span>                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="1ce79-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="1ce79-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="1ce79-118">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="1ce79-118">The operation was successful.</span></span><br/>           |
| <dl> <span data-ttu-id="1ce79-119"><dt>S \_ FALSE</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="1ce79-119"><dt>S\_FALSE</dt> <dt>1</dt></span></span> </dl>                    | <span data-ttu-id="1ce79-120">La macchina virtuale non è attivata.</span><span class="sxs-lookup"><span data-stu-id="1ce79-120">The virtual machine is not turned on.</span></span><br/>   |
| <dl> <span data-ttu-id="1ce79-121"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="1ce79-121"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="1ce79-122">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="1ce79-122">The parameter is **NULL**.</span></span><br/>              |
| <dl> <span data-ttu-id="1ce79-123"><dt>Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="1ce79-123"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="1ce79-124">Impossibile trovare la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="1ce79-124">The virtual machine could not be found.</span></span><br/> |
| <dl> <span data-ttu-id="1ce79-125"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="1ce79-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="1ce79-126">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="1ce79-126">An unexpected error has occurred.</span></span><br/>       |



## <a name="requirements"></a><span data-ttu-id="1ce79-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1ce79-127">Requirements</span></span>



| <span data-ttu-id="1ce79-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ce79-128">Requirement</span></span> | <span data-ttu-id="1ce79-129">Valore</span><span class="sxs-lookup"><span data-stu-id="1ce79-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ce79-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1ce79-130">Minimum supported client</span></span><br/> | <span data-ttu-id="1ce79-131">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="1ce79-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1ce79-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1ce79-132">Minimum supported server</span></span><br/> | <span data-ttu-id="1ce79-133">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="1ce79-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="1ce79-134">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="1ce79-134">End of client support</span></span><br/>    | <span data-ttu-id="1ce79-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1ce79-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="1ce79-136">Prodotto</span><span class="sxs-lookup"><span data-stu-id="1ce79-136">Product</span></span><br/>                  | <span data-ttu-id="1ce79-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="1ce79-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="1ce79-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1ce79-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="1ce79-139"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="1ce79-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="1ce79-140">IID</span><span class="sxs-lookup"><span data-stu-id="1ce79-140">IID</span></span><br/>                      | <span data-ttu-id="1ce79-141">IID \_ IVMGuestOS è definito come 99fea0db-4880-499a-B6D8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="1ce79-141">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="1ce79-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1ce79-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ce79-143">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="1ce79-143">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

