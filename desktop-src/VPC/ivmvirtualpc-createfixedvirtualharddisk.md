---
title: Metodo IVMVirtualPC CreateFixedVirtualHardDisk (VPCCOMInterfaces. h)
description: Crea un disco rigido virtuale a dimensione fissa.
ms.assetid: c58a7f2c-efd7-4a39-9ce5-617baa82084b
keywords:
- Metodo CreateFixedVirtualHardDisk Virtual PC
- Metodo CreateFixedVirtualHardDisk Virtual PC, interfaccia IVMVirtualPC
- Interfaccia IVMVirtualPC Virtual PC, metodo CreateFixedVirtualHardDisk
topic_type:
- apiref
api_name:
- IVMVirtualPC.CreateFixedVirtualHardDisk
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c1c260611ba3a8b55f87f23d0957c53a304a471
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119958"
---
# <a name="ivmvirtualpccreatefixedvirtualharddisk-method"></a><span data-ttu-id="126bd-106">Metodo IVMVirtualPC:: CreateFixedVirtualHardDisk</span><span class="sxs-lookup"><span data-stu-id="126bd-106">IVMVirtualPC::CreateFixedVirtualHardDisk method</span></span>

<span data-ttu-id="126bd-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="126bd-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="126bd-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="126bd-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="126bd-109">Crea un disco rigido virtuale a dimensione fissa.</span><span class="sxs-lookup"><span data-stu-id="126bd-109">Creates a fixed-size virtual hard disk.</span></span>

## <a name="syntax"></a><span data-ttu-id="126bd-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="126bd-110">Syntax</span></span>


```C++
HRESULT CreateFixedVirtualHardDisk(
  [in]          BSTR    imagePath,
  [in]          long    size,
  [out, retval] IVMTask **diskTask
);
```



## <a name="parameters"></a><span data-ttu-id="126bd-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="126bd-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="126bd-112">*imagePath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="126bd-112">*imagePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="126bd-113">Percorso completo del nuovo file di immagine del disco.</span><span class="sxs-lookup"><span data-stu-id="126bd-113">The full path to the new disk image file.</span></span> <span data-ttu-id="126bd-114">Se non esiste, verrà creata la cartella che lo contiene.</span><span class="sxs-lookup"><span data-stu-id="126bd-114">The containing folder will be created if it does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="126bd-115">*dimensioni* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="126bd-115">*size* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="126bd-116">Dimensione, in megabyte, dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="126bd-116">The size, in megabytes, of the image.</span></span> <span data-ttu-id="126bd-117">La dimensione massima è 2.088.960 MB (2040GB).</span><span class="sxs-lookup"><span data-stu-id="126bd-117">Maximum size is 2,088,960 MB (2040GB).</span></span>

</dd> <dt>

<span data-ttu-id="126bd-118">*diskTask* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="126bd-118">*diskTask* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="126bd-119">Oggetto [**IVMTask**](ivmtask.md) utilizzato per tenere traccia della creazione dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="126bd-119">An [**IVMTask**](ivmtask.md) object that is used to track the creation of the image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="126bd-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="126bd-120">Return value</span></span>

<span data-ttu-id="126bd-121">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="126bd-121">This method can return one of these values.</span></span>



