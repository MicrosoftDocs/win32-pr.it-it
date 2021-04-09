---
title: Proprietà IVMHardDisk SizeOnHost (VPCCOMInterfaces. h)
description: Dimensioni del file del disco rigido virtuale nel computer host.
ms.assetid: f787ec4b-7b4f-4d35-b07c-4844424d91cf
keywords:
- Proprietà SizeOnHost Virtual PC
- Proprietà SizeOnHost Virtual PC, interfaccia IVMHardDisk
- Interfaccia IVMHardDisk Virtual PC, proprietà SizeOnHost
topic_type:
- apiref
api_name:
- IVMHardDisk.SizeOnHost
- IVMHardDisk.get_SizeOnHost
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d3a000a70e1713b28f8fb8eea3590a53fb46ff0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048575"
---
# <a name="ivmharddisksizeonhost-property"></a><span data-ttu-id="af36e-106">Proprietà IVMHardDisk:: SizeOnHost</span><span class="sxs-lookup"><span data-stu-id="af36e-106">IVMHardDisk::SizeOnHost property</span></span>

<span data-ttu-id="af36e-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="af36e-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="af36e-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="af36e-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="af36e-109">Recupera le dimensioni del file del disco rigido virtuale nel computer host.</span><span class="sxs-lookup"><span data-stu-id="af36e-109">Retrieves the size of the virtual hard disk file on the host computer.</span></span>

<span data-ttu-id="af36e-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="af36e-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="af36e-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="af36e-111">Syntax</span></span>


```C++
HRESULT get_SizeOnHost(
  [out, retval] VARIANT *fileSize
);
```



## <a name="property-value"></a><span data-ttu-id="af36e-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="af36e-112">Property value</span></span>

<span data-ttu-id="af36e-113">Dimensione, in byte, del file di immagine del disco rigido.</span><span class="sxs-lookup"><span data-stu-id="af36e-113">The size, in bytes, of the hard disk image file.</span></span> <span data-ttu-id="af36e-114">Questo valore è una **variante** di tipo **\_ decimale VT**.</span><span class="sxs-lookup"><span data-stu-id="af36e-114">This value is a **VARIANT** of type **VT\_DECIMAL**.</span></span>

## <a name="error-codes"></a><span data-ttu-id="af36e-115">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="af36e-115">Error codes</span></span>



| <span data-ttu-id="af36e-116">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="af36e-116">Name/value</span></span>                                                                                                                                                                               | <span data-ttu-id="af36e-117">Significato</span><span class="sxs-lookup"><span data-stu-id="af36e-117">Meaning</span></span>                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="af36e-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="af36e-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="af36e-119">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="af36e-119">The operation was successful.</span></span><br/>           |
| <dl> <span data-ttu-id="af36e-120"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="af36e-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="af36e-121">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="af36e-121">The parameter is **NULL**.</span></span><br/>              |
| <dl> <span data-ttu-id="af36e-122"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="af36e-122"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="af36e-123">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="af36e-123">An unexpected error has occurred.</span></span><br/>       |
| <dl> <span data-ttu-id="af36e-124"><dt>HRESULT \_ DA \_ Win32 (file degli errori \_ \_ non \_ trovato)</dt> <dt>0x80070002</dt></span><span class="sxs-lookup"><span data-stu-id="af36e-124"><dt>HRESULT\_FROM\_WIN32(ERROR\_FILE\_NOT\_FOUND)</dt> <dt>0x80070002</dt></span></span> </dl> | <span data-ttu-id="af36e-125">Il file di immagine del disco rigido non è stato trovato.</span><span class="sxs-lookup"><span data-stu-id="af36e-125">The hard disk image file was not found.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="af36e-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="af36e-126">Requirements</span></span>



| <span data-ttu-id="af36e-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="af36e-127">Requirement</span></span> | <span data-ttu-id="af36e-128">Valore</span><span class="sxs-lookup"><span data-stu-id="af36e-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="af36e-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="af36e-129">Minimum supported client</span></span><br/> | <span data-ttu-id="af36e-130">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="af36e-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="af36e-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="af36e-131">Minimum supported server</span></span><br/> | <span data-ttu-id="af36e-132">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="af36e-132">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="af36e-133">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="af36e-133">End of client support</span></span><br/>    | <span data-ttu-id="af36e-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="af36e-134">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="af36e-135">Prodotto</span><span class="sxs-lookup"><span data-stu-id="af36e-135">Product</span></span><br/>                  | <span data-ttu-id="af36e-136">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="af36e-136">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="af36e-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="af36e-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="af36e-138"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="af36e-138"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="af36e-139">IID</span><span class="sxs-lookup"><span data-stu-id="af36e-139">IID</span></span><br/>                      | <span data-ttu-id="af36e-140">IID \_ IVMHardDisk è definito come ffa14ae6-48f5-42A4-8a22-186f2e5c7db0</span><span class="sxs-lookup"><span data-stu-id="af36e-140">IID\_IVMHardDisk is defined as ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="af36e-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="af36e-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af36e-142">**IVMHardDisk**</span><span class="sxs-lookup"><span data-stu-id="af36e-142">**IVMHardDisk**</span></span>](ivmharddisk.md)
</dt> </dl>

 

