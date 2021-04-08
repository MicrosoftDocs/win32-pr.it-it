---
title: Metodo IVMKeyboard TypeKeySequence (VPCCOMInterfaces. h)
description: Simula un elenco delimitato da virgole di chiavi digitate.
ms.assetid: ba4d4e43-cb2e-49ae-940d-2e81286d3473
keywords:
- Metodo TypeKeySequence Virtual PC
- Metodo TypeKeySequence Virtual PC, interfaccia IVMKeyboard
- Interfaccia IVMKeyboard Virtual PC, metodo TypeKeySequence
topic_type:
- apiref
api_name:
- IVMKeyboard.TypeKeySequence
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c34bd96077c1d28aad196ee0d6b11de122725d68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964874"
---
# <a name="ivmkeyboardtypekeysequence-method"></a><span data-ttu-id="a9e78-106">Metodo IVMKeyboard:: TypeKeySequence</span><span class="sxs-lookup"><span data-stu-id="a9e78-106">IVMKeyboard::TypeKeySequence method</span></span>

<span data-ttu-id="a9e78-107">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="a9e78-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="a9e78-108">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="a9e78-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="a9e78-109">Simula un elenco delimitato da virgole di chiavi digitate.</span><span class="sxs-lookup"><span data-stu-id="a9e78-109">Simulates a comma-delimited list of keys being typed.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9e78-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a9e78-110">Syntax</span></span>


```C++
HRESULT TypeKeySequence(
  [in] BSTR keySequence
);
```



## <a name="parameters"></a><span data-ttu-id="a9e78-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="a9e78-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9e78-112">*sequenza di sequenze* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a9e78-112">*keySequence* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9e78-113">Sequenza delimitata da virgole dei codici chiave da tipizzare.</span><span class="sxs-lookup"><span data-stu-id="a9e78-113">The comma-delimited sequence of key codes to be typed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a9e78-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a9e78-114">Return value</span></span>

<span data-ttu-id="a9e78-115">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="a9e78-115">This method can return one of these values.</span></span>



| <span data-ttu-id="a9e78-116">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="a9e78-116">Return code/value</span></span>                                                                                                                                                 | <span data-ttu-id="a9e78-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a9e78-117">Description</span></span>                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a9e78-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="a9e78-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="a9e78-119">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="a9e78-119">The operation was successful.</span></span><br/>                                   |
| <dl> <span data-ttu-id="a9e78-120"><dt>**E \_ PUNTATORE**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="a9e78-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="a9e78-121">Il parametro è **null**.</span><span class="sxs-lookup"><span data-stu-id="a9e78-121">The parameter is **NULL**.</span></span><br/>                                      |
| <dl> <span data-ttu-id="a9e78-122"><dt>**E \_**</dt> <dt>0x80000003</dt> INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="a9e78-122"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>      | <span data-ttu-id="a9e78-123">La stringa specificata è vuota o contiene un codice chiave non valido.</span><span class="sxs-lookup"><span data-stu-id="a9e78-123">The specified string is empty, or contains an invalid key code.</span></span><br/> |
| <dl> <span data-ttu-id="a9e78-124"><dt>**Disp \_ 0x80020009 \_ eccezione E**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="a9e78-124"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="a9e78-125">Si è verificato un errore imprevisto.</span><span class="sxs-lookup"><span data-stu-id="a9e78-125">An unexpected error has occurred.</span></span><br/>                               |



 

## <a name="remarks"></a><span data-ttu-id="a9e78-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="a9e78-126">Remarks</span></span>

<span data-ttu-id="a9e78-127">Una stringa di sequenza di chiavi è un set delimitato da virgole di identificatori di chiave usati per simulare la sequenza di stampa e di rilascio della chiave di una tastiera standard in stile US 101-Key.</span><span class="sxs-lookup"><span data-stu-id="a9e78-127">A key sequence string is a comma-delimited set of key identifiers which are used to simulate the key press and release sequence of a standard U.S. 101-key AT-style keyboard.</span></span>