| <span data-ttu-id="126bd-122">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="126bd-122">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="126bd-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="126bd-123">Description</span></span>                                                                                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="126bd-124"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="126bd-124"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="126bd-125">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="126bd-125">The operation was successful.</span></span><br/>                                                                                                                        |
| <dl> <span data-ttu-id="126bd-126"><dt>**E \_ PUNTATORE**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="126bd-126"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="126bd-127">Un parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="126bd-127">A parameter is **NULL**.</span></span><br/>                                                                                                                             |
| <dl> <span data-ttu-id="126bd-128"><dt>**E \_**</dt> <dt>0x80000003</dt> INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="126bd-128"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                                 | <span data-ttu-id="126bd-129">Il parametro *size* è minore o uguale a 0.</span><span class="sxs-lookup"><span data-stu-id="126bd-129">The *size* parameter is less than or equal to 0.</span></span><br/>                                                                                                     |
| <dl> <span data-ttu-id="126bd-130"><dt>**HRESULT \_ DA \_ Win32 ( \_ percorso errore \_ non \_ trovato)**</dt> <dt>0 x 80070003</dt></span><span class="sxs-lookup"><span data-stu-id="126bd-130"><dt>**HRESULT\_FROM\_WIN32(ERROR\_PATH\_NOT\_FOUND)**</dt> <dt>0x80070003</dt></span></span> </dl> | <span data-ttu-id="126bd-131">Il sistema non è in grado di trovare il percorso specificato dal parametro *imagePath* .</span><span class="sxs-lookup"><span data-stu-id="126bd-131">The system cannot find the path specified by the *imagePath* parameter.</span></span><br/>                                                                              |
| <dl> <span data-ttu-id="126bd-132"><dt>**HRESULT \_ DA \_ Win32 (errore \_ unità non valida \_ )**</dt> <dt>0x8007000f</dt></span><span class="sxs-lookup"><span data-stu-id="126bd-132"><dt>**HRESULT\_FROM\_WIN32(ERROR\_INVALID\_DRIVE)**</dt> <dt>0x8007000f</dt></span></span> </dl>   | <span data-ttu-id="126bd-133">Il file specificato dal parametro *imagePath* si trova su un CD-ROM o un DVD-ROM.</span><span class="sxs-lookup"><span data-stu-id="126bd-133">The file specified by the *imagePath* parameter is on a CD-ROM or DVD-ROM.</span></span><br/>                                                                           |
| <dl> <span data-ttu-id="126bd-134"><dt>**HRESULT \_ DA \_ Win32 (errore \_ nome non valido \_ )**</dt> <dt>0x8007007b</dt></span><span class="sxs-lookup"><span data-stu-id="126bd-134"><dt>**HRESULT\_FROM\_WIN32(ERROR\_INVALID\_NAME)**</dt> <dt>0x8007007b</dt></span></span> </dl>    | <span data-ttu-id="126bd-135">Il parametro *imagePath* contiene un carattere non valido (uno di " \* ?: <>/ \| " ").</span><span class="sxs-lookup"><span data-stu-id="126bd-135">The *imagePath* parameter contains an invalid character (one of "\*?:<>/\|"").</span></span><br/>                                                                 |
| <dl> <span data-ttu-id="126bd-136"><dt>**HRESULT \_ DA \_ Win32 (errore \_ \_ percorso errato)**</dt> <dt>0x800700a1</dt></span><span class="sxs-lookup"><span data-stu-id="126bd-136"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BAD\_PATHNAME)**</dt> <dt>0x800700a1</dt></span></span> </dl>    | <span data-ttu-id="126bd-137">Il parametro *imagePath* specifica un percorso vuoto o relativo.</span><span class="sxs-lookup"><span data-stu-id="126bd-137">Both the *imagePath* parameter specifies an empty or relative path.</span></span> <span data-ttu-id="126bd-138">Almeno uno dei parametri deve essere un percorso assoluto.</span><span class="sxs-lookup"><span data-stu-id="126bd-138">At least one of the parameters must be an absolute path.</span></span><br/>                         |
| <dl> <span data-ttu-id="126bd-139"><dt>**HRESULT \_ Da \_ Win32 (overflow del buffer degli errori \_ \_ )**</dt> <dt>0x8007006f</dt></span><span class="sxs-lookup"><span data-stu-id="126bd-139"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BUFFER\_OVERFLOW)**</dt> <dt>0x8007006f</dt></span></span> </dl> | <span data-ttu-id="126bd-140">Il percorso specificato dal parametro *imagePath* è troppo lungo.</span><span class="sxs-lookup"><span data-stu-id="126bd-140">The path specified by the *imagePath* parameter is too long.</span></span> <span data-ttu-id="126bd-141">La lunghezza del percorso deve essere minore di **Max \_ path** (260) caratteri.</span><span class="sxs-lookup"><span data-stu-id="126bd-141">The length of the path must be less than **MAX\_PATH** (260) characters.</span></span><br/>                |
| <dl> <span data-ttu-id="126bd-142"><dt>**HRESULT \_ DA \_ Win32 (errore \_ già \_ esistente)**</dt> <dt>0x800700b7</dt></span><span class="sxs-lookup"><span data-stu-id="126bd-142"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ALREADY\_EXISTS)**</dt> <dt>0x800700b7</dt></span></span> </dl>  | <span data-ttu-id="126bd-143">Il file a cui fa riferimento il parametro *imagePath* esiste già.</span><span class="sxs-lookup"><span data-stu-id="126bd-143">The file referenced by the *imagePath* parameter already exists.</span></span><br/>                                                                                     |
| <dl> <span data-ttu-id="126bd-144"><dt>**HRESULT \_ DA \_ Win32 (errore \_ disco \_ completo)**</dt> <dt>0x80070070</dt></span><span class="sxs-lookup"><span data-stu-id="126bd-144"><dt>**HRESULT\_FROM\_WIN32(ERROR\_DISK\_FULL)**</dt> <dt>0x80070070</dt></span></span> </dl>       | <span data-ttu-id="126bd-145">Per l'immagine del disco rigido virtuale a espansione dinamica sono necessari almeno 8 MB di spazio sul volume host.</span><span class="sxs-lookup"><span data-stu-id="126bd-145">The dynamically expanding virtual hard disk image needs at least 8 MB free on the host volume.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="126bd-146"><dt>**Macchina virtuale \_ Dimensioni dell'immagine E 0xA0040683 \_ \_ \_ troppo \_ grandi**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="126bd-146"><dt>**VM\_E\_IMAGE\_SIZE\_TOO\_LARGE**</dt> <dt>0xA0040683</dt></span></span> </dl>                | <span data-ttu-id="126bd-147">Il parametro *size* deve essere minore di 2.088.960 MB.</span><span class="sxs-lookup"><span data-stu-id="126bd-147">The *size* parameter must be less than 2,088,960 MB.</span></span> <span data-ttu-id="126bd-148">Se il formato è FAT16, il parametro *size* deve essere minore di 2000 MB.</span><span class="sxs-lookup"><span data-stu-id="126bd-148">If the format is FAT16, then the *size* parameter must be less than 2000 MB.</span></span><br/>                    |
| <dl> <span data-ttu-id="126bd-149"><dt>**Macchina virtuale \_ \_Dimensioni immagine E \_ dimensioni \_ troppo \_ ridotte**</dt> <dt>0xA0040684</dt></span><span class="sxs-lookup"><span data-stu-id="126bd-149"><dt>**VM\_E\_IMAGE\_SIZE\_TOO\_SMALL**</dt> <dt>0xA0040684</dt></span></span> </dl>                | <span data-ttu-id="126bd-150">Le immagini del disco rigido virtuale in formato FAT16 e non formattato devono essere di almeno 3 MB.</span><span class="sxs-lookup"><span data-stu-id="126bd-150">Unformatted and FAT16 formatted virtual hard disk images must be at least 3 MB.</span></span> <span data-ttu-id="126bd-151">Le immagini del disco rigido virtuale formattato FAT32 devono essere di almeno 514 MB.</span><span class="sxs-lookup"><span data-stu-id="126bd-151">FAT32 formatted virtual hard disk images must be at least 514 MB.</span></span><br/>    |
| <dl> <span data-ttu-id="126bd-152"><dt>**Macchina virtuale \_ Il \_ file E è \_ troppo \_ grande \_ per il \_ volume**</dt> <dt>0xA0040679</dt></span><span class="sxs-lookup"><span data-stu-id="126bd-152"><dt>**VM\_E\_FILE\_TOO\_LARGE\_FOR\_VOLUME**</dt> <dt>0xA0040679</dt></span></span> </dl>          | <span data-ttu-id="126bd-153">Il volume host non può supportare le dimensioni di un file.</span><span class="sxs-lookup"><span data-stu-id="126bd-153">The host volume cannot support a file this size.</span></span> <span data-ttu-id="126bd-154">Le dimensioni massime del file per un volume FAT32 sono pari a 4 GB.</span><span class="sxs-lookup"><span data-stu-id="126bd-154">The maximum file size for a FAT32 volume is 4 GB.</span></span> <span data-ttu-id="126bd-155">Le dimensioni massime del file per un volume FAT16 sono pari a 2 GB.</span><span class="sxs-lookup"><span data-stu-id="126bd-155">The maximum file size for a FAT16 volume is 2 GB.</span></span><br/> |
| <dl> <span data-ttu-id="126bd-156"><dt>**Macchina virtuale \_ E \_ \_ chiusura \_ dell'app**</dt> <dt>0xA0040209</dt></span><span class="sxs-lookup"><span data-stu-id="126bd-156"><dt>**VM\_E\_APP\_SHUTTING\_DOWN**</dt> <dt>0xA0040209</dt></span></span> </dl>                    | <span data-ttu-id="126bd-157">Non è possibile creare il disco rigido virtuale dopo che l'applicazione è stata avviata.</span><span class="sxs-lookup"><span data-stu-id="126bd-157">The virtual hard disk cannot be created after the application has started shutting down.</span></span><br/>                                                             |
| <dl> <span data-ttu-id="126bd-158"><dt>**Macchina virtuale \_ E \_ \_ virtualizzazione hardware \_ disabilitato**</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="126bd-158"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl>     | <span data-ttu-id="126bd-159">Il processore non supporta le estensioni di virtualizzazione accelerata hardware (HAV).</span><span class="sxs-lookup"><span data-stu-id="126bd-159">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/>                                                                 |
| <dl> <span data-ttu-id="126bd-160"><dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="126bd-160"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="126bd-161">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="126bd-161">An unexpected error has occurred.</span></span><br/>                                                                                                                    |



 

