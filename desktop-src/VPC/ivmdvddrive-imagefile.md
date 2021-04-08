---
title: Proprietà IVMDVDDrive ImageFile (VPCCOMInterfaces. h)
description: Recupera il percorso completo del file di immagine impostato per il dispositivo.
ms.assetid: e7910d37-d3a5-4291-b374-aaa67db50f1b
keywords:
- Proprietà ImageFile Virtual PC
- Proprietà ImageFile Virtual PC, interfaccia IVMDVDDrive
- Interfaccia IVMDVDDrive Virtual PC, proprietà ImageFile
topic_type:
- apiref
api_name:
- IVMDVDDrive.ImageFile
- IVMDVDDrive.get_ImageFile
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c71ed5328e41a72c9896147c6dcd824b2bd2ab1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874433"
---
# <a name="ivmdvddriveimagefile-property"></a><span data-ttu-id="785ca-106">Proprietà IVMDVDDrive:: ImageFile</span><span class="sxs-lookup"><span data-stu-id="785ca-106">IVMDVDDrive::ImageFile property</span></span>

<span data-ttu-id="785ca-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="785ca-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="785ca-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="785ca-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="785ca-109">Recupera il percorso completo del file di immagine impostato per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="785ca-109">Retrieves the full path of the image file set for this device.</span></span>

<span data-ttu-id="785ca-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="785ca-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="785ca-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="785ca-111">Syntax</span></span>


```C++
HRESULT get_ImageFile(
  [out, retval] BSTR *imagePath
);
```



## <a name="property-value"></a><span data-ttu-id="785ca-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="785ca-112">Property value</span></span>

<span data-ttu-id="785ca-113">Percorso completo del file di immagine.</span><span class="sxs-lookup"><span data-stu-id="785ca-113">The full path to the image file.</span></span>

## <a name="error-codes"></a><span data-ttu-id="785ca-114">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="785ca-114">Error codes</span></span>



| <span data-ttu-id="785ca-115">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="785ca-115">Name/value</span></span>                                                                                                                                                            | <span data-ttu-id="785ca-116">Significato</span><span class="sxs-lookup"><span data-stu-id="785ca-116">Meaning</span></span>                                                                   |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="785ca-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="785ca-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                               | <span data-ttu-id="785ca-118">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="785ca-118">The operation was successful.</span></span><br/>                                  |
| <dl> <span data-ttu-id="785ca-119"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="785ca-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                 | <span data-ttu-id="785ca-120">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="785ca-120">The parameter is **NULL**.</span></span><br/>                                     |
| <dl> <span data-ttu-id="785ca-121"><dt>E \_ ERRORE</dt> <dt>0x80004005</dt></span><span class="sxs-lookup"><span data-stu-id="785ca-121"><dt>E\_FAIL</dt> <dt>0x80004005</dt></span></span> </dl>                    | <span data-ttu-id="785ca-122">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="785ca-122">An unexpected error has occurred.</span></span><br/>                              |
| <dl> <span data-ttu-id="785ca-123"><dt>Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="785ca-123"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>         | <span data-ttu-id="785ca-124">Impossibile trovare la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="785ca-124">The virtual machine could not be found.</span></span><br/>                        |
| <dl> <span data-ttu-id="785ca-125"><dt>Macchina virtuale \_ Unità E 0xA0040502 \_ \_ non valide</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="785ca-125"><dt>VM\_E\_DRIVE\_INVALID</dt> <dt>0xA0040502</dt></span></span> </dl>      | <span data-ttu-id="785ca-126">Il percorso del bus per questa unità non è valido.</span><span class="sxs-lookup"><span data-stu-id="785ca-126">The bus location for this drive is not valid.</span></span><br/>                  |
| <dl> <span data-ttu-id="785ca-127"><dt>Macchina virtuale \_ E \_ media \_ di \_ tipo errato</dt> <dt>0xA00400728</dt></span><span class="sxs-lookup"><span data-stu-id="785ca-127"><dt>VM\_E\_MEDIA\_WRONG\_TYPE</dt> <dt>0xA00400728</dt></span></span> </dl> | <span data-ttu-id="785ca-128">Il supporto acquisito da questa unità DVD non è un file di immagine ISO.</span><span class="sxs-lookup"><span data-stu-id="785ca-128">The media captured by this DVD drive is not an ISO image file.</span></span><br/> |
| <dl> <span data-ttu-id="785ca-129"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="785ca-129"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>         | <span data-ttu-id="785ca-130">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="785ca-130">An unexpected error has occurred.</span></span><br/>                              |



## <a name="requirements"></a><span data-ttu-id="785ca-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="785ca-131">Requirements</span></span>



| <span data-ttu-id="785ca-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="785ca-132">Requirement</span></span> | <span data-ttu-id="785ca-133">Valore</span><span class="sxs-lookup"><span data-stu-id="785ca-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="785ca-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="785ca-134">Minimum supported client</span></span><br/> | <span data-ttu-id="785ca-135">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="785ca-135">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="785ca-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="785ca-136">Minimum supported server</span></span><br/> | <span data-ttu-id="785ca-137">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="785ca-137">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="785ca-138">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="785ca-138">End of client support</span></span><br/>    | <span data-ttu-id="785ca-139">Windows 7</span><span class="sxs-lookup"><span data-stu-id="785ca-139">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="785ca-140">Prodotto</span><span class="sxs-lookup"><span data-stu-id="785ca-140">Product</span></span><br/>                  | <span data-ttu-id="785ca-141">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="785ca-141">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="785ca-142">Intestazione</span><span class="sxs-lookup"><span data-stu-id="785ca-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="785ca-143"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="785ca-143"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="785ca-144">IID</span><span class="sxs-lookup"><span data-stu-id="785ca-144">IID</span></span><br/>                      | <span data-ttu-id="785ca-145">IID \_ IVMDVDDrive è definito come b96328f6-6732-437D-a00d-ffa47e43971c</span><span class="sxs-lookup"><span data-stu-id="785ca-145">IID\_IVMDVDDrive is defined as b96328f6-6732-437d-a00d-ffa47e43971c</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="785ca-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="785ca-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="785ca-147">**IVMDVDDrive**</span><span class="sxs-lookup"><span data-stu-id="785ca-147">**IVMDVDDrive**</span></span>](ivmdvddrive.md)
</dt> </dl>

 

