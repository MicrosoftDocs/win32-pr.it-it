---
title: Metodo Compact IVMHardDisk (VPCCOMInterfaces. h)
description: Compatta un'immagine del disco rigido virtuale ad espansione dinamica.
ms.assetid: bd3ec493-1bc0-4c28-8b41-56beac3d0d6d
keywords:
- Metodo Compact Virtual PC
- Metodo Compact Virtual PC, interfaccia IVMHardDisk
- Interfaccia IVMHardDisk Virtual PC, metodo Compact
topic_type:
- apiref
api_name:
- IVMHardDisk.Compact
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51b28b47709fdf956b679a4f16c50adde4a1b335
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743247"
---
# <a name="ivmharddiskcompact-method"></a><span data-ttu-id="bcbd4-106">Metodo IVMHardDisk:: Compact</span><span class="sxs-lookup"><span data-stu-id="bcbd4-106">IVMHardDisk::Compact method</span></span>

<span data-ttu-id="bcbd4-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="bcbd4-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="bcbd4-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="bcbd4-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="bcbd4-109">Compatta un'immagine del disco rigido virtuale ad espansione dinamica.</span><span class="sxs-lookup"><span data-stu-id="bcbd4-109">Compacts a dynamically expanding virtual hard disk image.</span></span>

## <a name="syntax"></a><span data-ttu-id="bcbd4-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bcbd4-110">Syntax</span></span>


```C++
HRESULT Compact(
  [out, retval] IVMTask **compactTask
);
```



## <a name="parameters"></a><span data-ttu-id="bcbd4-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="bcbd4-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bcbd4-112">*compactTask* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="bcbd4-112">*compactTask* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="bcbd4-113">Oggetto [**IVMTask**](ivmtask.md) utilizzato per tenere traccia del processo di compattazione.</span><span class="sxs-lookup"><span data-stu-id="bcbd4-113">An [**IVMTask**](ivmtask.md) object that is used to track the completion the compaction process.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bcbd4-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bcbd4-114">Return value</span></span>

<span data-ttu-id="bcbd4-115">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="bcbd4-115">This method can return one of these values.</span></span>



| <span data-ttu-id="bcbd4-116">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="bcbd4-116">Return code/value</span></span>                                                                                                                                                                              | <span data-ttu-id="bcbd4-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bcbd4-117">Description</span></span>                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="bcbd4-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="bcbd4-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                    | <span data-ttu-id="bcbd4-119">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="bcbd4-119">The operation was successful.</span></span><br/>                                                                                                        |
| <dl> <span data-ttu-id="bcbd4-120"><dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="bcbd4-120"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                              | <span data-ttu-id="bcbd4-121">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="bcbd4-121">An unexpected error has occurred.</span></span><br/>                                                                                                    |
| <dl> <span data-ttu-id="bcbd4-122"><dt>**E \_ PUNTATORE**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="bcbd4-122"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                      | <span data-ttu-id="bcbd4-123">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="bcbd4-123">The parameter is **NULL**.</span></span><br/>                                                                                                           |
| <dl> <span data-ttu-id="bcbd4-124"><dt>**HRESULT \_ Da \_ Win32 (violazione della condivisione degli errori \_ \_ )**</dt> <dt>0x80070020</dt></span><span class="sxs-lookup"><span data-stu-id="bcbd4-124"><dt>**HRESULT\_FROM\_WIN32(ERROR\_SHARING\_VIOLATION)**</dt> <dt>0x80070020</dt></span></span> </dl> | <span data-ttu-id="bcbd4-125">L'immagine del disco rigido virtuale a cui fa riferimento questo oggetto [**IVMHardDisk**](ivmharddisk.md) è in uso.</span><span class="sxs-lookup"><span data-stu-id="bcbd4-125">The virtual hard disk image referenced by this [**IVMHardDisk**](ivmharddisk.md) object is in use.</span></span><br/>                                  |
| <dl> <span data-ttu-id="bcbd4-126"><dt>**HRESULT \_ DA \_ Win32 (errore \_ disco \_ completo)**</dt> <dt>0x80070070</dt></span><span class="sxs-lookup"><span data-stu-id="bcbd4-126"><dt>**HRESULT\_FROM\_WIN32(ERROR\_DISK\_FULL)**</dt> <dt>0x80070070</dt></span></span> </dl>         | <span data-ttu-id="bcbd4-127">Il volume host non dispone di spazio sufficiente per la creazione di un file temporaneo necessario per la compattazione di questa immagine del disco rigido virtuale.</span><span class="sxs-lookup"><span data-stu-id="bcbd4-127">The host volume does not have enough space to create a temporary file needed for the compaction of this virtual hard disk image.</span></span><br/>     |
| <dl> <span data-ttu-id="bcbd4-128"><dt>**Macchina virtuale \_ E \_ \_ chiusura \_ dell'app**</dt> <dt>0xA0040209</dt></span><span class="sxs-lookup"><span data-stu-id="bcbd4-128"><dt>**VM\_E\_APP\_SHUTTING\_DOWN**</dt> <dt>0xA0040209</dt></span></span> </dl>                      | <span data-ttu-id="bcbd4-129">L'immagine del disco rigido virtuale non può essere compattata perché è in corso la chiusura dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="bcbd4-129">The virtual hard disk image cannot be compacted because the application is shutting down.</span></span><br/>                                            |
| <dl> <span data-ttu-id="bcbd4-130"><dt>**Macchina virtuale \_ E \_ file \_ \_**</dt> di sola lettura <dt>0xA004067A</dt></span><span class="sxs-lookup"><span data-stu-id="bcbd4-130"><dt>**VM\_E\_FILE\_READ\_ONLY**</dt> <dt>0xA004067A</dt></span></span> </dl>                         | <span data-ttu-id="bcbd4-131">L'immagine del disco rigido virtuale a cui fa riferimento questo oggetto [**IVMHardDisk**](ivmharddisk.md) è contrassegnata come di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="bcbd4-131">The virtual hard disk image referenced by this [**IVMHardDisk**](ivmharddisk.md) object is marked as read only.</span></span><br/>                     |
| <dl> <span data-ttu-id="bcbd4-132"><dt>**Macchina virtuale \_ E \_ \_ tipo di \_ immagine \_ HD errato**</dt> <dt>0xA004067B</dt></span><span class="sxs-lookup"><span data-stu-id="bcbd4-132"><dt>**VM\_E\_WRONG\_HD\_IMAGE\_TYPE**</dt> <dt>0xA004067B</dt></span></span> </dl>                   | <span data-ttu-id="bcbd4-133">L'immagine del disco rigido virtuale a cui fa riferimento questo oggetto [**IVMHardDisk**](ivmharddisk.md) deve essere un tipo di immagine **vmDiskTypeDynamic** .</span><span class="sxs-lookup"><span data-stu-id="bcbd4-133">The virtual hard disk image referenced by this [**IVMHardDisk**](ivmharddisk.md) object must be a **vmDiskTypeDynamic** image type.</span></span><br/> |
| <dl> <span data-ttu-id="bcbd4-134"><dt>**Macchina virtuale \_ E \_ \_ \_ file HD non valido**</dt> <dt>0xA0040682</dt></span><span class="sxs-lookup"><span data-stu-id="bcbd4-134"><dt>**VM\_E\_INVALID\_HD\_FILE**</dt> <dt>0xA0040682</dt></span></span> </dl>                        | <span data-ttu-id="bcbd4-135">L'immagine del disco rigido virtuale a cui fa riferimento questo oggetto [**IVMHardDisk**](ivmharddisk.md) non sembra essere un'immagine valida.</span><span class="sxs-lookup"><span data-stu-id="bcbd4-135">The virtual hard disk image referenced by this [**IVMHardDisk**](ivmharddisk.md) object does not seem to be a valid image.</span></span><br/>          |



 

