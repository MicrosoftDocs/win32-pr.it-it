---
title: Proprietà IVMHostInfo ProcessorFeaturesString (VPCCOMInterfaces. h)
description: Recupera le funzionalità dell'elenco supportate dal processore host.
ms.assetid: 036c6376-0e9b-46fa-90f4-a40c71c5cf23
keywords:
- Proprietà ProcessorFeaturesString Virtual PC
- Proprietà ProcessorFeaturesString Virtual PC, interfaccia IVMHostInfo
- Interfaccia IVMHostInfo Virtual PC, proprietà ProcessorFeaturesString
topic_type:
- apiref
api_name:
- IVMHostInfo.ProcessorFeaturesString
- IVMHostInfo.get_ProcessorFeaturesString
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 118aaa2eabe7ddb2fd608892775a17eac6a77d16
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106300930"
---
# <a name="ivmhostinfoprocessorfeaturesstring-property"></a><span data-ttu-id="065b6-106">IVMHostInfo::P proprietà rocessorFeaturesString</span><span class="sxs-lookup"><span data-stu-id="065b6-106">IVMHostInfo::ProcessorFeaturesString property</span></span>

<span data-ttu-id="065b6-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="065b6-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="065b6-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="065b6-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="065b6-109">Recupera le funzionalità dell'elenco supportate dal processore host.</span><span class="sxs-lookup"><span data-stu-id="065b6-109">Retrieves the list features supported by the host processor.</span></span>

<span data-ttu-id="065b6-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="065b6-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="065b6-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="065b6-111">Syntax</span></span>


```C++
HRESULT get_ProcessorFeaturesString(
  [out, retval] BSTR *featuresString
);
```



## <a name="property-value"></a><span data-ttu-id="065b6-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="065b6-112">Property value</span></span>

<span data-ttu-id="065b6-113">Elenco delimitato da virgole di funzionalità.</span><span class="sxs-lookup"><span data-stu-id="065b6-113">A comma-delimited list of features.</span></span> <span data-ttu-id="065b6-114">Un esempio è "MMX, SSE, SSE2, x86-64".</span><span class="sxs-lookup"><span data-stu-id="065b6-114">An example would be "MMX,SSE,SSE2,x86-64".</span></span>



| <span data-ttu-id="065b6-115">Valore</span><span class="sxs-lookup"><span data-stu-id="065b6-115">Value</span></span>                                                                                 | <span data-ttu-id="065b6-116">Significato</span><span class="sxs-lookup"><span data-stu-id="065b6-116">Meaning</span></span>                                                             |
|---------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <span data-ttu-id="065b6-117"><dt>"AMD-V"</dt></span><span class="sxs-lookup"><span data-stu-id="065b6-117"><dt>"AMD-V"</dt></span></span> </dl>    | <span data-ttu-id="065b6-118">Supporta le estensioni di virtualizzazione AMD.</span><span class="sxs-lookup"><span data-stu-id="065b6-118">Supports the AMD Virtualization extensions.</span></span><br/>              |
| <dl> <span data-ttu-id="065b6-119"><dt>"Intel VT"</dt></span><span class="sxs-lookup"><span data-stu-id="065b6-119"><dt>"Intel VT"</dt></span></span> </dl> | <span data-ttu-id="065b6-120">Supporta le estensioni della tecnologia di virtualizzazione Intel.</span><span class="sxs-lookup"><span data-stu-id="065b6-120">Supports the Intel Virtualization Technology extensions.</span></span><br/> |
| <dl> <span data-ttu-id="065b6-121"><dt>HAVD</dt></span><span class="sxs-lookup"><span data-stu-id="065b6-121"><dt>"HAVD"</dt></span></span> </dl>     | <span data-ttu-id="065b6-122">La virtualizzazione assistita mediante hardware è disabilitata.</span><span class="sxs-lookup"><span data-stu-id="065b6-122">Hardware Assisted Virtualization is disabled.</span></span><br/>            |
| <dl> <span data-ttu-id="065b6-123"><dt>AVERE</dt></span><span class="sxs-lookup"><span data-stu-id="065b6-123"><dt>"HAVE"</dt></span></span> </dl>     | <span data-ttu-id="065b6-124">La virtualizzazione assistita mediante hardware è abilitata.</span><span class="sxs-lookup"><span data-stu-id="065b6-124">Hardware Assisted Virtualization is enabled.</span></span><br/>             |
| <dl> <span data-ttu-id="065b6-125"><dt>MMX</dt></span><span class="sxs-lookup"><span data-stu-id="065b6-125"><dt>"MMX"</dt></span></span> </dl>      | <span data-ttu-id="065b6-126">Supporta le estensioni MMX.</span><span class="sxs-lookup"><span data-stu-id="065b6-126">Supports the MMX extensions.</span></span><br/>                             |
| <dl> <span data-ttu-id="065b6-127"><dt>SSE</dt></span><span class="sxs-lookup"><span data-stu-id="065b6-127"><dt>"SSE"</dt></span></span> </dl>      | <span data-ttu-id="065b6-128">Supporta il Streaming SIMD Extensions.</span><span class="sxs-lookup"><span data-stu-id="065b6-128">Supports the Streaming SIMD Extensions.</span></span><br/>                  |
| <dl> <span data-ttu-id="065b6-129"><dt>SSE2</dt></span><span class="sxs-lookup"><span data-stu-id="065b6-129"><dt>"SSE2"</dt></span></span> </dl>     | <span data-ttu-id="065b6-130">Supporta il Streaming SIMD Extensions 2.</span><span class="sxs-lookup"><span data-stu-id="065b6-130">Supports the Streaming SIMD Extensions 2.</span></span><br/>                |
| <dl> <span data-ttu-id="065b6-131"><dt>SSE3</dt></span><span class="sxs-lookup"><span data-stu-id="065b6-131"><dt>"SSE3"</dt></span></span> </dl>     | <span data-ttu-id="065b6-132">Supporta il Streaming SIMD Extensions 3.</span><span class="sxs-lookup"><span data-stu-id="065b6-132">Supports the Streaming SIMD Extensions 3.</span></span><br/>                |
| <dl> <span data-ttu-id="065b6-133"><dt>"TXTE"</dt></span><span class="sxs-lookup"><span data-stu-id="065b6-133"><dt>"TXTE"</dt></span></span> </dl>     | <span data-ttu-id="065b6-134">Supporta le estensioni della tecnologia di esecuzione attendibile.</span><span class="sxs-lookup"><span data-stu-id="065b6-134">Supports the Trusted Execution Technology extensions.</span></span><br/>    |
| <dl> <span data-ttu-id="065b6-135"><dt>"x86-64"</dt></span><span class="sxs-lookup"><span data-stu-id="065b6-135"><dt>"x86-64"</dt></span></span> </dl>   | <span data-ttu-id="065b6-136">Supporta le estensioni x86-64.</span><span class="sxs-lookup"><span data-stu-id="065b6-136">Supports x86-64 extensions.</span></span><br/>                              |



 

