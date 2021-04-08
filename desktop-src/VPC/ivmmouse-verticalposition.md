---
title: Proprietà IVMMouse VerticalPosition (VPCCOMInterfaces. h)
description: Coordinata y assoluta del mouse.
ms.assetid: 02fd3677-95d8-44b4-b398-d3ec62e5d9f0
keywords:
- Proprietà VerticalPosition Virtual PC
- Proprietà VerticalPosition Virtual PC, interfaccia IVMMouse
- Interfaccia IVMMouse Virtual PC, proprietà VerticalPosition
topic_type:
- apiref
api_name:
- IVMMouse.VerticalPosition
- IVMMouse.get_VerticalPosition
- IVMMouse.put_VerticalPosition
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64712f557a3fcd59181e8ce65d835b630da68e48
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964870"
---
# <a name="ivmmouseverticalposition-property"></a><span data-ttu-id="f3c1c-106">Proprietà IVMMouse:: VerticalPosition</span><span class="sxs-lookup"><span data-stu-id="f3c1c-106">IVMMouse::VerticalPosition property</span></span>

<span data-ttu-id="f3c1c-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="f3c1c-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="f3c1c-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="f3c1c-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="f3c1c-109">Recupera la coordinata y assoluta del mouse.</span><span class="sxs-lookup"><span data-stu-id="f3c1c-109">Retrieves the absolute y-coordinate of the mouse.</span></span>

<span data-ttu-id="f3c1c-110">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="f3c1c-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3c1c-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f3c1c-111">Syntax</span></span>


```C++
HRESULT put_VerticalPosition(
  [in]          long position
);

HRESULT get_VerticalPosition(
  [out, retval] long *position
);
```



## <a name="property-value"></a><span data-ttu-id="f3c1c-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="f3c1c-112">Property value</span></span>

<span data-ttu-id="f3c1c-113">Coordinata y che indica la nuova posizione del mouse.</span><span class="sxs-lookup"><span data-stu-id="f3c1c-113">The y-coordinate indicating the new position of the mouse.</span></span> <span data-ttu-id="f3c1c-114">Quando si usano le coordinate assolute, questo valore specifica la nuova coordinata y del mouse.</span><span class="sxs-lookup"><span data-stu-id="f3c1c-114">When using absolute coordinates, this value specifies the new y-coordinate of the mouse.</span></span> <span data-ttu-id="f3c1c-115">Quando si usano le coordinate relative, questo valore specifica il numero di pixel che il mouse deve spostare nella direzione y.</span><span class="sxs-lookup"><span data-stu-id="f3c1c-115">When using relative coordinates, this value specifies the number of pixels the mouse should be moved in the y direction.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f3c1c-116">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="f3c1c-116">Error codes</span></span>



