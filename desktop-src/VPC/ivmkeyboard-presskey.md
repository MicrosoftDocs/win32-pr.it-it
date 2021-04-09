---
title: Metodo IVMKeyboard pulsanteper (VPCCOMInterfaces. h)
description: Simula un tasto premuto.
ms.assetid: d945128a-ffde-465c-b615-83a1d5dc789f
keywords:
- Metodo pulsanteper Virtual PC
- Metodo pulsanteper Virtual PC, interfaccia IVMKeyboard
- Interfaccia IVMKeyboard Virtual PC, metodo pulsanteper
topic_type:
- apiref
api_name:
- IVMKeyboard.PressKey
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8175447a819afa7f761899a7e0dd3cbbcc780631
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048496"
---
# <a name="ivmkeyboardpresskey-method"></a><span data-ttu-id="c8167-106">IVMKeyboard::P metodo ressKey</span><span class="sxs-lookup"><span data-stu-id="c8167-106">IVMKeyboard::PressKey method</span></span>

<span data-ttu-id="c8167-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="c8167-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="c8167-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="c8167-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="c8167-109">Simula un tasto premuto.</span><span class="sxs-lookup"><span data-stu-id="c8167-109">Simulates a key being pressed down.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8167-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c8167-110">Syntax</span></span>


```C++
HRESULT PressKey(
  [in] BSTR key
);
```



## <a name="parameters"></a><span data-ttu-id="c8167-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="c8167-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8167-112">*chiave* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="c8167-112">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8167-113">Codice chiave per la chiave da premere.</span><span class="sxs-lookup"><span data-stu-id="c8167-113">The key code for the key to be pressed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8167-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c8167-114">Return value</span></span>

<span data-ttu-id="c8167-115">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="c8167-115">This method can return one of these values.</span></span>



| <span data-ttu-id="c8167-116">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="c8167-116">Return code/value</span></span>                                                                                                                                                 | <span data-ttu-id="c8167-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c8167-117">Description</span></span>                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c8167-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="c8167-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="c8167-119">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="c8167-119">The operation was successful.</span></span><br/>                                   |
| <dl> <span data-ttu-id="c8167-120"><dt>**E \_ PUNTATORE**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="c8167-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="c8167-121">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="c8167-121">The parameter is **NULL**.</span></span><br/>                                      |
| <dl> <span data-ttu-id="c8167-122"><dt>**E \_**</dt> <dt>0x80000003</dt> INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="c8167-122"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>      | <span data-ttu-id="c8167-123">La stringa specificata è vuota o contiene un codice chiave non valido.</span><span class="sxs-lookup"><span data-stu-id="c8167-123">The specified string is empty, or contains an invalid key code.</span></span><br/> |
| <dl> <span data-ttu-id="c8167-124"><dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="c8167-124"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="c8167-125">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="c8167-125">An unexpected error has occurred.</span></span><br/>                               |



 

## <a name="requirements"></a><span data-ttu-id="c8167-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c8167-126">Requirements</span></span>



| <span data-ttu-id="c8167-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8167-127">Requirement</span></span> | <span data-ttu-id="c8167-128">Valore</span><span class="sxs-lookup"><span data-stu-id="c8167-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8167-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c8167-129">Minimum supported client</span></span><br/> | <span data-ttu-id="c8167-130">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="c8167-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c8167-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c8167-131">Minimum supported server</span></span><br/> | <span data-ttu-id="c8167-132">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="c8167-132">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="c8167-133">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="c8167-133">End of client support</span></span><br/>    | <span data-ttu-id="c8167-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c8167-134">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="c8167-135">Prodotto</span><span class="sxs-lookup"><span data-stu-id="c8167-135">Product</span></span><br/>                  | <span data-ttu-id="c8167-136">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="c8167-136">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="c8167-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c8167-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="c8167-138"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="c8167-138"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="c8167-139">IID</span><span class="sxs-lookup"><span data-stu-id="c8167-139">IID</span></span><br/>                      | <span data-ttu-id="c8167-140">IID \_ IVMKeyboard è definito come 00695f2e-c5ad-4d6e-b1ab-336ed121f8c4</span><span class="sxs-lookup"><span data-stu-id="c8167-140">IID\_IVMKeyboard is defined as 00695f2e-c5ad-4d6e-b1ab-336ed121f8c4</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="c8167-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c8167-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8167-142">**IVMKeyboard**</span><span class="sxs-lookup"><span data-stu-id="c8167-142">**IVMKeyboard**</span></span>](ivmkeyboard.md)
</dt> </dl>

 