<span data-ttu-id="a9e78-128">Se un identificatore di chiave viene visualizzato nella stringa senza un modificatore precedente, viene inviato un codice con pressione di tasto alla sessione della macchina virtuale, seguito immediatamente dal codice corrispondente rilasciato dalla chiave.</span><span class="sxs-lookup"><span data-stu-id="a9e78-128">If a key identifier appears in the string without a preceding modifier, a key-pressed code is sent to the virtual machine session, followed immediately by its corresponding key-released code.</span></span> <span data-ttu-id="a9e78-129">Per modificare questo comportamento, è possibile usare i modificatori di chiave.</span><span class="sxs-lookup"><span data-stu-id="a9e78-129">Key modifiers can be used to change this behavior.</span></span>

<span data-ttu-id="a9e78-130">Il modificatore DOWN, ad esempio, invierà il codice premuto per la chiave per l'identificatore di chiave seguente senza inviare il codice rilasciato dalla chiave.</span><span class="sxs-lookup"><span data-stu-id="a9e78-130">For example, the DOWN modifier will send the key-pressed code for the following key identifier without sending the key-released code.</span></span> <span data-ttu-id="a9e78-131">Questa operazione è utile per la simulazione dei tasti CTRL, ALT e MAIUSC quando vengono mantenuti mentre sono in corso l'invio di altri tasti.</span><span class="sxs-lookup"><span data-stu-id="a9e78-131">This is useful for simulating Ctrl, Alt, and Shift keys when they are held down while other keys are being sent.</span></span> <span data-ttu-id="a9e78-132">Per rilasciare la chiave, è necessario includerla nuovamente nella stringa della chiave insieme a un modificatore UP precedente.</span><span class="sxs-lookup"><span data-stu-id="a9e78-132">To release the key, it must be included in the key string again along with a preceding UP modifier.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9e78-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a9e78-133">Requirements</span></span>



| <span data-ttu-id="a9e78-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="a9e78-134">Requirement</span></span> | <span data-ttu-id="a9e78-135">Valore</span><span class="sxs-lookup"><span data-stu-id="a9e78-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9e78-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a9e78-136">Minimum supported client</span></span><br/> | <span data-ttu-id="a9e78-137">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="a9e78-137">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a9e78-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a9e78-138">Minimum supported server</span></span><br/> | <span data-ttu-id="a9e78-139">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="a9e78-139">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="a9e78-140">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="a9e78-140">End of client support</span></span><br/>    | <span data-ttu-id="a9e78-141">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a9e78-141">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="a9e78-142">Prodotto</span><span class="sxs-lookup"><span data-stu-id="a9e78-142">Product</span></span><br/>                  | <span data-ttu-id="a9e78-143">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="a9e78-143">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="a9e78-144">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a9e78-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="a9e78-145"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="a9e78-145"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="a9e78-146">IID</span><span class="sxs-lookup"><span data-stu-id="a9e78-146">IID</span></span><br/>                      | <span data-ttu-id="a9e78-147">IID \_ IVMKeyboard è definito come 00695f2e-c5ad-4d6e-b1ab-336ed121f8c4</span><span class="sxs-lookup"><span data-stu-id="a9e78-147">IID\_IVMKeyboard is defined as 00695f2e-c5ad-4d6e-b1ab-336ed121f8c4</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="a9e78-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a9e78-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9e78-149">**IVMKeyboard**</span><span class="sxs-lookup"><span data-stu-id="a9e78-149">**IVMKeyboard**</span></span>](ivmkeyboard.md)
</dt> <dt>

[<span data-ttu-id="a9e78-150">Sequenze di chiavi</span><span class="sxs-lookup"><span data-stu-id="a9e78-150">Key Sequences</span></span>](key-sequences.md)
</dt> </dl>

 

