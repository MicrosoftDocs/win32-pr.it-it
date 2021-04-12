---
title: Proprietà Width IVMDisplay (VPCCOMInterfaces. h)
description: Larghezza, in pixel, dello schermo della macchina virtuale.
ms.assetid: a0062d75-dbb3-41ff-8112-87c1a31b088e
keywords:
- Proprietà larghezza PC virtuale
- Proprietà Width Virtual PC, interfaccia IVMDisplay
- Interfaccia IVMDisplay Virtual PC, proprietà Width
topic_type:
- apiref
api_name:
- IVMDisplay.Width
- IVMDisplay.get_Width
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12b6fe7d329498b0f1ffc36304311f733cd990c9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518802"
---
# <a name="ivmdisplaywidth-property"></a><span data-ttu-id="b14d3-106">Proprietà IVMDisplay:: Width</span><span class="sxs-lookup"><span data-stu-id="b14d3-106">IVMDisplay::Width property</span></span>

<span data-ttu-id="b14d3-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="b14d3-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="b14d3-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="b14d3-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="b14d3-109">Recupera la larghezza della visualizzazione della macchina virtuale (VM), in pixel.</span><span class="sxs-lookup"><span data-stu-id="b14d3-109">Retrieves the width of the virtual machine's (VM's) display, in pixels.</span></span>

<span data-ttu-id="b14d3-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="b14d3-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="b14d3-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b14d3-111">Syntax</span></span>


```C++
HRESULT get_Width(
  [out, retval] long *displayPixelWidth
);
```



## <a name="property-value"></a><span data-ttu-id="b14d3-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="b14d3-112">Property value</span></span>

<span data-ttu-id="b14d3-113">Larghezza, in pixel.</span><span class="sxs-lookup"><span data-stu-id="b14d3-113">The width, in pixels.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b14d3-114">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="b14d3-114">Error codes</span></span>



| <span data-ttu-id="b14d3-115">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="b14d3-115">Name/value</span></span>                                                                                                                                                         | <span data-ttu-id="b14d3-116">Significato</span><span class="sxs-lookup"><span data-stu-id="b14d3-116">Meaning</span></span>                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b14d3-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b14d3-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                            | <span data-ttu-id="b14d3-118">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="b14d3-118">The operation was successful.</span></span><br/>                                 |
| <dl> <span data-ttu-id="b14d3-119"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="b14d3-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>              | <span data-ttu-id="b14d3-120">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="b14d3-120">The parameter is **NULL**.</span></span><br/>                                    |
| <dl> <span data-ttu-id="b14d3-121"><dt>Macchina virtuale \_ \_VM E \_ non \_ in esecuzione</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="b14d3-121"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl> | <span data-ttu-id="b14d3-122">Per questa operazione è necessario che la macchina virtuale sia in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="b14d3-122">The virtual machine must be running for this operation.</span></span><br/>       |
| <dl> <span data-ttu-id="b14d3-123"><dt>Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="b14d3-123"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>      | <span data-ttu-id="b14d3-124">La macchina virtuale non è valida o non è attualmente in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="b14d3-124">The virtual machine is not valid or is not currently running.</span></span><br/> |
| <dl> <span data-ttu-id="b14d3-125"><dt>Macchina virtuale \_ E \_ Nessuna \_ visualizzazione</dt> <dt>0xA0040850</dt></span><span class="sxs-lookup"><span data-stu-id="b14d3-125"><dt>VM\_E\_NO\_DISPLAY</dt> <dt>0xA0040850</dt></span></span> </dl>      | <span data-ttu-id="b14d3-126">Non è possibile individuare una visualizzazione valida per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b14d3-126">Unable to locate a valid display for the virtual machine.</span></span><br/>     |
| <dl> <span data-ttu-id="b14d3-127"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="b14d3-127"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>      | <span data-ttu-id="b14d3-128">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="b14d3-128">An unexpected error has occurred.</span></span><br/>                             |



## <a name="requirements"></a><span data-ttu-id="b14d3-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b14d3-129">Requirements</span></span>



| <span data-ttu-id="b14d3-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="b14d3-130">Requirement</span></span> | <span data-ttu-id="b14d3-131">Valore</span><span class="sxs-lookup"><span data-stu-id="b14d3-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b14d3-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b14d3-132">Minimum supported client</span></span><br/> | <span data-ttu-id="b14d3-133">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="b14d3-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b14d3-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b14d3-134">Minimum supported server</span></span><br/> | <span data-ttu-id="b14d3-135">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="b14d3-135">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="b14d3-136">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="b14d3-136">End of client support</span></span><br/>    | <span data-ttu-id="b14d3-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b14d3-137">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="b14d3-138">Prodotto</span><span class="sxs-lookup"><span data-stu-id="b14d3-138">Product</span></span><br/>                  | <span data-ttu-id="b14d3-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="b14d3-139">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="b14d3-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b14d3-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="b14d3-141"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="b14d3-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="b14d3-142">IID</span><span class="sxs-lookup"><span data-stu-id="b14d3-142">IID</span></span><br/>                      | <span data-ttu-id="b14d3-143">IID \_ IVMDisplay è definito come 960895e9-f743-4498-96aa-261f867e7fc5</span><span class="sxs-lookup"><span data-stu-id="b14d3-143">IID\_IVMDisplay is defined as 960895e9-f743-4498-96aa-261f867e7fc5</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="b14d3-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b14d3-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b14d3-145">**IVMDisplay**</span><span class="sxs-lookup"><span data-stu-id="b14d3-145">**IVMDisplay**</span></span>](ivmdisplay.md)
</dt> </dl>

 

