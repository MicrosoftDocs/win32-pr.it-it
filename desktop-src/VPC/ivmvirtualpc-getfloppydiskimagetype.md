---
title: Metodo IVMVirtualPC GetFloppyDiskImageType (VPCCOMInterfaces. h)
description: Recupera il tipo di un file di immagine del disco floppy esistente.
ms.assetid: 34956a0c-1da0-4968-9a6c-c114d7037da1
keywords:
- Metodo GetFloppyDiskImageType Virtual PC
- Metodo GetFloppyDiskImageType Virtual PC, interfaccia IVMVirtualPC
- Interfaccia IVMVirtualPC Virtual PC, metodo GetFloppyDiskImageType
topic_type:
- apiref
api_name:
- IVMVirtualPC.GetFloppyDiskImageType
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e5e2974f80865f8572f1153721cf10233fdb389
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121346"
---
# <a name="ivmvirtualpcgetfloppydiskimagetype-method"></a><span data-ttu-id="21a8b-106">Metodo IVMVirtualPC:: GetFloppyDiskImageType</span><span class="sxs-lookup"><span data-stu-id="21a8b-106">IVMVirtualPC::GetFloppyDiskImageType method</span></span>

<span data-ttu-id="21a8b-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="21a8b-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="21a8b-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="21a8b-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="21a8b-109">Recupera il tipo di un file di immagine del disco floppy esistente.</span><span class="sxs-lookup"><span data-stu-id="21a8b-109">Retrieves the type of an existing floppy disk image file.</span></span>

## <a name="syntax"></a><span data-ttu-id="21a8b-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="21a8b-110">Syntax</span></span>


```C++
HRESULT GetFloppyDiskImageType(
  [in]          BSTR                  imagePath,
  [out, retval] VMFloppyDiskImageType *imageType
);
```



## <a name="parameters"></a><span data-ttu-id="21a8b-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="21a8b-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21a8b-112">*imagePath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="21a8b-112">*imagePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21a8b-113">Percorso completo del file di immagine del disco.</span><span class="sxs-lookup"><span data-stu-id="21a8b-113">The full path to the disk image file.</span></span>

</dd> <dt>

