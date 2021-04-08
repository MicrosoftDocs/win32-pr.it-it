---
title: Proprietà IVMGuestOS IntegrationComponentsVersion (VPCCOMInterfaces. h)
description: Recupera la versione dei componenti di integrazione installati nel sistema operativo guest.
ms.assetid: 4baccb7d-5a3e-460f-9669-ee8dbaec91a9
keywords:
- Proprietà IntegrationComponentsVersion Virtual PC
- Proprietà IntegrationComponentsVersion Virtual PC, interfaccia IVMGuestOS
- Interfaccia IVMGuestOS Virtual PC, proprietà IntegrationComponentsVersion
topic_type:
- apiref
api_name:
- IVMGuestOS.IntegrationComponentsVersion
- IVMGuestOS.get_IntegrationComponentsVersion
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f85352614b89ab208377fe44fe3b970c693d60dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740167"
---
# <a name="ivmguestosintegrationcomponentsversion-property"></a><span data-ttu-id="51cd7-106">Proprietà IVMGuestOS:: IntegrationComponentsVersion</span><span class="sxs-lookup"><span data-stu-id="51cd7-106">IVMGuestOS::IntegrationComponentsVersion property</span></span>

<span data-ttu-id="51cd7-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="51cd7-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="51cd7-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="51cd7-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="51cd7-109">Recupera la versione dei componenti di integrazione installati nel sistema operativo guest.</span><span class="sxs-lookup"><span data-stu-id="51cd7-109">Retrieves the version of the Integration Components installed in the guest operating system.</span></span>

<span data-ttu-id="51cd7-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="51cd7-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="51cd7-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="51cd7-111">Syntax</span></span>


```C++
HRESULT get_IntegrationComponentsVersion(
  [out, retval] BSTR *ICVersion
);
```



## <a name="property-value"></a><span data-ttu-id="51cd7-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="51cd7-112">Property value</span></span>

<span data-ttu-id="51cd7-113">Versione.</span><span class="sxs-lookup"><span data-stu-id="51cd7-113">The version.</span></span>

## <a name="error-codes"></a><span data-ttu-id="51cd7-114">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="51cd7-114">Error codes</span></span>



| <span data-ttu-id="51cd7-115">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="51cd7-115">Name/value</span></span>                                                                                                                                                              | <span data-ttu-id="51cd7-116">Significato</span><span class="sxs-lookup"><span data-stu-id="51cd7-116">Meaning</span></span>                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="51cd7-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="51cd7-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                 | <span data-ttu-id="51cd7-118">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="51cd7-118">The operation was successful.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="51cd7-119"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="51cd7-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                   | <span data-ttu-id="51cd7-120">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="51cd7-120">The parameter is **NULL**.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="51cd7-121"><dt>Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="51cd7-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>           | <span data-ttu-id="51cd7-122">La macchina virtuale (VM) non è stata trovata.</span><span class="sxs-lookup"><span data-stu-id="51cd7-122">The virtual machine (VM) could not be found.</span></span><br/>                                      |
| <dl> <span data-ttu-id="51cd7-123"><dt>Macchina virtuale \_ \_Aggiunte di E \_ non \_ disponibili</dt> <dt>0xA0040504</dt></span><span class="sxs-lookup"><span data-stu-id="51cd7-123"><dt>VM\_E\_ADDITIONS\_NOT\_AVAIL</dt> <dt>0xA0040504</dt></span></span> </dl> | <span data-ttu-id="51cd7-124">I componenti di integrazione non sono installati in questa macchina virtuale oppure la macchina virtuale non è mai stata avviata.</span><span class="sxs-lookup"><span data-stu-id="51cd7-124">Integration Components are not installed in this VM, or the VM was never started.</span></span><br/> |
| <dl> <span data-ttu-id="51cd7-125"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="51cd7-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>           | <span data-ttu-id="51cd7-126">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="51cd7-126">An unexpected error has occurred.</span></span><br/>                                                 |



## <a name="requirements"></a><span data-ttu-id="51cd7-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="51cd7-127">Requirements</span></span>



| <span data-ttu-id="51cd7-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="51cd7-128">Requirement</span></span> | <span data-ttu-id="51cd7-129">Valore</span><span class="sxs-lookup"><span data-stu-id="51cd7-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="51cd7-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="51cd7-130">Minimum supported client</span></span><br/> | <span data-ttu-id="51cd7-131">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="51cd7-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="51cd7-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="51cd7-132">Minimum supported server</span></span><br/> | <span data-ttu-id="51cd7-133">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="51cd7-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="51cd7-134">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="51cd7-134">End of client support</span></span><br/>    | <span data-ttu-id="51cd7-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="51cd7-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="51cd7-136">Prodotto</span><span class="sxs-lookup"><span data-stu-id="51cd7-136">Product</span></span><br/>                  | <span data-ttu-id="51cd7-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="51cd7-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="51cd7-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="51cd7-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="51cd7-139"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="51cd7-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="51cd7-140">IID</span><span class="sxs-lookup"><span data-stu-id="51cd7-140">IID</span></span><br/>                      | <span data-ttu-id="51cd7-141">IID \_ IVMGuestOS è definito come 99fea0db-4880-499a-B6D8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="51cd7-141">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="51cd7-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="51cd7-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51cd7-143">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="51cd7-143">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

