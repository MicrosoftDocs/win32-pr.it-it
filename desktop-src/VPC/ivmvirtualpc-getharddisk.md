---
title: Metodo getharddisk IVMVirtualPC (VPCCOMInterfaces. h)
description: Recupera un oggetto corrispondente a un file di immagine del disco esistente.
ms.assetid: 648a3f8a-5114-4c14-b9a9-f175941333ab
keywords:
- Metodo getharddisk Virtual PC
- Metodo getharddisk Virtual PC, interfaccia IVMVirtualPC
- Interfaccia IVMVirtualPC Virtual PC, metodo getharddisk
topic_type:
- apiref
api_name:
- IVMVirtualPC.GetHardDisk
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 558d098b6745718830c63dd700c14febf4f6bed2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964702"
---
# <a name="ivmvirtualpcgetharddisk-method"></a><span data-ttu-id="59d4f-106">Metodo IVMVirtualPC:: getharddisk</span><span class="sxs-lookup"><span data-stu-id="59d4f-106">IVMVirtualPC::GetHardDisk method</span></span>

<span data-ttu-id="59d4f-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="59d4f-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="59d4f-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="59d4f-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="59d4f-109">Recupera un oggetto corrispondente a un file di immagine del disco esistente.</span><span class="sxs-lookup"><span data-stu-id="59d4f-109">Retrieves an object corresponding to an existing disk image file.</span></span>

## <a name="syntax"></a><span data-ttu-id="59d4f-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="59d4f-110">Syntax</span></span>


```C++
HRESULT GetHardDisk(
  [in]          BSTR        imagePath,
  [out, retval] IVMHardDisk **hardDisk
);
```



## <a name="parameters"></a><span data-ttu-id="59d4f-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="59d4f-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59d4f-112">*imagePath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="59d4f-112">*imagePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59d4f-113">Percorso completo di un file di immagine disco esistente.</span><span class="sxs-lookup"><span data-stu-id="59d4f-113">The full path to an existing disk image file.</span></span>

</dd> <dt>

<span data-ttu-id="59d4f-114">*disco rigido* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="59d4f-114">*hardDisk* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="59d4f-115">Oggetto [**IVMHardDisk**](ivmharddisk.md) che corrisponde a questa immagine del disco.</span><span class="sxs-lookup"><span data-stu-id="59d4f-115">An [**IVMHardDisk**](ivmharddisk.md) object corresponding to this disk image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59d4f-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="59d4f-116">Return value</span></span>

<span data-ttu-id="59d4f-117">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="59d4f-117">This method can return one of these values.</span></span>