## <a name="requirements"></a><span data-ttu-id="126bd-162">Requisiti</span><span class="sxs-lookup"><span data-stu-id="126bd-162">Requirements</span></span>



| <span data-ttu-id="126bd-163">Requisito</span><span class="sxs-lookup"><span data-stu-id="126bd-163">Requirement</span></span> | <span data-ttu-id="126bd-164">Valore</span><span class="sxs-lookup"><span data-stu-id="126bd-164">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="126bd-165">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="126bd-165">Minimum supported client</span></span><br/> | <span data-ttu-id="126bd-166">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="126bd-166">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="126bd-167">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="126bd-167">Minimum supported server</span></span><br/> | <span data-ttu-id="126bd-168">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="126bd-168">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="126bd-169">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="126bd-169">End of client support</span></span><br/>    | <span data-ttu-id="126bd-170">Windows 7</span><span class="sxs-lookup"><span data-stu-id="126bd-170">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="126bd-171">Prodotto</span><span class="sxs-lookup"><span data-stu-id="126bd-171">Product</span></span><br/>                  | <span data-ttu-id="126bd-172">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="126bd-172">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="126bd-173">Intestazione</span><span class="sxs-lookup"><span data-stu-id="126bd-173">Header</span></span><br/>                   | <dl> <span data-ttu-id="126bd-174"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="126bd-174"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="126bd-175">IID</span><span class="sxs-lookup"><span data-stu-id="126bd-175">IID</span></span><br/>                      | <span data-ttu-id="126bd-176">IID \_ IVMVirtualPC è definito come 236ba0d9-A24A-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="126bd-176">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="126bd-177">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="126bd-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="126bd-178">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="126bd-178">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

