---
title: Proprietà IVMFloppyDrive ImageFile (VPCCOMInterfaces. h)
description: Recupera il percorso completo del file di immagine a cui è collegata l'unità floppy.
ms.assetid: fc87e438-e5d4-494d-8ac2-27a4312ee81d
keywords:
- Proprietà ImageFile Virtual PC
- Proprietà ImageFile Virtual PC, interfaccia IVMFloppyDrive
- Interfaccia IVMFloppyDrive Virtual PC, proprietà ImageFile
topic_type:
- apiref
api_name:
- IVMFloppyDrive.ImageFile
- IVMFloppyDrive.get_ImageFile
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa18c4a1da3137613e0106f828f59805e5615384
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048576"
---
# <a name="ivmfloppydriveimagefile-property"></a><span data-ttu-id="75413-106">Proprietà IVMFloppyDrive:: ImageFile</span><span class="sxs-lookup"><span data-stu-id="75413-106">IVMFloppyDrive::ImageFile property</span></span>

<span data-ttu-id="75413-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="75413-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="75413-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="75413-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="75413-109">Recupera il percorso completo del file di immagine a cui è collegata l'unità floppy.</span><span class="sxs-lookup"><span data-stu-id="75413-109">Retrieves the full path of the image file to which the floppy drive is attached.</span></span>

<span data-ttu-id="75413-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="75413-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="75413-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="75413-111">Syntax</span></span>


```C++
HRESULT get_ImageFile(
  [out, retval] BSTR *imageFile
);
```



## <a name="property-value"></a><span data-ttu-id="75413-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="75413-112">Property value</span></span>

<span data-ttu-id="75413-113">Percorso completo del file di immagine.</span><span class="sxs-lookup"><span data-stu-id="75413-113">The full path of the image file.</span></span>

## <a name="error-codes"></a><span data-ttu-id="75413-114">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="75413-114">Error codes</span></span>



| <span data-ttu-id="75413-115">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="75413-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="75413-116">Significato</span><span class="sxs-lookup"><span data-stu-id="75413-116">Meaning</span></span>                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="75413-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="75413-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="75413-118">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="75413-118">The operation was successful.</span></span><br/>                                               |
| <dl> <span data-ttu-id="75413-119"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="75413-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="75413-120">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="75413-120">The parameter is **NULL**.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="75413-121"><dt>Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="75413-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="75413-122">La configurazione per questa macchina virtuale non è valida o non è stata trovata.</span><span class="sxs-lookup"><span data-stu-id="75413-122">The configuration for this virtual machine is not valid or cannot be found.</span></span><br/> |
| <dl> <span data-ttu-id="75413-123"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="75413-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="75413-124">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="75413-124">An unexpected error has occurred.</span></span><br/>                                           |



## <a name="requirements"></a><span data-ttu-id="75413-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="75413-125">Requirements</span></span>



| <span data-ttu-id="75413-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="75413-126">Requirement</span></span> | <span data-ttu-id="75413-127">Valore</span><span class="sxs-lookup"><span data-stu-id="75413-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="75413-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="75413-128">Minimum supported client</span></span><br/> | <span data-ttu-id="75413-129">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="75413-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="75413-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="75413-130">Minimum supported server</span></span><br/> | <span data-ttu-id="75413-131">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="75413-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="75413-132">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="75413-132">End of client support</span></span><br/>    | <span data-ttu-id="75413-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="75413-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="75413-134">Prodotto</span><span class="sxs-lookup"><span data-stu-id="75413-134">Product</span></span><br/>                  | <span data-ttu-id="75413-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="75413-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="75413-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="75413-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="75413-137"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="75413-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="75413-138">IID</span><span class="sxs-lookup"><span data-stu-id="75413-138">IID</span></span><br/>                      | <span data-ttu-id="75413-139">IID \_ IVMFloppyDrive è definito come 661abee6-112A-4ED9-babf-3c874969f10e</span><span class="sxs-lookup"><span data-stu-id="75413-139">IID\_IVMFloppyDrive is defined as 661abee6-112a-4ed9-babf-3c874969f10e</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="75413-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="75413-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75413-141">**IVMFloppyDrive**</span><span class="sxs-lookup"><span data-stu-id="75413-141">**IVMFloppyDrive**</span></span>](ivmfloppydrive.md)
</dt> </dl>

 

