---
title: Metodo IVMVirtualPC CreateFloppyDiskImage (VPCCOMInterfaces. h)
description: Consente di creare un file di immagine disco floppy.
ms.assetid: 474e86a4-2019-41bd-9361-e494291d1961
keywords:
- Metodo CreateFloppyDiskImage Virtual PC
- Metodo CreateFloppyDiskImage Virtual PC, interfaccia IVMVirtualPC
- Interfaccia IVMVirtualPC Virtual PC, metodo CreateFloppyDiskImage
topic_type:
- apiref
api_name:
- IVMVirtualPC.CreateFloppyDiskImage
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ff94ba5cb922aeb75f4effac413bb83b080b3fd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478149"
---
# <a name="ivmvirtualpccreatefloppydiskimage-method"></a><span data-ttu-id="04f7f-106">Metodo IVMVirtualPC:: CreateFloppyDiskImage</span><span class="sxs-lookup"><span data-stu-id="04f7f-106">IVMVirtualPC::CreateFloppyDiskImage method</span></span>

<span data-ttu-id="04f7f-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="04f7f-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="04f7f-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="04f7f-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="04f7f-109">Consente di creare un file di immagine disco floppy.</span><span class="sxs-lookup"><span data-stu-id="04f7f-109">Creates a floppy disk image file.</span></span>

## <a name="syntax"></a><span data-ttu-id="04f7f-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="04f7f-110">Syntax</span></span>


```C++
HRESULT CreateFloppyDiskImage(
  [in] BSTR                  imagePath,
  [in] VMFloppyDiskImageType imageType
);
```



## <a name="parameters"></a><span data-ttu-id="04f7f-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="04f7f-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04f7f-112">*imagePath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="04f7f-112">*imagePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04f7f-113">Percorso completo del nuovo file di immagine del disco.</span><span class="sxs-lookup"><span data-stu-id="04f7f-113">The full path to the new disk image file.</span></span> <span data-ttu-id="04f7f-114">Se non esiste, verrà creata la cartella che lo contiene.</span><span class="sxs-lookup"><span data-stu-id="04f7f-114">The containing folder will be created if it does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="04f7f-115">*ImageType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="04f7f-115">*imageType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04f7f-116">Tipo di immagine del disco floppy da creare.</span><span class="sxs-lookup"><span data-stu-id="04f7f-116">The type of floppy disk image to create.</span></span> <span data-ttu-id="04f7f-117">Sono supportati solo **vmFloppyDiskImage \_ LowDensity** (1) e **vmFloppyDiskImage \_ ad alta densità** (2).</span><span class="sxs-lookup"><span data-stu-id="04f7f-117">Only **vmFloppyDiskImage\_LowDensity** (1) and **vmFloppyDiskImage\_HighDensity** (2) are supported.</span></span> <span data-ttu-id="04f7f-118">Vedere [**VMFloppyDiskImageType**](vmfloppydiskimagetype.md).</span><span class="sxs-lookup"><span data-stu-id="04f7f-118">See [**VMFloppyDiskImageType**](vmfloppydiskimagetype.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04f7f-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="04f7f-119">Return value</span></span>

<span data-ttu-id="04f7f-120">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="04f7f-120">This method can return one of these values.</span></span>



