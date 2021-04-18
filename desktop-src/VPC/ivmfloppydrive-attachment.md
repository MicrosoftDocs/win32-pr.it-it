---
title: Proprietà allegato IVMFloppyDrive (VPCCOMInterfaces. h)
description: Recupera il tipo di supporto collegato all'unità floppy nella macchina virtuale.
ms.assetid: 0b7e43ac-de56-4c4b-82e6-75877aea06f2
keywords:
- Proprietà allegato Virtual PC
- Proprietà allegato Virtual PC, interfaccia IVMFloppyDrive
- Interfaccia IVMFloppyDrive Virtual PC, proprietà Attachment
topic_type:
- apiref
api_name:
- IVMFloppyDrive.Attachment
- IVMFloppyDrive.get_Attachment
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44814148baf27672f30b8e3c5015d841aaaba4b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301735"
---
# <a name="ivmfloppydriveattachment-property"></a><span data-ttu-id="688ef-106">Proprietà IVMFloppyDrive:: Attachment</span><span class="sxs-lookup"><span data-stu-id="688ef-106">IVMFloppyDrive::Attachment property</span></span>

<span data-ttu-id="688ef-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="688ef-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="688ef-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="688ef-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="688ef-109">Recupera il tipo di supporto collegato all'unità floppy nella macchina virtuale (VM).</span><span class="sxs-lookup"><span data-stu-id="688ef-109">Retrieves the type of media attached to the floppy drive in the virtual machine (VM).</span></span>

<span data-ttu-id="688ef-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="688ef-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="688ef-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="688ef-111">Syntax</span></span>


```C++
HRESULT get_Attachment(
  [out, retval] VMFloppyDriveAttachmentType *driveAttachment
);
```



## <a name="property-value"></a><span data-ttu-id="688ef-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="688ef-112">Property value</span></span>

<span data-ttu-id="688ef-113">Tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="688ef-113">The type of media.</span></span> <span data-ttu-id="688ef-114">Per un elenco di valori, vedere [**VMFloppyDriveAttachmentType**](vmfloppydriveattachmenttype.md).</span><span class="sxs-lookup"><span data-stu-id="688ef-114">For a list of values, see [**VMFloppyDriveAttachmentType**](vmfloppydriveattachmenttype.md).</span></span>

## <a name="error-codes"></a><span data-ttu-id="688ef-115">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="688ef-115">Error codes</span></span>



| <span data-ttu-id="688ef-116">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="688ef-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="688ef-117">Significato</span><span class="sxs-lookup"><span data-stu-id="688ef-117">Meaning</span></span>                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="688ef-118"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="688ef-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="688ef-119">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="688ef-119">The operation was successful.</span></span><br/>                                  |
| <dl> <span data-ttu-id="688ef-120"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="688ef-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="688ef-121">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="688ef-121">The parameter is **NULL**.</span></span><br/>                                     |
| <dl> <span data-ttu-id="688ef-122"><dt>Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="688ef-122"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="688ef-123">La configurazione per questa macchina virtuale non è valida o non è stata trovata.</span><span class="sxs-lookup"><span data-stu-id="688ef-123">The configuration for this VM is not valid or cannot be found.</span></span><br/> |
| <dl> <span data-ttu-id="688ef-124"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="688ef-124"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="688ef-125">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="688ef-125">An unexpected error has occurred.</span></span><br/>                              |



## <a name="requirements"></a><span data-ttu-id="688ef-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="688ef-126">Requirements</span></span>



| <span data-ttu-id="688ef-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="688ef-127">Requirement</span></span> | <span data-ttu-id="688ef-128">Valore</span><span class="sxs-lookup"><span data-stu-id="688ef-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="688ef-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="688ef-129">Minimum supported client</span></span><br/> | <span data-ttu-id="688ef-130">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="688ef-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="688ef-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="688ef-131">Minimum supported server</span></span><br/> | <span data-ttu-id="688ef-132">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="688ef-132">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="688ef-133">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="688ef-133">End of client support</span></span><br/>    | <span data-ttu-id="688ef-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="688ef-134">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="688ef-135">Prodotto</span><span class="sxs-lookup"><span data-stu-id="688ef-135">Product</span></span><br/>                  | <span data-ttu-id="688ef-136">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="688ef-136">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="688ef-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="688ef-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="688ef-138"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="688ef-138"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="688ef-139">IID</span><span class="sxs-lookup"><span data-stu-id="688ef-139">IID</span></span><br/>                      | <span data-ttu-id="688ef-140">IID \_ IVMFloppyDrive è definito come 661abee6-112A-4ED9-babf-3c874969f10e</span><span class="sxs-lookup"><span data-stu-id="688ef-140">IID\_IVMFloppyDrive is defined as 661abee6-112a-4ed9-babf-3c874969f10e</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="688ef-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="688ef-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="688ef-142">**IVMFloppyDrive**</span><span class="sxs-lookup"><span data-stu-id="688ef-142">**IVMFloppyDrive**</span></span>](ivmfloppydrive.md)
</dt> </dl>

 

