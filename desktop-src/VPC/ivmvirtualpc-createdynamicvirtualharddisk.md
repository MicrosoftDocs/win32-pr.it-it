---
title: Metodo IVMVirtualPC CreateDynamicVirtualHardDisk (VPCCOMInterfaces. h)
description: Crea un disco rigido virtuale di ridimensionamento dinamico.
ms.assetid: 2373ac41-c4c4-44c6-93e1-92814cd40b81
keywords:
- Metodo CreateDynamicVirtualHardDisk Virtual PC
- Metodo CreateDynamicVirtualHardDisk Virtual PC, interfaccia IVMVirtualPC
- Interfaccia IVMVirtualPC Virtual PC, metodo CreateDynamicVirtualHardDisk
topic_type:
- apiref
api_name:
- IVMVirtualPC.CreateDynamicVirtualHardDisk
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d245072fd5b3135decd814a29dd8a87d2b6a956
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400930"
---
# <a name="ivmvirtualpccreatedynamicvirtualharddisk-method"></a><span data-ttu-id="cdaa3-106">Metodo IVMVirtualPC:: CreateDynamicVirtualHardDisk</span><span class="sxs-lookup"><span data-stu-id="cdaa3-106">IVMVirtualPC::CreateDynamicVirtualHardDisk method</span></span>

<span data-ttu-id="cdaa3-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="cdaa3-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="cdaa3-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="cdaa3-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="cdaa3-109">Crea un disco rigido virtuale di ridimensionamento dinamico.</span><span class="sxs-lookup"><span data-stu-id="cdaa3-109">Creates a dynamically resizing virtual hard disk.</span></span>

## <a name="syntax"></a><span data-ttu-id="cdaa3-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cdaa3-110">Syntax</span></span>


```C++
HRESULT CreateDynamicVirtualHardDisk(
  [in]          BSTR    imagePath,
  [in]          long    size,
  [out, retval] IVMTask **diskTask
);
```



## <a name="parameters"></a><span data-ttu-id="cdaa3-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="cdaa3-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cdaa3-112">*imagePath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cdaa3-112">*imagePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cdaa3-113">Percorso completo del nuovo file di immagine del disco.</span><span class="sxs-lookup"><span data-stu-id="cdaa3-113">The full path to the new disk image file.</span></span> <span data-ttu-id="cdaa3-114">Se non esiste, verrà creata la cartella che lo contiene.</span><span class="sxs-lookup"><span data-stu-id="cdaa3-114">The containing folder will be created if it does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="cdaa3-115">*dimensioni* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cdaa3-115">*size* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cdaa3-116">Dimensione dell'immagine, in megabyte.</span><span class="sxs-lookup"><span data-stu-id="cdaa3-116">The size of the image, in megabytes.</span></span> <span data-ttu-id="cdaa3-117">Questo valore può essere al massimo 2.088.960 MB (2040GB).</span><span class="sxs-lookup"><span data-stu-id="cdaa3-117">This value can be at most 2,088,960 MB (2040GB).</span></span>

</dd> <dt>

<span data-ttu-id="cdaa3-118">*diskTask* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="cdaa3-118">*diskTask* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="cdaa3-119">Oggetto [**IVMTask**](ivmtask.md) utilizzato per tenere traccia della creazione dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="cdaa3-119">An [**IVMTask**](ivmtask.md) object that is used to track the creation of the image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cdaa3-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cdaa3-120">Return value</span></span>

<span data-ttu-id="cdaa3-121">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="cdaa3-121">This method can return one of these values.</span></span>



