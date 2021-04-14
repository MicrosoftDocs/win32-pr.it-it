---
title: Metodo Click IVMMouse (VPCCOMInterfaces. h)
description: Simula un clic del pulsante del mouse.
ms.assetid: f16e36d6-34ca-4d65-95e4-1a6660d0abd0
keywords:
- Fare clic su metodo Virtual PC
- Fare clic su metodo Virtual PC, interfaccia IVMMouse
- Interfaccia IVMMouse Virtual PC, metodo click
topic_type:
- apiref
api_name:
- IVMMouse.Click
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad3ea1b861db0a92ad92e689770182d225778aee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479000"
---
# <a name="ivmmouseclick-method"></a><span data-ttu-id="95d74-106">Metodo IVMMouse:: click</span><span class="sxs-lookup"><span data-stu-id="95d74-106">IVMMouse::Click method</span></span>

<span data-ttu-id="95d74-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="95d74-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="95d74-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="95d74-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="95d74-109">Simula un clic del pulsante del mouse.</span><span class="sxs-lookup"><span data-stu-id="95d74-109">Simulates a mouse button click.</span></span>

## <a name="syntax"></a><span data-ttu-id="95d74-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="95d74-110">Syntax</span></span>


```C++
HRESULT Click(
  [in] VMMouseButton buttonIndex
);
```



## <a name="parameters"></a><span data-ttu-id="95d74-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="95d74-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95d74-112">*ButtonIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="95d74-112">*buttonIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95d74-113">Indice del pulsante su cui si fa clic.</span><span class="sxs-lookup"><span data-stu-id="95d74-113">The index of the button being clicked.</span></span> <span data-ttu-id="95d74-114">Per un elenco di valori, vedere [**VMMouseButton**](vmmousebutton.md).</span><span class="sxs-lookup"><span data-stu-id="95d74-114">For a list of values, see [**VMMouseButton**](vmmousebutton.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95d74-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="95d74-115">Return value</span></span>

<span data-ttu-id="95d74-116">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="95d74-116">This method can return one of these values.</span></span>



| <span data-ttu-id="95d74-117">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="95d74-117">Return code/value</span></span>                                                                                                                                                        | <span data-ttu-id="95d74-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="95d74-118">Description</span></span>                                                                                                                                       |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="95d74-119"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="95d74-119"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                              | <span data-ttu-id="95d74-120">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="95d74-120">The operation was successful.</span></span><br/>                                                                                                          |
| <dl> <span data-ttu-id="95d74-121"><dt>**E \_**</dt> <dt>0x80000003</dt> INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="95d74-121"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>             | <span data-ttu-id="95d74-122">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="95d74-122">The parameter is **NULL**.</span></span><br/>                                                                                                             |
| <dl> <span data-ttu-id="95d74-123"><dt>**Macchina virtuale \_ \_VM E \_ non \_ in esecuzione**</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="95d74-123"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>   | <span data-ttu-id="95d74-124">La macchina virtuale a cui questo dispositivo mouse è collegato non è attualmente in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="95d74-124">The virtual machine to which this mouse device is attached is not currently running.</span></span><br/>                                                   |
| <dl> <span data-ttu-id="95d74-125"><dt>**Macchina virtuale \_ E \_ mouse \_ non \_ attivo**</dt> <dt>0xA0040800</dt></span><span class="sxs-lookup"><span data-stu-id="95d74-125"><dt>**VM\_E\_MOUSE\_NOT\_ACTIVE**</dt> <dt>0xA0040800</dt></span></span> </dl> | <span data-ttu-id="95d74-126">Non è stato possibile completare l'operazione perché il dispositivo mouse non è acceso o non è attualmente attivo nella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="95d74-126">The operation could not be completed because the mouse device is not powered up, or it is not currently active in the virtual machine.</span></span><br/> |
| <dl> <span data-ttu-id="95d74-127"><dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="95d74-127"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>        | <span data-ttu-id="95d74-128">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="95d74-128">An unexpected error has occurred.</span></span><br/>                                                                                                      |



 

## <a name="requirements"></a><span data-ttu-id="95d74-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="95d74-129">Requirements</span></span>



| <span data-ttu-id="95d74-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="95d74-130">Requirement</span></span> | <span data-ttu-id="95d74-131">Valore</span><span class="sxs-lookup"><span data-stu-id="95d74-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="95d74-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="95d74-132">Minimum supported client</span></span><br/> | <span data-ttu-id="95d74-133">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="95d74-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="95d74-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="95d74-134">Minimum supported server</span></span><br/> | <span data-ttu-id="95d74-135">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="95d74-135">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="95d74-136">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="95d74-136">End of client support</span></span><br/>    | <span data-ttu-id="95d74-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="95d74-137">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="95d74-138">Prodotto</span><span class="sxs-lookup"><span data-stu-id="95d74-138">Product</span></span><br/>                  | <span data-ttu-id="95d74-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="95d74-139">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="95d74-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="95d74-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="95d74-141"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="95d74-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="95d74-142">IID</span><span class="sxs-lookup"><span data-stu-id="95d74-142">IID</span></span><br/>                      | <span data-ttu-id="95d74-143">IID \_ IVMmouse è definito come ac903f6d-6346-4F29-8875-5d511a13895e</span><span class="sxs-lookup"><span data-stu-id="95d74-143">IID\_IVMmouse is defined as ac903f6d-6346-4f29-8875-5d511a13895e</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="95d74-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="95d74-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95d74-145">**IVMMouse**</span><span class="sxs-lookup"><span data-stu-id="95d74-145">**IVMMouse**</span></span>](ivmmouse.md)
</dt> </dl>

 

