---
title: Metodo Merge IVMHardDisk (VPCCOMInterfaces. h)
description: Unisce un disco rigido virtuale differenze con l'immagine del disco padre.
ms.assetid: e2aca4d3-79c1-416a-b135-f4680c03d200
keywords:
- Metodo Merge Virtual PC
- Metodo Merge Virtual PC, interfaccia IVMHardDisk
- Interfaccia IVMHardDisk Virtual PC, metodo Merge
topic_type:
- apiref
api_name:
- IVMHardDisk.Merge
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb5e4b32cb1df2f754463cee7f8275b00f86513b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964414"
---
# <a name="ivmharddiskmerge-method"></a><span data-ttu-id="66bbf-106">Metodo IVMHardDisk:: merge</span><span class="sxs-lookup"><span data-stu-id="66bbf-106">IVMHardDisk::Merge method</span></span>

<span data-ttu-id="66bbf-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="66bbf-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="66bbf-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="66bbf-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="66bbf-109">Unisce un disco rigido virtuale differenze con l'immagine del disco padre.</span><span class="sxs-lookup"><span data-stu-id="66bbf-109">Merges a differencing virtual hard disk with its parent disk image.</span></span>

## <a name="syntax"></a><span data-ttu-id="66bbf-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="66bbf-110">Syntax</span></span>


```C++
HRESULT Merge(
  [out, retval] IVMTask **mergeTask
);
```



## <a name="parameters"></a><span data-ttu-id="66bbf-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="66bbf-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66bbf-112">*mergeTask* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="66bbf-112">*mergeTask* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="66bbf-113">Oggetto [**IVMTask**](ivmtask.md) utilizzato per tenere traccia del completamento del processo di Unione.</span><span class="sxs-lookup"><span data-stu-id="66bbf-113">An [**IVMTask**](ivmtask.md) object that is used to track the completion of the merging process.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66bbf-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="66bbf-114">Return value</span></span>

<span data-ttu-id="66bbf-115">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="66bbf-115">This method can return one of these values.</span></span>



