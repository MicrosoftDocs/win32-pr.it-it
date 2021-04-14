---
title: Metodo Convert IVMHardDisk (VPCCOMInterfaces. h)
description: Converte un disco rigido virtuale a dimensione fissa in un disco rigido virtuale a espansione dinamica o converte un disco rigido virtuale a espansione dinamica in un disco rigido virtuale a dimensione fissa.
ms.assetid: 0dee802a-1cac-499e-918a-7dbb6c98415f
keywords:
- Convertire il metodo Virtual PC
- Convert Method Virtual PC, interfaccia IVMHardDisk
- Interfaccia IVMHardDisk Virtual PC, Convert (metodo)
topic_type:
- apiref
api_name:
- IVMHardDisk.Convert
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2398cf4a2f3b366709c009885bf2c2767828fee1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478803"
---
# <a name="ivmharddiskconvert-method"></a><span data-ttu-id="3363f-106">Metodo IVMHardDisk:: Convert</span><span class="sxs-lookup"><span data-stu-id="3363f-106">IVMHardDisk::Convert method</span></span>

<span data-ttu-id="3363f-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="3363f-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="3363f-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="3363f-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="3363f-109">Converte un disco rigido virtuale a dimensione fissa in un disco rigido virtuale a espansione dinamica o converte un disco rigido virtuale a espansione dinamica in un disco rigido virtuale a dimensione fissa.</span><span class="sxs-lookup"><span data-stu-id="3363f-109">Converts a fixed-size virtual hard disk to a dynamically expanding virtual hard disk or converts a dynamically expanding virtual hard disk to a fixed-size virtual hard disk.</span></span>

## <a name="syntax"></a><span data-ttu-id="3363f-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3363f-110">Syntax</span></span>


```C++
HRESULT Convert(
  [in]          BSTR           convertedDiskImagePath,
  [in]          VMHardDiskType convertedDiskImageType,
  [out, retval] IVMTask        **convertTask
);
```



## <a name="parameters"></a><span data-ttu-id="3363f-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="3363f-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3363f-112">*convertedDiskImagePath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3363f-112">*convertedDiskImagePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3363f-113">Percorso del file di immagine del disco di destinazione.</span><span class="sxs-lookup"><span data-stu-id="3363f-113">The path to the target disk image file.</span></span>

</dd> <dt>

<span data-ttu-id="3363f-114">*convertedDiskImageType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3363f-114">*convertedDiskImageType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3363f-115">Tipo di immagine del disco di destinazione.</span><span class="sxs-lookup"><span data-stu-id="3363f-115">The type of the target disk image.</span></span> <span data-ttu-id="3363f-116">Per un elenco di valori, vedere [**VMHardDiskType**](vmharddisktype.md).</span><span class="sxs-lookup"><span data-stu-id="3363f-116">For a list of values, see [**VMHardDiskType**](vmharddisktype.md).</span></span>

</dd> <dt>

<span data-ttu-id="3363f-117">*convertTask* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="3363f-117">*convertTask* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="3363f-118">Oggetto [**IVMTask**](ivmtask.md) utilizzato per tenere traccia del completamento del processo di conversione.</span><span class="sxs-lookup"><span data-stu-id="3363f-118">An [**IVMTask**](ivmtask.md) object that is used to track the completion of the conversion process.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3363f-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3363f-119">Return value</span></span>

<span data-ttu-id="3363f-120">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="3363f-120">This method can return one of these values.</span></span>



