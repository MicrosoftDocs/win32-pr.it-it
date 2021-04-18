---
title: Proprietà IVMGuestOS OSMinorVersion (VPCCOMInterfaces. h)
description: Versione secondaria del sistema operativo guest in esecuzione nella macchina virtuale.
ms.assetid: fa71e215-8633-4f53-ab71-bc9bfdb56cc8
keywords:
- Proprietà OSMinorVersion Virtual PC
- Proprietà OSMinorVersion Virtual PC, interfaccia IVMGuestOS
- Interfaccia IVMGuestOS Virtual PC, proprietà OSMinorVersion
topic_type:
- apiref
api_name:
- IVMGuestOS.OSMinorVersion
- IVMGuestOS.get_OSMinorVersion
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df7c068ee6d8112561f57d0644f6bc7bc4844096
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301565"
---
# <a name="ivmguestososminorversion-property"></a><span data-ttu-id="0d3cd-106">Proprietà IVMGuestOS:: OSMinorVersion</span><span class="sxs-lookup"><span data-stu-id="0d3cd-106">IVMGuestOS::OSMinorVersion property</span></span>

<span data-ttu-id="0d3cd-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="0d3cd-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="0d3cd-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="0d3cd-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="0d3cd-109">Recupera la versione secondaria del sistema operativo guest in esecuzione nella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="0d3cd-109">Retrieves the minor version of the guest operating system running in the virtual machine.</span></span>

<span data-ttu-id="0d3cd-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="0d3cd-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d3cd-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0d3cd-111">Syntax</span></span>


```C++
HRESULT get_OSMinorVersion(
  [out, retval] BSTR *minorVersion
);
```



## <a name="property-value"></a><span data-ttu-id="0d3cd-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="0d3cd-112">Property value</span></span>

<span data-ttu-id="0d3cd-113">La versione secondaria.</span><span class="sxs-lookup"><span data-stu-id="0d3cd-113">The minor version.</span></span>

## <a name="error-codes"></a><span data-ttu-id="0d3cd-114">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="0d3cd-114">Error codes</span></span>



| <span data-ttu-id="0d3cd-115">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="0d3cd-115">Name/value</span></span>                                                                                                                                                                       | <span data-ttu-id="0d3cd-116">Significato</span><span class="sxs-lookup"><span data-stu-id="0d3cd-116">Meaning</span></span>                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="0d3cd-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="0d3cd-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="0d3cd-118">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="0d3cd-118">The operation was successful.</span></span><br/>                        |
| <dl> <span data-ttu-id="0d3cd-119"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="0d3cd-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                            | <span data-ttu-id="0d3cd-120">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="0d3cd-120">The parameter is **NULL**.</span></span><br/>                           |
| <dl> <span data-ttu-id="0d3cd-121"><dt>Macchina virtuale \_ \_VM E \_ non \_ in esecuzione</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="0d3cd-121"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="0d3cd-122">La macchina virtuale non è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="0d3cd-122">The VM is not running.</span></span><br/>                               |
| <dl> <span data-ttu-id="0d3cd-123"><dt>Macchina virtuale \_ E \_ funzionalità aggiuntive \_ \_ non \_ disponibili</dt> <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="0d3cd-123"><dt>VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="0d3cd-124">I componenti di integrazione non sono installati in questa macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="0d3cd-124">Integration components are not installed in this VM.</span></span><br/> |
| <dl> <span data-ttu-id="0d3cd-125"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="0d3cd-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="0d3cd-126">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="0d3cd-126">An unexpected error has occurred.</span></span><br/>                    |



## <a name="requirements"></a><span data-ttu-id="0d3cd-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0d3cd-127">Requirements</span></span>



| <span data-ttu-id="0d3cd-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d3cd-128">Requirement</span></span> | <span data-ttu-id="0d3cd-129">Valore</span><span class="sxs-lookup"><span data-stu-id="0d3cd-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d3cd-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0d3cd-130">Minimum supported client</span></span><br/> | <span data-ttu-id="0d3cd-131">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="0d3cd-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0d3cd-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0d3cd-132">Minimum supported server</span></span><br/> | <span data-ttu-id="0d3cd-133">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="0d3cd-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="0d3cd-134">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="0d3cd-134">End of client support</span></span><br/>    | <span data-ttu-id="0d3cd-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="0d3cd-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="0d3cd-136">Prodotto</span><span class="sxs-lookup"><span data-stu-id="0d3cd-136">Product</span></span><br/>                  | <span data-ttu-id="0d3cd-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="0d3cd-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="0d3cd-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0d3cd-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="0d3cd-139"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d3cd-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="0d3cd-140">IID</span><span class="sxs-lookup"><span data-stu-id="0d3cd-140">IID</span></span><br/>                      | <span data-ttu-id="0d3cd-141">IID \_ IVMGuestOS è definito come 99fea0db-4880-499a-B6D8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="0d3cd-141">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="0d3cd-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0d3cd-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d3cd-143">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="0d3cd-143">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

