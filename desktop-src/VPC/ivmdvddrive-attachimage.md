---
title: Metodo IVMDVDDrive AttachImage (VPCCOMInterfaces. h)
description: Connette un'immagine ISO all'unità DVD all'interno della macchina virtuale.
ms.assetid: 08947898-ca3f-41b6-97a3-52dc6977fc6d
keywords:
- Metodo AttachImage Virtual PC
- Metodo AttachImage Virtual PC, interfaccia IVMDVDDrive
- Interfaccia IVMDVDDrive Virtual PC, metodo AttachImage
topic_type:
- apiref
api_name:
- IVMDVDDrive.AttachImage
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58204545e21bd7dbf48d21acbc232b9fc5d1e3b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400870"
---
# <a name="ivmdvddriveattachimage-method"></a><span data-ttu-id="7c787-106">Metodo IVMDVDDrive:: AttachImage</span><span class="sxs-lookup"><span data-stu-id="7c787-106">IVMDVDDrive::AttachImage method</span></span>

<span data-ttu-id="7c787-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="7c787-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="7c787-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="7c787-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="7c787-109">Connette un'immagine ISO all'unità DVD all'interno della macchina virtuale (VM).</span><span class="sxs-lookup"><span data-stu-id="7c787-109">Attaches an ISO image to the DVD drive within the virtual machine (VM).</span></span>

## <a name="syntax"></a><span data-ttu-id="7c787-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7c787-110">Syntax</span></span>


```C++
HRESULT AttachImage(
  [in] BSTR imagePath
);
```



## <a name="parameters"></a><span data-ttu-id="7c787-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="7c787-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c787-112">*imagePath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7c787-112">*imagePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c787-113">Percorso completo dell'immagine ISO da collegare.</span><span class="sxs-lookup"><span data-stu-id="7c787-113">The full path to the ISO image that is to be attached.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c787-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7c787-114">Return value</span></span>

<span data-ttu-id="7c787-115">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="7c787-115">This method can return one of these values.</span></span>



| <span data-ttu-id="7c787-116">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="7c787-116">Return code/value</span></span>                                                                                                                                                    | <span data-ttu-id="7c787-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7c787-117">Description</span></span>                                                                                                  |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7c787-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="7c787-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                          | <span data-ttu-id="7c787-119">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="7c787-119">The operation was successful.</span></span><br/>                                                                     |
| <dl> <span data-ttu-id="7c787-120"><dt>**E \_**</dt> <dt>0x80000003</dt> INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="7c787-120"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>         | <span data-ttu-id="7c787-121">Il parametro *imagePath* è una directory.</span><span class="sxs-lookup"><span data-stu-id="7c787-121">The *imagePath* parameter is a directory.</span></span><br/>                                                         |
| <dl> <span data-ttu-id="7c787-122"><dt>**E \_ PUNTATORE**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="7c787-122"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>            | <span data-ttu-id="7c787-123">Il parametro *imagePath* è **null**.</span><span class="sxs-lookup"><span data-stu-id="7c787-123">The *imagePath* parameter is **NULL**.</span></span><br/>                                                            |
| <dl> <span data-ttu-id="7c787-124"><dt>**Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="7c787-124"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>    | <span data-ttu-id="7c787-125">Non è stato possibile trovare la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7c787-125">The VM could not be found.</span></span><br/>                                                                        |
| <dl> <span data-ttu-id="7c787-126"><dt>**Macchina virtuale \_ \_Unità E \_ in \_ use**</dt> <dt>0xA0040727</dt></span><span class="sxs-lookup"><span data-stu-id="7c787-126"><dt>**VM\_E\_DRIVE\_IN\_USE**</dt> <dt>0xA0040727</dt></span></span> </dl> | <span data-ttu-id="7c787-127">Un'unità DVD o un'immagine ISO host è già collegata a questa unità.</span><span class="sxs-lookup"><span data-stu-id="7c787-127">A host DVD drive or ISO image is already attached to this drive.</span></span><br/>                                  |
| <dl> <span data-ttu-id="7c787-128"><dt>**Macchina virtuale \_ Unità E 0xA0040502 \_ \_ non valide**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="7c787-128"><dt>**VM\_E\_DRIVE\_INVALID**</dt> <dt>0xA0040502</dt></span></span> </dl> | <span data-ttu-id="7c787-129">Il percorso del bus per questa unità non è valido o l'unità non sembra essere un'unità DVD valida.</span><span class="sxs-lookup"><span data-stu-id="7c787-129">The bus location for this drive is invalid, or the drive does not appear to be a valid DVD drive.</span></span><br/> |
| <dl> <span data-ttu-id="7c787-130"><dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="7c787-130"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>    | <span data-ttu-id="7c787-131">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="7c787-131">An unexpected error has occurred.</span></span><br/>                                                                 |



 

## <a name="requirements"></a><span data-ttu-id="7c787-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7c787-132">Requirements</span></span>



| <span data-ttu-id="7c787-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c787-133">Requirement</span></span> | <span data-ttu-id="7c787-134">Valore</span><span class="sxs-lookup"><span data-stu-id="7c787-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c787-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7c787-135">Minimum supported client</span></span><br/> | <span data-ttu-id="7c787-136">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="7c787-136">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7c787-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7c787-137">Minimum supported server</span></span><br/> | <span data-ttu-id="7c787-138">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="7c787-138">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="7c787-139">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="7c787-139">End of client support</span></span><br/>    | <span data-ttu-id="7c787-140">Windows 7</span><span class="sxs-lookup"><span data-stu-id="7c787-140">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="7c787-141">Prodotto</span><span class="sxs-lookup"><span data-stu-id="7c787-141">Product</span></span><br/>                  | <span data-ttu-id="7c787-142">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="7c787-142">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="7c787-143">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7c787-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c787-144"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c787-144"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="7c787-145">IID</span><span class="sxs-lookup"><span data-stu-id="7c787-145">IID</span></span><br/>                      | <span data-ttu-id="7c787-146">IID \_ IVMDVDDrive è definito come b96328f6-6732-437D-a00d-ffa47e43971c</span><span class="sxs-lookup"><span data-stu-id="7c787-146">IID\_IVMDVDDrive is defined as b96328f6-6732-437d-a00d-ffa47e43971c</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="7c787-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7c787-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c787-148">**IVMDVDDrive**</span><span class="sxs-lookup"><span data-stu-id="7c787-148">**IVMDVDDrive**</span></span>](ivmdvddrive.md)
</dt> </dl>

 

