---
title: Proprietà IVMMouse HorizontalPosition (VPCCOMInterfaces. h)
description: Coordinata x assoluta del mouse.
ms.assetid: 8cf2a247-b6db-49f6-8e19-c862004f26cd
keywords:
- Proprietà HorizontalPosition Virtual PC
- Proprietà HorizontalPosition Virtual PC, interfaccia IVMMouse
- Interfaccia IVMMouse Virtual PC, proprietà HorizontalPosition
topic_type:
- apiref
api_name:
- IVMMouse.HorizontalPosition
- IVMMouse.get_HorizontalPosition
- IVMMouse.put_HorizontalPosition
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8506ad0d4583b9829ca2b1832686d32e67ded261
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964871"
---
# <a name="ivmmousehorizontalposition-property"></a><span data-ttu-id="4392a-106">Proprietà IVMMouse:: HorizontalPosition</span><span class="sxs-lookup"><span data-stu-id="4392a-106">IVMMouse::HorizontalPosition property</span></span>

<span data-ttu-id="4392a-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="4392a-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="4392a-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="4392a-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="4392a-109">Recupera la coordinata x assoluta del mouse.</span><span class="sxs-lookup"><span data-stu-id="4392a-109">Retrieves the absolute x-coordinate of the mouse.</span></span>

<span data-ttu-id="4392a-110">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="4392a-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="4392a-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4392a-111">Syntax</span></span>


```C++
HRESULT put_HorizontalPosition(
  [in]          long position
);

HRESULT get_HorizontalPosition(
  [out, retval] long *position
);
```



## <a name="property-value"></a><span data-ttu-id="4392a-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="4392a-112">Property value</span></span>

<span data-ttu-id="4392a-113">Coordinata x che indica la nuova posizione del mouse.</span><span class="sxs-lookup"><span data-stu-id="4392a-113">The x-coordinate indicating the new position of the mouse.</span></span> <span data-ttu-id="4392a-114">Quando si usano le coordinate assolute, questo valore specifica la nuova coordinata x del mouse.</span><span class="sxs-lookup"><span data-stu-id="4392a-114">When using absolute coordinates, this value specifies the new x-coordinate of the mouse.</span></span> <span data-ttu-id="4392a-115">Quando si usano le coordinate relative, questo valore specifica il numero di pixel che il mouse deve spostare nella direzione x.</span><span class="sxs-lookup"><span data-stu-id="4392a-115">When using relative coordinates, this value specifies the number of pixels the mouse should be moved in the x direction.</span></span>

## <a name="error-codes"></a><span data-ttu-id="4392a-116">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="4392a-116">Error codes</span></span>