| <span data-ttu-id="cdaa3-122">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="cdaa3-122">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="cdaa3-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cdaa3-123">Description</span></span>                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="cdaa3-124"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="cdaa3-124"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="cdaa3-125">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="cdaa3-125">The operation was successful.</span></span><br/>                                                                                                                                                                                                       |
| <dl> <span data-ttu-id="cdaa3-126"><dt>**E \_ PUNTATORE**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="cdaa3-126"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="cdaa3-127">Un parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="cdaa3-127">A parameter is **NULL**.</span></span><br/>                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="cdaa3-128"><dt>**E \_**</dt> <dt>0x80000003</dt> INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="cdaa3-128"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                                 | <span data-ttu-id="cdaa3-129">Il parametro *size* è minore o uguale a 0.</span><span class="sxs-lookup"><span data-stu-id="cdaa3-129">The *size* parameter is less than or equal to 0.</span></span><br/>                                                                                                                                                                                    |
| <dl> <span data-ttu-id="cdaa3-130"><dt>**HRESULT \_ DA \_ Win32 ( \_ percorso errore \_ non \_ trovato)**</dt> <dt>0 x 80070003</dt></span><span class="sxs-lookup"><span data-stu-id="cdaa3-130"><dt>**HRESULT\_FROM\_WIN32(ERROR\_PATH\_NOT\_FOUND)**</dt> <dt>0x80070003</dt></span></span> </dl> | <span data-ttu-id="cdaa3-131">Il sistema non è in grado di trovare il percorso specificato dal parametro *imagePath* .</span><span class="sxs-lookup"><span data-stu-id="cdaa3-131">The system cannot find the path specified by the *imagePath* parameter.</span></span><br/>                                                                                                                                                             |
| <dl> <span data-ttu-id="cdaa3-132"><dt>**HRESULT \_ DA \_ Win32 (errore \_ unità non valida \_ )**</dt> <dt>0x8007000f</dt></span><span class="sxs-lookup"><span data-stu-id="cdaa3-132"><dt>**HRESULT\_FROM\_WIN32(ERROR\_INVALID\_DRIVE)**</dt> <dt>0x8007000f</dt></span></span> </dl>   | <span data-ttu-id="cdaa3-133">Il file specificato dal parametro *imagePath* si trova su un CD-ROM o un DVD-ROM.</span><span class="sxs-lookup"><span data-stu-id="cdaa3-133">The file specified by the *imagePath* parameter is on a CD-ROM or DVD-ROM.</span></span><br/>                                                                                                                                                          |
| <dl> <span data-ttu-id="cdaa3-134"><dt>**HRESULT \_ DA \_ Win32 (errore \_ nome non valido \_ )**</dt> <dt>0x8007007b</dt></span><span class="sxs-lookup"><span data-stu-id="cdaa3-134"><dt>**HRESULT\_FROM\_WIN32(ERROR\_INVALID\_NAME)**</dt> <dt>0x8007007b</dt></span></span> </dl>    | <span data-ttu-id="cdaa3-135">Il parametro *imagePath* contiene un carattere non valido (uno di " \* ?: <>/ \| " ").</span><span class="sxs-lookup"><span data-stu-id="cdaa3-135">The *imagePath* parameter contains an invalid character (one of "\*?:<>/\|"").</span></span><br/>                                                                                                                                                |
| <dl> <span data-ttu-id="cdaa3-136"><dt>**HRESULT \_ DA \_ Win32 (errore \_ \_ percorso errato)**</dt> <dt>0x800700a1</dt></span><span class="sxs-lookup"><span data-stu-id="cdaa3-136"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BAD\_PATHNAME)**</dt> <dt>0x800700a1</dt></span></span> </dl>    | <span data-ttu-id="cdaa3-137">Il parametro *imagePath* specifica un percorso vuoto o relativo.</span><span class="sxs-lookup"><span data-stu-id="cdaa3-137">Both the *imagePath* parameter specifies an empty or relative path.</span></span> <span data-ttu-id="cdaa3-138">Almeno uno dei parametri deve essere un percorso assoluto.</span><span class="sxs-lookup"><span data-stu-id="cdaa3-138">At least one of the parameters must be an absolute path.</span></span><br/>                                                                                                        |
| <dl> <span data-ttu-id="cdaa3-139"><dt>**HRESULT \_ Da \_ Win32 (overflow del buffer degli errori \_ \_ )**</dt> <dt>0x8007006f</dt></span><span class="sxs-lookup"><span data-stu-id="cdaa3-139"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BUFFER\_OVERFLOW)**</dt> <dt>0x8007006f</dt></span></span> </dl> | <span data-ttu-id="cdaa3-140">Il percorso specificato dal parametro *imagePath* è troppo lungo.</span><span class="sxs-lookup"><span data-stu-id="cdaa3-140">The path specified by the *imagePath* parameter is too long.</span></span> <span data-ttu-id="cdaa3-141">La lunghezza del percorso deve essere inferiore a 260 caratteri.</span><span class="sxs-lookup"><span data-stu-id="cdaa3-141">The length of the path must be less than 260 characters.</span></span><br/>                                                                                                               |
| <dl> <span data-ttu-id="cdaa3-142"><dt>**HRESULT \_ DA \_ Win32 (errore \_ già \_ esistente)**</dt> <dt>0x800700b7</dt></span><span class="sxs-lookup"><span data-stu-id="cdaa3-142"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ALREADY\_EXISTS)**</dt> <dt>0x800700b7</dt></span></span> </dl>  | <span data-ttu-id="cdaa3-143">Il file a cui fa riferimento il parametro *imagePath* esiste già.</span><span class="sxs-lookup"><span data-stu-id="cdaa3-143">The file referenced by the *imagePath* parameter already exists.</span></span><br/>                                                                                                                                                                    |
| <dl> <span data-ttu-id="cdaa3-144"><dt>**HRESULT \_ DA \_ Win32 (errore \_ disco \_ completo)**</dt> <dt>0x80070070</dt></span><span class="sxs-lookup"><span data-stu-id="cdaa3-144"><dt>**HRESULT\_FROM\_WIN32(ERROR\_DISK\_FULL)**</dt> <dt>0x80070070</dt></span></span> </dl>       | <span data-ttu-id="cdaa3-145">Per l'immagine del disco rigido virtuale a espansione dinamica sono necessari almeno 8 MB di spazio sul volume host.</span><span class="sxs-lookup"><span data-stu-id="cdaa3-145">The dynamically expanding virtual hard disk image needs at least 8 MB free on the host volume.</span></span><br/>                                                                                                                                      |
| <dl> <span data-ttu-id="cdaa3-146"><dt>**Macchina virtuale \_ Dimensioni dell'immagine E 0xA0040683 \_ \_ \_ troppo \_ grandi**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="cdaa3-146"><dt>**VM\_E\_IMAGE\_SIZE\_TOO\_LARGE**</dt> <dt>0xA0040683</dt></span></span> </dl>                | <span data-ttu-id="cdaa3-147">Le *dimensioni* del parametro devono essere minori di 2.088.960 MB.</span><span class="sxs-lookup"><span data-stu-id="cdaa3-147">The parameter *size* must be less than 2,088,960 MB.</span></span> <span data-ttu-id="cdaa3-148">Se il formato è FAT16, le dimensioni devono essere minori di 2000 MB.</span><span class="sxs-lookup"><span data-stu-id="cdaa3-148">If the format is FAT16, then size must be less than 2000 MB.</span></span><br/>                                                                                                                   |
| <dl> <span data-ttu-id="cdaa3-149"><dt>**Macchina virtuale \_ \_Dimensioni immagine E \_ dimensioni \_ troppo \_ ridotte**</dt> <dt>0xA0040684</dt></span><span class="sxs-lookup"><span data-stu-id="cdaa3-149"><dt>**VM\_E\_IMAGE\_SIZE\_TOO\_SMALL**</dt> <dt>0xA0040684</dt></span></span> </dl>                | <span data-ttu-id="cdaa3-150">Le immagini del disco rigido virtuale in formato FAT16 e non formattato devono essere di almeno 3 MB.</span><span class="sxs-lookup"><span data-stu-id="cdaa3-150">Unformatted and FAT16 formatted virtual hard disk images must be at least 3 MB.</span></span> <span data-ttu-id="cdaa3-151">Le immagini del disco rigido virtuale formattato FAT32 devono essere di almeno 514 MB.</span><span class="sxs-lookup"><span data-stu-id="cdaa3-151">FAT32 formatted virtual hard disk images must be at least 514 MB.</span></span><br/>                                                                                   |
| <dl> <span data-ttu-id="cdaa3-152"><dt>**Macchina virtuale \_ Il \_ file E è \_ troppo \_ grande \_ per il \_ volume**</dt> <dt>0xA0040679</dt></span><span class="sxs-lookup"><span data-stu-id="cdaa3-152"><dt>**VM\_E\_FILE\_TOO\_LARGE\_FOR\_VOLUME**</dt> <dt>0xA0040679</dt></span></span> </dl>          | <span data-ttu-id="cdaa3-153">Il volume host non può supportare un file di questa dimensione se l'immagine del disco rigido virtuale a espansione dinamica si espande fino al limite massimo.</span><span class="sxs-lookup"><span data-stu-id="cdaa3-153">The host volume cannot support a file this size if the dynamically expanding virtual hard disk image expands to its full limit.</span></span> <span data-ttu-id="cdaa3-154">Le dimensioni massime del file per un volume FAT32 sono pari a 4 GB.</span><span class="sxs-lookup"><span data-stu-id="cdaa3-154">The maximum file size for a FAT32 volume is 4 GB.</span></span> <span data-ttu-id="cdaa3-155">Le dimensioni massime del file per un volume FAT16 sono pari a 2 GB.</span><span class="sxs-lookup"><span data-stu-id="cdaa3-155">The maximum file size for a FAT16 volume is 2 GB.</span></span><br/> |
| <dl> <span data-ttu-id="cdaa3-156"><dt>**Macchina virtuale \_ E \_ \_ chiusura \_ dell'app**</dt> <dt>0xA0040209</dt></span><span class="sxs-lookup"><span data-stu-id="cdaa3-156"><dt>**VM\_E\_APP\_SHUTTING\_DOWN**</dt> <dt>0xA0040209</dt></span></span> </dl>                    | <span data-ttu-id="cdaa3-157">Non è possibile creare il disco rigido virtuale dopo che l'applicazione è stata avviata.</span><span class="sxs-lookup"><span data-stu-id="cdaa3-157">The virtual hard disk cannot be created after the application has started shutting down.</span></span><br/>                                                                                                                                            |
| <dl> <span data-ttu-id="cdaa3-158"><dt>**Macchina virtuale \_ E \_ \_ virtualizzazione hardware \_ disabilitato**</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="cdaa3-158"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl>     | <span data-ttu-id="cdaa3-159">Il processore non supporta le estensioni di virtualizzazione accelerata hardware (HAV).</span><span class="sxs-lookup"><span data-stu-id="cdaa3-159">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/>                                                                                                                                                |
| <dl> <span data-ttu-id="cdaa3-160"><dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="cdaa3-160"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="cdaa3-161">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="cdaa3-161">An unexpected error has occurred.</span></span><br/>                                                                                                                                                                                                   |



 

