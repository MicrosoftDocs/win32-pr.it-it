---
title: Proprietà IVMGuestOS OSName (VPCCOMInterfaces. h)
description: Nome del sistema operativo guest in esecuzione nella macchina virtuale.
ms.assetid: 6381fc15-a6ab-429b-809d-7f89e7ec666d
keywords:
- Proprietà OSName Virtual PC
- Proprietà OSName Virtual PC, interfaccia IVMGuestOS
- Interfaccia IVMGuestOS Virtual PC, proprietà OSName
topic_type:
- apiref
api_name:
- IVMGuestOS.OSName
- IVMGuestOS.get_OSName
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 672c7b2c852bcbb1ec39b61889b03738e3a2df23
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476553"
---
# <a name="ivmguestososname-property"></a><span data-ttu-id="54b94-106">Proprietà IVMGuestOS:: OSName</span><span class="sxs-lookup"><span data-stu-id="54b94-106">IVMGuestOS::OSName property</span></span>

<span data-ttu-id="54b94-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="54b94-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="54b94-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="54b94-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="54b94-109">Recupera il nome del sistema operativo guest in esecuzione nella macchina virtuale (VM).</span><span class="sxs-lookup"><span data-stu-id="54b94-109">Retrieves the name of the guest operating system running in the virtual machine (VM).</span></span>

<span data-ttu-id="54b94-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="54b94-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="54b94-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="54b94-111">Syntax</span></span>


```C++
HRESULT get_OSName(
  [out, retval] BSTR *guestOSName
);
```



## <a name="property-value"></a><span data-ttu-id="54b94-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="54b94-112">Property value</span></span>

<span data-ttu-id="54b94-113">Nome completo (incluso il nome del gruppo) del sistema operativo guest.</span><span class="sxs-lookup"><span data-stu-id="54b94-113">The full name (including suite name) of the guest operating system.</span></span>

## <a name="error-codes"></a><span data-ttu-id="54b94-114">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="54b94-114">Error codes</span></span>



| <span data-ttu-id="54b94-115">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="54b94-115">Name/value</span></span>                                                                                                                                                                       | <span data-ttu-id="54b94-116">Significato</span><span class="sxs-lookup"><span data-stu-id="54b94-116">Meaning</span></span>                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="54b94-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="54b94-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="54b94-118">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="54b94-118">The operation was successful.</span></span><br/>                        |
| <dl> <span data-ttu-id="54b94-119"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="54b94-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                            | <span data-ttu-id="54b94-120">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="54b94-120">The parameter is **NULL**.</span></span><br/>                           |
| <dl> <span data-ttu-id="54b94-121"><dt>Macchina virtuale \_ \_VM E \_ non \_ in esecuzione</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="54b94-121"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="54b94-122">La macchina virtuale non è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="54b94-122">The VM is not running.</span></span><br/>                               |
| <dl> <span data-ttu-id="54b94-123"><dt>Macchina virtuale \_ E \_ funzionalità aggiuntive \_ \_ non \_ disponibili</dt> <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="54b94-123"><dt>VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="54b94-124">I componenti di integrazione non sono installati in questa macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="54b94-124">Integration components are not installed in this VM.</span></span><br/> |
| <dl> <span data-ttu-id="54b94-125"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="54b94-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="54b94-126">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="54b94-126">An unexpected error has occurred.</span></span><br/>                    |



## <a name="remarks"></a><span data-ttu-id="54b94-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="54b94-127">Remarks</span></span>

<span data-ttu-id="54b94-128">Quando viene richiamato questo metodo, la macchina virtuale deve essere in esecuzione (ovvero completamente avviata e non arrestata) e installare i componenti di integrazione.</span><span class="sxs-lookup"><span data-stu-id="54b94-128">The VM must be running (that is, fully booted and not shutting down) and integration components must be installed when this method is invoked.</span></span>

## <a name="requirements"></a><span data-ttu-id="54b94-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="54b94-129">Requirements</span></span>



| <span data-ttu-id="54b94-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="54b94-130">Requirement</span></span> | <span data-ttu-id="54b94-131">Valore</span><span class="sxs-lookup"><span data-stu-id="54b94-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="54b94-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="54b94-132">Minimum supported client</span></span><br/> | <span data-ttu-id="54b94-133">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="54b94-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="54b94-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="54b94-134">Minimum supported server</span></span><br/> | <span data-ttu-id="54b94-135">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="54b94-135">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="54b94-136">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="54b94-136">End of client support</span></span><br/>    | <span data-ttu-id="54b94-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="54b94-137">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="54b94-138">Prodotto</span><span class="sxs-lookup"><span data-stu-id="54b94-138">Product</span></span><br/>                  | <span data-ttu-id="54b94-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="54b94-139">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="54b94-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="54b94-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="54b94-141"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="54b94-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="54b94-142">IID</span><span class="sxs-lookup"><span data-stu-id="54b94-142">IID</span></span><br/>                      | <span data-ttu-id="54b94-143">IID \_ IVMGuestOS è definito come 99fea0db-4880-499a-B6D8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="54b94-143">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="54b94-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="54b94-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54b94-145">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="54b94-145">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

