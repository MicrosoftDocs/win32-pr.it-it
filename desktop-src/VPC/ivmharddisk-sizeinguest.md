---
title: Proprietà IVMHardDisk SizeInGuest (VPCCOMInterfaces. h)
description: Recupera le dimensioni del disco rigido virtuale nel sistema operativo guest.
ms.assetid: 895598db-cd54-414c-8783-13102cfbd453
keywords:
- Proprietà SizeInGuest Virtual PC
- Proprietà SizeInGuest Virtual PC, interfaccia IVMHardDisk
- Interfaccia IVMHardDisk Virtual PC, proprietà SizeInGuest
topic_type:
- apiref
api_name:
- IVMHardDisk.SizeInGuest
- IVMHardDisk.get_SizeInGuest
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ace142bf7c0dc612de47c8b2cb043ce24d6e9e9e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120595"
---
# <a name="ivmharddisksizeinguest-property"></a><span data-ttu-id="71611-106">Proprietà IVMHardDisk:: SizeInGuest</span><span class="sxs-lookup"><span data-stu-id="71611-106">IVMHardDisk::SizeInGuest property</span></span>

<span data-ttu-id="71611-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="71611-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="71611-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="71611-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="71611-109">Recupera le dimensioni del disco rigido virtuale nel sistema operativo guest.</span><span class="sxs-lookup"><span data-stu-id="71611-109">Retrieves the size of the virtual hard disk in the guest operating system.</span></span>

<span data-ttu-id="71611-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="71611-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="71611-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="71611-111">Syntax</span></span>


```C++
HRESULT get_SizeInGuest(
  [out, retval] VARIANT *fileSize
);
```



## <a name="property-value"></a><span data-ttu-id="71611-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="71611-112">Property value</span></span>

<span data-ttu-id="71611-113">Dimensione, in byte, dell'immagine del disco rigido.</span><span class="sxs-lookup"><span data-stu-id="71611-113">The size, in bytes, of the hard disk image.</span></span> <span data-ttu-id="71611-114">Questo valore è una **variante** di tipo \_ decimale VT.</span><span class="sxs-lookup"><span data-stu-id="71611-114">This value is a **VARIANT** of type VT\_DECIMAL.</span></span>

## <a name="error-codes"></a><span data-ttu-id="71611-115">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="71611-115">Error codes</span></span>



| <span data-ttu-id="71611-116">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="71611-116">Name/value</span></span>                                                                                                                                                                               | <span data-ttu-id="71611-117">Significato</span><span class="sxs-lookup"><span data-stu-id="71611-117">Meaning</span></span>                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="71611-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="71611-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="71611-119">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="71611-119">The operation was successful.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="71611-120"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="71611-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="71611-121">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="71611-121">The parameter is **NULL**.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="71611-122"><dt>HRESULT \_ DA \_ Win32 (file degli errori \_ \_ non \_ trovato)</dt> <dt>0x80070002</dt></span><span class="sxs-lookup"><span data-stu-id="71611-122"><dt>HRESULT\_FROM\_WIN32(ERROR\_FILE\_NOT\_FOUND)</dt> <dt>0x80070002</dt></span></span> </dl> | <span data-ttu-id="71611-123">Impossibile trovare il file del disco rigido virtuale corrente.</span><span class="sxs-lookup"><span data-stu-id="71611-123">The current virtual hard disk file could not be found.</span></span><br/>                         |
| <dl> <span data-ttu-id="71611-124"><dt>Macchina virtuale \_ E \_ \_ immagine HD \_ \_ non riuscita</dt> <dt>0xA004067C</dt></span><span class="sxs-lookup"><span data-stu-id="71611-124"><dt>VM\_E\_HD\_IMAGE\_OPEN\_FAIL</dt> <dt>0xA004067C</dt></span></span> </dl>                  | <span data-ttu-id="71611-125">Si è verificato un errore durante il tentativo di aprire il file di immagine del disco rigido corrente.</span><span class="sxs-lookup"><span data-stu-id="71611-125">An error occurred while attempting to open the current hard disk image file.</span></span><br/>   |
| <dl> <span data-ttu-id="71611-126"><dt>Macchina virtuale \_ E \_ \_ \_ accesso alle immagini HD</dt> <dt>0xA0040681</dt></span><span class="sxs-lookup"><span data-stu-id="71611-126"><dt>VM\_E\_HD\_IMAGE\_ACCESS</dt> <dt>0xA0040681</dt></span></span> </dl>                      | <span data-ttu-id="71611-127">Si è verificato un errore durante il tentativo di accesso al file di immagine del disco rigido corrente.</span><span class="sxs-lookup"><span data-stu-id="71611-127">An error occurred while attempting to access the current hard disk image file.</span></span><br/> |
| <dl> <span data-ttu-id="71611-128"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="71611-128"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="71611-129">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="71611-129">An unexpected error has occurred.</span></span><br/>                                              |



## <a name="requirements"></a><span data-ttu-id="71611-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="71611-130">Requirements</span></span>



| <span data-ttu-id="71611-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="71611-131">Requirement</span></span> | <span data-ttu-id="71611-132">Valore</span><span class="sxs-lookup"><span data-stu-id="71611-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="71611-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="71611-133">Minimum supported client</span></span><br/> | <span data-ttu-id="71611-134">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="71611-134">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="71611-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="71611-135">Minimum supported server</span></span><br/> | <span data-ttu-id="71611-136">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="71611-136">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="71611-137">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="71611-137">End of client support</span></span><br/>    | <span data-ttu-id="71611-138">Windows 7</span><span class="sxs-lookup"><span data-stu-id="71611-138">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="71611-139">Prodotto</span><span class="sxs-lookup"><span data-stu-id="71611-139">Product</span></span><br/>                  | <span data-ttu-id="71611-140">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="71611-140">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="71611-141">Intestazione</span><span class="sxs-lookup"><span data-stu-id="71611-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="71611-142"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="71611-142"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="71611-143">IID</span><span class="sxs-lookup"><span data-stu-id="71611-143">IID</span></span><br/>                      | <span data-ttu-id="71611-144">IID \_ IVMHardDisk è definito come ffa14ae6-48f5-42A4-8a22-186f2e5c7db0</span><span class="sxs-lookup"><span data-stu-id="71611-144">IID\_IVMHardDisk is defined as ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="71611-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="71611-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71611-146">**IVMHardDisk**</span><span class="sxs-lookup"><span data-stu-id="71611-146">**IVMHardDisk**</span></span>](ivmharddisk.md)
</dt> </dl>

 

