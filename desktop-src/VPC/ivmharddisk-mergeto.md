---
title: Metodo IVMHardDisk MergeTo (VPCCOMInterfaces. h)
description: Unisce un disco rigido virtuale differenze con tutti i relativi elementi padre.
ms.assetid: 3c63f892-7c05-4ed6-a59a-914a921ec391
keywords:
- Metodo MergeTo Virtual PC
- Metodo MergeTo Virtual PC, interfaccia IVMHardDisk
- Interfaccia IVMHardDisk Virtual PC, metodo MergeTo
topic_type:
- apiref
api_name:
- IVMHardDisk.MergeTo
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13d0db44388c8ee021fa8cc8c8fdbfe2c434833f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119962"
---
# <a name="ivmharddiskmergeto-method"></a><span data-ttu-id="27814-106">Metodo IVMHardDisk:: MergeTo</span><span class="sxs-lookup"><span data-stu-id="27814-106">IVMHardDisk::MergeTo method</span></span>

<span data-ttu-id="27814-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="27814-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="27814-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="27814-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="27814-109">Unisce un disco rigido virtuale differenze con tutti i relativi elementi padre (fino al disco rigido virtuale padre radice) in un nuovo file di disco rigido.</span><span class="sxs-lookup"><span data-stu-id="27814-109">Merges a differencing virtual hard disk with all of its parents (up to and including the root parent virtual hard disk) to a new hard disk file.</span></span>

## <a name="syntax"></a><span data-ttu-id="27814-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="27814-110">Syntax</span></span>


```C++
HRESULT MergeTo(
  [in]          BSTR           newDiskImagePath,
  [in]          VMHardDiskType newDiskImageType,
  [out, retval] IVMTask        **mergeTask
);
```



## <a name="parameters"></a><span data-ttu-id="27814-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="27814-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27814-112">*newDiskImagePath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="27814-112">*newDiskImagePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27814-113">Percorso della nuova immagine del disco di destinazione in cui verranno unite le immagini del disco selezionate.</span><span class="sxs-lookup"><span data-stu-id="27814-113">The path to the new target disk image where the selected disk images will be merged.</span></span>

</dd> <dt>

<span data-ttu-id="27814-114">*newDiskImageType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="27814-114">*newDiskImageType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27814-115">Tipo di nuova immagine del disco di destinazione.</span><span class="sxs-lookup"><span data-stu-id="27814-115">The type of new target disk image.</span></span> <span data-ttu-id="27814-116">I tipi di immagine consentiti per la nuova immagine del disco di destinazione sono **vmDiskType \_ Dynamic** e **vmDiskType \_ FixedSize**.</span><span class="sxs-lookup"><span data-stu-id="27814-116">The image types allowed for the new target disk image are **vmDiskType\_Dynamic** and **vmDiskType\_FixedSize**.</span></span> <span data-ttu-id="27814-117">Per ulteriori informazioni, vedere [**VMHardDiskType**](vmharddisktype.md).</span><span class="sxs-lookup"><span data-stu-id="27814-117">For more information, see [**VMHardDiskType**](vmharddisktype.md).</span></span>

</dd> <dt>

<span data-ttu-id="27814-118">*mergeTask* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="27814-118">*mergeTask* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="27814-119">Oggetto [**IVMTask**](ivmtask.md) utilizzato per tenere traccia del completamento del processo di Unione.</span><span class="sxs-lookup"><span data-stu-id="27814-119">An [**IVMTask**](ivmtask.md) object that is used to track the completion of the merging process.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27814-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="27814-120">Return value</span></span>

<span data-ttu-id="27814-121">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="27814-121">This method can return one of these values.</span></span>