| <span data-ttu-id="3363f-121">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="3363f-121">Return code/value</span></span>                                                                                                                                                                              | <span data-ttu-id="3363f-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3363f-122">Description</span></span>                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3363f-123"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="3363f-123"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                    | <span data-ttu-id="3363f-124">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="3363f-124">The operation was successful.</span></span><br/>                                                                                                        |
| <dl> <span data-ttu-id="3363f-125"><dt>**E \_**</dt> <dt>0x80000003</dt> INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="3363f-125"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                                   | <span data-ttu-id="3363f-126">Il parametro *convertedDiskImagePath* è vuoto o manca l'estensione VHD sul nome del file.</span><span class="sxs-lookup"><span data-stu-id="3363f-126">The *convertedDiskImagePath* parameter is empty or missing the .vhd extension on the file name.</span></span><br/>                                      |
| <dl> <span data-ttu-id="3363f-127"><dt>**E \_ PUNTATORE**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="3363f-127"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                      | <span data-ttu-id="3363f-128">Un parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="3363f-128">A parameter is **NULL**.</span></span><br/>                                                                                                             |
| <dl> <span data-ttu-id="3363f-129"><dt>**HRESULT \_ DA \_ Win32 ( \_ percorso errore \_ non \_ trovato)**</dt> <dt>0 x 80070003</dt></span><span class="sxs-lookup"><span data-stu-id="3363f-129"><dt>**HRESULT\_FROM\_WIN32(ERROR\_PATH\_NOT\_FOUND)**</dt> <dt>0x80070003</dt></span></span> </dl>   | <span data-ttu-id="3363f-130">Il sistema non è in grado di trovare il percorso specificato dal parametro *convertedDiskImagePath* .</span><span class="sxs-lookup"><span data-stu-id="3363f-130">The system cannot find the path specified by the *convertedDiskImagePath* parameter.</span></span><br/>                                                 |
| <dl> <span data-ttu-id="3363f-131"><dt>**HRESULT \_ DA \_ Win32 (errore \_ nome non valido \_ )**</dt> <dt>0x8007007b</dt></span><span class="sxs-lookup"><span data-stu-id="3363f-131"><dt>**HRESULT\_FROM\_WIN32(ERROR\_INVALID\_NAME)**</dt> <dt>0x8007007b</dt></span></span> </dl>      | <span data-ttu-id="3363f-132">Il parametro *convertedDiskImagePath* contiene un carattere non valido (uno di " \* ? <>/ \| ": ").</span><span class="sxs-lookup"><span data-stu-id="3363f-132">The *convertedDiskImagePath* parameter contains an invalid character (one of "\*?<>/\|":").</span></span><br/>                                    |
| <dl> <span data-ttu-id="3363f-133"><dt>**HRESULT \_ DA \_ Win32 (errore \_ \_ percorso errato)**</dt> <dt>0x800700a1</dt></span><span class="sxs-lookup"><span data-stu-id="3363f-133"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BAD\_PATHNAME)**</dt> <dt>0x800700a1</dt></span></span> </dl>      | <span data-ttu-id="3363f-134">Il parametro *convertedDiskImagePath* specifica un percorso vuoto o relativo.</span><span class="sxs-lookup"><span data-stu-id="3363f-134">The *convertedDiskImagePath* parameter specifies an empty or relative path.</span></span> <span data-ttu-id="3363f-135">È necessario specificare un percorso assoluto.</span><span class="sxs-lookup"><span data-stu-id="3363f-135">An absolute path is required.</span></span><br/>                            |
| <dl> <span data-ttu-id="3363f-136"><dt>**HRESULT \_ Da \_ Win32 (overflow del buffer degli errori \_ \_ )**</dt> <dt>0x8007006f</dt></span><span class="sxs-lookup"><span data-stu-id="3363f-136"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BUFFER\_OVERFLOW)**</dt> <dt>0x8007006f</dt></span></span> </dl>   | <span data-ttu-id="3363f-137">Il percorso specificato dal parametro *convertedDiskImagePath* è troppo lungo.</span><span class="sxs-lookup"><span data-stu-id="3363f-137">The path specified by the *convertedDiskImagePath* parameter is too long.</span></span> <span data-ttu-id="3363f-138">Il percorso deve essere minore di **Max \_ path** (260) caratteri.</span><span class="sxs-lookup"><span data-stu-id="3363f-138">The path must be less than **MAX\_PATH** (260) characters.</span></span><br/> |
| <dl> <span data-ttu-id="3363f-139"><dt>**HRESULT \_ Da \_ Win32 (violazione della condivisione degli errori \_ \_ )**</dt> <dt>0x80070020</dt></span><span class="sxs-lookup"><span data-stu-id="3363f-139"><dt>**HRESULT\_FROM\_WIN32(ERROR\_SHARING\_VIOLATION)**</dt> <dt>0x80070020</dt></span></span> </dl> | <span data-ttu-id="3363f-140">Il disco rigido virtuale a cui fa riferimento questo oggetto è in uso o l'elemento padre di questo disco rigido virtuale è in uso.</span><span class="sxs-lookup"><span data-stu-id="3363f-140">Either the virtual hard disk referenced by this object is in use or the parent of this virtual hard disk is in use.</span></span><br/>                  |
| <dl> <span data-ttu-id="3363f-141"><dt>**HRESULT \_ DA \_ Win32 (errore \_ disco \_ completo)**</dt> <dt>0x80070070</dt></span><span class="sxs-lookup"><span data-stu-id="3363f-141"><dt>**HRESULT\_FROM\_WIN32(ERROR\_DISK\_FULL)**</dt> <dt>0x80070070</dt></span></span> </dl>         | <span data-ttu-id="3363f-142">Il volume host non dispone di spazio sufficiente per la conversione del disco rigido virtuale.</span><span class="sxs-lookup"><span data-stu-id="3363f-142">The host volume does not have enough space to convert this virtual hard disk.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="3363f-143"><dt>**HRESULT \_ DA \_ Win32 (errore \_ già \_ esistente)**</dt> <dt>0x800700b7</dt></span><span class="sxs-lookup"><span data-stu-id="3363f-143"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ALREADY\_EXISTS)**</dt> <dt>0x800700b7</dt></span></span> </dl>    | <span data-ttu-id="3363f-144">Il file a cui fa riferimento il parametro *convertedDiskImagePath* esiste già.</span><span class="sxs-lookup"><span data-stu-id="3363f-144">The file referenced by the *convertedDiskImagePath* parameter already exists.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="3363f-145"><dt>**Macchina virtuale \_ E \_ \_ tipo di \_ immagine \_ HD errato**</dt> <dt>0xA004067B</dt></span><span class="sxs-lookup"><span data-stu-id="3363f-145"><dt>**VM\_E\_WRONG\_HD\_IMAGE\_TYPE**</dt> <dt>0xA004067B</dt></span></span> </dl>                   | <span data-ttu-id="3363f-146">Il parametro *convertedDiskImagePath* deve essere **VmDiskType \_ Dynamic** o **vmDiskType \_ FixedSize**.</span><span class="sxs-lookup"><span data-stu-id="3363f-146">The *convertedDiskImagePath* parameter must be either **vmDiskType\_Dynamic** or **vmDiskType\_FixedSize**.</span></span><br/>                          |
| <dl> <span data-ttu-id="3363f-147"><dt>**Macchina virtuale \_ E \_ \_ \_ file HD non valido**</dt> <dt>0xA0040682</dt></span><span class="sxs-lookup"><span data-stu-id="3363f-147"><dt>**VM\_E\_INVALID\_HD\_FILE**</dt> <dt>0xA0040682</dt></span></span> </dl>                        | <span data-ttu-id="3363f-148">L'immagine del disco rigido virtuale a cui fa riferimento questo oggetto [**IVMHardDisk**](ivmharddisk.md) non sembra essere un'immagine valida.</span><span class="sxs-lookup"><span data-stu-id="3363f-148">The virtual hard disk image referenced by this [**IVMHardDisk**](ivmharddisk.md) object does not seem to be a valid image.</span></span><br/>          |
| <dl> <span data-ttu-id="3363f-149"><dt>**Macchina virtuale \_ \_Percorso padre \_ E \_ non \_ trovato**</dt> <dt>0xA0040677</dt></span><span class="sxs-lookup"><span data-stu-id="3363f-149"><dt>**VM\_E\_PARENT\_PATH\_NOT\_FOUND**</dt> <dt>0xA0040677</dt></span></span> </dl>                 | <span data-ttu-id="3363f-150">L'elemento padre del disco rigido virtuale a cui fa riferimento questo oggetto non esiste.</span><span class="sxs-lookup"><span data-stu-id="3363f-150">The parent of the virtual hard disk referenced by this object does not exist.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="3363f-151"><dt>**Macchina virtuale \_ E \_ \_ chiusura \_ dell'app**</dt> <dt>0xA0040209</dt></span><span class="sxs-lookup"><span data-stu-id="3363f-151"><dt>**VM\_E\_APP\_SHUTTING\_DOWN**</dt> <dt>0xA0040209</dt></span></span> </dl>                      | <span data-ttu-id="3363f-152">Non è possibile convertire l'immagine del disco rigido virtuale perché è in corso la chiusura dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="3363f-152">The virtual hard disk image cannot be converted because the application is shutting down.</span></span><br/>                                            |
| <dl> <span data-ttu-id="3363f-153"><dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="3363f-153"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                              | <span data-ttu-id="3363f-154">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="3363f-154">An unexpected error has occurred.</span></span><br/>                                                                                                    |



 