<span data-ttu-id="21a8b-114">*ImageType* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="21a8b-114">*imageType* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="21a8b-115">Tipo di immagine disco.</span><span class="sxs-lookup"><span data-stu-id="21a8b-115">The disk image type.</span></span> <span data-ttu-id="21a8b-116">Per un elenco di valori, vedere [**VMFloppyDiskImageType**](vmfloppydiskimagetype.md).</span><span class="sxs-lookup"><span data-stu-id="21a8b-116">For a list of values, see [**VMFloppyDiskImageType**](vmfloppydiskimagetype.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21a8b-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="21a8b-117">Return value</span></span>

<span data-ttu-id="21a8b-118">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="21a8b-118">This method can return one of these values.</span></span>



| <span data-ttu-id="21a8b-119">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="21a8b-119">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="21a8b-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="21a8b-120">Description</span></span>                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="21a8b-121"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="21a8b-121"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="21a8b-122">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="21a8b-122">The operation was successful.</span></span><br/>                                                                                         |
| <dl> <span data-ttu-id="21a8b-123"><dt>**E \_ PUNTATORE**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="21a8b-123"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="21a8b-124">Il parametro *imagePath* o *ImageType* è **null**.</span><span class="sxs-lookup"><span data-stu-id="21a8b-124">The *imagePath* or *imageType* parameter is **NULL**.</span></span><br/>                                                                 |
| <dl> <span data-ttu-id="21a8b-125"><dt>**HRESULT \_ DA \_ Win32 (file degli errori \_ \_ non \_ trovato)**</dt> <dt>0x80070002</dt></span><span class="sxs-lookup"><span data-stu-id="21a8b-125"><dt>**HRESULT\_FROM\_WIN32(ERROR\_FILE\_NOT\_FOUND)**</dt> <dt>0x80070002</dt></span></span> </dl> | <span data-ttu-id="21a8b-126">Il sistema non è in grado di trovare il file specificato dal parametro *imagePath* .</span><span class="sxs-lookup"><span data-stu-id="21a8b-126">The system cannot find the file specified by the *imagePath* parameter.</span></span><br/>                                               |
| <dl> <span data-ttu-id="21a8b-127"><dt>**HRESULT \_ DA \_ Win32 ( \_ percorso errore \_ non \_ trovato)**</dt> <dt>0 x 80070003</dt></span><span class="sxs-lookup"><span data-stu-id="21a8b-127"><dt>**HRESULT\_FROM\_WIN32(ERROR\_PATH\_NOT\_FOUND)**</dt> <dt>0x80070003</dt></span></span> </dl> | <span data-ttu-id="21a8b-128">Il sistema non è in grado di trovare il percorso specificato dal parametro *imagePath* .</span><span class="sxs-lookup"><span data-stu-id="21a8b-128">The system cannot find the path specified by the *imagePath* parameter.</span></span><br/>                                               |
| <dl> <span data-ttu-id="21a8b-129"><dt>**HRESULT \_ DA \_ Win32 (errore \_ nome non valido \_ )**</dt> <dt>0x8007007b</dt></span><span class="sxs-lookup"><span data-stu-id="21a8b-129"><dt>**HRESULT\_FROM\_WIN32(ERROR\_INVALID\_NAME)**</dt> <dt>0x8007007b</dt></span></span> </dl>    | <span data-ttu-id="21a8b-130">Il parametro *imagePath* contiene un carattere non valido (uno di " \* ?: <>/ \| " ").</span><span class="sxs-lookup"><span data-stu-id="21a8b-130">The *imagePath* parameter contains an invalid character (one of "\*?:<>/\|"").</span></span><br/>                                  |
| <dl> <span data-ttu-id="21a8b-131"><dt>**HRESULT \_ DA \_ Win32 (errore \_ \_ percorso errato)**</dt> <dt>0x800700a1</dt></span><span class="sxs-lookup"><span data-stu-id="21a8b-131"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BAD\_PATHNAME)**</dt> <dt>0x800700a1</dt></span></span> </dl>    | <span data-ttu-id="21a8b-132">Il parametro *imagePath* specifica un percorso vuoto o relativo.</span><span class="sxs-lookup"><span data-stu-id="21a8b-132">The *imagePath* parameter specifies an empty or relative path.</span></span> <span data-ttu-id="21a8b-133">È necessario specificare un percorso assoluto.</span><span class="sxs-lookup"><span data-stu-id="21a8b-133">An absolute path is required.</span></span><br/>                          |
| <dl> <span data-ttu-id="21a8b-134"><dt>**HRESULT \_ Da \_ Win32 (overflow del buffer degli errori \_ \_ )**</dt> <dt>0x8007006f</dt></span><span class="sxs-lookup"><span data-stu-id="21a8b-134"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BUFFER\_OVERFLOW)**</dt> <dt>0x8007006f</dt></span></span> </dl> | <span data-ttu-id="21a8b-135">Il percorso specificato dal parametro *imagePath* è troppo lungo.</span><span class="sxs-lookup"><span data-stu-id="21a8b-135">The path specified by the *imagePath* parameter is too long.</span></span> <span data-ttu-id="21a8b-136">La lunghezza del percorso deve essere inferiore a 260 caratteri.</span><span class="sxs-lookup"><span data-stu-id="21a8b-136">The length of the path must be less than 260 characters.</span></span><br/> |
| <dl> <span data-ttu-id="21a8b-137"><dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="21a8b-137"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="21a8b-138">Il file specificato da *imagePath* non è un'immagine floppy oppure si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="21a8b-138">The file specified by *imagePath* is not a floppy image, or an unexpected error has occurred.</span></span><br/>                         |
| <dl> <span data-ttu-id="21a8b-139"><dt>**Macchina virtuale \_ E \_ \_ virtualizzazione hardware \_ disabilitato**</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="21a8b-139"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl>     | <span data-ttu-id="21a8b-140">Il processore non supporta le estensioni di virtualizzazione accelerata hardware (HAV).</span><span class="sxs-lookup"><span data-stu-id="21a8b-140">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/>                                  |



 

## <a name="requirements"></a><span data-ttu-id="21a8b-141">Requisiti</span><span class="sxs-lookup"><span data-stu-id="21a8b-141">Requirements</span></span>



| <span data-ttu-id="21a8b-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="21a8b-142">Requirement</span></span> | <span data-ttu-id="21a8b-143">Valore</span><span class="sxs-lookup"><span data-stu-id="21a8b-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="21a8b-144">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="21a8b-144">Minimum supported client</span></span><br/> | <span data-ttu-id="21a8b-145">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="21a8b-145">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="21a8b-146">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="21a8b-146">Minimum supported server</span></span><br/> | <span data-ttu-id="21a8b-147">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="21a8b-147">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="21a8b-148">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="21a8b-148">End of client support</span></span><br/>    | <span data-ttu-id="21a8b-149">Windows 7</span><span class="sxs-lookup"><span data-stu-id="21a8b-149">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="21a8b-150">Prodotto</span><span class="sxs-lookup"><span data-stu-id="21a8b-150">Product</span></span><br/>                  | <span data-ttu-id="21a8b-151">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="21a8b-151">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="21a8b-152">Intestazione</span><span class="sxs-lookup"><span data-stu-id="21a8b-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="21a8b-153"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="21a8b-153"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="21a8b-154">IID</span><span class="sxs-lookup"><span data-stu-id="21a8b-154">IID</span></span><br/>                      | <span data-ttu-id="21a8b-155">IID \_ IVMVirtualPC è definito come 236ba0d9-A24A-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="21a8b-155">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="21a8b-156">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="21a8b-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21a8b-157">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="21a8b-157">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

