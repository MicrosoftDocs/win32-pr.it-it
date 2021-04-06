---
title: Proprietà IVMDisplay CanResize (VPCCOMInterfaces. h)
description: Determina se il Guest consente le modifiche di risoluzione.
ms.assetid: 97f2aad9-aa27-4db2-ac5d-fa9645f0e674
keywords:
- Proprietà CanResize Virtual PC
- Proprietà CanResize Virtual PC, interfaccia IVMDisplay
- Interfaccia IVMDisplay Virtual PC, proprietà CanResize
topic_type:
- apiref
api_name:
- IVMDisplay.CanResize
- IVMDisplay.get_CanResize
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca865189b1fd155e0edf85bac9a36d94ffe5d656
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743471"
---
# <a name="ivmdisplaycanresize-property"></a><span data-ttu-id="fab44-106">Proprietà IVMDisplay:: CanResize</span><span class="sxs-lookup"><span data-stu-id="fab44-106">IVMDisplay::CanResize property</span></span>

<span data-ttu-id="fab44-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="fab44-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="fab44-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="fab44-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="fab44-109">Determina se il Guest consente le modifiche di risoluzione.</span><span class="sxs-lookup"><span data-stu-id="fab44-109">Determines whether the Guest allows resolution changes.</span></span>

<span data-ttu-id="fab44-110">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="fab44-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="fab44-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fab44-111">Syntax</span></span>


```C++
HRESULT get_CanResize(
  [out, retval] VARIANT_BOOL *canResize
);
```



## <a name="property-value"></a><span data-ttu-id="fab44-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="fab44-112">Property value</span></span>

<span data-ttu-id="fab44-113">**Variante \_ TRUE** se il Guest consente modifiche di risoluzione e **Variant \_ false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="fab44-113">**VARIANT\_TRUE** if the Guest allows resolution changes and **VARIANT\_FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="fab44-114">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="fab44-114">Error codes</span></span>



| <span data-ttu-id="fab44-115">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="fab44-115">Name/value</span></span>                                                                                                                                                                       | <span data-ttu-id="fab44-116">Significato</span><span class="sxs-lookup"><span data-stu-id="fab44-116">Meaning</span></span>                                                                                                                                               |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="fab44-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="fab44-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="fab44-118">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="fab44-118">The operation was successful.</span></span><br/>                                                                                                              |
| <dl> <span data-ttu-id="fab44-119"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="fab44-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                            | <span data-ttu-id="fab44-120">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="fab44-120">The parameter is **NULL**.</span></span><br/>                                                                                                                 |
| <dl> <span data-ttu-id="fab44-121"><dt>Macchina virtuale \_ 0xA0040207 E \_ VM \_ sconosciute</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="fab44-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>                    | <span data-ttu-id="fab44-122">La configurazione è sconosciuta.</span><span class="sxs-lookup"><span data-stu-id="fab44-122">The configuration is unknown.</span></span><br/>                                                                                                              |
| <dl> <span data-ttu-id="fab44-123"><dt>Macchina virtuale \_ \_VM E \_ non \_ in esecuzione</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="fab44-123"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="fab44-124">Per questa operazione è necessario che la macchina virtuale sia in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="fab44-124">The virtual machine must be running for this operation.</span></span><br/>                                                                                    |
| <dl> <span data-ttu-id="fab44-125"><dt>Macchina virtuale \_ E \_ Nessuna \_ visualizzazione</dt> <dt>0xA0040850</dt></span><span class="sxs-lookup"><span data-stu-id="fab44-125"><dt>VM\_E\_NO\_DISPLAY</dt> <dt>0xA0040850</dt></span></span> </dl>                    | <span data-ttu-id="fab44-126">Non sono stati trovati dispositivi video per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="fab44-126">There was no video device found for the virtual machine.</span></span><br/>                                                                                   |
| <dl> <span data-ttu-id="fab44-127"><dt>Macchina virtuale \_ E \_ funzionalità aggiuntive \_ \_ non \_ disponibili</dt> <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="fab44-127"><dt>VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="fab44-128">La funzionalità componenti di integrazione non è disponibile. i componenti di integrazione non sono installati o la funzionalità è stata disabilitata.</span><span class="sxs-lookup"><span data-stu-id="fab44-128">The integration components feature is not available; either the integration components are not installed or the feature has been disabled.</span></span><br/> |
| <dl> <span data-ttu-id="fab44-129"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="fab44-129"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="fab44-130">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="fab44-130">An unexpected error has occurred.</span></span><br/>                                                                                                          |



## <a name="requirements"></a><span data-ttu-id="fab44-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fab44-131">Requirements</span></span>



| <span data-ttu-id="fab44-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="fab44-132">Requirement</span></span> | <span data-ttu-id="fab44-133">Valore</span><span class="sxs-lookup"><span data-stu-id="fab44-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="fab44-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fab44-134">Minimum supported client</span></span><br/> | <span data-ttu-id="fab44-135">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="fab44-135">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fab44-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fab44-136">Minimum supported server</span></span><br/> | <span data-ttu-id="fab44-137">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="fab44-137">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="fab44-138">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="fab44-138">End of client support</span></span><br/>    | <span data-ttu-id="fab44-139">Windows 7</span><span class="sxs-lookup"><span data-stu-id="fab44-139">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="fab44-140">Prodotto</span><span class="sxs-lookup"><span data-stu-id="fab44-140">Product</span></span><br/>                  | <span data-ttu-id="fab44-141">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="fab44-141">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="fab44-142">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fab44-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="fab44-143"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="fab44-143"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="fab44-144">IID</span><span class="sxs-lookup"><span data-stu-id="fab44-144">IID</span></span><br/>                      | <span data-ttu-id="fab44-145">IID \_ IVMDisplay è definito come 960895e9-f743-4498-96aa-261f867e7fc5</span><span class="sxs-lookup"><span data-stu-id="fab44-145">IID\_IVMDisplay is defined as 960895e9-f743-4498-96aa-261f867e7fc5</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="fab44-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fab44-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fab44-147">**IVMDisplay**</span><span class="sxs-lookup"><span data-stu-id="fab44-147">**IVMDisplay**</span></span>](ivmdisplay.md)
</dt> </dl>

 

