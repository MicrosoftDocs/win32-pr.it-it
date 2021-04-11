---
title: Metodo IVMFloppyDrive AttachImage (VPCCOMInterfaces. h)
description: Connette un'immagine multimediale floppy nell'host all'unità floppy della macchina virtuale.
ms.assetid: ee7ea6ac-47ef-4e7b-8df3-28c716a728b0
keywords:
- Metodo AttachImage Virtual PC
- Metodo AttachImage Virtual PC, interfaccia IVMFloppyDrive
- Interfaccia IVMFloppyDrive Virtual PC, metodo AttachImage
topic_type:
- apiref
api_name:
- IVMFloppyDrive.AttachImage
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f8821a6d9bdae979f45477d1fe2ba666eb6da10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964071"
---
# <a name="ivmfloppydriveattachimage-method"></a><span data-ttu-id="d85a4-106">Metodo IVMFloppyDrive:: AttachImage</span><span class="sxs-lookup"><span data-stu-id="d85a4-106">IVMFloppyDrive::AttachImage method</span></span>

<span data-ttu-id="d85a4-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="d85a4-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="d85a4-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="d85a4-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="d85a4-109">Connette un'immagine multimediale floppy nell'host all'unità floppy della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="d85a4-109">Attaches a floppy media image on the host to the floppy drive of the virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="d85a4-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d85a4-110">Syntax</span></span>


```C++
HRESULT AttachImage(
  [in] BSTR mediaImagePath
);
```



## <a name="parameters"></a><span data-ttu-id="d85a4-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="d85a4-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d85a4-112">*mediaImagePath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d85a4-112">*mediaImagePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d85a4-113">Percorso completo dell'immagine multimediale floppy da collegare.</span><span class="sxs-lookup"><span data-stu-id="d85a4-113">The full path to the floppy media image that is to be attached.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d85a4-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d85a4-114">Return value</span></span>

<span data-ttu-id="d85a4-115">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="d85a4-115">This method can return one of these values.</span></span>



