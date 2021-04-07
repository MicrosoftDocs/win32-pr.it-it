---
title: Proprietà Height IVMDisplay (VPCCOMInterfaces. h)
description: Altezza, in pixel, della visualizzazione della macchina virtuale.
ms.assetid: 4fbb7c2b-6d5f-4af6-b8cc-3a7546b15cbd
keywords:
- Proprietà altezza PC virtuale
- Proprietà Height Virtual PC, interfaccia IVMDisplay
- Interfaccia IVMDisplay Virtual PC, proprietà Height
topic_type:
- apiref
api_name:
- IVMDisplay.Height
- IVMDisplay.get_Height
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab6ff5746c817dcc81b353f80e2daa345b5587fd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048436"
---
# <a name="ivmdisplayheight-property"></a><span data-ttu-id="fb414-106">Proprietà IVMDisplay:: Height</span><span class="sxs-lookup"><span data-stu-id="fb414-106">IVMDisplay::Height property</span></span>

<span data-ttu-id="fb414-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="fb414-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="fb414-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="fb414-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="fb414-109">Recupera l'altezza, in pixel, della visualizzazione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="fb414-109">Retrieves the height of the virtual machine's display, in pixels.</span></span>

<span data-ttu-id="fb414-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="fb414-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb414-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fb414-111">Syntax</span></span>


```C++
HRESULT get_Height(
  [out, retval] long *displayPixelHeight
);
```



## <a name="property-value"></a><span data-ttu-id="fb414-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="fb414-112">Property value</span></span>

<span data-ttu-id="fb414-113">Altezza, in pixel.</span><span class="sxs-lookup"><span data-stu-id="fb414-113">The height, in pixels.</span></span>

## <a name="error-codes"></a><span data-ttu-id="fb414-114">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="fb414-114">Error codes</span></span>



| <span data-ttu-id="fb414-115">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="fb414-115">Name/value</span></span>                                                                                                                                                         | <span data-ttu-id="fb414-116">Significato</span><span class="sxs-lookup"><span data-stu-id="fb414-116">Meaning</span></span>                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <span data-ttu-id="fb414-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="fb414-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                            | <span data-ttu-id="fb414-118">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="fb414-118">The operation was successful.</span></span><br/>                                 |
| <dl> <span data-ttu-id="fb414-119"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="fb414-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>              | <span data-ttu-id="fb414-120">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="fb414-120">The parameter is **NULL**.</span></span><br/>                                    |
| <dl> <span data-ttu-id="fb414-121"><dt>Macchina virtuale \_ \_VM E \_ non \_ in esecuzione</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="fb414-121"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl> | <span data-ttu-id="fb414-122">Per questa operazione è necessario che la macchina virtuale sia in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="fb414-122">The virtual machine must be running for this operation.</span></span><br/>       |
| <dl> <span data-ttu-id="fb414-123"><dt>Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="fb414-123"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>      | <span data-ttu-id="fb414-124">La macchina virtuale non è valida o non è attualmente in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="fb414-124">The virtual machine is not valid or is not currently running.</span></span><br/> |
| <dl> <span data-ttu-id="fb414-125"><dt>Macchina virtuale \_ E \_ Nessuna \_ visualizzazione</dt> <dt>0xA0040850</dt></span><span class="sxs-lookup"><span data-stu-id="fb414-125"><dt>VM\_E\_NO\_DISPLAY</dt> <dt>0xA0040850</dt></span></span> </dl>      | <span data-ttu-id="fb414-126">Non è possibile individuare una visualizzazione valida per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="fb414-126">Unable to locate a valid display for the virtual machine.</span></span><br/>     |
| <dl> <span data-ttu-id="fb414-127"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="fb414-127"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>      | <span data-ttu-id="fb414-128">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="fb414-128">An unexpected error has occurred.</span></span><br/>                             |



## <a name="requirements"></a><span data-ttu-id="fb414-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fb414-129">Requirements</span></span>



| <span data-ttu-id="fb414-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb414-130">Requirement</span></span> | <span data-ttu-id="fb414-131">Valore</span><span class="sxs-lookup"><span data-stu-id="fb414-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb414-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fb414-132">Minimum supported client</span></span><br/> | <span data-ttu-id="fb414-133">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="fb414-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fb414-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fb414-134">Minimum supported server</span></span><br/> | <span data-ttu-id="fb414-135">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="fb414-135">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="fb414-136">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="fb414-136">End of client support</span></span><br/>    | <span data-ttu-id="fb414-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="fb414-137">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="fb414-138">Prodotto</span><span class="sxs-lookup"><span data-stu-id="fb414-138">Product</span></span><br/>                  | <span data-ttu-id="fb414-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="fb414-139">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="fb414-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fb414-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="fb414-141"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="fb414-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="fb414-142">IID</span><span class="sxs-lookup"><span data-stu-id="fb414-142">IID</span></span><br/>                      | <span data-ttu-id="fb414-143">IID \_ IVMDisplay è definito come 960895e9-f743-4498-96aa-261f867e7fc5</span><span class="sxs-lookup"><span data-stu-id="fb414-143">IID\_IVMDisplay is defined as 960895e9-f743-4498-96aa-261f867e7fc5</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="fb414-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fb414-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb414-145">**IVMDisplay**</span><span class="sxs-lookup"><span data-stu-id="fb414-145">**IVMDisplay**</span></span>](ivmdisplay.md)
</dt> </dl>

 

