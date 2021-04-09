---
title: Proprietà IVMVirtualPC SearchPaths (VPCCOMInterfaces. h)
description: Percorsi del file System usati per trovare i file associati a Windows Virtual PC.
ms.assetid: 2a2deee5-7e6b-4b90-8ce9-0b0dbeef0f30
keywords:
- Proprietà SearchPaths Virtual PC
- Proprietà SearchPaths Virtual PC, interfaccia IVMVirtualPC
- Interfaccia IVMVirtualPC Virtual PC, proprietà SearchPaths
topic_type:
- apiref
api_name:
- IVMVirtualPC.SearchPaths
- IVMVirtualPC.get_SearchPaths
- IVMVirtualPC.put_SearchPaths
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 287eb07bc9205f9b6f0851bd8809f9a49dcf3242
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739746"
---
# <a name="ivmvirtualpcsearchpaths-property"></a><span data-ttu-id="3d1f3-106">Proprietà IVMVirtualPC:: SearchPaths</span><span class="sxs-lookup"><span data-stu-id="3d1f3-106">IVMVirtualPC::SearchPaths property</span></span>

<span data-ttu-id="3d1f3-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="3d1f3-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="3d1f3-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="3d1f3-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="3d1f3-109">Recupera e imposta i percorsi di file system utilizzati per trovare i file associati a Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="3d1f3-109">Retrieves and sets the file system paths that are used to find files associated with Windows Virtual PC.</span></span>

<span data-ttu-id="3d1f3-110">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="3d1f3-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d1f3-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3d1f3-111">Syntax</span></span>


```C++
HRESULT put_SearchPaths(
  [in]          VARIANT searchPaths
);

HRESULT get_SearchPaths(
  [out, retval] VARIANT *searchPaths
);
```



## <a name="property-value"></a><span data-ttu-id="3d1f3-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="3d1f3-112">Property value</span></span>

<span data-ttu-id="3d1f3-113">Specifica un SafeArray contenente un percorso di file system per ogni voce.</span><span class="sxs-lookup"><span data-stu-id="3d1f3-113">Specifies a safearray containing a file system path for each entry.</span></span>

## <a name="error-codes"></a><span data-ttu-id="3d1f3-114">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="3d1f3-114">Error codes</span></span>



