---
title: Proprietà IVMMouse ScrollWheelPosition (VPCCOMInterfaces. h)
description: Regola la coordinata z del mouse (solo relativa).
ms.assetid: 52269d0c-a7a8-4dc2-bb27-c891d1e9c293
keywords:
- Proprietà ScrollWheelPosition Virtual PC
- Proprietà ScrollWheelPosition Virtual PC, interfaccia IVMMouse
- Interfaccia IVMMouse Virtual PC, proprietà ScrollWheelPosition
topic_type:
- apiref
api_name:
- IVMMouse.ScrollWheelPosition
- IVMMouse.put_ScrollWheelPosition
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e374011dc87ad00d4edef1f33e9787d5a2e6d787
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743455"
---
# <a name="ivmmousescrollwheelposition-property"></a><span data-ttu-id="61d94-106">Proprietà IVMMouse:: ScrollWheelPosition</span><span class="sxs-lookup"><span data-stu-id="61d94-106">IVMMouse::ScrollWheelPosition property</span></span>

<span data-ttu-id="61d94-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="61d94-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="61d94-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="61d94-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="61d94-109">Regola la coordinata z del mouse (solo relativa).</span><span class="sxs-lookup"><span data-stu-id="61d94-109">Adjusts the z-coordinate of the mouse (relative only).</span></span>

<span data-ttu-id="61d94-110">Questa proprietà è di sola scrittura.</span><span class="sxs-lookup"><span data-stu-id="61d94-110">This property is write-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="61d94-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="61d94-111">Syntax</span></span>


```C++
HRESULT put_ScrollWheelPosition(
  [in] long position
);
```



## <a name="property-value"></a><span data-ttu-id="61d94-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="61d94-112">Property value</span></span>

<span data-ttu-id="61d94-113">Coordinata z che indica il numero di pixel che il mouse deve spostare lungo l'asse z.</span><span class="sxs-lookup"><span data-stu-id="61d94-113">The z-coordinate indicating the number of pixels the mouse is to be moved along the z-axis.</span></span>

## <a name="error-codes"></a><span data-ttu-id="61d94-114">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="61d94-114">Error codes</span></span>



| <span data-ttu-id="61d94-115">Nome/valore</span><span class="sxs-lookup"><span data-stu-id="61d94-115">Name/value</span></span>                                                                                                                                                                     | <span data-ttu-id="61d94-116">Significato</span><span class="sxs-lookup"><span data-stu-id="61d94-116">Meaning</span></span>                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="61d94-117"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="61d94-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                        | <span data-ttu-id="61d94-118">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="61d94-118">The operation was successful.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="61d94-119"><dt>Macchina virtuale \_ \_VM E \_ non \_ in esecuzione</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="61d94-119"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl>             | <span data-ttu-id="61d94-120">La macchina virtuale a cui questo dispositivo mouse è collegato non è attualmente in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="61d94-120">The virtual machine to which this mouse device is attached is not currently running.</span></span><br/>         |
| <dl> <span data-ttu-id="61d94-121"><dt>Macchina virtuale \_ E \_ mouse \_ non \_ attivo</dt> <dt>0xA0040800</dt></span><span class="sxs-lookup"><span data-stu-id="61d94-121"><dt>VM\_E\_MOUSE\_NOT\_ACTIVE</dt> <dt>0xA0040800</dt></span></span> </dl>           | <span data-ttu-id="61d94-122">Il dispositivo mouse non è stato alimentato o non è attualmente attivo nella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="61d94-122">The mouse device has not been powered up, or is not currently active in the virtual machine.</span></span><br/> |
| <dl> <span data-ttu-id="61d94-123"><dt>Macchina virtuale \_ E \_ utilizzo \_ delle \_ coordinate assolute</dt> <dt>0xA0040801</dt></span><span class="sxs-lookup"><span data-stu-id="61d94-123"><dt>VM\_E\_USING\_ABSOLUTE\_COORDINATES</dt> <dt>0xA0040801</dt></span></span> </dl> | <span data-ttu-id="61d94-124">Impossibile impostare la posizione della rotellina di scorrimento quando il dispositivo mouse utilizza coordinate assolute.</span><span class="sxs-lookup"><span data-stu-id="61d94-124">The scroll wheel position cannot be set when the mouse device is using absolute coordinates.</span></span><br/> |
| <dl> <span data-ttu-id="61d94-125"><dt>Disp \_ 0x80020009 \_ eccezione E</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="61d94-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                  | <span data-ttu-id="61d94-126">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="61d94-126">An unexpected error has occurred.</span></span><br/>                                                            |



## <a name="requirements"></a><span data-ttu-id="61d94-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="61d94-127">Requirements</span></span>



| <span data-ttu-id="61d94-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="61d94-128">Requirement</span></span> | <span data-ttu-id="61d94-129">Valore</span><span class="sxs-lookup"><span data-stu-id="61d94-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="61d94-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="61d94-130">Minimum supported client</span></span><br/> | <span data-ttu-id="61d94-131">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="61d94-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="61d94-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="61d94-132">Minimum supported server</span></span><br/> | <span data-ttu-id="61d94-133">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="61d94-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="61d94-134">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="61d94-134">End of client support</span></span><br/>    | <span data-ttu-id="61d94-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="61d94-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="61d94-136">Prodotto</span><span class="sxs-lookup"><span data-stu-id="61d94-136">Product</span></span><br/>                  | <span data-ttu-id="61d94-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="61d94-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="61d94-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="61d94-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="61d94-139"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="61d94-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="61d94-140">IID</span><span class="sxs-lookup"><span data-stu-id="61d94-140">IID</span></span><br/>                      | <span data-ttu-id="61d94-141">IID \_ IVMmouse è definito come ac903f6d-6346-4F29-8875-5d511a13895e</span><span class="sxs-lookup"><span data-stu-id="61d94-141">IID\_IVMmouse is defined as ac903f6d-6346-4f29-8875-5d511a13895e</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="61d94-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="61d94-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61d94-143">**IVMMouse**</span><span class="sxs-lookup"><span data-stu-id="61d94-143">**IVMMouse**</span></span>](ivmmouse.md)
</dt> </dl>

 

