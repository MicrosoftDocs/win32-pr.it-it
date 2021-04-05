---
title: Proprietà Type di IVMHardDisk (VPCCOMInterfaces. h)
description: Tipo del disco rigido virtuale.
ms.assetid: a855ed9b-a573-471c-ad98-521c80e9ab8c
keywords:
- Tipo proprietà PC virtuale
- Proprietà del tipo Virtual PC, interfaccia IVMHardDisk
- Interfaccia IVMHardDisk Virtual PC, proprietà Type
topic_type:
- apiref
api_name:
- IVMHardDisk.Type
- IVMHardDisk.get_Type
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3757d74de5fc99972be3c7d267b15c56da6bee16
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048322"
---
# <a name="ivmharddisktype-property"></a><span data-ttu-id="1e49c-106">Proprietà IVMHardDisk:: Type</span><span class="sxs-lookup"><span data-stu-id="1e49c-106">IVMHardDisk::Type property</span></span>

<span data-ttu-id="1e49c-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="1e49c-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="1e49c-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="1e49c-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="1e49c-109">Recupera il tipo del disco rigido virtuale.</span><span class="sxs-lookup"><span data-stu-id="1e49c-109">Retrieves the type of the virtual hard disk.</span></span>

<span data-ttu-id="1e49c-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="1e49c-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e49c-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1e49c-111">Syntax</span></span>


```C++
HRESULT get_Type(
  [out, retval] VMHardDiskType *type
);
```



## <a name="property-value"></a><span data-ttu-id="1e49c-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="1e49c-112">Property value</span></span>

<span data-ttu-id="1e49c-113">Tipo di immagine del disco rigido corrente.</span><span class="sxs-lookup"><span data-stu-id="1e49c-113">The type of the current hard disk image.</span></span>

## <a name="error-codes"></a><span data-ttu-id="1e49c-114">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="1e49c-114">Error codes</span></span>



| <span data-ttu-id="1e49c-115">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="1e49c-115">Name/value</span></span>                                                                                                                                                                               | <span data-ttu-id="1e49c-116">Significato</span><span class="sxs-lookup"><span data-stu-id="1e49c-116">Meaning</span></span>                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1e49c-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="1e49c-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="1e49c-118">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="1e49c-118">The operation was successful.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="1e49c-119"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="1e49c-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="1e49c-120">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="1e49c-120">The parameter is **NULL**.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="1e49c-121"><dt>HRESULT \_ DA \_ Win32 (file degli errori \_ \_ non \_ trovato)</dt> <dt>0x80070002</dt></span><span class="sxs-lookup"><span data-stu-id="1e49c-121"><dt>HRESULT\_FROM\_WIN32(ERROR\_FILE\_NOT\_FOUND)</dt> <dt>0x80070002</dt></span></span> </dl> | <span data-ttu-id="1e49c-122">Impossibile trovare il file di immagine del disco rigido corrente.</span><span class="sxs-lookup"><span data-stu-id="1e49c-122">The current hard disk image file could not be found.</span></span><br/>                           |
| <dl> <span data-ttu-id="1e49c-123"><dt>Macchina virtuale \_ Unità E 0xA0040502 \_ \_ non valide</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="1e49c-123"><dt>VM\_E\_DRIVE\_INVALID</dt> <dt>0xA0040502</dt></span></span> </dl>                         | <span data-ttu-id="1e49c-124">Il tipo di immagine del disco rigido corrente non è valido.</span><span class="sxs-lookup"><span data-stu-id="1e49c-124">The type of the current hard disk image is invalid.</span></span><br/>                            |
| <dl> <span data-ttu-id="1e49c-125"><dt>Macchina virtuale \_ E \_ \_ immagine HD \_ \_ non riuscita</dt> <dt>0xA004067C</dt></span><span class="sxs-lookup"><span data-stu-id="1e49c-125"><dt>VM\_E\_HD\_IMAGE\_OPEN\_FAIL</dt> <dt>0xA004067C</dt></span></span> </dl>                  | <span data-ttu-id="1e49c-126">Si è verificato un errore durante il tentativo di aprire il file di immagine del disco rigido corrente.</span><span class="sxs-lookup"><span data-stu-id="1e49c-126">An error occurred while attempting to open the current hard disk image file.</span></span><br/>   |
| <dl> <span data-ttu-id="1e49c-127"><dt>Macchina virtuale \_ E \_ \_ \_ accesso alle immagini HD</dt> <dt>0xA0040681</dt></span><span class="sxs-lookup"><span data-stu-id="1e49c-127"><dt>VM\_E\_HD\_IMAGE\_ACCESS</dt> <dt>0xA0040681</dt></span></span> </dl>                      | <span data-ttu-id="1e49c-128">Si è verificato un errore durante il tentativo di accesso al file di immagine del disco rigido corrente.</span><span class="sxs-lookup"><span data-stu-id="1e49c-128">An error occurred while attempting to access the current hard disk image file.</span></span><br/> |
| <dl> <span data-ttu-id="1e49c-129"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="1e49c-129"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="1e49c-130">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="1e49c-130">An unexpected error has occurred.</span></span><br/>                                              |



## <a name="requirements"></a><span data-ttu-id="1e49c-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1e49c-131">Requirements</span></span>



| <span data-ttu-id="1e49c-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="1e49c-132">Requirement</span></span> | <span data-ttu-id="1e49c-133">Valore</span><span class="sxs-lookup"><span data-stu-id="1e49c-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e49c-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1e49c-134">Minimum supported client</span></span><br/> | <span data-ttu-id="1e49c-135">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="1e49c-135">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1e49c-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1e49c-136">Minimum supported server</span></span><br/> | <span data-ttu-id="1e49c-137">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="1e49c-137">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="1e49c-138">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="1e49c-138">End of client support</span></span><br/>    | <span data-ttu-id="1e49c-139">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1e49c-139">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="1e49c-140">Prodotto</span><span class="sxs-lookup"><span data-stu-id="1e49c-140">Product</span></span><br/>                  | <span data-ttu-id="1e49c-141">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="1e49c-141">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="1e49c-142">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1e49c-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="1e49c-143"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="1e49c-143"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="1e49c-144">IID</span><span class="sxs-lookup"><span data-stu-id="1e49c-144">IID</span></span><br/>                      | <span data-ttu-id="1e49c-145">IID \_ IVMHardDisk è definito come ffa14ae6-48f5-42A4-8a22-186f2e5c7db0</span><span class="sxs-lookup"><span data-stu-id="1e49c-145">IID\_IVMHardDisk is defined as ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="1e49c-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1e49c-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e49c-147">**IVMHardDisk**</span><span class="sxs-lookup"><span data-stu-id="1e49c-147">**IVMHardDisk**</span></span>](ivmharddisk.md)
</dt> </dl>

 