| <span data-ttu-id="4392a-117">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="4392a-117">Name/value</span></span>                                                                                                                                                                       | <span data-ttu-id="4392a-118">Significato</span><span class="sxs-lookup"><span data-stu-id="4392a-118">Meaning</span></span>                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4392a-119"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="4392a-119"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="4392a-120">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="4392a-120">The operation was successful.</span></span><br/>                                                                                                                |
| <dl> <span data-ttu-id="4392a-121"><dt>E \_ PUNTATORE</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="4392a-121"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                            | <span data-ttu-id="4392a-122">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="4392a-122">The parameter is **NULL**.</span></span><br/>                                                                                                                   |
| <dl> <span data-ttu-id="4392a-123"><dt>Macchina virtuale \_ \_VM E \_ non \_ in esecuzione</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="4392a-123"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="4392a-124">La macchina virtuale a cui questo dispositivo mouse è collegato non è attualmente in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="4392a-124">The virtual machine to which this mouse device is attached is not currently running.</span></span><br/>                                                         |
| <dl> <span data-ttu-id="4392a-125"><dt>Macchina virtuale \_ E \_ funzionalità aggiuntive \_ \_ non \_ disponibili</dt> <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="4392a-125"><dt>VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="4392a-126">È necessario installare i componenti di integrazione per recuperare la posizione del mouse o per impostare la posizione del mouse quando si utilizzano le coordinate assolute.</span><span class="sxs-lookup"><span data-stu-id="4392a-126">Integration components must be installed to retrieve the mouse position, or to set the mouse position when using absolute coordinates.</span></span><br/>       |
| <dl> <span data-ttu-id="4392a-127"><dt>Macchina virtuale \_ E \_ utilizzo \_ di \_ coordinate relative</dt> <dt>0xA0040802</dt></span><span class="sxs-lookup"><span data-stu-id="4392a-127"><dt>VM\_E\_USING\_RELATIVE\_COORDINATES</dt> <dt>0xA0040802</dt></span></span> </dl>   | <span data-ttu-id="4392a-128">Il dispositivo mouse è attualmente impostato per l'utilizzo di coordinate relative del mouse.</span><span class="sxs-lookup"><span data-stu-id="4392a-128">The mouse device is currently set to use relative mouse coordinates.</span></span><br/>                                                                         |
| <dl> <span data-ttu-id="4392a-129"><dt>Macchina virtuale \_ E \_ mouse \_ non \_ attivo</dt> <dt>0xA0040800</dt></span><span class="sxs-lookup"><span data-stu-id="4392a-129"><dt>VM\_E\_MOUSE\_NOT\_ACTIVE</dt> <dt>0xA0040800</dt></span></span> </dl>             | <span data-ttu-id="4392a-130">Non è possibile recuperare le coordinate assolute se il dispositivo mouse non è acceso o se non è attualmente attivo nella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="4392a-130">The absolute coordinates cannot be retrieved if the mouse device is not powered up, or if it is not currently active in the virtual machine.</span></span><br/> |
| <dl> <span data-ttu-id="4392a-131"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="4392a-131"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="4392a-132">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="4392a-132">An unexpected error has occurred.</span></span><br/>                                                                                                            |



## <a name="remarks"></a><span data-ttu-id="4392a-133">Commenti</span><span class="sxs-lookup"><span data-stu-id="4392a-133">Remarks</span></span>

<span data-ttu-id="4392a-134">Impossibile recuperare questa proprietà quando si utilizzano le coordinate relative.</span><span class="sxs-lookup"><span data-stu-id="4392a-134">This property cannot be retrieved when using relative coordinates.</span></span>

## <a name="requirements"></a><span data-ttu-id="4392a-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4392a-135">Requirements</span></span>



| <span data-ttu-id="4392a-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="4392a-136">Requirement</span></span> | <span data-ttu-id="4392a-137">Valore</span><span class="sxs-lookup"><span data-stu-id="4392a-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="4392a-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4392a-138">Minimum supported client</span></span><br/> | <span data-ttu-id="4392a-139">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="4392a-139">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4392a-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4392a-140">Minimum supported server</span></span><br/> | <span data-ttu-id="4392a-141">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="4392a-141">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="4392a-142">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="4392a-142">End of client support</span></span><br/>    | <span data-ttu-id="4392a-143">Windows 7</span><span class="sxs-lookup"><span data-stu-id="4392a-143">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="4392a-144">Prodotto</span><span class="sxs-lookup"><span data-stu-id="4392a-144">Product</span></span><br/>                  | <span data-ttu-id="4392a-145">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="4392a-145">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="4392a-146">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4392a-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="4392a-147"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="4392a-147"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="4392a-148">IID</span><span class="sxs-lookup"><span data-stu-id="4392a-148">IID</span></span><br/>                      | <span data-ttu-id="4392a-149">IID \_ IVMmouse è definito come ac903f6d-6346-4F29-8875-5d511a13895e</span><span class="sxs-lookup"><span data-stu-id="4392a-149">IID\_IVMmouse is defined as ac903f6d-6346-4f29-8875-5d511a13895e</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="4392a-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4392a-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4392a-151">**IVMMouse**</span><span class="sxs-lookup"><span data-stu-id="4392a-151">**IVMMouse**</span></span>](ivmmouse.md)
</dt> </dl>

 

