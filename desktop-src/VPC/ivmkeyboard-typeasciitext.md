---
title: Metodo IVMKeyboard TypeAsciiText (VPCCOMInterfaces. h)
description: Simula una serie di chiavi ASCII digitate nel guest.
ms.assetid: 6c7fbfed-d495-4f11-a7d1-dc08bd075870
keywords:
- Metodo TypeAsciiText Virtual PC
- Metodo TypeAsciiText Virtual PC, interfaccia IVMKeyboard
- Interfaccia IVMKeyboard Virtual PC, metodo TypeAsciiText
topic_type:
- apiref
api_name:
- IVMKeyboard.TypeAsciiText
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 538df9fc3036e43dc36f4ca7425688157e9fca77
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120166"
---
# <a name="ivmkeyboardtypeasciitext-method"></a><span data-ttu-id="62ec1-106">Metodo IVMKeyboard:: TypeAsciiText</span><span class="sxs-lookup"><span data-stu-id="62ec1-106">IVMKeyboard::TypeAsciiText method</span></span>

<span data-ttu-id="62ec1-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="62ec1-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="62ec1-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="62ec1-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="62ec1-109">Simula una serie di chiavi ASCII digitate nel guest.</span><span class="sxs-lookup"><span data-stu-id="62ec1-109">Simulates a series of ASCII keys being typed into the guest.</span></span>

## <a name="syntax"></a><span data-ttu-id="62ec1-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="62ec1-110">Syntax</span></span>


```C++
HRESULT TypeAsciiText(
  [in] BSTR text
);
```



## <a name="parameters"></a><span data-ttu-id="62ec1-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="62ec1-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62ec1-112">*testo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="62ec1-112">*text* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62ec1-113">Stringa di testo ASCII da tipizzare all'interno della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="62ec1-113">The ASCII text string to be typed inside the virtual machine.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62ec1-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="62ec1-114">Return value</span></span>

<span data-ttu-id="62ec1-115">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="62ec1-115">This method can return one of these values.</span></span>



| <span data-ttu-id="62ec1-116">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="62ec1-116">Return code/value</span></span>                                                                                                                                                 | <span data-ttu-id="62ec1-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="62ec1-117">Description</span></span>                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="62ec1-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="62ec1-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="62ec1-119">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="62ec1-119">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="62ec1-120"><dt>**E \_ PUNTATORE**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="62ec1-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="62ec1-121">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="62ec1-121">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="62ec1-122"><dt>**E \_**</dt> <dt>0x80000003</dt> INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="62ec1-122"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>      | <span data-ttu-id="62ec1-123">La stringa specificata è vuota.</span><span class="sxs-lookup"><span data-stu-id="62ec1-123">The specified string is empty.</span></span><br/>    |
| <dl> <span data-ttu-id="62ec1-124"><dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="62ec1-124"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="62ec1-125">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="62ec1-125">An unexpected error has occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="62ec1-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="62ec1-126">Requirements</span></span>



| <span data-ttu-id="62ec1-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="62ec1-127">Requirement</span></span> | <span data-ttu-id="62ec1-128">Valore</span><span class="sxs-lookup"><span data-stu-id="62ec1-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="62ec1-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="62ec1-129">Minimum supported client</span></span><br/> | <span data-ttu-id="62ec1-130">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="62ec1-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="62ec1-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="62ec1-131">Minimum supported server</span></span><br/> | <span data-ttu-id="62ec1-132">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="62ec1-132">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="62ec1-133">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="62ec1-133">End of client support</span></span><br/>    | <span data-ttu-id="62ec1-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="62ec1-134">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="62ec1-135">Prodotto</span><span class="sxs-lookup"><span data-stu-id="62ec1-135">Product</span></span><br/>                  | <span data-ttu-id="62ec1-136">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="62ec1-136">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="62ec1-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="62ec1-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="62ec1-138"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="62ec1-138"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="62ec1-139">IID</span><span class="sxs-lookup"><span data-stu-id="62ec1-139">IID</span></span><br/>                      | <span data-ttu-id="62ec1-140">IID \_ IVMKeyboard è definito come 00695f2e-c5ad-4d6e-b1ab-336ed121f8c4</span><span class="sxs-lookup"><span data-stu-id="62ec1-140">IID\_IVMKeyboard is defined as 00695f2e-c5ad-4d6e-b1ab-336ed121f8c4</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="62ec1-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="62ec1-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62ec1-142">**IVMKeyboard**</span><span class="sxs-lookup"><span data-stu-id="62ec1-142">**IVMKeyboard**</span></span>](ivmkeyboard.md)
</dt> </dl>

 

