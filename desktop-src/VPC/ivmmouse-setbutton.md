---
title: Metodo IVMMouse (VPCCOMInterfaces. h)
description: Imposta lo stato corrente (verso l'alto o verso il basso) del pulsante del mouse specificato.
ms.assetid: 52b24472-68d6-4a42-8ae5-b1434a6d67f3
keywords:
- Metodo sebutton Virtual PC
- Metodo sebutton Virtual PC, interfaccia IVMMouse
- Interfaccia IVMMouse Virtual PC, metodo sebutton
topic_type:
- apiref
api_name:
- IVMMouse.SetButton
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2d30ae131ac33eeff339b98511fd2da60a1e606
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121102"
---
# <a name="ivmmousesetbutton-method"></a><span data-ttu-id="958a1-106">Metodo IVMMouse:: MyButton</span><span class="sxs-lookup"><span data-stu-id="958a1-106">IVMMouse::SetButton method</span></span>

<span data-ttu-id="958a1-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="958a1-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="958a1-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="958a1-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="958a1-109">Imposta lo stato corrente (verso l'alto o verso il basso) del pulsante del mouse specificato.</span><span class="sxs-lookup"><span data-stu-id="958a1-109">Sets the current state (up or down) of the specified mouse button.</span></span>

## <a name="syntax"></a><span data-ttu-id="958a1-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="958a1-110">Syntax</span></span>


```C++
HRESULT SetButton(
  [in] VMMouseButton buttonIndex,
  [in] VARIANT_BOOL  down
);
```



## <a name="parameters"></a><span data-ttu-id="958a1-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="958a1-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="958a1-112">*ButtonIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="958a1-112">*buttonIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="958a1-113">Indice del pulsante.</span><span class="sxs-lookup"><span data-stu-id="958a1-113">The button index.</span></span> <span data-ttu-id="958a1-114">Per un elenco di valori, vedere [**VMMouseButton**](vmmousebutton.md).</span><span class="sxs-lookup"><span data-stu-id="958a1-114">For a list of values, see [**VMMouseButton**](vmmousebutton.md).</span></span>

</dd> <dt>

<span data-ttu-id="958a1-115">in *basso* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="958a1-115">*down* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="958a1-116">Nuovo stato del pulsante.</span><span class="sxs-lookup"><span data-stu-id="958a1-116">The new button state.</span></span> <span data-ttu-id="958a1-117">Utilizzare **true** se lo stato del pulsante deve essere impostato su inattivo e **false** se deve essere impostato su up.</span><span class="sxs-lookup"><span data-stu-id="958a1-117">Use **TRUE** if the button state is to be set to down, and **FALSE** if it is to be set to up.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="958a1-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="958a1-118">Return value</span></span>

<span data-ttu-id="958a1-119">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="958a1-119">This method can return one of these values.</span></span>



| <span data-ttu-id="958a1-120">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="958a1-120">Return code/value</span></span>                                                                                                                                                        | <span data-ttu-id="958a1-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="958a1-121">Description</span></span>                                                                                                                                       |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="958a1-122"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="958a1-122"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                              | <span data-ttu-id="958a1-123">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="958a1-123">The operation was successful.</span></span><br/>                                                                                                          |
| <dl> <span data-ttu-id="958a1-124"><dt>**E \_**</dt> <dt>0x80000003</dt> INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="958a1-124"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>             | <span data-ttu-id="958a1-125">Il parametro *ButtonIndex* non è valido.</span><span class="sxs-lookup"><span data-stu-id="958a1-125">The *buttonIndex* parameter is not valid.</span></span><br/>                                                                                              |
| <dl> <span data-ttu-id="958a1-126"><dt>**Macchina virtuale \_ \_VM E \_ non \_ in esecuzione**</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="958a1-126"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>   | <span data-ttu-id="958a1-127">La macchina virtuale a cui questo dispositivo mouse è collegato non è attualmente in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="958a1-127">The virtual machine to which this mouse device is attached is not currently running.</span></span><br/>                                                   |
| <dl> <span data-ttu-id="958a1-128"><dt>**Macchina virtuale \_ E \_ mouse \_ non \_ attivo**</dt> <dt>0xA0040800</dt></span><span class="sxs-lookup"><span data-stu-id="958a1-128"><dt>**VM\_E\_MOUSE\_NOT\_ACTIVE**</dt> <dt>0xA0040800</dt></span></span> </dl> | <span data-ttu-id="958a1-129">Non è stato possibile completare l'operazione perché il dispositivo mouse non è acceso o non è attualmente attivo nella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="958a1-129">The operation could not be completed because the mouse device is not powered up, or it is not currently active in the virtual machine.</span></span><br/> |
| <dl> <span data-ttu-id="958a1-130"><dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="958a1-130"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>        | <span data-ttu-id="958a1-131">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="958a1-131">An unexpected error has occurred.</span></span><br/>                                                                                                      |



 

## <a name="requirements"></a><span data-ttu-id="958a1-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="958a1-132">Requirements</span></span>



| <span data-ttu-id="958a1-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="958a1-133">Requirement</span></span> | <span data-ttu-id="958a1-134">Valore</span><span class="sxs-lookup"><span data-stu-id="958a1-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="958a1-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="958a1-135">Minimum supported client</span></span><br/> | <span data-ttu-id="958a1-136">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="958a1-136">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="958a1-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="958a1-137">Minimum supported server</span></span><br/> | <span data-ttu-id="958a1-138">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="958a1-138">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="958a1-139">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="958a1-139">End of client support</span></span><br/>    | <span data-ttu-id="958a1-140">Windows 7</span><span class="sxs-lookup"><span data-stu-id="958a1-140">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="958a1-141">Prodotto</span><span class="sxs-lookup"><span data-stu-id="958a1-141">Product</span></span><br/>                  | <span data-ttu-id="958a1-142">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="958a1-142">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="958a1-143">Intestazione</span><span class="sxs-lookup"><span data-stu-id="958a1-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="958a1-144"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="958a1-144"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="958a1-145">IID</span><span class="sxs-lookup"><span data-stu-id="958a1-145">IID</span></span><br/>                      | <span data-ttu-id="958a1-146">IID \_ IVMmouse è definito come ac903f6d-6346-4F29-8875-5d511a13895e</span><span class="sxs-lookup"><span data-stu-id="958a1-146">IID\_IVMmouse is defined as ac903f6d-6346-4f29-8875-5d511a13895e</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="958a1-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="958a1-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="958a1-148">**IVMMouse**</span><span class="sxs-lookup"><span data-stu-id="958a1-148">**IVMMouse**</span></span>](ivmmouse.md)
</dt> </dl>

 

