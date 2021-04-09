---
title: Proprietà padre IVMHardDisk (VPCCOMInterfaces. h)
description: Elemento padre del disco rigido virtuale differenze.
ms.assetid: 9a400fa0-ee0d-4474-a410-82756ea544fe
keywords:
- Proprietà padre Virtual PC
- Proprietà padre Virtual PC, interfaccia IVMHardDisk
- Interfaccia IVMHardDisk Virtual PC, proprietà Parent
topic_type:
- apiref
api_name:
- IVMHardDisk.Parent
- IVMHardDisk.get_Parent
- IVMHardDisk.put_Parent
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af9487750b67fc133f4b15f15050a74638f3d0f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963727"
---
# <a name="ivmharddiskparent-property"></a><span data-ttu-id="62e66-106">IVMHardDisk::P proprietà adre</span><span class="sxs-lookup"><span data-stu-id="62e66-106">IVMHardDisk::Parent property</span></span>

<span data-ttu-id="62e66-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="62e66-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="62e66-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="62e66-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="62e66-109">Recupera e imposta l'elemento padre del disco rigido virtuale differenze.</span><span class="sxs-lookup"><span data-stu-id="62e66-109">Retrieves and sets the parent of the differencing virtual hard disk.</span></span>

<span data-ttu-id="62e66-110">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="62e66-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="62e66-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="62e66-111">Syntax</span></span>


```C++
HRESULT put_Parent(
  [in]          IVMHardDisk *parent
);

HRESULT get_Parent(
  [out, retval] IVMHardDisk **parent
);
```



## <a name="property-value"></a><span data-ttu-id="62e66-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="62e66-112">Property value</span></span>

<span data-ttu-id="62e66-113">Imposta l'oggetto [**IVMHardDisk**](ivmharddisk.md) associato all'immagine del disco rigido padre.</span><span class="sxs-lookup"><span data-stu-id="62e66-113">Sets the [**IVMHardDisk**](ivmharddisk.md) object associated with the parent hard disk image.</span></span>

## <a name="error-codes"></a><span data-ttu-id="62e66-114">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="62e66-114">Error codes</span></span>



| <span data-ttu-id="62e66-115">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="62e66-115">Name/value</span></span>                                                                                                                                                                               | <span data-ttu-id="62e66-116">Significato</span><span class="sxs-lookup"><span data-stu-id="62e66-116">Meaning</span></span>                                                                                                                                                                                                                                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="62e66-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="62e66-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="62e66-118">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="62e66-118">The operation was successful.</span></span><br/>                                                                                                                                                                                                                                              |
| <dl> <span data-ttu-id="62e66-119"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="62e66-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="62e66-120">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="62e66-120">The parameter is **NULL**.</span></span><br/>                                                                                                                                                                                                                                                 |
| <dl> <span data-ttu-id="62e66-121"><dt>S \_ FALSE</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="62e66-121"><dt>S\_FALSE</dt> <dt>1</dt></span></span> </dl>                                               | <span data-ttu-id="62e66-122">Non si tratta di un disco rigido differenze, pertanto non dispone di un elemento padre.</span><span class="sxs-lookup"><span data-stu-id="62e66-122">This is not a differencing hard disk, so it has no parent.</span></span><br/>                                                                                                                                                                                                                 |
| <dl> <span data-ttu-id="62e66-123"><dt>HRESULT \_ DA \_ Win32 (file degli errori \_ \_ non \_ trovato)</dt> <dt>0x80070002</dt></span><span class="sxs-lookup"><span data-stu-id="62e66-123"><dt>HRESULT\_FROM\_WIN32(ERROR\_FILE\_NOT\_FOUND)</dt> <dt>0x80070002</dt></span></span> </dl> | <span data-ttu-id="62e66-124">Il sistema non è riuscito a trovare il file del disco rigido virtuale padre.</span><span class="sxs-lookup"><span data-stu-id="62e66-124">The system could not find the parent virtual hard disk file.</span></span><br/>                                                                                                                                                                                                               |
| <dl> <span data-ttu-id="62e66-125"><dt>HRESULT \_ DA \_ Win32 ( \_ percorso errore \_ non \_ trovato)</dt> <dt>0 x 80070003</dt></span><span class="sxs-lookup"><span data-stu-id="62e66-125"><dt>HRESULT\_FROM\_WIN32(ERROR\_PATH\_NOT\_FOUND)</dt> <dt>0x80070003</dt></span></span> </dl> | <span data-ttu-id="62e66-126">Il sistema non è riuscito a trovare il percorso del file del disco rigido virtuale padre.</span><span class="sxs-lookup"><span data-stu-id="62e66-126">The system could not find the path to the parent virtual hard disk file.</span></span><br/>                                                                                                                                                                                                   |
| <dl> <span data-ttu-id="62e66-127"><dt>Macchina virtuale \_ E \_ \_ immagine HD \_ \_ non riuscita</dt> <dt>0xA004067C</dt></span><span class="sxs-lookup"><span data-stu-id="62e66-127"><dt>VM\_E\_HD\_IMAGE\_OPEN\_FAIL</dt> <dt>0xA004067C</dt></span></span> </dl>                  | <span data-ttu-id="62e66-128">Si è verificato un errore durante il tentativo di aprire il file di immagine del disco rigido corrente.</span><span class="sxs-lookup"><span data-stu-id="62e66-128">An error occurred while attempting to open the current hard disk image file.</span></span><br/>                                                                                                                                                                                               |
| <dl> <span data-ttu-id="62e66-129"><dt>Macchina virtuale \_ E \_ \_ \_ accesso alle immagini HD</dt> <dt>0xA0040681</dt></span><span class="sxs-lookup"><span data-stu-id="62e66-129"><dt>VM\_E\_HD\_IMAGE\_ACCESS</dt> <dt>0xA0040681</dt></span></span> </dl>                      | <span data-ttu-id="62e66-130">Si è verificato un errore durante il tentativo di accesso al file di immagine del disco rigido corrente.</span><span class="sxs-lookup"><span data-stu-id="62e66-130">An error occurred while attempting to access the current hard disk image file.</span></span><br/>                                                                                                                                                                                             |
| <dl> <span data-ttu-id="62e66-131"><dt>Macchina virtuale \_ \_ID figlio padre E non \_ \_ \_ corrispondente</dt> <dt>0xA0040685</dt></span><span class="sxs-lookup"><span data-stu-id="62e66-131"><dt>VM\_E\_PARENT\_CHILD\_ID\_MISMATCH</dt> <dt>0xA0040685</dt></span></span> </dl>            | <span data-ttu-id="62e66-132">L'immagine del disco rigido virtuale individuata dal parametro *padre* non ha lo stesso ID dell'immagine del disco figlio.</span><span class="sxs-lookup"><span data-stu-id="62e66-132">The virtual hard disk image located by the *parent* parameter does not have the same ID as the child disk image.</span></span> <span data-ttu-id="62e66-133">Verificare che l'immagine del disco rigido virtuale padre individuata dal parametro *padre* sia la stessa immagine usata per creare l'immagine del disco rigido virtuale differenze.</span><span class="sxs-lookup"><span data-stu-id="62e66-133">Make sure the parent virtual hard disk image located by the *parent* parameter is the same image used to create the differencing virtual hard disk image.</span></span><br/> |
| <dl> <span data-ttu-id="62e66-134"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="62e66-134"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="62e66-135">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="62e66-135">An unexpected error has occurred.</span></span><br/>                                                                                                                                                                                                                                          |



