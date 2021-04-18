---
title: Proprietà IVMMouse UsingAbsoluteCoordinates (VPCCOMInterfaces. h)
description: Recupera un valore che indica se le coordinate del mouse rappresentano coordinate assolute o relative.
ms.assetid: 668278f8-28ae-4128-9653-4985bddbe184
keywords:
- Proprietà UsingAbsoluteCoordinates Virtual PC
- Proprietà UsingAbsoluteCoordinates Virtual PC, interfaccia IVMMouse
- Interfaccia IVMMouse Virtual PC, proprietà UsingAbsoluteCoordinates
topic_type:
- apiref
api_name:
- IVMMouse.UsingAbsoluteCoordinates
- IVMMouse.get_UsingAbsoluteCoordinates
- IVMMouse.put_UsingAbsoluteCoordinates
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc216466ab8ef0483d3c1a229f6a493d4ba913dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518712"
---
# <a name="ivmmouseusingabsolutecoordinates-property"></a><span data-ttu-id="e6e7b-106">Proprietà IVMMouse:: UsingAbsoluteCoordinates</span><span class="sxs-lookup"><span data-stu-id="e6e7b-106">IVMMouse::UsingAbsoluteCoordinates property</span></span>

<span data-ttu-id="e6e7b-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="e6e7b-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="e6e7b-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="e6e7b-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="e6e7b-109">Recupera un valore che indica se le coordinate del mouse rappresentano coordinate assolute o relative.</span><span class="sxs-lookup"><span data-stu-id="e6e7b-109">Retrieves whether mouse coordinates represent absolute or relative coordinates.</span></span>

<span data-ttu-id="e6e7b-110">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="e6e7b-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6e7b-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e6e7b-111">Syntax</span></span>


```C++
HRESULT put_UsingAbsoluteCoordinates(
  [in]          VARIANT_BOOL usingAbsoluteCoordinates
);

HRESULT get_UsingAbsoluteCoordinates(
  [out, retval] VARIANT_BOOL *usingAbsoluteCoordinates
);
```



## <a name="property-value"></a><span data-ttu-id="e6e7b-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="e6e7b-112">Property value</span></span>

<span data-ttu-id="e6e7b-113">**Variante \_ TRUE** per impostare il dispositivo mouse per utilizzare coordinate assolute, **Variant \_ false** per utilizzare le coordinate relative.</span><span class="sxs-lookup"><span data-stu-id="e6e7b-113">**VARIANT\_TRUE** to set the mouse device to use absolute coordinates, **VARIANT\_FALSE** to use relative coordinates.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e6e7b-114">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="e6e7b-114">Error codes</span></span>



| <span data-ttu-id="e6e7b-115">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="e6e7b-115">Name/value</span></span>                                                                                                                                                                       | <span data-ttu-id="e6e7b-116">Significato</span><span class="sxs-lookup"><span data-stu-id="e6e7b-116">Meaning</span></span>                                                                                                               |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e6e7b-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e6e7b-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="e6e7b-118">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="e6e7b-118">The operation was successful.</span></span><br/>                                                                              |
| <dl> <span data-ttu-id="e6e7b-119"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="e6e7b-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                            | <span data-ttu-id="e6e7b-120">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="e6e7b-120">The parameter is **NULL**.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="e6e7b-121"><dt>Macchina virtuale \_ \_VM E \_ non \_ in esecuzione</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="e6e7b-121"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="e6e7b-122">La macchina virtuale a cui questo dispositivo mouse è collegato non è attualmente in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="e6e7b-122">The virtual machine to which this mouse device is attached is not currently running.</span></span><br/>                       |
| <dl> <span data-ttu-id="e6e7b-123"><dt>Macchina virtuale \_ E \_ funzionalità aggiuntive \_ \_ non \_ disponibili</dt> <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="e6e7b-123"><dt>VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="e6e7b-124">I componenti di integrazione non sono installati.</span><span class="sxs-lookup"><span data-stu-id="e6e7b-124">Integration components are not installed.</span></span> <span data-ttu-id="e6e7b-125">I componenti di integrazione sono necessari per usare le coordinate assolute.</span><span class="sxs-lookup"><span data-stu-id="e6e7b-125">Integration components are required to use absolute coordinates.</span></span><br/> |
| <dl> <span data-ttu-id="e6e7b-126"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="e6e7b-126"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="e6e7b-127">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="e6e7b-127">An unexpected error has occurred.</span></span><br/>                                                                          |



## <a name="remarks"></a><span data-ttu-id="e6e7b-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="e6e7b-128">Remarks</span></span>

<span data-ttu-id="e6e7b-129">Questa proprietà è locale solo per questo oggetto e per impostazione predefinita viene impostato su **Variant \_ false** per un nuovo oggetto [**IVMMouse**](ivmmouse.md) .</span><span class="sxs-lookup"><span data-stu-id="e6e7b-129">This property is local only to this object and will default to **VARIANT\_FALSE** for a new [**IVMMouse**](ivmmouse.md) object.</span></span> <span data-ttu-id="e6e7b-130">Si noti che è necessario installare i componenti di integrazione per usare le coordinate assolute.</span><span class="sxs-lookup"><span data-stu-id="e6e7b-130">Note that integration components must be installed in order to use absolute coordinates.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6e7b-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e6e7b-131">Requirements</span></span>



| <span data-ttu-id="e6e7b-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6e7b-132">Requirement</span></span> | <span data-ttu-id="e6e7b-133">Valore</span><span class="sxs-lookup"><span data-stu-id="e6e7b-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6e7b-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e6e7b-134">Minimum supported client</span></span><br/> | <span data-ttu-id="e6e7b-135">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="e6e7b-135">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e6e7b-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e6e7b-136">Minimum supported server</span></span><br/> | <span data-ttu-id="e6e7b-137">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="e6e7b-137">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="e6e7b-138">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="e6e7b-138">End of client support</span></span><br/>    | <span data-ttu-id="e6e7b-139">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e6e7b-139">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="e6e7b-140">Prodotto</span><span class="sxs-lookup"><span data-stu-id="e6e7b-140">Product</span></span><br/>                  | <span data-ttu-id="e6e7b-141">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="e6e7b-141">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="e6e7b-142">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e6e7b-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="e6e7b-143"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="e6e7b-143"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="e6e7b-144">IID</span><span class="sxs-lookup"><span data-stu-id="e6e7b-144">IID</span></span><br/>                      | <span data-ttu-id="e6e7b-145">IID \_ IVMmouse è definito come ac903f6d-6346-4F29-8875-5d511a13895e</span><span class="sxs-lookup"><span data-stu-id="e6e7b-145">IID\_IVMmouse is defined as ac903f6d-6346-4f29-8875-5d511a13895e</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="e6e7b-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e6e7b-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6e7b-147">**IVMMouse**</span><span class="sxs-lookup"><span data-stu-id="e6e7b-147">**IVMMouse**</span></span>](ivmmouse.md)
</dt> </dl>

 