| <span data-ttu-id="3d1f3-115">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="3d1f3-115">Name/value</span></span>                                                                                                                                                                               | <span data-ttu-id="3d1f3-116">Significato</span><span class="sxs-lookup"><span data-stu-id="3d1f3-116">Meaning</span></span>                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3d1f3-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="3d1f3-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="3d1f3-118">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="3d1f3-118">The operation was successful.</span></span><br/>                                                                                               |
| <dl> <span data-ttu-id="3d1f3-119"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="3d1f3-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="3d1f3-120">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="3d1f3-120">The parameter is **NULL**.</span></span><br/>                                                                                                  |
| <dl> <span data-ttu-id="3d1f3-121"><dt>E \_ </dt> <dt>0x80000003</dt> INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="3d1f3-121"><dt>E\_INVALIDARG</dt> <dt>0x80000003</dt></span></span> </dl>                                 | <span data-ttu-id="3d1f3-122">Il parametro *SearchPaths* non è valido e non può essere analizzato in una matrice di percorsi.</span><span class="sxs-lookup"><span data-stu-id="3d1f3-122">The *searchPaths* parameter is not valid and could not be parsed into an array of paths.</span></span><br/>                                    |
| <dl> <span data-ttu-id="3d1f3-123"><dt>HRESULT \_ DA \_ Win32 (file degli errori \_ \_ non \_ trovato)</dt> <dt>0x80070002</dt></span><span class="sxs-lookup"><span data-stu-id="3d1f3-123"><dt>HRESULT\_FROM\_WIN32(ERROR\_FILE\_NOT\_FOUND)</dt> <dt>0x80070002</dt></span></span> </dl> | <span data-ttu-id="3d1f3-124">Il sistema non è in grado di trovare una directory specificata nel parametro *SearchPaths* .</span><span class="sxs-lookup"><span data-stu-id="3d1f3-124">The system cannot find a directory specified in the *searchPaths* parameter.</span></span><br/>                                                |
| <dl> <span data-ttu-id="3d1f3-125"><dt>HRESULT \_ DA \_ Win32 ( \_ percorso errore \_ non \_ trovato)</dt> <dt>0 x 80070003</dt></span><span class="sxs-lookup"><span data-stu-id="3d1f3-125"><dt>HRESULT\_FROM\_WIN32(ERROR\_PATH\_NOT\_FOUND)</dt> <dt>0x80070003</dt></span></span> </dl> | <span data-ttu-id="3d1f3-126">Il sistema non è in grado di trovare un percorso specificato dal parametro *SearchPaths* .</span><span class="sxs-lookup"><span data-stu-id="3d1f3-126">The system cannot find a path specified by the *searchPaths* parameter.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="3d1f3-127"><dt>HRESULT \_ DA \_ Win32 (errore \_ nome non valido \_ )</dt> <dt>0x8007007b</dt></span><span class="sxs-lookup"><span data-stu-id="3d1f3-127"><dt>HRESULT\_FROM\_WIN32(ERROR\_INVALID\_NAME)</dt> <dt>0x8007007b</dt></span></span> </dl>    | <span data-ttu-id="3d1f3-128">Un percorso specificato nel parametro *SearchPaths* contiene caratteri non validi.</span><span class="sxs-lookup"><span data-stu-id="3d1f3-128">A path specified in the *searchPaths* parameter contains illegal characters.</span></span> <span data-ttu-id="3d1f3-129">I caratteri non validi sono " \* ? <>/ \| ": ".</span><span class="sxs-lookup"><span data-stu-id="3d1f3-129">The illegal characters are "\*?<>/\|":".</span></span><br/> |
| <dl> <span data-ttu-id="3d1f3-130"><dt>HRESULT \_ DA \_ Win32 (errore \_ \_ percorso errato)</dt> <dt>0x800700a1</dt></span><span class="sxs-lookup"><span data-stu-id="3d1f3-130"><dt>HRESULT\_FROM\_WIN32(ERROR\_BAD\_PATHNAME)</dt> <dt>0x800700a1</dt></span></span> </dl>    | <span data-ttu-id="3d1f3-131">Un percorso contenuto nel parametro *SearchPaths* specifica un percorso vuoto o relativo.</span><span class="sxs-lookup"><span data-stu-id="3d1f3-131">A path contained in the *searchPaths* parameter specifies an empty or relative path.</span></span> <span data-ttu-id="3d1f3-132">È necessario specificare un percorso assoluto.</span><span class="sxs-lookup"><span data-stu-id="3d1f3-132">An absolute path is required.</span></span><br/>          |
| <dl> <span data-ttu-id="3d1f3-133"><dt>HRESULT \_ Da \_ Win32 (overflow del buffer degli errori \_ \_ )</dt> <dt>0x8007006f</dt></span><span class="sxs-lookup"><span data-stu-id="3d1f3-133"><dt>HRESULT\_FROM\_WIN32(ERROR\_BUFFER\_OVERFLOW)</dt> <dt>0x8007006f</dt></span></span> </dl> | <span data-ttu-id="3d1f3-134">Il percorso specificato nel parametro *SearchPaths* è troppo lungo.</span><span class="sxs-lookup"><span data-stu-id="3d1f3-134">The path specified in the *searchPaths* parameter is too long.</span></span> <span data-ttu-id="3d1f3-135">La lunghezza del percorso deve essere inferiore a 260 caratteri.</span><span class="sxs-lookup"><span data-stu-id="3d1f3-135">The length of the path must be less than 260 characters.</span></span><br/>     |
| <dl> <span data-ttu-id="3d1f3-136"><dt>Macchina virtuale \_ E \_ pref \_ non \_ trovato</dt> <dt>0xA0040300</dt></span><span class="sxs-lookup"><span data-stu-id="3d1f3-136"><dt>VM\_E\_PREF\_NOT\_FOUND</dt> <dt>0xA0040300</dt></span></span> </dl>                       | <span data-ttu-id="3d1f3-137">La preferenza non è stata trovata.</span><span class="sxs-lookup"><span data-stu-id="3d1f3-137">The preference was not found.</span></span><br/>                                                                                               |
| <dl> <span data-ttu-id="3d1f3-138"><dt>Macchina virtuale \_ E \_ \_ virtualizzazione hardware \_ disabilitato</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="3d1f3-138"><dt>VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED</dt> <dt>0xA0040951</dt></span></span> </dl>     | <span data-ttu-id="3d1f3-139">Il processore non supporta le estensioni di virtualizzazione accelerata hardware (HAV).</span><span class="sxs-lookup"><span data-stu-id="3d1f3-139">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/>                                        |
| <dl> <span data-ttu-id="3d1f3-140"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="3d1f3-140"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="3d1f3-141">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="3d1f3-141">An unexpected error has occurred.</span></span><br/>                                                                                           |



## <a name="requirements"></a><span data-ttu-id="3d1f3-142">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3d1f3-142">Requirements</span></span>



| <span data-ttu-id="3d1f3-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="3d1f3-143">Requirement</span></span> | <span data-ttu-id="3d1f3-144">Valore</span><span class="sxs-lookup"><span data-stu-id="3d1f3-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d1f3-145">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3d1f3-145">Minimum supported client</span></span><br/> | <span data-ttu-id="3d1f3-146">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="3d1f3-146">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3d1f3-147">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3d1f3-147">Minimum supported server</span></span><br/> | <span data-ttu-id="3d1f3-148">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="3d1f3-148">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="3d1f3-149">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="3d1f3-149">End of client support</span></span><br/>    | <span data-ttu-id="3d1f3-150">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3d1f3-150">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="3d1f3-151">Prodotto</span><span class="sxs-lookup"><span data-stu-id="3d1f3-151">Product</span></span><br/>                  | <span data-ttu-id="3d1f3-152">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="3d1f3-152">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="3d1f3-153">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3d1f3-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="3d1f3-154"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="3d1f3-154"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="3d1f3-155">IID</span><span class="sxs-lookup"><span data-stu-id="3d1f3-155">IID</span></span><br/>                      | <span data-ttu-id="3d1f3-156">IID \_ IVMVirtualPC è definito come 236ba0d9-A24A-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="3d1f3-156">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="3d1f3-157">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3d1f3-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d1f3-158">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="3d1f3-158">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