| <span data-ttu-id="04f7f-121">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="04f7f-121">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="04f7f-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="04f7f-122">Description</span></span>                                                                                                                                               |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="04f7f-123"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="04f7f-123"><dt>**S\_OK**</dt></span></span> </dl>                                                                                                         | <span data-ttu-id="04f7f-124">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="04f7f-124">The operation was successful.</span></span><br/>                                                                                                                  |
| <dl> <span data-ttu-id="04f7f-125"><dt>**E \_ PUNTATORE**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="04f7f-125"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="04f7f-126">Il parametro *imagePath* è **null**.</span><span class="sxs-lookup"><span data-stu-id="04f7f-126">The *imagePath* parameter is **NULL**.</span></span><br/>                                                                                                         |
| <dl> <span data-ttu-id="04f7f-127"><dt>**E \_**</dt> <dt>0x80000003</dt> INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="04f7f-127"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                                 | <span data-ttu-id="04f7f-128">Il parametro *ImageType* non è [**vmFloppyDiskImage \_ LowDensity**](vmfloppydiskimagetype.md) (1) o **vmFloppyDiskImage \_ ad alta densità** (2).</span><span class="sxs-lookup"><span data-stu-id="04f7f-128">The *imageType* parameter is not [**vmFloppyDiskImage\_LowDensity**](vmfloppydiskimagetype.md) (1) or **vmFloppyDiskImage\_HighDensity** (2).</span></span><br/> |
| <dl> <span data-ttu-id="04f7f-129"><dt>**HRESULT \_ DA \_ Win32 ( \_ percorso errore \_ non \_ trovato)**</dt> <dt>0 x 80070003</dt></span><span class="sxs-lookup"><span data-stu-id="04f7f-129"><dt>**HRESULT\_FROM\_WIN32(ERROR\_PATH\_NOT\_FOUND)**</dt> <dt>0x80070003</dt></span></span> </dl> | <span data-ttu-id="04f7f-130">Il sistema non è in grado di trovare il percorso specificato dal parametro *imagePath* .</span><span class="sxs-lookup"><span data-stu-id="04f7f-130">The system cannot find the path specified by the *imagePath* parameter.</span></span><br/>                                                                        |
| <dl> <span data-ttu-id="04f7f-131"><dt>**HRESULT \_ DA \_ Win32 (errore \_ nome non valido \_ )**</dt> <dt>0x8007007b</dt></span><span class="sxs-lookup"><span data-stu-id="04f7f-131"><dt>**HRESULT\_FROM\_WIN32(ERROR\_INVALID\_NAME)**</dt> <dt>0x8007007b</dt></span></span> </dl>    | <span data-ttu-id="04f7f-132">Il parametro *imagePath* contiene un carattere non valido (uno di " \* ?: <>/ \| " ").</span><span class="sxs-lookup"><span data-stu-id="04f7f-132">The *imagePath* parameter contains an invalid character (one of "\*?:<>/\|"").</span></span><br/>                                                           |
| <dl> <span data-ttu-id="04f7f-133"><dt>**HRESULT \_ DA \_ Win32 (errore \_ \_ percorso errato)**</dt> <dt>0x800700a1</dt></span><span class="sxs-lookup"><span data-stu-id="04f7f-133"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BAD\_PATHNAME)**</dt> <dt>0x800700a1</dt></span></span> </dl>    | <span data-ttu-id="04f7f-134">Il parametro *imagePath* specifica un percorso vuoto o relativo.</span><span class="sxs-lookup"><span data-stu-id="04f7f-134">The *imagePath* parameter specifies an empty or relative path.</span></span> <span data-ttu-id="04f7f-135">È necessario specificare un percorso assoluto.</span><span class="sxs-lookup"><span data-stu-id="04f7f-135">An absolute path is required.</span></span><br/>                                                   |
| <dl> <span data-ttu-id="04f7f-136"><dt>**HRESULT \_ Da \_ Win32 (overflow del buffer degli errori \_ \_ )**</dt> <dt>0x8007006f</dt></span><span class="sxs-lookup"><span data-stu-id="04f7f-136"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BUFFER\_OVERFLOW)**</dt> <dt>0x8007006f</dt></span></span> </dl> | <span data-ttu-id="04f7f-137">Il percorso specificato dal parametro *imagePath* è troppo lungo.</span><span class="sxs-lookup"><span data-stu-id="04f7f-137">The path specified by the *imagePath* parameter is too long.</span></span> <span data-ttu-id="04f7f-138">La lunghezza del percorso deve essere inferiore a 260 caratteri.</span><span class="sxs-lookup"><span data-stu-id="04f7f-138">The length of the path must be less than 260 characters.</span></span><br/>                          |
| <dl> <span data-ttu-id="04f7f-139"><dt>**HRESULT \_ DA \_ Win32 (errore \_ già \_ esistente)**</dt> <dt>0x800700b7</dt></span><span class="sxs-lookup"><span data-stu-id="04f7f-139"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ALREADY\_EXISTS)**</dt> <dt>0x800700b7</dt></span></span> </dl>  | <span data-ttu-id="04f7f-140">Il file a cui fa riferimento il parametro *imagePath* esiste già.</span><span class="sxs-lookup"><span data-stu-id="04f7f-140">The file referenced by the parameter *imagePath* already exists.</span></span><br/>                                                                               |
| <dl> <span data-ttu-id="04f7f-141"><dt>**HRESULT \_ DA \_ Win32 (errore \_ disco \_ completo)**</dt> <dt>0x80070070</dt></span><span class="sxs-lookup"><span data-stu-id="04f7f-141"><dt>**HRESULT\_FROM\_WIN32(ERROR\_DISK\_FULL)**</dt> <dt>0x80070070</dt></span></span> </dl>       | <span data-ttu-id="04f7f-142">Spazio insufficiente nel volume host per creare l'immagine del disco floppy virtuale.</span><span class="sxs-lookup"><span data-stu-id="04f7f-142">There is insufficient space on the host volume to create the virtual floppy disk image.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="04f7f-143"><dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="04f7f-143"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="04f7f-144">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="04f7f-144">An unexpected error occurred.</span></span><br/>                                                                                                                  |
| <dl> <span data-ttu-id="04f7f-145"><dt>**Macchina virtuale \_ E \_ \_ virtualizzazione hardware \_ disabilitato**</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="04f7f-145"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl>     | <span data-ttu-id="04f7f-146">Il processore non supporta le estensioni di virtualizzazione accelerata hardware (HAV).</span><span class="sxs-lookup"><span data-stu-id="04f7f-146">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/>                                                           |



 

## <a name="requirements"></a><span data-ttu-id="04f7f-147">Requisiti</span><span class="sxs-lookup"><span data-stu-id="04f7f-147">Requirements</span></span>



| <span data-ttu-id="04f7f-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="04f7f-148">Requirement</span></span> | <span data-ttu-id="04f7f-149">Valore</span><span class="sxs-lookup"><span data-stu-id="04f7f-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="04f7f-150">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="04f7f-150">Minimum supported client</span></span><br/> | <span data-ttu-id="04f7f-151">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="04f7f-151">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="04f7f-152">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="04f7f-152">Minimum supported server</span></span><br/> | <span data-ttu-id="04f7f-153">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="04f7f-153">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="04f7f-154">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="04f7f-154">End of client support</span></span><br/>    | <span data-ttu-id="04f7f-155">Windows 7</span><span class="sxs-lookup"><span data-stu-id="04f7f-155">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="04f7f-156">Prodotto</span><span class="sxs-lookup"><span data-stu-id="04f7f-156">Product</span></span><br/>                  | <span data-ttu-id="04f7f-157">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="04f7f-157">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="04f7f-158">Intestazione</span><span class="sxs-lookup"><span data-stu-id="04f7f-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="04f7f-159"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="04f7f-159"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="04f7f-160">IID</span><span class="sxs-lookup"><span data-stu-id="04f7f-160">IID</span></span><br/>                      | <span data-ttu-id="04f7f-161">IID \_ IVMVirtualPC è definito come 236ba0d9-A24A-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="04f7f-161">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="04f7f-162">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="04f7f-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04f7f-163">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="04f7f-163">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

