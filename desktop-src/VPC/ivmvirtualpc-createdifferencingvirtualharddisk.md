---
title: Metodo IVMVirtualPC CreateDifferencingVirtualHardDisk (VPCCOMInterfaces. h)
description: Crea un disco rigido virtuale differenze.
ms.assetid: 6a33aa6f-a0e8-45d8-bdc1-0864561db162
keywords:
- Metodo CreateDifferencingVirtualHardDisk Virtual PC
- Metodo CreateDifferencingVirtualHardDisk Virtual PC, interfaccia IVMVirtualPC
- Interfaccia IVMVirtualPC Virtual PC, metodo CreateDifferencingVirtualHardDisk
topic_type:
- apiref
api_name:
- IVMVirtualPC.CreateDifferencingVirtualHardDisk
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2bab178d64008b236988bfb723bd75a09a7edaa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302337"
---
# <a name="ivmvirtualpccreatedifferencingvirtualharddisk-method"></a><span data-ttu-id="8bdf2-106">Metodo IVMVirtualPC:: CreateDifferencingVirtualHardDisk</span><span class="sxs-lookup"><span data-stu-id="8bdf2-106">IVMVirtualPC::CreateDifferencingVirtualHardDisk method</span></span>

<span data-ttu-id="8bdf2-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="8bdf2-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="8bdf2-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="8bdf2-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="8bdf2-109">Crea un disco rigido virtuale differenze.</span><span class="sxs-lookup"><span data-stu-id="8bdf2-109">Creates a differencing virtual hard disk.</span></span>

## <a name="syntax"></a><span data-ttu-id="8bdf2-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8bdf2-110">Syntax</span></span>


```C++
HRESULT CreateDifferencingVirtualHardDisk(
  [in]          BSTR    imagePath,
  [in]          BSTR    parentPath,
  [out, retval] IVMTask **diskTask
);
```



## <a name="parameters"></a><span data-ttu-id="8bdf2-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="8bdf2-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8bdf2-112">*imagePath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8bdf2-112">*imagePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8bdf2-113">Percorso del nuovo file di immagine del disco.</span><span class="sxs-lookup"><span data-stu-id="8bdf2-113">The path to the new disk image file.</span></span> <span data-ttu-id="8bdf2-114">Se non esiste, verrà creata la cartella che lo contiene.</span><span class="sxs-lookup"><span data-stu-id="8bdf2-114">The containing folder will be created if it does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="8bdf2-115">*ParentPath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8bdf2-115">*parentPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8bdf2-116">Percorso del file di immagine del disco padre.</span><span class="sxs-lookup"><span data-stu-id="8bdf2-116">The path to the parent disk image file.</span></span>

</dd> <dt>

<span data-ttu-id="8bdf2-117">*diskTask* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="8bdf2-117">*diskTask* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="8bdf2-118">Oggetto [**IVMTask**](ivmtask.md) utilizzato per tenere traccia della creazione dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="8bdf2-118">An [**IVMTask**](ivmtask.md) object that is used to track the creation of the image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8bdf2-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8bdf2-119">Return value</span></span>

<span data-ttu-id="8bdf2-120">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="8bdf2-120">This method can return one of these values.</span></span>



