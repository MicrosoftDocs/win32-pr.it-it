---
title: Metodo IVMKeyboard (VPCCOMInterfaces. h)
description: Determina se il tasto specificato è inattivo.
ms.assetid: 7541d678-762a-4c2e-80cd-686bb56c9cd7
keywords:
- Metodo di stampa Virtual PC
- Metodo di stampa Virtual PC, interfaccia IVMKeyboard
- Interfaccia IVMKeyboard Virtual PC, metodo di stampa
topic_type:
- apiref
api_name:
- IVMKeyboard.IsPressed
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0a4185fa0310994bc1cffa917348dfca2fdedfe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742599"
---
# <a name="ivmkeyboardispressed-method"></a><span data-ttu-id="392c2-106">Metodo IVMKeyboard::</span><span class="sxs-lookup"><span data-stu-id="392c2-106">IVMKeyboard::IsPressed method</span></span>

<span data-ttu-id="392c2-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="392c2-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="392c2-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="392c2-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="392c2-109">Determina se il tasto specificato è inattivo.</span><span class="sxs-lookup"><span data-stu-id="392c2-109">Determines whether the specified key is down.</span></span>

## <a name="syntax"></a><span data-ttu-id="392c2-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="392c2-110">Syntax</span></span>


```C++
HRESULT IsPressed(
  [in]          BSTR         key,
  [out, retval] VARIANT_BOOL *pressed
);
```



## <a name="parameters"></a><span data-ttu-id="392c2-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="392c2-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="392c2-112">*chiave* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="392c2-112">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="392c2-113">Codice chiave per la chiave il cui stato deve essere sottoposto a query.</span><span class="sxs-lookup"><span data-stu-id="392c2-113">The key code for the key whose state is to be queried.</span></span>

</dd> <dt>

<span data-ttu-id="392c2-114">con *pressione* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="392c2-114">*pressed* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="392c2-115">**True** se la chiave è attualmente premuta; in caso contrario, **false** .</span><span class="sxs-lookup"><span data-stu-id="392c2-115">**TRUE** if the key is currently pressed down, **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="392c2-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="392c2-116">Return value</span></span>

<span data-ttu-id="392c2-117">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="392c2-117">This method can return one of these values.</span></span>



| <span data-ttu-id="392c2-118">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="392c2-118">Return code/value</span></span>                                                                                                                                                 | <span data-ttu-id="392c2-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="392c2-119">Description</span></span>                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="392c2-120"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="392c2-120"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="392c2-121">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="392c2-121">The operation was successful.</span></span><br/>                                   |
| <dl> <span data-ttu-id="392c2-122"><dt>**E \_ PUNTATORE**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="392c2-122"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="392c2-123">Un parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="392c2-123">A parameter is **NULL**.</span></span><br/>                                        |
| <dl> <span data-ttu-id="392c2-124"><dt>**E \_**</dt> <dt>0x80000003</dt> INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="392c2-124"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>      | <span data-ttu-id="392c2-125">La stringa specificata è vuota o contiene un codice chiave non valido.</span><span class="sxs-lookup"><span data-stu-id="392c2-125">The specified string is empty, or contains an invalid key code.</span></span><br/> |
| <dl> <span data-ttu-id="392c2-126"><dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="392c2-126"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="392c2-127">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="392c2-127">An unexpected error has occurred.</span></span><br/>                               |



 

## <a name="requirements"></a><span data-ttu-id="392c2-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="392c2-128">Requirements</span></span>



| <span data-ttu-id="392c2-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="392c2-129">Requirement</span></span> | <span data-ttu-id="392c2-130">Valore</span><span class="sxs-lookup"><span data-stu-id="392c2-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="392c2-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="392c2-131">Minimum supported client</span></span><br/> | <span data-ttu-id="392c2-132">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="392c2-132">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="392c2-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="392c2-133">Minimum supported server</span></span><br/> | <span data-ttu-id="392c2-134">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="392c2-134">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="392c2-135">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="392c2-135">End of client support</span></span><br/>    | <span data-ttu-id="392c2-136">Windows 7</span><span class="sxs-lookup"><span data-stu-id="392c2-136">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="392c2-137">Prodotto</span><span class="sxs-lookup"><span data-stu-id="392c2-137">Product</span></span><br/>                  | <span data-ttu-id="392c2-138">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="392c2-138">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="392c2-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="392c2-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="392c2-140"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="392c2-140"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="392c2-141">IID</span><span class="sxs-lookup"><span data-stu-id="392c2-141">IID</span></span><br/>                      | <span data-ttu-id="392c2-142">IID \_ IVMKeyboard è definito come 00695f2e-c5ad-4d6e-b1ab-336ed121f8c4</span><span class="sxs-lookup"><span data-stu-id="392c2-142">IID\_IVMKeyboard is defined as 00695f2e-c5ad-4d6e-b1ab-336ed121f8c4</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="392c2-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="392c2-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="392c2-144">**IVMKeyboard**</span><span class="sxs-lookup"><span data-stu-id="392c2-144">**IVMKeyboard**</span></span>](ivmkeyboard.md)
</dt> </dl>

 