| <span data-ttu-id="27814-122">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="27814-122">Return code/value</span></span>                                                                                                                                                                              | <span data-ttu-id="27814-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="27814-123">Description</span></span>                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="27814-124"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="27814-124"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                    | <span data-ttu-id="27814-125">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="27814-125">The operation was successful.</span></span><br/>                                                                                                                                                                                                                                                                      |
| <dl> <span data-ttu-id="27814-126"><dt>**E \_ PUNTATORE**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="27814-126"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                      | <span data-ttu-id="27814-127">Un parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="27814-127">A parameter is **NULL**.</span></span><br/>                                                                                                                                                                                                                                                                           |
| <dl> <span data-ttu-id="27814-128"><dt>**E \_**</dt> <dt>0x80000003</dt> INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="27814-128"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                                   | <span data-ttu-id="27814-129">Il parametro *newDiskImagePath* è vuoto.</span><span class="sxs-lookup"><span data-stu-id="27814-129">The *newDiskImagePath* parameter is empty.</span></span><br/>                                                                                                                                                                                                                                                         |
| <dl> <span data-ttu-id="27814-130"><dt>**HRESULT \_ DA \_ Win32 (file degli errori \_ \_ non \_ trovato)**</dt> <dt>0x80070002</dt></span><span class="sxs-lookup"><span data-stu-id="27814-130"><dt>**HRESULT\_FROM\_WIN32(ERROR\_FILE\_NOT\_FOUND)**</dt> <dt>0x80070002</dt></span></span> </dl>   | <span data-ttu-id="27814-131">Il sistema non è in grado di trovare il file specificato dal parametro *newDiskImagePath* .</span><span class="sxs-lookup"><span data-stu-id="27814-131">The system cannot find the file specified by the *newDiskImagePath* parameter.</span></span><br/>                                                                                                                                                                                                                     |
| <dl> <span data-ttu-id="27814-132"><dt>**HRESULT \_ DA \_ Win32 ( \_ percorso errore \_ non \_ trovato)**</dt> <dt>0 x 80070003</dt></span><span class="sxs-lookup"><span data-stu-id="27814-132"><dt>**HRESULT\_FROM\_WIN32(ERROR\_PATH\_NOT\_FOUND)**</dt> <dt>0x80070003</dt></span></span> </dl>   | <span data-ttu-id="27814-133">Il sistema non è in grado di trovare il percorso specificato dal parametro *newDiskImagePath* .</span><span class="sxs-lookup"><span data-stu-id="27814-133">The system cannot find the path specified by the *newDiskImagePath* parameter.</span></span><br/>                                                                                                                                                                                                                     |
| <dl> <span data-ttu-id="27814-134"><dt>**HRESULT \_ DA \_ Win32 (errore \_ nome non valido \_ )**</dt> <dt>0x8007007b</dt></span><span class="sxs-lookup"><span data-stu-id="27814-134"><dt>**HRESULT\_FROM\_WIN32(ERROR\_INVALID\_NAME)**</dt> <dt>0x8007007b</dt></span></span> </dl>      | <span data-ttu-id="27814-135">Il parametro *newDiskImagePath* contiene un carattere non valido (uno dei seguenti: " \* ? <>/ \| ": ").</span><span class="sxs-lookup"><span data-stu-id="27814-135">The *newDiskImagePath* parameter contains an invalid character (one of the following: "\*?<>/\|":").</span></span><br/>                                                                                                                                                                                         |
| <dl> <span data-ttu-id="27814-136"><dt>**HRESULT \_ DA \_ Win32 (errore \_ \_ percorso errato)**</dt> <dt>0x800700a1</dt></span><span class="sxs-lookup"><span data-stu-id="27814-136"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BAD\_PATHNAME)**</dt> <dt>0x800700a1</dt></span></span> </dl>      | <span data-ttu-id="27814-137">Il parametro *newDiskImagePath* specifica un percorso vuoto o relativo.</span><span class="sxs-lookup"><span data-stu-id="27814-137">The *newDiskImagePath* parameter specifies an empty or relative path.</span></span> <span data-ttu-id="27814-138">È necessario specificare un percorso assoluto.</span><span class="sxs-lookup"><span data-stu-id="27814-138">An absolute path is required.</span></span><br/>                                                                                                                                                                                                |
| <dl> <span data-ttu-id="27814-139"><dt>**HRESULT \_ Da \_ Win32 (overflow del buffer degli errori \_ \_ )**</dt> <dt>0x8007006f</dt></span><span class="sxs-lookup"><span data-stu-id="27814-139"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BUFFER\_OVERFLOW)**</dt> <dt>0x8007006f</dt></span></span> </dl>   | <span data-ttu-id="27814-140">Il percorso specificato dal parametro *newDiskImagePath* è troppo lungo.</span><span class="sxs-lookup"><span data-stu-id="27814-140">The path specified by the *newDiskImagePath* parameter is too long.</span></span> <span data-ttu-id="27814-141">Il percorso deve essere composto da meno di 260 caratteri.</span><span class="sxs-lookup"><span data-stu-id="27814-141">The path must be less than 260 characters.</span></span><br/>                                                                                                                                                                                     |
| <dl> <span data-ttu-id="27814-142"><dt>**HRESULT \_ Da \_ Win32 (violazione della condivisione degli errori \_ \_ )**</dt> <dt>0x80070020</dt></span><span class="sxs-lookup"><span data-stu-id="27814-142"><dt>**HRESULT\_FROM\_WIN32(ERROR\_SHARING\_VIOLATION)**</dt> <dt>0x80070020</dt></span></span> </dl> | <span data-ttu-id="27814-143">Il disco rigido virtuale a cui fa riferimento questo oggetto è in uso o l'elemento padre di questo disco rigido virtuale è in uso.</span><span class="sxs-lookup"><span data-stu-id="27814-143">Either the virtual hard disk referenced by this object is in use or the parent of this virtual hard disk is in use.</span></span><br/>                                                                                                                                                                                |
| <dl> <span data-ttu-id="27814-144"><dt>**Macchina virtuale \_ E \_ \_ tipo di \_ immagine \_ HD errato**</dt> <dt>0xA004067B</dt></span><span class="sxs-lookup"><span data-stu-id="27814-144"><dt>**VM\_E\_WRONG\_HD\_IMAGE\_TYPE**</dt> <dt>0xA004067B</dt></span></span> </dl>                   | <span data-ttu-id="27814-145">Questo errore è causato dal fatto che l'immagine del disco rigido virtuale a cui fa riferimento questo oggetto [**IVMHardDisk**](ivmharddisk.md) non è un'immagine del disco differenze o perché il parametro *newDiskImageType* non è uno dei valori accettati, **vmDiskType \_ Dynamic** o **vmDiskType \_ FixedSize**.</span><span class="sxs-lookup"><span data-stu-id="27814-145">This error is caused either because the virtual hard disk image referenced by this [**IVMHardDisk**](ivmharddisk.md) object is not a differencing disk image or because the parameter *newDiskImageType* is not one of the accepted values, **vmDiskType\_Dynamic** or **vmDiskType\_FixedSize**.</span></span><br/> |
| <dl> <span data-ttu-id="27814-146"><dt>**HRESULT \_ DA \_ Win32 (errore \_ già \_ esistente)**</dt> <dt>0x800700b7</dt></span><span class="sxs-lookup"><span data-stu-id="27814-146"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ALREADY\_EXISTS)**</dt> <dt>0x800700b7</dt></span></span> </dl>    | <span data-ttu-id="27814-147">Il file a cui fa riferimento il parametro *newDiskImagePath* esiste già.</span><span class="sxs-lookup"><span data-stu-id="27814-147">The file referenced by the *newDiskImagePath* parameter already exists.</span></span><br/>                                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="27814-148"><dt>**HRESULT \_ DA \_ Win32 (errore \_ disco \_ completo)**</dt> <dt>0x80070070</dt></span><span class="sxs-lookup"><span data-stu-id="27814-148"><dt>**HRESULT\_FROM\_WIN32(ERROR\_DISK\_FULL)**</dt> <dt>0x80070070</dt></span></span> </dl>         | <span data-ttu-id="27814-149">Il volume host non dispone di spazio sufficiente per unire questo disco rigido virtuale.</span><span class="sxs-lookup"><span data-stu-id="27814-149">The host volume does not have enough space to merge this virtual hard disk.</span></span><br/>                                                                                                                                                                                                                        |
| <dl> <span data-ttu-id="27814-150"><dt>**Macchina virtuale \_ \_Percorso padre \_ E \_ non \_ trovato**</dt> <dt>0xA0040677</dt></span><span class="sxs-lookup"><span data-stu-id="27814-150"><dt>**VM\_E\_PARENT\_PATH\_NOT\_FOUND**</dt> <dt>0xA0040677</dt></span></span> </dl>                 | <span data-ttu-id="27814-151">L'elemento padre del disco rigido virtuale a cui fa riferimento questo oggetto non esiste.</span><span class="sxs-lookup"><span data-stu-id="27814-151">The parent of the virtual hard disk referenced by this object does not exist.</span></span><br/>                                                                                                                                                                                                                      |
| <dl> <span data-ttu-id="27814-152"><dt>**Macchina virtuale \_ E \_ \_ chiusura \_ dell'app**</dt> <dt>0xA0040209</dt></span><span class="sxs-lookup"><span data-stu-id="27814-152"><dt>**VM\_E\_APP\_SHUTTING\_DOWN**</dt> <dt>0xA0040209</dt></span></span> </dl>                      | <span data-ttu-id="27814-153">Non è possibile eseguire il merge dell'immagine del disco rigido virtuale perché è in corso la chiusura dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="27814-153">The virtual hard disk image cannot be merged because the application is shutting down.</span></span><br/>                                                                                                                                                                                                             |
| <dl> <span data-ttu-id="27814-154"><dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="27814-154"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                              | <span data-ttu-id="27814-155">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="27814-155">An unexpected error has occurred.</span></span><br/>                                                                                                                                                                                                                                                                  |



 