## <a name="remarks"></a><span data-ttu-id="3363f-155">Commenti</span><span class="sxs-lookup"><span data-stu-id="3363f-155">Remarks</span></span>

<span data-ttu-id="3363f-156">Il file di origine viene lasciato intatto dopo il processo di conversione.</span><span class="sxs-lookup"><span data-stu-id="3363f-156">The source file is left intact after the conversion process.</span></span>

## <a name="requirements"></a><span data-ttu-id="3363f-157">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3363f-157">Requirements</span></span>



| <span data-ttu-id="3363f-158">Requisito</span><span class="sxs-lookup"><span data-stu-id="3363f-158">Requirement</span></span> | <span data-ttu-id="3363f-159">Valore</span><span class="sxs-lookup"><span data-stu-id="3363f-159">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="3363f-160">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3363f-160">Minimum supported client</span></span><br/> | <span data-ttu-id="3363f-161">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="3363f-161">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3363f-162">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3363f-162">Minimum supported server</span></span><br/> | <span data-ttu-id="3363f-163">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="3363f-163">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="3363f-164">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="3363f-164">End of client support</span></span><br/>    | <span data-ttu-id="3363f-165">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3363f-165">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="3363f-166">Prodotto</span><span class="sxs-lookup"><span data-stu-id="3363f-166">Product</span></span><br/>                  | <span data-ttu-id="3363f-167">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="3363f-167">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="3363f-168">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3363f-168">Header</span></span><br/>                   | <dl> <span data-ttu-id="3363f-169"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="3363f-169"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="3363f-170">IID</span><span class="sxs-lookup"><span data-stu-id="3363f-170">IID</span></span><br/>                      | <span data-ttu-id="3363f-171">IID \_ IVMHardDisk è definito come ffa14ae6-48f5-42A4-8a22-186f2e5c7db0</span><span class="sxs-lookup"><span data-stu-id="3363f-171">IID\_IVMHardDisk is defined as ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="3363f-172">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3363f-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3363f-173">**IVMHardDisk**</span><span class="sxs-lookup"><span data-stu-id="3363f-173">**IVMHardDisk**</span></span>](ivmharddisk.md)
</dt> </dl>

 

