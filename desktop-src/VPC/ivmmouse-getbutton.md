---
title: Metodo GetButton IVMMouse (VPCCOMInterfaces. h)
description: Recupera lo stato corrente del pulsante del mouse specificato.
ms.assetid: eb534f88-387d-42fb-bfc3-bca17685021e
keywords:
- Metodo GetButton Virtual PC
- Metodo GetButton Virtual PC, interfaccia IVMMouse
- Interfaccia IVMMouse Virtual PC, Metodo GetButton
topic_type:
- apiref
api_name:
- IVMMouse.GetButton
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab73929a1fc9dfaa3942ed49f8a449343a594eec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743458"
---
# <a name="ivmmousegetbutton-method"></a><span data-ttu-id="39eef-106">Metodo IVMMouse:: GetButton</span><span class="sxs-lookup"><span data-stu-id="39eef-106">IVMMouse::GetButton method</span></span>

<span data-ttu-id="39eef-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="39eef-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="39eef-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="39eef-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="39eef-109">Recupera lo stato corrente (verso l'alto o verso il basso) del pulsante del mouse specificato.</span><span class="sxs-lookup"><span data-stu-id="39eef-109">Retrieves the current state (up or down) of the specified mouse button.</span></span>

## <a name="syntax"></a><span data-ttu-id="39eef-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="39eef-110">Syntax</span></span>


```C++
HRESULT GetButton(
  [in]          VMMouseButton buttonIndex,
  [out, retval] VARIANT_BOOL  *isDown
);
```



## <a name="parameters"></a><span data-ttu-id="39eef-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="39eef-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39eef-112">*ButtonIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="39eef-112">*buttonIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39eef-113">Indice del pulsante di cui viene richiesto lo stato.</span><span class="sxs-lookup"><span data-stu-id="39eef-113">The index of the button whose state is being requested.</span></span> <span data-ttu-id="39eef-114">Per un elenco di valori, vedere [**VMMouseButton**](vmmousebutton.md).</span><span class="sxs-lookup"><span data-stu-id="39eef-114">For a list of values, see [**VMMouseButton**](vmmousebutton.md).</span></span>

</dd> <dt>

<span data-ttu-id="39eef-115">in *basso* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="39eef-115">*isDown* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="39eef-116">Stato del pulsante indicato.</span><span class="sxs-lookup"><span data-stu-id="39eef-116">The state of the indicated button.</span></span> <span data-ttu-id="39eef-117">**True** se il pulsante è attualmente inattivo nella macchina virtuale; in caso contrario, **false** .</span><span class="sxs-lookup"><span data-stu-id="39eef-117">**TRUE** if the button is currently down in the virtual machine, **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39eef-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="39eef-118">Return value</span></span>

<span data-ttu-id="39eef-119">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="39eef-119">This method can return one of these values.</span></span>



| <span data-ttu-id="39eef-120">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="39eef-120">Return code/value</span></span>                                                                                                                                                        | <span data-ttu-id="39eef-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="39eef-121">Description</span></span>                                                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="39eef-122"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="39eef-122"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                              | <span data-ttu-id="39eef-123">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="39eef-123">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="39eef-124"><dt>**E \_ PUNTATORE**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="39eef-124"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                | <span data-ttu-id="39eef-125">Il parametro *UpDown* è **null**.</span><span class="sxs-lookup"><span data-stu-id="39eef-125">The *isDown* parameter is **NULL**.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="39eef-126"><dt>**E \_**</dt> <dt>0x80000003</dt> INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="39eef-126"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>             | <span data-ttu-id="39eef-127">Il parametro *ButtonIndex* non è valido.</span><span class="sxs-lookup"><span data-stu-id="39eef-127">The *buttonIndex* parameter is not valid.</span></span><br/>                                            |
| <dl> <span data-ttu-id="39eef-128"><dt>**Macchina virtuale \_ \_VM E \_ non \_ in esecuzione**</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="39eef-128"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>   | <span data-ttu-id="39eef-129">La macchina virtuale a cui questo dispositivo mouse è collegato non è attualmente in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="39eef-129">The virtual machine to which this mouse device is attached is not currently running.</span></span><br/> |
| <dl> <span data-ttu-id="39eef-130"><dt>**Macchina virtuale \_ E \_ mouse \_ non \_ attivo**</dt> <dt>0xA0040800</dt></span><span class="sxs-lookup"><span data-stu-id="39eef-130"><dt>**VM\_E\_MOUSE\_NOT\_ACTIVE**</dt> <dt>0xA0040800</dt></span></span> </dl> | <span data-ttu-id="39eef-131">Il dispositivo mouse non è stato alimentato.</span><span class="sxs-lookup"><span data-stu-id="39eef-131">The mouse device has not been powered up.</span></span><br/>                                            |
| <dl> <span data-ttu-id="39eef-132"><dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="39eef-132"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>        | <span data-ttu-id="39eef-133">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="39eef-133">An unexpected error has occurred.</span></span><br/>                                                    |



 

## <a name="requirements"></a><span data-ttu-id="39eef-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="39eef-134">Requirements</span></span>



| <span data-ttu-id="39eef-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="39eef-135">Requirement</span></span> | <span data-ttu-id="39eef-136">Valore</span><span class="sxs-lookup"><span data-stu-id="39eef-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="39eef-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="39eef-137">Minimum supported client</span></span><br/> | <span data-ttu-id="39eef-138">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="39eef-138">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="39eef-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="39eef-139">Minimum supported server</span></span><br/> | <span data-ttu-id="39eef-140">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="39eef-140">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="39eef-141">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="39eef-141">End of client support</span></span><br/>    | <span data-ttu-id="39eef-142">Windows 7</span><span class="sxs-lookup"><span data-stu-id="39eef-142">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="39eef-143">Prodotto</span><span class="sxs-lookup"><span data-stu-id="39eef-143">Product</span></span><br/>                  | <span data-ttu-id="39eef-144">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="39eef-144">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="39eef-145">Intestazione</span><span class="sxs-lookup"><span data-stu-id="39eef-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="39eef-146"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="39eef-146"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="39eef-147">IID</span><span class="sxs-lookup"><span data-stu-id="39eef-147">IID</span></span><br/>                      | <span data-ttu-id="39eef-148">IID \_ IVMmouse è definito come ac903f6d-6346-4F29-8875-5d511a13895e</span><span class="sxs-lookup"><span data-stu-id="39eef-148">IID\_IVMmouse is defined as ac903f6d-6346-4f29-8875-5d511a13895e</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="39eef-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="39eef-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39eef-150">**IVMMouse**</span><span class="sxs-lookup"><span data-stu-id="39eef-150">**IVMMouse**</span></span>](ivmmouse.md)
</dt> </dl>

 

