---
title: Proprietà allegato IVMDVDDrive (VPCCOMInterfaces. h)
description: Recupera il tipo di supporto collegato all'unità DVD all'interno della macchina virtuale.
ms.assetid: 7ae1714d-e5e9-4f6a-85a6-c0b3c4d21820
keywords:
- Proprietà allegato Virtual PC
- Proprietà allegato Virtual PC, interfaccia IVMDVDDrive
- Interfaccia IVMDVDDrive Virtual PC, proprietà Attachment
topic_type:
- apiref
api_name:
- IVMDVDDrive.Attachment
- IVMDVDDrive.get_Attachment
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de5c7801e11534249da899797b73b632a7eda307
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874181"
---
# <a name="ivmdvddriveattachment-property"></a><span data-ttu-id="f9541-106">Proprietà IVMDVDDrive:: Attachment</span><span class="sxs-lookup"><span data-stu-id="f9541-106">IVMDVDDrive::Attachment property</span></span>

<span data-ttu-id="f9541-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="f9541-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="f9541-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="f9541-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="f9541-109">Recupera il tipo di supporto collegato all'unità DVD all'interno della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="f9541-109">Retrieves the type of media attached to the DVD drive within the virtual machine.</span></span>

<span data-ttu-id="f9541-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="f9541-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9541-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f9541-111">Syntax</span></span>


```C++
HRESULT get_Attachment(
  [out, retval] VMDVDDriveAttachmentType *driveAttachment
);
```



## <a name="property-value"></a><span data-ttu-id="f9541-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="f9541-112">Property value</span></span>

<span data-ttu-id="f9541-113">Tipo di supporto collegato.</span><span class="sxs-lookup"><span data-stu-id="f9541-113">The attached media type.</span></span> <span data-ttu-id="f9541-114">Per un elenco di valori, vedere [**VMDVDDriveAttachmentType**](vmdvddriveattachmenttype.md).</span><span class="sxs-lookup"><span data-stu-id="f9541-114">For a list of values, see [**VMDVDDriveAttachmentType**](vmdvddriveattachmenttype.md).</span></span>

## <a name="error-codes"></a><span data-ttu-id="f9541-115">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="f9541-115">Error codes</span></span>



| <span data-ttu-id="f9541-116">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="f9541-116">Name/value</span></span>                                                                                                                                                       | <span data-ttu-id="f9541-117">Significato</span><span class="sxs-lookup"><span data-stu-id="f9541-117">Meaning</span></span>                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <span data-ttu-id="f9541-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f9541-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                          | <span data-ttu-id="f9541-119">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="f9541-119">The operation was successful.</span></span><br/>               |
| <dl> <span data-ttu-id="f9541-120"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="f9541-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>            | <span data-ttu-id="f9541-121">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="f9541-121">The parameter is **NULL**.</span></span><br/>                  |
| <dl> <span data-ttu-id="f9541-122"><dt>E \_ ERRORE</dt> <dt>0x80004005</dt></span><span class="sxs-lookup"><span data-stu-id="f9541-122"><dt>E\_FAIL</dt> <dt>0x80004005</dt></span></span> </dl>               | <span data-ttu-id="f9541-123">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="f9541-123">An unexpected error has occurred.</span></span><br/>           |
| <dl> <span data-ttu-id="f9541-124"><dt>Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="f9541-124"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>    | <span data-ttu-id="f9541-125">Impossibile trovare la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="f9541-125">The virtual machine could not be found.</span></span><br/>     |
| <dl> <span data-ttu-id="f9541-126"><dt>Macchina virtuale \_ Unità E 0xA0040502 \_ \_ non valide</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="f9541-126"><dt>VM\_E\_DRIVE\_INVALID</dt> <dt>0xA0040502</dt></span></span> </dl> | <span data-ttu-id="f9541-127">Il percorso del bus per questa unità non è valido.</span><span class="sxs-lookup"><span data-stu-id="f9541-127">The bus location for this drive is invalid.</span></span><br/> |
| <dl> <span data-ttu-id="f9541-128"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="f9541-128"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>    | <span data-ttu-id="f9541-129">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="f9541-129">An unexpected error has occurred.</span></span><br/>           |



## <a name="requirements"></a><span data-ttu-id="f9541-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f9541-130">Requirements</span></span>



| <span data-ttu-id="f9541-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="f9541-131">Requirement</span></span> | <span data-ttu-id="f9541-132">Valore</span><span class="sxs-lookup"><span data-stu-id="f9541-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9541-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f9541-133">Minimum supported client</span></span><br/> | <span data-ttu-id="f9541-134">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="f9541-134">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f9541-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f9541-135">Minimum supported server</span></span><br/> | <span data-ttu-id="f9541-136">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="f9541-136">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="f9541-137">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="f9541-137">End of client support</span></span><br/>    | <span data-ttu-id="f9541-138">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f9541-138">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="f9541-139">Prodotto</span><span class="sxs-lookup"><span data-stu-id="f9541-139">Product</span></span><br/>                  | <span data-ttu-id="f9541-140">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="f9541-140">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="f9541-141">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f9541-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="f9541-142"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="f9541-142"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="f9541-143">IID</span><span class="sxs-lookup"><span data-stu-id="f9541-143">IID</span></span><br/>                      | <span data-ttu-id="f9541-144">IID \_ IVMDVDDrive è definito come b96328f6-6732-437D-a00d-ffa47e43971c</span><span class="sxs-lookup"><span data-stu-id="f9541-144">IID\_IVMDVDDrive is defined as b96328f6-6732-437d-a00d-ffa47e43971c</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="f9541-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f9541-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9541-146">**IVMDVDDrive**</span><span class="sxs-lookup"><span data-stu-id="f9541-146">**IVMDVDDrive**</span></span>](ivmdvddrive.md)
</dt> </dl>

 