| <span data-ttu-id="f3c1c-117">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="f3c1c-117">Name/value</span></span>                                                                                                                                                                       | <span data-ttu-id="f3c1c-118">Significato</span><span class="sxs-lookup"><span data-stu-id="f3c1c-118">Meaning</span></span>                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f3c1c-119"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f3c1c-119"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="f3c1c-120">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="f3c1c-120">The operation was successful.</span></span><br/>                                                                                                                |
| <dl> <span data-ttu-id="f3c1c-121"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="f3c1c-121"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                            | <span data-ttu-id="f3c1c-122">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="f3c1c-122">The parameter is **NULL**.</span></span><br/>                                                                                                                   |
| <dl> <span data-ttu-id="f3c1c-123"><dt>Macchina virtuale \_ \_VM E \_ non \_ in esecuzione</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="f3c1c-123"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="f3c1c-124">La macchina virtuale a cui questo dispositivo mouse è collegato non è attualmente in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="f3c1c-124">The virtual machine to which this mouse device is attached is not currently running.</span></span><br/>                                                         |
| <dl> <span data-ttu-id="f3c1c-125"><dt>Macchina virtuale \_ E \_ funzionalità aggiuntive \_ \_ non \_ disponibili</dt> <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="f3c1c-125"><dt>VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="f3c1c-126">È necessario installare i componenti di integrazione per recuperare la posizione del mouse o per impostare la posizione del mouse quando si utilizzano le coordinate assolute.</span><span class="sxs-lookup"><span data-stu-id="f3c1c-126">Integration components must be installed to retrieve the mouse position, or to set the mouse position when using absolute coordinates.</span></span><br/>       |
| <dl> <span data-ttu-id="f3c1c-127"><dt>Macchina virtuale \_ E \_ utilizzo \_ di \_ coordinate relative</dt> <dt>0xA0040802</dt></span><span class="sxs-lookup"><span data-stu-id="f3c1c-127"><dt>VM\_E\_USING\_RELATIVE\_COORDINATES</dt> <dt>0xA0040802</dt></span></span> </dl>   | <span data-ttu-id="f3c1c-128">Il dispositivo mouse è attualmente impostato per l'utilizzo di coordinate relative del mouse.</span><span class="sxs-lookup"><span data-stu-id="f3c1c-128">The mouse device is currently set to use relative mouse coordinates.</span></span><br/>                                                                         |
| <dl> <span data-ttu-id="f3c1c-129"><dt>Macchina virtuale \_ E \_ mouse \_ non \_ attivo</dt> <dt>0xA0040800</dt></span><span class="sxs-lookup"><span data-stu-id="f3c1c-129"><dt>VM\_E\_MOUSE\_NOT\_ACTIVE</dt> <dt>0xA0040800</dt></span></span> </dl>             | <span data-ttu-id="f3c1c-130">Non è possibile recuperare le coordinate assolute se il dispositivo mouse non è acceso o se non è attualmente attivo nella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="f3c1c-130">The absolute coordinates cannot be retrieved if the mouse device is not powered up, or if it is not currently active in the virtual machine.</span></span><br/> |
| <dl> <span data-ttu-id="f3c1c-131"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="f3c1c-131"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="f3c1c-132">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="f3c1c-132">An unexpected error has occurred.</span></span><br/>                                                                                                            |



## <a name="remarks"></a><span data-ttu-id="f3c1c-133">Commenti</span><span class="sxs-lookup"><span data-stu-id="f3c1c-133">Remarks</span></span>

<span data-ttu-id="f3c1c-134">Impossibile recuperare questa proprietà quando si utilizzano le coordinate relative.</span><span class="sxs-lookup"><span data-stu-id="f3c1c-134">This property cannot be retrieved when using relative coordinates.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3c1c-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f3c1c-135">Requirements</span></span>



| <span data-ttu-id="f3c1c-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3c1c-136">Requirement</span></span> | <span data-ttu-id="f3c1c-137">Valore</span><span class="sxs-lookup"><span data-stu-id="f3c1c-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3c1c-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f3c1c-138">Minimum supported client</span></span><br/> | <span data-ttu-id="f3c1c-139">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="f3c1c-139">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f3c1c-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f3c1c-140">Minimum supported server</span></span><br/> | <span data-ttu-id="f3c1c-141">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="f3c1c-141">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="f3c1c-142">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="f3c1c-142">End of client support</span></span><br/>    | <span data-ttu-id="f3c1c-143">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f3c1c-143">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="f3c1c-144">Prodotto</span><span class="sxs-lookup"><span data-stu-id="f3c1c-144">Product</span></span><br/>                  | <span data-ttu-id="f3c1c-145">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="f3c1c-145">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="f3c1c-146">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f3c1c-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="f3c1c-147"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="f3c1c-147"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="f3c1c-148">IID</span><span class="sxs-lookup"><span data-stu-id="f3c1c-148">IID</span></span><br/>                      | <span data-ttu-id="f3c1c-149">IID \_ IVMmouse è definito come ac903f6d-6346-4F29-8875-5d511a13895e</span><span class="sxs-lookup"><span data-stu-id="f3c1c-149">IID\_IVMmouse is defined as ac903f6d-6346-4f29-8875-5d511a13895e</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="f3c1c-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f3c1c-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3c1c-151">**IVMMouse**</span><span class="sxs-lookup"><span data-stu-id="f3c1c-151">**IVMMouse**</span></span>](ivmmouse.md)
</dt> </dl>

 