| <span data-ttu-id="8bdf2-121">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="8bdf2-121">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="8bdf2-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8bdf2-122">Description</span></span>                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8bdf2-123"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="8bdf2-123"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="8bdf2-124">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="8bdf2-124">The operation was successful.</span></span><br/>                                                                                                                                                                                                       |
| <dl> <span data-ttu-id="8bdf2-125"><dt>**E \_ PUNTATORE**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="8bdf2-125"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="8bdf2-126">Un parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="8bdf2-126">A parameter is **NULL**.</span></span><br/>                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="8bdf2-127"><dt>**HRESULT \_ DA \_ Win32 ( \_ percorso errore \_ non \_ trovato)**</dt> <dt>0 x 80070003</dt></span><span class="sxs-lookup"><span data-stu-id="8bdf2-127"><dt>**HRESULT\_FROM\_WIN32(ERROR\_PATH\_NOT\_FOUND)**</dt> <dt>0x80070003</dt></span></span> </dl> | <span data-ttu-id="8bdf2-128">Il sistema non è in grado di trovare il percorso specificato dal parametro *imagePath* o *ParentPath* .</span><span class="sxs-lookup"><span data-stu-id="8bdf2-128">The system cannot find the path specified by the *imagePath* or *parentPath* parameter.</span></span><br/>                                                                                                                                             |
| <dl> <span data-ttu-id="8bdf2-129"><dt>**HRESULT \_ DA \_ Win32 (errore \_ unità non valida \_ )**</dt> <dt>0x8007000f</dt></span><span class="sxs-lookup"><span data-stu-id="8bdf2-129"><dt>**HRESULT\_FROM\_WIN32(ERROR\_INVALID\_DRIVE)**</dt> <dt>0x8007000f</dt></span></span> </dl>   | <span data-ttu-id="8bdf2-130">Il file specificato dal parametro *imagePath* si trova su un CD-ROM o un DVD-ROM.</span><span class="sxs-lookup"><span data-stu-id="8bdf2-130">The file specified by the *imagePath* parameter is on a CD-ROM or DVD-ROM.</span></span><br/>                                                                                                                                                          |
| <dl> <span data-ttu-id="8bdf2-131"><dt>**HRESULT \_ DA \_ Win32 (errore \_ nome non valido \_ )**</dt> <dt>0x8007007b</dt></span><span class="sxs-lookup"><span data-stu-id="8bdf2-131"><dt>**HRESULT\_FROM\_WIN32(ERROR\_INVALID\_NAME)**</dt> <dt>0x8007007b</dt></span></span> </dl>    | <span data-ttu-id="8bdf2-132">Il parametro *imagePath* o *ParentPath* contiene un carattere non valido (uno di " \* ?: <>/ \| " ").</span><span class="sxs-lookup"><span data-stu-id="8bdf2-132">The *imagePath* or *parentPath* parameter contains an invalid character (one of "\*?:<>/\|"").</span></span><br/>                                                                                                                                |
| <dl> <span data-ttu-id="8bdf2-133"><dt>**HRESULT \_ DA \_ Win32 (errore \_ \_ percorso errato)**</dt> <dt>0x800700a1</dt></span><span class="sxs-lookup"><span data-stu-id="8bdf2-133"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BAD\_PATHNAME)**</dt> <dt>0x800700a1</dt></span></span> </dl>    | <span data-ttu-id="8bdf2-134">Il parametro *imagePath* e *ParentPath* specifica un percorso vuoto o relativo.</span><span class="sxs-lookup"><span data-stu-id="8bdf2-134">Both the *imagePath* and *parentPath* parameter specifies an empty or relative path.</span></span> <span data-ttu-id="8bdf2-135">Almeno uno dei parametri deve essere un percorso assoluto.</span><span class="sxs-lookup"><span data-stu-id="8bdf2-135">At least one of the parameters must be an absolute path.</span></span><br/>                                                                                       |
| <dl> <span data-ttu-id="8bdf2-136"><dt>**HRESULT \_ Da \_ Win32 (overflow del buffer degli errori \_ \_ )**</dt> <dt>0x8007006f</dt></span><span class="sxs-lookup"><span data-stu-id="8bdf2-136"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BUFFER\_OVERFLOW)**</dt> <dt>0x8007006f</dt></span></span> </dl> | <span data-ttu-id="8bdf2-137">Il percorso specificato dai parametri *imagePath* o *ParentPath* è troppo lungo.</span><span class="sxs-lookup"><span data-stu-id="8bdf2-137">The path specified by the *imagePath* or *parentPath* parameters is too long.</span></span> <span data-ttu-id="8bdf2-138">La lunghezza del percorso deve essere inferiore a 260 caratteri.</span><span class="sxs-lookup"><span data-stu-id="8bdf2-138">The length of the path must be less than 260 characters.</span></span><br/>                                                                                              |
| <dl> <span data-ttu-id="8bdf2-139"><dt>**HRESULT \_ DA \_ Win32 (errore \_ già \_ esistente)**</dt> <dt>0x800700b7</dt></span><span class="sxs-lookup"><span data-stu-id="8bdf2-139"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ALREADY\_EXISTS)**</dt> <dt>0x800700b7</dt></span></span> </dl>  | <span data-ttu-id="8bdf2-140">Il file a cui fa riferimento il parametro *imagePath* esiste già.</span><span class="sxs-lookup"><span data-stu-id="8bdf2-140">The file referenced by the *imagePath* parameter already exists.</span></span><br/>                                                                                                                                                                    |
| <dl> <span data-ttu-id="8bdf2-141"><dt>**HRESULT \_ DA \_ Win32 (errore \_ disco \_ completo)**</dt> <dt>0x80070070</dt></span><span class="sxs-lookup"><span data-stu-id="8bdf2-141"><dt>**HRESULT\_FROM\_WIN32(ERROR\_DISK\_FULL)**</dt> <dt>0x80070070</dt></span></span> </dl>       | <span data-ttu-id="8bdf2-142">Per l'immagine del disco rigido virtuale a espansione dinamica sono necessari almeno 8 MB di spazio sul volume host.</span><span class="sxs-lookup"><span data-stu-id="8bdf2-142">The dynamically expanding virtual hard disk image needs at least 8 MB free on the host volume.</span></span><br/>                                                                                                                                      |
| <dl> <span data-ttu-id="8bdf2-143"><dt>**Macchina virtuale \_ Dimensioni dell'immagine E 0xA0040683 \_ \_ \_ troppo \_ grandi**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="8bdf2-143"><dt>**VM\_E\_IMAGE\_SIZE\_TOO\_LARGE**</dt> <dt>0xA0040683</dt></span></span> </dl>                | <span data-ttu-id="8bdf2-144">Le *dimensioni* del parametro devono essere minori di 2.088.960 MB.</span><span class="sxs-lookup"><span data-stu-id="8bdf2-144">The parameter *size* must be less than 2,088,960 MB.</span></span> <span data-ttu-id="8bdf2-145">Se il formato è FAT16, le dimensioni devono essere minori di 2000 MB.</span><span class="sxs-lookup"><span data-stu-id="8bdf2-145">If the format is FAT16, then size must be less than 2000 MB.</span></span><br/>                                                                                                                   |
| <dl> <span data-ttu-id="8bdf2-146"><dt>**Macchina virtuale \_ \_Dimensioni immagine E \_ dimensioni \_ troppo \_ ridotte**</dt> <dt>0xA0040684</dt></span><span class="sxs-lookup"><span data-stu-id="8bdf2-146"><dt>**VM\_E\_IMAGE\_SIZE\_TOO\_SMALL**</dt> <dt>0xA0040684</dt></span></span> </dl>                | <span data-ttu-id="8bdf2-147">Le immagini del disco rigido virtuale in formato FAT16 e non formattato devono essere di almeno 3 MB.</span><span class="sxs-lookup"><span data-stu-id="8bdf2-147">Unformatted and FAT16 formatted virtual hard disk images must be at least 3 MB.</span></span> <span data-ttu-id="8bdf2-148">Le immagini del disco rigido virtuale formattato FAT32 devono essere di almeno 514 MB.</span><span class="sxs-lookup"><span data-stu-id="8bdf2-148">FAT32 formatted virtual hard disk images must be at least 514 MB.</span></span><br/>                                                                                   |
| <dl> <span data-ttu-id="8bdf2-149"><dt>**Macchina virtuale \_ Il \_ file E è \_ troppo \_ grande \_ per il \_ volume**</dt> <dt>0xA0040679</dt></span><span class="sxs-lookup"><span data-stu-id="8bdf2-149"><dt>**VM\_E\_FILE\_TOO\_LARGE\_FOR\_VOLUME**</dt> <dt>0xA0040679</dt></span></span> </dl>          | <span data-ttu-id="8bdf2-150">Il volume host non può supportare un file di questa dimensione se l'immagine del disco rigido virtuale a espansione dinamica si espande fino al limite massimo.</span><span class="sxs-lookup"><span data-stu-id="8bdf2-150">The host volume cannot support a file this size if the dynamically expanding virtual hard disk image expands to its full limit.</span></span> <span data-ttu-id="8bdf2-151">Le dimensioni massime del file per un volume FAT32 sono pari a 4 GB.</span><span class="sxs-lookup"><span data-stu-id="8bdf2-151">The maximum file size for a FAT32 volume is 4 GB.</span></span> <span data-ttu-id="8bdf2-152">Le dimensioni massime del file per un volume FAT16 sono pari a 2 GB.</span><span class="sxs-lookup"><span data-stu-id="8bdf2-152">The maximum file size for a FAT16 volume is 2 GB.</span></span><br/> |
| <dl> <span data-ttu-id="8bdf2-153"><dt>**Macchina virtuale \_ E \_ \_ chiusura \_ dell'app**</dt> <dt>0xA0040209</dt></span><span class="sxs-lookup"><span data-stu-id="8bdf2-153"><dt>**VM\_E\_APP\_SHUTTING\_DOWN**</dt> <dt>0xA0040209</dt></span></span> </dl>                    | <span data-ttu-id="8bdf2-154">Non è possibile creare il disco rigido virtuale dopo che l'applicazione è stata avviata.</span><span class="sxs-lookup"><span data-stu-id="8bdf2-154">The virtual hard disk cannot be created after the application has started shutting down.</span></span><br/>                                                                                                                                            |
| <dl> <span data-ttu-id="8bdf2-155"><dt>**Macchina virtuale \_ E \_ \_ virtualizzazione hardware \_ disabilitato**</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="8bdf2-155"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl>     | <span data-ttu-id="8bdf2-156">Il processore non supporta le estensioni di virtualizzazione accelerata hardware (HAV).</span><span class="sxs-lookup"><span data-stu-id="8bdf2-156">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/>                                                                                                                                                |
| <dl> <span data-ttu-id="8bdf2-157"><dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="8bdf2-157"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="8bdf2-158">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="8bdf2-158">An unexpected error has occurred.</span></span><br/>                                                                                                                                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="8bdf2-159">Commenti</span><span class="sxs-lookup"><span data-stu-id="8bdf2-159">Remarks</span></span>