## <a name="remarks"></a><span data-ttu-id="bcbd4-136">Commenti</span><span class="sxs-lookup"><span data-stu-id="bcbd4-136">Remarks</span></span>

<span data-ttu-id="bcbd4-137">Per comprimere un'immagine del disco rigido a espansione dinamica, lo spazio disponibile nell'immagine del disco deve prima essere azzerato.</span><span class="sxs-lookup"><span data-stu-id="bcbd4-137">To compact a dynamically expanding hard disk image, free space on the disk image should first be zeroed.</span></span>

## <a name="requirements"></a><span data-ttu-id="bcbd4-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bcbd4-138">Requirements</span></span>



| <span data-ttu-id="bcbd4-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="bcbd4-139">Requirement</span></span> | <span data-ttu-id="bcbd4-140">Valore</span><span class="sxs-lookup"><span data-stu-id="bcbd4-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="bcbd4-141">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bcbd4-141">Minimum supported client</span></span><br/> | <span data-ttu-id="bcbd4-142">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="bcbd4-142">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="bcbd4-143">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bcbd4-143">Minimum supported server</span></span><br/> | <span data-ttu-id="bcbd4-144">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="bcbd4-144">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="bcbd4-145">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="bcbd4-145">End of client support</span></span><br/>    | <span data-ttu-id="bcbd4-146">Windows 7</span><span class="sxs-lookup"><span data-stu-id="bcbd4-146">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="bcbd4-147">Prodotto</span><span class="sxs-lookup"><span data-stu-id="bcbd4-147">Product</span></span><br/>                  | <span data-ttu-id="bcbd4-148">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="bcbd4-148">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="bcbd4-149">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bcbd4-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="bcbd4-150"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="bcbd4-150"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="bcbd4-151">IID</span><span class="sxs-lookup"><span data-stu-id="bcbd4-151">IID</span></span><br/>                      | <span data-ttu-id="bcbd4-152">IID \_ IVMHardDisk è definito come ffa14ae6-48f5-42A4-8a22-186f2e5c7db0</span><span class="sxs-lookup"><span data-stu-id="bcbd4-152">IID\_IVMHardDisk is defined as ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="bcbd4-153">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bcbd4-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bcbd4-154">**IVMHardDisk**</span><span class="sxs-lookup"><span data-stu-id="bcbd4-154">**IVMHardDisk**</span></span>](ivmharddisk.md)
</dt> </dl>

 

