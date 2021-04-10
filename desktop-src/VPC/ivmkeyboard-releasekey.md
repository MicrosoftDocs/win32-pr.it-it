---
title: Metodo IVMKeyboard ReleaseKey (VPCCOMInterfaces. h)
description: Simula una chiave rilasciata.
ms.assetid: 112bf11d-d768-4487-ab41-e915aa4e6a24
keywords:
- Metodo ReleaseKey Virtual PC
- Metodo ReleaseKey Virtual PC, interfaccia IVMKeyboard
- Interfaccia IVMKeyboard Virtual PC, metodo ReleaseKey
topic_type:
- apiref
api_name:
- IVMKeyboard.ReleaseKey
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8585f592ae1cad65157536f841500c42bb06bfd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964412"
---
# <a name="ivmkeyboardreleasekey-method"></a><span data-ttu-id="ccd88-106">Metodo IVMKeyboard:: ReleaseKey</span><span class="sxs-lookup"><span data-stu-id="ccd88-106">IVMKeyboard::ReleaseKey method</span></span>

<span data-ttu-id="ccd88-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="ccd88-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="ccd88-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="ccd88-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="ccd88-109">Simula una chiave rilasciata.</span><span class="sxs-lookup"><span data-stu-id="ccd88-109">Simulates a key being released.</span></span>

## <a name="syntax"></a><span data-ttu-id="ccd88-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ccd88-110">Syntax</span></span>


```C++
HRESULT ReleaseKey(
  [in] BSTR key
);
```



## <a name="parameters"></a><span data-ttu-id="ccd88-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="ccd88-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ccd88-112">*chiave* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="ccd88-112">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ccd88-113">Codice chiave per la chiave da rilasciare.</span><span class="sxs-lookup"><span data-stu-id="ccd88-113">The key code for the key to be released.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ccd88-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ccd88-114">Return value</span></span>

<span data-ttu-id="ccd88-115">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="ccd88-115">This method can return one of these values.</span></span>



| <span data-ttu-id="ccd88-116">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="ccd88-116">Return code/value</span></span>                                                                                                                                                 | <span data-ttu-id="ccd88-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ccd88-117">Description</span></span>                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ccd88-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="ccd88-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="ccd88-119">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="ccd88-119">The operation was successful.</span></span><br/>                                   |
| <dl> <span data-ttu-id="ccd88-120"><dt>**E \_ PUNTATORE**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="ccd88-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="ccd88-121">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="ccd88-121">The parameter is **NULL**.</span></span><br/>                                      |
| <dl> <span data-ttu-id="ccd88-122"><dt>**E \_**</dt> <dt>0x80000003</dt> INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="ccd88-122"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>      | <span data-ttu-id="ccd88-123">La stringa specificata è vuota o contiene un codice chiave non valido.</span><span class="sxs-lookup"><span data-stu-id="ccd88-123">The specified string is empty, or contains an invalid key code.</span></span><br/> |
| <dl> <span data-ttu-id="ccd88-124"><dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="ccd88-124"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="ccd88-125">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="ccd88-125">An unexpected error has occurred.</span></span><br/>                               |



 

## <a name="requirements"></a><span data-ttu-id="ccd88-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ccd88-126">Requirements</span></span>



| <span data-ttu-id="ccd88-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="ccd88-127">Requirement</span></span> | <span data-ttu-id="ccd88-128">Valore</span><span class="sxs-lookup"><span data-stu-id="ccd88-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ccd88-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ccd88-129">Minimum supported client</span></span><br/> | <span data-ttu-id="ccd88-130">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="ccd88-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ccd88-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ccd88-131">Minimum supported server</span></span><br/> | <span data-ttu-id="ccd88-132">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="ccd88-132">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="ccd88-133">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="ccd88-133">End of client support</span></span><br/>    | <span data-ttu-id="ccd88-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ccd88-134">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="ccd88-135">Prodotto</span><span class="sxs-lookup"><span data-stu-id="ccd88-135">Product</span></span><br/>                  | <span data-ttu-id="ccd88-136">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="ccd88-136">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="ccd88-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ccd88-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="ccd88-138"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="ccd88-138"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="ccd88-139">IID</span><span class="sxs-lookup"><span data-stu-id="ccd88-139">IID</span></span><br/>                      | <span data-ttu-id="ccd88-140">IID \_ IVMKeyboard è definito come 00695f2e-c5ad-4d6e-b1ab-336ed121f8c4</span><span class="sxs-lookup"><span data-stu-id="ccd88-140">IID\_IVMKeyboard is defined as 00695f2e-c5ad-4d6e-b1ab-336ed121f8c4</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="ccd88-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ccd88-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ccd88-142">**IVMKeyboard**</span><span class="sxs-lookup"><span data-stu-id="ccd88-142">**IVMKeyboard**</span></span>](ivmkeyboard.md)
</dt> </dl>

 

