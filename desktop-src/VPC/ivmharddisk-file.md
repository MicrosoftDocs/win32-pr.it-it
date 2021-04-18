---
title: Proprietà file IVMHardDisk (VPCCOMInterfaces. h)
description: Recupera il nome del percorso completo del file del disco rigido virtuale.
ms.assetid: 8c1f028a-32e6-4b70-b19c-bed7c2d53de1
keywords:
- Proprietà file Virtual PC
- Proprietà file Virtual PC, interfaccia IVMHardDisk
- Interfaccia IVMHardDisk Virtual PC, proprietà file
topic_type:
- apiref
api_name:
- IVMHardDisk.File
- IVMHardDisk.get_File
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43b2a83b92bb5d02049066f9be90543a34a2fe7d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302417"
---
# <a name="ivmharddiskfile-property"></a><span data-ttu-id="78ce4-106">Proprietà IVMHardDisk:: file</span><span class="sxs-lookup"><span data-stu-id="78ce4-106">IVMHardDisk::File property</span></span>

<span data-ttu-id="78ce4-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="78ce4-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="78ce4-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="78ce4-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="78ce4-109">Recupera il nome del percorso completo del file del disco rigido virtuale.</span><span class="sxs-lookup"><span data-stu-id="78ce4-109">Retrieves the full path name of the virtual hard disk file.</span></span>

<span data-ttu-id="78ce4-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="78ce4-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="78ce4-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="78ce4-111">Syntax</span></span>


```C++
HRESULT get_File(
  [out, retval] BSTR *hardDiskfile
);
```



## <a name="property-value"></a><span data-ttu-id="78ce4-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="78ce4-112">Property value</span></span>

<span data-ttu-id="78ce4-113">Nome del percorso completo del file di immagine del disco rigido corrente.</span><span class="sxs-lookup"><span data-stu-id="78ce4-113">The full path name of the current hard disk image file.</span></span>

## <a name="error-codes"></a><span data-ttu-id="78ce4-114">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="78ce4-114">Error codes</span></span>



| <span data-ttu-id="78ce4-115">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="78ce4-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="78ce4-116">Significato</span><span class="sxs-lookup"><span data-stu-id="78ce4-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="78ce4-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="78ce4-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="78ce4-118">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="78ce4-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="78ce4-119"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="78ce4-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="78ce4-120">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="78ce4-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="78ce4-121"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="78ce4-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="78ce4-122">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="78ce4-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="78ce4-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="78ce4-123">Requirements</span></span>



| <span data-ttu-id="78ce4-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="78ce4-124">Requirement</span></span> | <span data-ttu-id="78ce4-125">Valore</span><span class="sxs-lookup"><span data-stu-id="78ce4-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="78ce4-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="78ce4-126">Minimum supported client</span></span><br/> | <span data-ttu-id="78ce4-127">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="78ce4-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="78ce4-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="78ce4-128">Minimum supported server</span></span><br/> | <span data-ttu-id="78ce4-129">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="78ce4-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="78ce4-130">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="78ce4-130">End of client support</span></span><br/>    | <span data-ttu-id="78ce4-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="78ce4-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="78ce4-132">Prodotto</span><span class="sxs-lookup"><span data-stu-id="78ce4-132">Product</span></span><br/>                  | <span data-ttu-id="78ce4-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="78ce4-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="78ce4-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="78ce4-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="78ce4-135"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="78ce4-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="78ce4-136">IID</span><span class="sxs-lookup"><span data-stu-id="78ce4-136">IID</span></span><br/>                      | <span data-ttu-id="78ce4-137">IID \_ IVMHardDisk è definito come ffa14ae6-48f5-42A4-8a22-186f2e5c7db0</span><span class="sxs-lookup"><span data-stu-id="78ce4-137">IID\_IVMHardDisk is defined as ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="78ce4-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="78ce4-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78ce4-139">**IVMHardDisk**</span><span class="sxs-lookup"><span data-stu-id="78ce4-139">**IVMHardDisk**</span></span>](ivmharddisk.md)
</dt> </dl>

 