## <a name="requirements"></a><span data-ttu-id="27814-156">Requisiti</span><span class="sxs-lookup"><span data-stu-id="27814-156">Requirements</span></span>



| <span data-ttu-id="27814-157">Requisito</span><span class="sxs-lookup"><span data-stu-id="27814-157">Requirement</span></span> | <span data-ttu-id="27814-158">Valore</span><span class="sxs-lookup"><span data-stu-id="27814-158">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="27814-159">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="27814-159">Minimum supported client</span></span><br/> | <span data-ttu-id="27814-160">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="27814-160">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="27814-161">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="27814-161">Minimum supported server</span></span><br/> | <span data-ttu-id="27814-162">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="27814-162">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="27814-163">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="27814-163">End of client support</span></span><br/>    | <span data-ttu-id="27814-164">Windows 7</span><span class="sxs-lookup"><span data-stu-id="27814-164">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="27814-165">Prodotto</span><span class="sxs-lookup"><span data-stu-id="27814-165">Product</span></span><br/>                  | <span data-ttu-id="27814-166">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="27814-166">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="27814-167">Intestazione</span><span class="sxs-lookup"><span data-stu-id="27814-167">Header</span></span><br/>                   | <dl> <span data-ttu-id="27814-168"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="27814-168"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="27814-169">IID</span><span class="sxs-lookup"><span data-stu-id="27814-169">IID</span></span><br/>                      | <span data-ttu-id="27814-170">IID \_ IVMHardDisk è definito come ffa14ae6-48f5-42A4-8a22-186f2e5c7db0</span><span class="sxs-lookup"><span data-stu-id="27814-170">IID\_IVMHardDisk is defined as ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="27814-171">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="27814-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27814-172">**IVMHardDisk**</span><span class="sxs-lookup"><span data-stu-id="27814-172">**IVMHardDisk**</span></span>](ivmharddisk.md)
</dt> </dl>

 