| <span data-ttu-id="59d4f-118">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="59d4f-118">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="59d4f-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="59d4f-119">Description</span></span>                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="59d4f-120"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="59d4f-120"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="59d4f-121">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="59d4f-121">The operation was successful.</span></span><br/>                                                                                         |
| <dl> <span data-ttu-id="59d4f-122"><dt>**E \_ PUNTATORE**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="59d4f-122"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="59d4f-123">Il parametro *imagePath* o *hardDisk* è **null**.</span><span class="sxs-lookup"><span data-stu-id="59d4f-123">The *imagePath* or *hardDisk* parameter is **NULL**.</span></span><br/>                                                                  |
| <dl> <span data-ttu-id="59d4f-124"><dt>**HRESULT \_ DA \_ Win32 (file degli errori \_ \_ non \_ trovato)**</dt> <dt>0x80070002</dt></span><span class="sxs-lookup"><span data-stu-id="59d4f-124"><dt>**HRESULT\_FROM\_WIN32(ERROR\_FILE\_NOT\_FOUND)**</dt> <dt>0x80070002</dt></span></span> </dl> | <span data-ttu-id="59d4f-125">Il sistema non è in grado di trovare il file specificato dal parametro *imagePath* .</span><span class="sxs-lookup"><span data-stu-id="59d4f-125">The system cannot find the file specified by the *imagePath* parameter.</span></span><br/>                                               |
| <dl> <span data-ttu-id="59d4f-126"><dt>**HRESULT \_ DA \_ Win32 ( \_ percorso errore \_ non \_ trovato)**</dt> <dt>0 x 80070003</dt></span><span class="sxs-lookup"><span data-stu-id="59d4f-126"><dt>**HRESULT\_FROM\_WIN32(ERROR\_PATH\_NOT\_FOUND)**</dt> <dt>0x80070003</dt></span></span> </dl> | <span data-ttu-id="59d4f-127">Il sistema non è in grado di trovare il percorso specificato dal parametro *imagePath* .</span><span class="sxs-lookup"><span data-stu-id="59d4f-127">The system cannot find the path specified by the *imagePath* parameter.</span></span><br/>                                               |
| <dl> <span data-ttu-id="59d4f-128"><dt>**HRESULT \_ DA \_ Win32 (errore \_ nome non valido \_ )**</dt> <dt>0x8007007b</dt></span><span class="sxs-lookup"><span data-stu-id="59d4f-128"><dt>**HRESULT\_FROM\_WIN32(ERROR\_INVALID\_NAME)**</dt> <dt>0x8007007b</dt></span></span> </dl>    | <span data-ttu-id="59d4f-129">Il parametro *imagePath* contiene un carattere non valido (uno di " \* ?: <>/ \| " ").</span><span class="sxs-lookup"><span data-stu-id="59d4f-129">The *imagePath* parameter contains an invalid character (one of "\*?:<>/\|"").</span></span><br/>                                  |
| <dl> <span data-ttu-id="59d4f-130"><dt>**HRESULT \_ DA \_ Win32 (errore \_ \_ percorso errato)**</dt> <dt>0x800700a1</dt></span><span class="sxs-lookup"><span data-stu-id="59d4f-130"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BAD\_PATHNAME)**</dt> <dt>0x800700a1</dt></span></span> </dl>    | <span data-ttu-id="59d4f-131">Il parametro *imagePath* specifica un percorso vuoto o relativo.</span><span class="sxs-lookup"><span data-stu-id="59d4f-131">The *imagePath* parameter specifies an empty or relative path.</span></span> <span data-ttu-id="59d4f-132">È necessario specificare un percorso assoluto.</span><span class="sxs-lookup"><span data-stu-id="59d4f-132">An absolute path is required.</span></span><br/>                          |
| <dl> <span data-ttu-id="59d4f-133"><dt>**HRESULT \_ Da \_ Win32 (overflow del buffer degli errori \_ \_ )**</dt> <dt>0x8007006f</dt></span><span class="sxs-lookup"><span data-stu-id="59d4f-133"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BUFFER\_OVERFLOW)**</dt> <dt>0x8007006f</dt></span></span> </dl> | <span data-ttu-id="59d4f-134">Il percorso specificato dal parametro *imagePath* è troppo lungo.</span><span class="sxs-lookup"><span data-stu-id="59d4f-134">The path specified by the *imagePath* parameter is too long.</span></span> <span data-ttu-id="59d4f-135">La lunghezza del percorso deve essere inferiore a 260 caratteri.</span><span class="sxs-lookup"><span data-stu-id="59d4f-135">The length of the path must be less than 260 characters.</span></span><br/> |
| <dl> <span data-ttu-id="59d4f-136"><dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="59d4f-136"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="59d4f-137">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="59d4f-137">An unexpected error has occurred.</span></span><br/>                                                                                     |
| <dl> <span data-ttu-id="59d4f-138"><dt>**Macchina virtuale \_ E \_ \_ virtualizzazione hardware \_ disabilitato**</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="59d4f-138"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl>     | <span data-ttu-id="59d4f-139">Il processore non supporta le estensioni di virtualizzazione accelerata hardware (HAV).</span><span class="sxs-lookup"><span data-stu-id="59d4f-139">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/>                                  |



 

## <a name="requirements"></a><span data-ttu-id="59d4f-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="59d4f-140">Requirements</span></span>



| <span data-ttu-id="59d4f-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="59d4f-141">Requirement</span></span> | <span data-ttu-id="59d4f-142">Valore</span><span class="sxs-lookup"><span data-stu-id="59d4f-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="59d4f-143">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="59d4f-143">Minimum supported client</span></span><br/> | <span data-ttu-id="59d4f-144">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="59d4f-144">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="59d4f-145">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="59d4f-145">Minimum supported server</span></span><br/> | <span data-ttu-id="59d4f-146">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="59d4f-146">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="59d4f-147">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="59d4f-147">End of client support</span></span><br/>    | <span data-ttu-id="59d4f-148">Windows 7</span><span class="sxs-lookup"><span data-stu-id="59d4f-148">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="59d4f-149">Prodotto</span><span class="sxs-lookup"><span data-stu-id="59d4f-149">Product</span></span><br/>                  | <span data-ttu-id="59d4f-150">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="59d4f-150">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="59d4f-151">Intestazione</span><span class="sxs-lookup"><span data-stu-id="59d4f-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="59d4f-152"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="59d4f-152"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="59d4f-153">IID</span><span class="sxs-lookup"><span data-stu-id="59d4f-153">IID</span></span><br/>                      | <span data-ttu-id="59d4f-154">IID \_ IVMVirtualPC è definito come 236ba0d9-A24A-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="59d4f-154">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="59d4f-155">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="59d4f-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59d4f-156">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="59d4f-156">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