<span data-ttu-id="8bdf2-160">Anche se *imagePath* o *ParentPath* può essere un percorso relativo, almeno uno di questi deve essere un percorso assoluto.</span><span class="sxs-lookup"><span data-stu-id="8bdf2-160">Although either *imagePath* or *parentPath* can be a relative path, at least one of these must be an absolute path.</span></span> <span data-ttu-id="8bdf2-161">Se un parametro path è un percorso relativo, si presuppone che sia relativo all'altro parametro path.</span><span class="sxs-lookup"><span data-stu-id="8bdf2-161">If one path parameter is a relative path, it is assumed to be relative to the other path parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="8bdf2-162">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8bdf2-162">Requirements</span></span>



| <span data-ttu-id="8bdf2-163">Requisito</span><span class="sxs-lookup"><span data-stu-id="8bdf2-163">Requirement</span></span> | <span data-ttu-id="8bdf2-164">Valore</span><span class="sxs-lookup"><span data-stu-id="8bdf2-164">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="8bdf2-165">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8bdf2-165">Minimum supported client</span></span><br/> | <span data-ttu-id="8bdf2-166">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="8bdf2-166">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8bdf2-167">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8bdf2-167">Minimum supported server</span></span><br/> | <span data-ttu-id="8bdf2-168">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="8bdf2-168">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="8bdf2-169">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="8bdf2-169">End of client support</span></span><br/>    | <span data-ttu-id="8bdf2-170">Windows 7</span><span class="sxs-lookup"><span data-stu-id="8bdf2-170">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="8bdf2-171">Prodotto</span><span class="sxs-lookup"><span data-stu-id="8bdf2-171">Product</span></span><br/>                  | <span data-ttu-id="8bdf2-172">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="8bdf2-172">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="8bdf2-173">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8bdf2-173">Header</span></span><br/>                   | <dl> <span data-ttu-id="8bdf2-174"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="8bdf2-174"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="8bdf2-175">IID</span><span class="sxs-lookup"><span data-stu-id="8bdf2-175">IID</span></span><br/>                      | <span data-ttu-id="8bdf2-176">IID \_ IVMVirtualPC è definito come 236ba0d9-A24A-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="8bdf2-176">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="8bdf2-177">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8bdf2-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8bdf2-178">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="8bdf2-178">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