| <span data-ttu-id="66bbf-116">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="66bbf-116">Return code/value</span></span>                                                                                                                                                                              | <span data-ttu-id="66bbf-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="66bbf-117">Description</span></span>                                                                                                                                                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="66bbf-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="66bbf-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                    | <span data-ttu-id="66bbf-119">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="66bbf-119">The operation was successful.</span></span><br/>                                                                                                                                                                                          |
| <dl> <span data-ttu-id="66bbf-120"><dt>**E \_ PUNTATORE**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="66bbf-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                      | <span data-ttu-id="66bbf-121">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="66bbf-121">The parameter is **NULL**.</span></span><br/>                                                                                                                                                                                             |
| <dl> <span data-ttu-id="66bbf-122"><dt>**HRESULT \_ Da \_ Win32 (violazione della condivisione degli errori \_ \_ )**</dt> <dt>0x80070020</dt></span><span class="sxs-lookup"><span data-stu-id="66bbf-122"><dt>**HRESULT\_FROM\_WIN32(ERROR\_SHARING\_VIOLATION)**</dt> <dt>0x80070020</dt></span></span> </dl> | <span data-ttu-id="66bbf-123">L'immagine del disco rigido virtuale a cui fa riferimento questo oggetto [**IVMHardDisk**](ivmharddisk.md) è in uso o l'elemento padre di questa immagine del disco rigido virtuale è in uso.</span><span class="sxs-lookup"><span data-stu-id="66bbf-123">The virtual hard disk image referenced by this [**IVMHardDisk**](ivmharddisk.md) object is in use or the parent of this virtual hard disk image is in use.</span></span> <span data-ttu-id="66bbf-124">In alternativa, è possibile che le immagini del disco rigido facciano parte di uno stato salvato.</span><span class="sxs-lookup"><span data-stu-id="66bbf-124">Or, these hard disk images could be part of a saved state.</span></span><br/> |
| <dl> <span data-ttu-id="66bbf-125"><dt>**Macchina virtuale \_ E \_ \_ tipo di \_ immagine \_ HD errato**</dt> <dt>0xA004067B</dt></span><span class="sxs-lookup"><span data-stu-id="66bbf-125"><dt>**VM\_E\_WRONG\_HD\_IMAGE\_TYPE**</dt> <dt>0xA004067B</dt></span></span> </dl>                   | <span data-ttu-id="66bbf-126">L'immagine del disco rigido virtuale a cui fa riferimento questo oggetto [**IVMHardDisk**](ivmharddisk.md) deve essere un'immagine del disco differenze.</span><span class="sxs-lookup"><span data-stu-id="66bbf-126">The virtual hard disk image referenced by this [**IVMHardDisk**](ivmharddisk.md) object must be a differencing disk image.</span></span><br/>                                                                                            |
| <dl> <span data-ttu-id="66bbf-127"><dt>**Macchina virtuale \_ E \_ file \_ \_**</dt> di sola lettura <dt>0xA004067A</dt></span><span class="sxs-lookup"><span data-stu-id="66bbf-127"><dt>**VM\_E\_FILE\_READ\_ONLY**</dt> <dt>0xA004067A</dt></span></span> </dl>                         | <span data-ttu-id="66bbf-128">L'elemento padre dell'immagine del disco rigido virtuale a cui fa riferimento questo oggetto [**IVMHardDisk**](ivmharddisk.md) è contrassegnato come di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="66bbf-128">The parent of virtual hard disk image referenced by this [**IVMHardDisk**](ivmharddisk.md) object is marked as read only.</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="66bbf-129"><dt>**Macchina virtuale \_ \_Percorso padre \_ E \_ non \_ trovato**</dt> <dt>0xA0040677</dt></span><span class="sxs-lookup"><span data-stu-id="66bbf-129"><dt>**VM\_E\_PARENT\_PATH\_NOT\_FOUND**</dt> <dt>0xA0040677</dt></span></span> </dl>                 | <span data-ttu-id="66bbf-130">L'elemento padre del disco rigido virtuale a cui fa riferimento questo oggetto [**IVMHardDisk**](ivmharddisk.md) non esiste.</span><span class="sxs-lookup"><span data-stu-id="66bbf-130">The parent of the virtual hard disk referenced by this [**IVMHardDisk**](ivmharddisk.md) object does not exist.</span></span><br/>                                                                                                       |
| <dl> <span data-ttu-id="66bbf-131"><dt>**Macchina virtuale \_ E \_ \_ chiusura \_ dell'app**</dt> <dt>0xA0040209</dt></span><span class="sxs-lookup"><span data-stu-id="66bbf-131"><dt>**VM\_E\_APP\_SHUTTING\_DOWN**</dt> <dt>0xA0040209</dt></span></span> </dl>                      | <span data-ttu-id="66bbf-132">Non è possibile eseguire il merge dell'immagine del disco rigido virtuale perché è in corso la chiusura dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="66bbf-132">The virtual hard disk image cannot be merged because the application is shutting down.</span></span><br/>                                                                                                                                 |
| <dl> <span data-ttu-id="66bbf-133"><dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="66bbf-133"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                              | <span data-ttu-id="66bbf-134">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="66bbf-134">An unexpected error has occurred.</span></span><br/>                                                                                                                                                                                      |



 

## <a name="requirements"></a><span data-ttu-id="66bbf-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="66bbf-135">Requirements</span></span>



| <span data-ttu-id="66bbf-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="66bbf-136">Requirement</span></span> | <span data-ttu-id="66bbf-137">Valore</span><span class="sxs-lookup"><span data-stu-id="66bbf-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="66bbf-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="66bbf-138">Minimum supported client</span></span><br/> | <span data-ttu-id="66bbf-139">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="66bbf-139">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="66bbf-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="66bbf-140">Minimum supported server</span></span><br/> | <span data-ttu-id="66bbf-141">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="66bbf-141">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="66bbf-142">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="66bbf-142">End of client support</span></span><br/>    | <span data-ttu-id="66bbf-143">Windows 7</span><span class="sxs-lookup"><span data-stu-id="66bbf-143">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="66bbf-144">Prodotto</span><span class="sxs-lookup"><span data-stu-id="66bbf-144">Product</span></span><br/>                  | <span data-ttu-id="66bbf-145">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="66bbf-145">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="66bbf-146">Intestazione</span><span class="sxs-lookup"><span data-stu-id="66bbf-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="66bbf-147"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="66bbf-147"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="66bbf-148">IID</span><span class="sxs-lookup"><span data-stu-id="66bbf-148">IID</span></span><br/>                      | <span data-ttu-id="66bbf-149">IID \_ IVMHardDisk è definito come ffa14ae6-48f5-42A4-8a22-186f2e5c7db0</span><span class="sxs-lookup"><span data-stu-id="66bbf-149">IID\_IVMHardDisk is defined as ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="66bbf-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="66bbf-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66bbf-151">**IVMHardDisk**</span><span class="sxs-lookup"><span data-stu-id="66bbf-151">**IVMHardDisk**</span></span>](ivmharddisk.md)
</dt> </dl>

 