## <a name="remarks"></a><span data-ttu-id="62e66-136">Commenti</span><span class="sxs-lookup"><span data-stu-id="62e66-136">Remarks</span></span>

<span data-ttu-id="62e66-137">Questa proprietà è valida solo con le immagini del disco rigido differenze.</span><span class="sxs-lookup"><span data-stu-id="62e66-137">This property is only valid with differencing hard disk images.</span></span>

## <a name="requirements"></a><span data-ttu-id="62e66-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="62e66-138">Requirements</span></span>



| <span data-ttu-id="62e66-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="62e66-139">Requirement</span></span> | <span data-ttu-id="62e66-140">Valore</span><span class="sxs-lookup"><span data-stu-id="62e66-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="62e66-141">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="62e66-141">Minimum supported client</span></span><br/> | <span data-ttu-id="62e66-142">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="62e66-142">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="62e66-143">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="62e66-143">Minimum supported server</span></span><br/> | <span data-ttu-id="62e66-144">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="62e66-144">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="62e66-145">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="62e66-145">End of client support</span></span><br/>    | <span data-ttu-id="62e66-146">Windows 7</span><span class="sxs-lookup"><span data-stu-id="62e66-146">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="62e66-147">Prodotto</span><span class="sxs-lookup"><span data-stu-id="62e66-147">Product</span></span><br/>                  | <span data-ttu-id="62e66-148">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="62e66-148">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="62e66-149">Intestazione</span><span class="sxs-lookup"><span data-stu-id="62e66-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="62e66-150"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="62e66-150"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="62e66-151">IID</span><span class="sxs-lookup"><span data-stu-id="62e66-151">IID</span></span><br/>                      | <span data-ttu-id="62e66-152">IID \_ IVMHardDisk è definito come ffa14ae6-48f5-42A4-8a22-186f2e5c7db0</span><span class="sxs-lookup"><span data-stu-id="62e66-152">IID\_IVMHardDisk is defined as ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="62e66-153">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="62e66-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62e66-154">**IVMHardDisk**</span><span class="sxs-lookup"><span data-stu-id="62e66-154">**IVMHardDisk**</span></span>](ivmharddisk.md)
</dt> </dl>

 