## <a name="error-codes"></a><span data-ttu-id="065b6-137">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="065b6-137">Error codes</span></span>



| <span data-ttu-id="065b6-138">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="065b6-138">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="065b6-139">Significato</span><span class="sxs-lookup"><span data-stu-id="065b6-139">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="065b6-140"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="065b6-140"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="065b6-141">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="065b6-141">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="065b6-142"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="065b6-142"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="065b6-143">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="065b6-143">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="065b6-144"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="065b6-144"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="065b6-145">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="065b6-145">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="065b6-146">Requisiti</span><span class="sxs-lookup"><span data-stu-id="065b6-146">Requirements</span></span>



| <span data-ttu-id="065b6-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="065b6-147">Requirement</span></span> | <span data-ttu-id="065b6-148">Valore</span><span class="sxs-lookup"><span data-stu-id="065b6-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="065b6-149">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="065b6-149">Minimum supported client</span></span><br/> | <span data-ttu-id="065b6-150">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="065b6-150">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="065b6-151">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="065b6-151">Minimum supported server</span></span><br/> | <span data-ttu-id="065b6-152">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="065b6-152">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="065b6-153">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="065b6-153">End of client support</span></span><br/>    | <span data-ttu-id="065b6-154">Windows 7</span><span class="sxs-lookup"><span data-stu-id="065b6-154">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="065b6-155">Prodotto</span><span class="sxs-lookup"><span data-stu-id="065b6-155">Product</span></span><br/>                  | <span data-ttu-id="065b6-156">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="065b6-156">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="065b6-157">Intestazione</span><span class="sxs-lookup"><span data-stu-id="065b6-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="065b6-158"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="065b6-158"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="065b6-159">IID</span><span class="sxs-lookup"><span data-stu-id="065b6-159">IID</span></span><br/>                      | <span data-ttu-id="065b6-160">IID \_ IVMHostInfo è definito come 5b5cf343-05ad-453B-be99-adf4e27b2ebc</span><span class="sxs-lookup"><span data-stu-id="065b6-160">IID\_IVMHostInfo is defined as 5b5cf343-05ad-453b-be99-adf4e27b2ebc</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="065b6-161">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="065b6-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="065b6-162">**IVMHostInfo**</span><span class="sxs-lookup"><span data-stu-id="065b6-162">**IVMHostInfo**</span></span>](ivmhostinfo.md)
</dt> </dl>

 

