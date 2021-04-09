---
title: Proprietà IVMHardDisk HostFreeDiskSpace (VPCCOMInterfaces. h)
description: Recupera la quantità di spazio su disco rimanente disponibile nell'host per il disco rigido virtuale.
ms.assetid: 08574bd3-e96d-465c-a1fc-265085fb3847
keywords:
- Proprietà HostFreeDiskSpace Virtual PC
- Proprietà HostFreeDiskSpace Virtual PC, interfaccia IVMHardDisk
- Interfaccia IVMHardDisk Virtual PC, proprietà HostFreeDiskSpace
topic_type:
- apiref
api_name:
- IVMHardDisk.HostFreeDiskSpace
- IVMHardDisk.get_HostFreeDiskSpace
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e647d94ddecfdc8e0b9265b3639508b797f37861
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121191"
---
# <a name="ivmharddiskhostfreediskspace-property"></a><span data-ttu-id="6b159-106">Proprietà IVMHardDisk:: HostFreeDiskSpace</span><span class="sxs-lookup"><span data-stu-id="6b159-106">IVMHardDisk::HostFreeDiskSpace property</span></span>

<span data-ttu-id="6b159-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="6b159-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="6b159-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="6b159-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="6b159-109">Recupera la quantità di spazio su disco rimanente disponibile nell'host per il disco rigido virtuale.</span><span class="sxs-lookup"><span data-stu-id="6b159-109">Retrieves the amount of remaining disk space available on the host for the virtual hard disk.</span></span>

<span data-ttu-id="6b159-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="6b159-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b159-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6b159-111">Syntax</span></span>


```C++
HRESULT get_HostFreeDiskSpace(
  [out, retval] VARIANT *freeBytes
);
```



## <a name="property-value"></a><span data-ttu-id="6b159-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="6b159-112">Property value</span></span>

<span data-ttu-id="6b159-113">Quantità di spazio su disco rimanente disponibile nel computer host per il file di immagine del disco rigido corrente.</span><span class="sxs-lookup"><span data-stu-id="6b159-113">The amount of remaining disk space available on the host computer for the current hard disk image file.</span></span> <span data-ttu-id="6b159-114">Questo valore è una **variante** di tipo \_ decimale VT.</span><span class="sxs-lookup"><span data-stu-id="6b159-114">This value is a **VARIANT** of type VT\_DECIMAL.</span></span>

## <a name="error-codes"></a><span data-ttu-id="6b159-115">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="6b159-115">Error codes</span></span>



| <span data-ttu-id="6b159-116">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="6b159-116">Name/value</span></span>                                                                                                                                                                            | <span data-ttu-id="6b159-117">Significato</span><span class="sxs-lookup"><span data-stu-id="6b159-117">Meaning</span></span>                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6b159-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="6b159-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                               | <span data-ttu-id="6b159-119">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="6b159-119">The operation was successful.</span></span><br/>                                |
| <dl> <span data-ttu-id="6b159-120"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="6b159-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                 | <span data-ttu-id="6b159-121">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="6b159-121">The parameter is **NULL**.</span></span><br/>                                   |
| <dl> <span data-ttu-id="6b159-122"><dt>HRESULT \_ DA \_ Win32 (errore \_ \_ percorso errato)</dt> <dt>0x800700a1</dt></span><span class="sxs-lookup"><span data-stu-id="6b159-122"><dt>HRESULT\_FROM\_WIN32(ERROR\_BAD\_PATHNAME)</dt> <dt>0x800700a1</dt></span></span> </dl> | <span data-ttu-id="6b159-123">Il percorso del file del disco rigido virtuale corrente non è valido.</span><span class="sxs-lookup"><span data-stu-id="6b159-123">The path to the current virtual hard disk file is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="6b159-124"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="6b159-124"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                         | <span data-ttu-id="6b159-125">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="6b159-125">An unexpected error has occurred.</span></span><br/>                            |



## <a name="requirements"></a><span data-ttu-id="6b159-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6b159-126">Requirements</span></span>



| <span data-ttu-id="6b159-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="6b159-127">Requirement</span></span> | <span data-ttu-id="6b159-128">Valore</span><span class="sxs-lookup"><span data-stu-id="6b159-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b159-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6b159-129">Minimum supported client</span></span><br/> | <span data-ttu-id="6b159-130">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="6b159-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6b159-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6b159-131">Minimum supported server</span></span><br/> | <span data-ttu-id="6b159-132">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="6b159-132">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="6b159-133">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="6b159-133">End of client support</span></span><br/>    | <span data-ttu-id="6b159-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="6b159-134">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="6b159-135">Prodotto</span><span class="sxs-lookup"><span data-stu-id="6b159-135">Product</span></span><br/>                  | <span data-ttu-id="6b159-136">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="6b159-136">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="6b159-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6b159-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="6b159-138"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="6b159-138"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="6b159-139">IID</span><span class="sxs-lookup"><span data-stu-id="6b159-139">IID</span></span><br/>                      | <span data-ttu-id="6b159-140">IID \_ IVMHardDisk è definito come ffa14ae6-48f5-42A4-8a22-186f2e5c7db0</span><span class="sxs-lookup"><span data-stu-id="6b159-140">IID\_IVMHardDisk is defined as ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="6b159-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6b159-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b159-142">**IVMHardDisk**</span><span class="sxs-lookup"><span data-stu-id="6b159-142">**IVMHardDisk**</span></span>](ivmharddisk.md)
</dt> </dl>

 

