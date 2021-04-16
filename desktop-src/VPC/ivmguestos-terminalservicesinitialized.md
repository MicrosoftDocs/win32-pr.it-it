---
title: Proprietà IVMGuestOS TerminalServicesInitialized (VPCCOMInterfaces. h)
description: Stato del Servizi Desktop remoto nel sistema operativo guest.
ms.assetid: 104d9256-6b2e-45ec-a290-21e0732c65ac
keywords:
- Proprietà TerminalServicesInitialized Virtual PC
- Proprietà TerminalServicesInitialized Virtual PC, interfaccia IVMGuestOS
- Interfaccia IVMGuestOS Virtual PC, proprietà TerminalServicesInitialized
topic_type:
- apiref
api_name:
- IVMGuestOS.TerminalServicesInitialized
- IVMGuestOS.get_TerminalServicesInitialized
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92ce23b4b07f3e2d06f605f4598c8b31e4c70692
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518916"
---
# <a name="ivmguestosterminalservicesinitialized-property"></a><span data-ttu-id="55330-106">Proprietà IVMGuestOS:: TerminalServicesInitialized</span><span class="sxs-lookup"><span data-stu-id="55330-106">IVMGuestOS::TerminalServicesInitialized property</span></span>

<span data-ttu-id="55330-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="55330-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="55330-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="55330-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="55330-109">Recupera lo stato di Servizi Desktop remoto (precedentemente noto come servizi Terminal) nel sistema operativo guest.</span><span class="sxs-lookup"><span data-stu-id="55330-109">Retrieves the status of Remote Desktop Services (formerly known as Terminal Services) in the guest operating system.</span></span>

<span data-ttu-id="55330-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="55330-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="55330-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="55330-111">Syntax</span></span>


```C++
HRESULT get_TerminalServicesInitialized(
  [out, retval] VARIANT_BOOL *termServStatus
);
```



## <a name="property-value"></a><span data-ttu-id="55330-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="55330-112">Property value</span></span>

<span data-ttu-id="55330-113">Stato di inizializzazione.</span><span class="sxs-lookup"><span data-stu-id="55330-113">The initialization status.</span></span>

## <a name="error-codes"></a><span data-ttu-id="55330-114">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="55330-114">Error codes</span></span>



| <span data-ttu-id="55330-115">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="55330-115">Name/value</span></span>                                                                                                                                                                       | <span data-ttu-id="55330-116">Significato</span><span class="sxs-lookup"><span data-stu-id="55330-116">Meaning</span></span>                                                                                                                                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="55330-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="55330-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="55330-118">L'operazione è stata completata e Servizi Desktop remoto è stata inizializzata.</span><span class="sxs-lookup"><span data-stu-id="55330-118">The operation was successful and Remote Desktop Services has been initialized.</span></span> <span data-ttu-id="55330-119">Il valore della proprietà restituito indica se Servizi Desktop remoto è disponibile nel sistema operativo guest.</span><span class="sxs-lookup"><span data-stu-id="55330-119">The returned property value indicates whether Remote Desktop Services is available in the guest operating system.</span></span><br/> |
| <dl> <span data-ttu-id="55330-120"><dt>S \_ FALSE</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="55330-120"><dt>S\_FALSE</dt> <dt>1</dt></span></span> </dl>                                       | <span data-ttu-id="55330-121">La funzionalità componenti di integrazione è in esecuzione, ma Servizi Desktop remoto non è ancora stata inizializzata.</span><span class="sxs-lookup"><span data-stu-id="55330-121">The integration components feature is running, but Remote Desktop Services is not yet initialized.</span></span><br/>                                                                                               |
| <dl> <span data-ttu-id="55330-122"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="55330-122"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                            | <span data-ttu-id="55330-123">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="55330-123">The parameter is **NULL**.</span></span><br/>                                                                                                                                                                       |
| <dl> <span data-ttu-id="55330-124"><dt>Macchina virtuale \_ \_VM E \_ non \_ in esecuzione</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="55330-124"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="55330-125">Per questa operazione è necessario che la macchina virtuale (VM) sia in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="55330-125">The virtual machine (VM) must be running for this operation.</span></span><br/>                                                                                                                                     |
| <dl> <span data-ttu-id="55330-126"><dt>Macchina virtuale \_ E \_ funzionalità aggiuntive \_ \_ non \_ disponibili</dt> <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="55330-126"><dt>VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="55330-127">La funzionalità componenti di integrazione non è in esecuzione nel sistema operativo guest.</span><span class="sxs-lookup"><span data-stu-id="55330-127">The integration components feature is not running in the guest operating system.</span></span><br/>                                                                                                                 |
| <dl> <span data-ttu-id="55330-128"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="55330-128"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="55330-129">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="55330-129">An unexpected error has occurred.</span></span><br/>                                                                                                                                                                |



## <a name="requirements"></a><span data-ttu-id="55330-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="55330-130">Requirements</span></span>



| <span data-ttu-id="55330-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="55330-131">Requirement</span></span> | <span data-ttu-id="55330-132">Valore</span><span class="sxs-lookup"><span data-stu-id="55330-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="55330-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="55330-133">Minimum supported client</span></span><br/> | <span data-ttu-id="55330-134">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="55330-134">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="55330-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="55330-135">Minimum supported server</span></span><br/> | <span data-ttu-id="55330-136">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="55330-136">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="55330-137">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="55330-137">End of client support</span></span><br/>    | <span data-ttu-id="55330-138">Windows 7</span><span class="sxs-lookup"><span data-stu-id="55330-138">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="55330-139">Prodotto</span><span class="sxs-lookup"><span data-stu-id="55330-139">Product</span></span><br/>                  | <span data-ttu-id="55330-140">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="55330-140">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="55330-141">Intestazione</span><span class="sxs-lookup"><span data-stu-id="55330-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="55330-142"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="55330-142"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="55330-143">IID</span><span class="sxs-lookup"><span data-stu-id="55330-143">IID</span></span><br/>                      | <span data-ttu-id="55330-144">IID \_ IVMGuestOS è definito come 99fea0db-4880-499a-B6D8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="55330-144">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="55330-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="55330-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55330-146">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="55330-146">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