| <span data-ttu-id="d85a4-116">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="d85a4-116">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="d85a4-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d85a4-117">Description</span></span>                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d85a4-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="d85a4-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="d85a4-119">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="d85a4-119">The operation was successful.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="d85a4-120"><dt>**E \_**</dt> <dt>0x80000003</dt> INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="d85a4-120"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                                 | <span data-ttu-id="d85a4-121">Il parametro *mediaImagePath* non è valido.</span><span class="sxs-lookup"><span data-stu-id="d85a4-121">The *mediaImagePath* parameter is not valid.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="d85a4-122"><dt>**E \_ PUNTATORE**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="d85a4-122"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="d85a4-123">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="d85a4-123">The parameter is **NULL**.</span></span><br/>                                                                                                   |
| <dl> <span data-ttu-id="d85a4-124"><dt>**HRESULT \_ DA \_ Win32 (Error \_ OutOfMemory)**</dt> <dt>0x8007000e</dt></span><span class="sxs-lookup"><span data-stu-id="d85a4-124"><dt>**HRESULT\_FROM\_WIN32(ERROR\_OUTOFMEMORY)**</dt> <dt>0x8007000e</dt></span></span> </dl>      | <span data-ttu-id="d85a4-125">La memoria disponibile non è sufficiente per completare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="d85a4-125">There is not enough memory available to complete this request.</span></span><br/>                                                               |
| <dl> <span data-ttu-id="d85a4-126"><dt>**HRESULT \_ Da \_ Win32 (overflow del buffer degli errori \_ \_ )**</dt> <dt>0x8007006f</dt></span><span class="sxs-lookup"><span data-stu-id="d85a4-126"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BUFFER\_OVERFLOW)**</dt> <dt>0x8007006f</dt></span></span> </dl> | <span data-ttu-id="d85a4-127">Il percorso specificato dal parametro *mediaImagePath* è troppo lungo.</span><span class="sxs-lookup"><span data-stu-id="d85a4-127">The path specified by the *mediaImagePath* parameter is too long.</span></span> <span data-ttu-id="d85a4-128">Il percorso deve essere minore di **Max \_ path** (260) caratteri.</span><span class="sxs-lookup"><span data-stu-id="d85a4-128">The path must be less than **MAX\_PATH** (260) characters.</span></span><br/> |
| <dl> <span data-ttu-id="d85a4-129"><dt>**HRESULT \_ DA \_ Win32 (errore \_ nome non valido \_ )**</dt> <dt>0x8007007b</dt></span><span class="sxs-lookup"><span data-stu-id="d85a4-129"><dt>**HRESULT\_FROM\_WIN32(ERROR\_INVALID\_NAME)**</dt> <dt>0x8007007b</dt></span></span> </dl>    | <span data-ttu-id="d85a4-130">Il parametro *mediaImagePath* contiene un carattere non valido (uno di " \* ? <>/ \| ": ").</span><span class="sxs-lookup"><span data-stu-id="d85a4-130">The *mediaImagePath* parameter contains an invalid character (one of "\*?<>/\|":").</span></span><br/>                                    |
| <dl> <span data-ttu-id="d85a4-131"><dt>**HRESULT \_ DA \_ Win32 (errore \_ \_ percorso errato)**</dt> <dt>0x800700a1</dt></span><span class="sxs-lookup"><span data-stu-id="d85a4-131"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BAD\_PATHNAME)**</dt> <dt>0x800700a1</dt></span></span> </dl>    | <span data-ttu-id="d85a4-132">Il parametro *mediaImagePath* specifica un percorso vuoto o relativo.</span><span class="sxs-lookup"><span data-stu-id="d85a4-132">The *mediaImagePath* parameter specifies an empty or relative path.</span></span> <span data-ttu-id="d85a4-133">È necessario specificare un percorso assoluto.</span><span class="sxs-lookup"><span data-stu-id="d85a4-133">An absolute path is required.</span></span><br/>                            |
| <dl> <span data-ttu-id="d85a4-134"><dt>**Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="d85a4-134"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>                            | <span data-ttu-id="d85a4-135">La configurazione per questa macchina virtuale non è valida o non è stata trovata.</span><span class="sxs-lookup"><span data-stu-id="d85a4-135">The configuration for this virtual machine is not valid or cannot be found.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="d85a4-136"><dt>**Macchina virtuale \_ \_Acquisizione immagini \_ E \_ non riuscita**</dt> <dt>0xA00400650</dt></span><span class="sxs-lookup"><span data-stu-id="d85a4-136"><dt>**VM\_E\_IMAGE\_CAPTURE\_FAIL**</dt> <dt>0xA00400650</dt></span></span> </dl>                  | <span data-ttu-id="d85a4-137">Impossibile acquisire il file di immagine specificato.</span><span class="sxs-lookup"><span data-stu-id="d85a4-137">The image file specified could not be captured.</span></span><br/>                                                                              |
| <dl> <span data-ttu-id="d85a4-138"><dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="d85a4-138"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="d85a4-139">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="d85a4-139">An unexpected error has occurred.</span></span><br/>                                                                                            |



 

## <a name="requirements"></a><span data-ttu-id="d85a4-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d85a4-140">Requirements</span></span>



| <span data-ttu-id="d85a4-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="d85a4-141">Requirement</span></span> | <span data-ttu-id="d85a4-142">Valore</span><span class="sxs-lookup"><span data-stu-id="d85a4-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d85a4-143">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d85a4-143">Minimum supported client</span></span><br/> | <span data-ttu-id="d85a4-144">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="d85a4-144">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d85a4-145">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d85a4-145">Minimum supported server</span></span><br/> | <span data-ttu-id="d85a4-146">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="d85a4-146">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="d85a4-147">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="d85a4-147">End of client support</span></span><br/>    | <span data-ttu-id="d85a4-148">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d85a4-148">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="d85a4-149">Prodotto</span><span class="sxs-lookup"><span data-stu-id="d85a4-149">Product</span></span><br/>                  | <span data-ttu-id="d85a4-150">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="d85a4-150">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="d85a4-151">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d85a4-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="d85a4-152"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="d85a4-152"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="d85a4-153">IID</span><span class="sxs-lookup"><span data-stu-id="d85a4-153">IID</span></span><br/>                      | <span data-ttu-id="d85a4-154">IID \_ IVMFloppyDrive è definito come 661abee6-112A-4ED9-babf-3c874969f10e</span><span class="sxs-lookup"><span data-stu-id="d85a4-154">IID\_IVMFloppyDrive is defined as 661abee6-112a-4ed9-babf-3c874969f10e</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="d85a4-155">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d85a4-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d85a4-156">**IVMFloppyDrive**</span><span class="sxs-lookup"><span data-stu-id="d85a4-156">**IVMFloppyDrive**</span></span>](ivmfloppydrive.md)
</dt> </dl>

 

