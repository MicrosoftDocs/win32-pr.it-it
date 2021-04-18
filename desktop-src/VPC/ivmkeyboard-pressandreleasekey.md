---
title: Metodo IVMKeyboard PressAndReleaseKey (VPCCOMInterfaces. h)
description: Simula un tasto premuto e quindi rilasciato.
ms.assetid: 2a7fc36f-f1bf-4f1d-b8f7-ea5b167c82a7
keywords:
- Metodo PressAndReleaseKey Virtual PC
- Metodo PressAndReleaseKey Virtual PC, interfaccia IVMKeyboard
- Interfaccia IVMKeyboard Virtual PC, metodo PressAndReleaseKey
topic_type:
- apiref
api_name:
- IVMKeyboard.PressAndReleaseKey
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4adbcac2c79c02ce69584bbfdf21a6b08b350a3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301845"
---
# <a name="ivmkeyboardpressandreleasekey-method"></a><span data-ttu-id="63be0-106">IVMKeyboard::P metodo ressAndReleaseKey</span><span class="sxs-lookup"><span data-stu-id="63be0-106">IVMKeyboard::PressAndReleaseKey method</span></span>

<span data-ttu-id="63be0-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="63be0-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="63be0-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="63be0-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="63be0-109">Simula un tasto premuto e quindi rilasciato.</span><span class="sxs-lookup"><span data-stu-id="63be0-109">Simulates a key being pressed down and then released.</span></span>

## <a name="syntax"></a><span data-ttu-id="63be0-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="63be0-110">Syntax</span></span>


```C++
HRESULT PressAndReleaseKey(
  [in] BSTR key
);
```



## <a name="parameters"></a><span data-ttu-id="63be0-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="63be0-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63be0-112">*chiave* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="63be0-112">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63be0-113">Codice chiave per la chiave da premere e rilasciare.</span><span class="sxs-lookup"><span data-stu-id="63be0-113">The key code for the key to be pressed and released.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63be0-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="63be0-114">Return value</span></span>

<span data-ttu-id="63be0-115">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="63be0-115">This method can return one of these values.</span></span>



| <span data-ttu-id="63be0-116">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="63be0-116">Return code/value</span></span>                                                                                                                                                 | <span data-ttu-id="63be0-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="63be0-117">Description</span></span>                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="63be0-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="63be0-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="63be0-119">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="63be0-119">The operation was successful.</span></span><br/>                                   |
| <dl> <span data-ttu-id="63be0-120"><dt>**E \_ PUNTATORE**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="63be0-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="63be0-121">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="63be0-121">The parameter is **NULL**.</span></span><br/>                                      |
| <dl> <span data-ttu-id="63be0-122"><dt>**E \_**</dt> <dt>0x80000003</dt> INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="63be0-122"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>      | <span data-ttu-id="63be0-123">La stringa specificata è vuota o contiene un codice chiave non valido.</span><span class="sxs-lookup"><span data-stu-id="63be0-123">The specified string is empty, or contains an invalid key code.</span></span><br/> |
| <dl> <span data-ttu-id="63be0-124"><dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="63be0-124"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="63be0-125">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="63be0-125">An unexpected error has occurred.</span></span><br/>                               |



 

## <a name="requirements"></a><span data-ttu-id="63be0-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="63be0-126">Requirements</span></span>



| <span data-ttu-id="63be0-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="63be0-127">Requirement</span></span> | <span data-ttu-id="63be0-128">Valore</span><span class="sxs-lookup"><span data-stu-id="63be0-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="63be0-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="63be0-129">Minimum supported client</span></span><br/> | <span data-ttu-id="63be0-130">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="63be0-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="63be0-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="63be0-131">Minimum supported server</span></span><br/> | <span data-ttu-id="63be0-132">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="63be0-132">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="63be0-133">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="63be0-133">End of client support</span></span><br/>    | <span data-ttu-id="63be0-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="63be0-134">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="63be0-135">Prodotto</span><span class="sxs-lookup"><span data-stu-id="63be0-135">Product</span></span><br/>                  | <span data-ttu-id="63be0-136">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="63be0-136">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="63be0-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="63be0-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="63be0-138"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="63be0-138"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="63be0-139">IID</span><span class="sxs-lookup"><span data-stu-id="63be0-139">IID</span></span><br/>                      | <span data-ttu-id="63be0-140">IID \_ IVMKeyboard è definito come 00695f2e-c5ad-4d6e-b1ab-336ed121f8c4</span><span class="sxs-lookup"><span data-stu-id="63be0-140">IID\_IVMKeyboard is defined as 00695f2e-c5ad-4d6e-b1ab-336ed121f8c4</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="63be0-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="63be0-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63be0-142">**IVMKeyboard**</span><span class="sxs-lookup"><span data-stu-id="63be0-142">**IVMKeyboard**</span></span>](ivmkeyboard.md)
</dt> </dl>

 