## <a name="requirements"></a><span data-ttu-id="cdaa3-162">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cdaa3-162">Requirements</span></span>



| <span data-ttu-id="cdaa3-163">Requisito</span><span class="sxs-lookup"><span data-stu-id="cdaa3-163">Requirement</span></span> | <span data-ttu-id="cdaa3-164">Valore</span><span class="sxs-lookup"><span data-stu-id="cdaa3-164">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="cdaa3-165">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cdaa3-165">Minimum supported client</span></span><br/> | <span data-ttu-id="cdaa3-166">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="cdaa3-166">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="cdaa3-167">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cdaa3-167">Minimum supported server</span></span><br/> | <span data-ttu-id="cdaa3-168">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="cdaa3-168">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="cdaa3-169">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="cdaa3-169">End of client support</span></span><br/>    | <span data-ttu-id="cdaa3-170">Windows 7</span><span class="sxs-lookup"><span data-stu-id="cdaa3-170">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="cdaa3-171">Prodotto</span><span class="sxs-lookup"><span data-stu-id="cdaa3-171">Product</span></span><br/>                  | <span data-ttu-id="cdaa3-172">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="cdaa3-172">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="cdaa3-173">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cdaa3-173">Header</span></span><br/>                   | <dl> <span data-ttu-id="cdaa3-174"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="cdaa3-174"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="cdaa3-175">IID</span><span class="sxs-lookup"><span data-stu-id="cdaa3-175">IID</span></span><br/>                      | <span data-ttu-id="cdaa3-176">IID \_ IVMVirtualPC è definito come 236ba0d9-A24A-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="cdaa3-176">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="cdaa3-177">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cdaa3-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cdaa3-178">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="cdaa3-178">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

