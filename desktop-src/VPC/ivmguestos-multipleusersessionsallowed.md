---
title: Proprietà MultipleUserSessionsAllowed di IVMGuestOS
description: Determina se nel sistema operativo guest sono consentite più sessioni utente simultanee.
ms.assetid: 8a4163bf-b805-4cf0-b785-ee82e8374ef6
keywords:
- Proprietà MultipleUserSessionsAllowed Virtual PC
- Proprietà MultipleUserSessionsAllowed Virtual PC, interfaccia IVMGuestOS
- Interfaccia IVMGuestOS Virtual PC, proprietà MultipleUserSessionsAllowed
topic_type:
- apiref
api_name:
- IVMGuestOS.MultipleUserSessionsAllowed
- IVMGuestOS.get_MultipleUserSessionsAllowed
api_location:
- IVMGuestOS.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f725a626ae13caaa36acd598694fef2f3b03e697
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119963"
---
# <a name="ivmguestosmultipleusersessionsallowed-property"></a><span data-ttu-id="d3ae0-106">Proprietà IVMGuestOS:: MultipleUserSessionsAllowed</span><span class="sxs-lookup"><span data-stu-id="d3ae0-106">IVMGuestOS::MultipleUserSessionsAllowed property</span></span>

<span data-ttu-id="d3ae0-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="d3ae0-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="d3ae0-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="d3ae0-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="d3ae0-109">Determina se nel sistema operativo guest sono consentite più sessioni utente simultanee.</span><span class="sxs-lookup"><span data-stu-id="d3ae0-109">Determines whether multiple simultaneous user sessions are allowed in the guest operating system.</span></span>

<span data-ttu-id="d3ae0-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="d3ae0-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3ae0-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d3ae0-111">Syntax</span></span>


```C++
HRESULT get_MultipleUserSessionsAllowed(
  [out, retval] VARIANT_BOOL *sessionStatus
);
```



## <a name="property-value"></a><span data-ttu-id="d3ae0-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="d3ae0-112">Property value</span></span>

<span data-ttu-id="d3ae0-113">**Variante \_ TRUE** se nel sistema operativo guest sono consentite più sessioni utente simultanee. in caso contrario, **Variant \_ false** .</span><span class="sxs-lookup"><span data-stu-id="d3ae0-113">**VARIANT\_TRUE** if multiple simultaneous user sessions are allowed in the guest operating system, **VARIANT\_FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d3ae0-114">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="d3ae0-114">Error codes</span></span>



| <span data-ttu-id="d3ae0-115">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="d3ae0-115">Name/value</span></span>                                                                                                                                                                       | <span data-ttu-id="d3ae0-116">Significato</span><span class="sxs-lookup"><span data-stu-id="d3ae0-116">Meaning</span></span>                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d3ae0-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="d3ae0-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="d3ae0-118">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="d3ae0-118">The operation was successful.</span></span><br/>                                                                                       |
| <dl> <span data-ttu-id="d3ae0-119"><dt>S \_ FALSE</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="d3ae0-119"><dt>S\_FALSE</dt> <dt>1</dt></span></span> </dl>                                       | <span data-ttu-id="d3ae0-120">Servizi Desktop remoto (precedentemente noto come servizi Terminal) non è ancora inizializzato nel sistema operativo guest.</span><span class="sxs-lookup"><span data-stu-id="d3ae0-120">Remote Desktop Services (formerly known as Terminal Services) is not yet initialized in the guest operating system.</span></span><br/> |
| <dl> <span data-ttu-id="d3ae0-121"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="d3ae0-121"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                            | <span data-ttu-id="d3ae0-122">Il parametro *sessionStatus* è **null**.</span><span class="sxs-lookup"><span data-stu-id="d3ae0-122">The *sessionStatus* parameter is **NULL**.</span></span><br/>                                                                          |
| <dl> <span data-ttu-id="d3ae0-123"><dt>Macchina virtuale \_ \_VM E \_ non \_ in esecuzione</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="d3ae0-123"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="d3ae0-124">La macchina virtuale non è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="d3ae0-124">The virtual machine is not running.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="d3ae0-125"><dt>Macchina virtuale \_ E \_ funzionalità aggiuntive \_ \_ non \_ disponibili</dt> <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="d3ae0-125"><dt>VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="d3ae0-126">I componenti di integrazione non sono installati in questa macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="d3ae0-126">Integration components are not installed in this virtual machine.</span></span><br/>                                                   |
| <dl> <span data-ttu-id="d3ae0-127"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="d3ae0-127"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="d3ae0-128">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="d3ae0-128">An unexpected error has occurred.</span></span><br/>                                                                                   |



## <a name="remarks"></a><span data-ttu-id="d3ae0-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="d3ae0-129">Remarks</span></span>

<span data-ttu-id="d3ae0-130">Il valore di questa proprietà non è valido a meno che la proprietà [**TerminalServicesInitialized**](ivmguestos-terminalservicesinitialized.md) non sia **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="d3ae0-130">The value of this property is not valid unless the [**TerminalServicesInitialized**](ivmguestos-terminalservicesinitialized.md) property is **VARIANT\_TRUE**.</span></span>

<span data-ttu-id="d3ae0-131">Per i sistemi operativi client Windows, **MultipleUserSessionsAllowed** è una **variante \_ true** se il cambio rapido utente è supportato.</span><span class="sxs-lookup"><span data-stu-id="d3ae0-131">For Windows client operating systems, **MultipleUserSessionsAllowed** is **VARIANT\_TRUE** if Fast User Switching is supported.</span></span> <span data-ttu-id="d3ae0-132">Per i sistemi operativi Windows Server, **MultipleUserSessionsAllowed** è una **variante \_ true** se Servizi Desktop remoto (denominato in precedenza Terminal Services) viene installata e abilitata.</span><span class="sxs-lookup"><span data-stu-id="d3ae0-132">For Windows Server operating systems, **MultipleUserSessionsAllowed** is **VARIANT\_TRUE** if Remote Desktop Services (formerly called Terminal Services) is installed and enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3ae0-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d3ae0-133">Requirements</span></span>



| <span data-ttu-id="d3ae0-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="d3ae0-134">Requirement</span></span> | <span data-ttu-id="d3ae0-135">Valore</span><span class="sxs-lookup"><span data-stu-id="d3ae0-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3ae0-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d3ae0-136">Minimum supported client</span></span><br/> | <span data-ttu-id="d3ae0-137">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="d3ae0-137">Windows 7 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="d3ae0-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d3ae0-138">Minimum supported server</span></span><br/> | <span data-ttu-id="d3ae0-139">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="d3ae0-139">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="d3ae0-140">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="d3ae0-140">End of client support</span></span><br/>    | <span data-ttu-id="d3ae0-141">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d3ae0-141">Windows 7</span></span><br/>                                                                      |
| <span data-ttu-id="d3ae0-142">IDL</span><span class="sxs-lookup"><span data-stu-id="d3ae0-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d3ae0-143"><dt>IVMGuestOS. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d3ae0-143"><dt>IVMGuestOS.idl</dt></span></span> </dl> |
| <span data-ttu-id="d3ae0-144">IID</span><span class="sxs-lookup"><span data-stu-id="d3ae0-144">IID</span></span><br/>                      | <span data-ttu-id="d3ae0-145">IID \_ IVMGuestOS è definito come 99fea0db-4880-499a-B6D8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="d3ae0-145">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="d3ae0-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d3ae0-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3ae0-147">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="d3ae0-147">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

