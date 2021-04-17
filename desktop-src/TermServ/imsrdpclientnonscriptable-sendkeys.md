---
title: Metodo IMsRdpClientNonScriptable SendKeys
description: Invia una serie di sequenze di tasti al controllo. Le sequenze di tasti sono nel formato del codice di analisi, ovvero i dati della tastiera delle chiavi fisiche effettive.
ms.assetid: 1f07a9cc-4795-43cb-ac99-4bb70b8b544a
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SendKeys
- Servizi Desktop remoto del metodo SendKeys, interfaccia IMsRdpClientNonScriptable
- Interfaccia IMsRdpClientNonScriptable Servizi Desktop remoto, metodo SendKeys
- Servizi Desktop remoto del metodo SendKeys, interfaccia IMsRdpClientNonScriptable2
- Interfaccia IMsRdpClientNonScriptable2 Servizi Desktop remoto, metodo SendKeys
- Servizi Desktop remoto del metodo SendKeys, interfaccia IMsRdpClientNonScriptable3
- Interfaccia IMsRdpClientNonScriptable3 Servizi Desktop remoto, metodo SendKeys
- Servizi Desktop remoto del metodo SendKeys, interfaccia IMsRdpClientNonScriptable4
- Interfaccia IMsRdpClientNonScriptable4 Servizi Desktop remoto, metodo SendKeys
- Servizi Desktop remoto del metodo SendKeys, interfaccia IMsRdpClientNonScriptable5
- Interfaccia IMsRdpClientNonScriptable5 Servizi Desktop remoto, metodo SendKeys
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable.SendKeys
- IMsRdpClientNonScriptable2.SendKeys
- IMsRdpClientNonScriptable3.SendKeys
- IMsRdpClientNonScriptable4.SendKeys
- IMsRdpClientNonScriptable5.SendKeys
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9effa3bbd40eb64df55914b9adbc07a03ea0c465
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477765"
---
# <a name="imsrdpclientnonscriptablesendkeys-method"></a><span data-ttu-id="d8e16-115">Metodo IMsRdpClientNonScriptable:: SendKeys</span><span class="sxs-lookup"><span data-stu-id="d8e16-115">IMsRdpClientNonScriptable::SendKeys method</span></span>

<span data-ttu-id="d8e16-116">Invia una serie di sequenze di tasti al controllo.</span><span class="sxs-lookup"><span data-stu-id="d8e16-116">Sends a series of keystrokes to the control.</span></span> <span data-ttu-id="d8e16-117">Le sequenze di tasti sono nel formato del codice di analisi, ovvero i dati della tastiera delle chiavi fisiche effettive.</span><span class="sxs-lookup"><span data-stu-id="d8e16-117">The keystrokes are in scan code form, which is the keyboard data from the actual physical keys.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8e16-118">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d8e16-118">Syntax</span></span>


```C++
HRESULT SendKeys(
  [in] LONG         numKeys,
  [in] VARIANT_BOOL *pbArrayKeyUp,
  [in] LONG         *plKeyData
);
```



## <a name="parameters"></a><span data-ttu-id="d8e16-119">Parametri</span><span class="sxs-lookup"><span data-stu-id="d8e16-119">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8e16-120">*numkeys* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d8e16-120">*numKeys* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8e16-121">Numero di sequenze di tasti da inviare.</span><span class="sxs-lookup"><span data-stu-id="d8e16-121">The number of keystrokes to send.</span></span> <span data-ttu-id="d8e16-122">Il numero massimo di chiavi che possono essere inviate in un'operazione è 20.</span><span class="sxs-lookup"><span data-stu-id="d8e16-122">The maximum number of keys that can be sent in one operation is 20.</span></span> <span data-ttu-id="d8e16-123">Il metodo restituisce **E \_ INVALIDARG** se questo parametro è maggiore di 20.</span><span class="sxs-lookup"><span data-stu-id="d8e16-123">The method returns **E\_INVALIDARG** if this parameter is greater than 20.</span></span> <span data-ttu-id="d8e16-124">Per ulteriori informazioni, vedere la sezione Osservazioni successiva.</span><span class="sxs-lookup"><span data-stu-id="d8e16-124">For more information, see the following Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="d8e16-125">*pbArrayKeyUp* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d8e16-125">*pbArrayKeyUp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8e16-126">Matrice la cui dimensione è uguale a *numkeys*.</span><span class="sxs-lookup"><span data-stu-id="d8e16-126">An array whose size is equal to *numKeys*.</span></span> <span data-ttu-id="d8e16-127">Un elemento è **true** se la chiave corrispondente è impostata su on e **false** se la chiave corrispondente è inattiva.</span><span class="sxs-lookup"><span data-stu-id="d8e16-127">An element is **TRUE** if the corresponding key is UP and **FALSE** if the corresponding key is DOWN.</span></span>

</dd> <dt>

<span data-ttu-id="d8e16-128">*plKeyData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d8e16-128">*plKeyData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8e16-129">Matrice la cui dimensione è uguale a *numkeys*.</span><span class="sxs-lookup"><span data-stu-id="d8e16-129">An array whose size is equal to *numKeys*.</span></span> <span data-ttu-id="d8e16-130">La matrice contiene dati della sequenza di tasti e corrisponde al valore del parametro *lParam* del messaggio di [WM \_ KeyDown](../inputdev/wm-keydown.md) .</span><span class="sxs-lookup"><span data-stu-id="d8e16-130">The array contains keystroke data and corresponds to the value of the *lParam* parameter of the [WM\_KEYDOWN](../inputdev/wm-keydown.md) message.</span></span> <span data-ttu-id="d8e16-131">I dati specificano il numero di ripetizioni, il codice di analisi, il flag di chiave estesa, il codice del contesto, il flag di stato di chiave precedente e il flag di stato di transizione.</span><span class="sxs-lookup"><span data-stu-id="d8e16-131">The data specifies the repeat count, scan code, extended-key flag, context code, previous key-state flag, and transition-state flag.</span></span> <span data-ttu-id="d8e16-132">Per una descrizione dei bit in questa matrice, vedere [WM \_ KeyDown](../inputdev/wm-keydown.md).</span><span class="sxs-lookup"><span data-stu-id="d8e16-132">For a description of the bits in this array, see [WM\_KEYDOWN](../inputdev/wm-keydown.md).</span></span>

<span data-ttu-id="d8e16-133">L'elemento corrispondente in *pbArrayKeyUp* indica se la chiave è verso l'alto o verso il basso.</span><span class="sxs-lookup"><span data-stu-id="d8e16-133">The corresponding element in *pbArrayKeyUp* indicates if the key is UP or DOWN.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8e16-134">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d8e16-134">Return value</span></span>

<span data-ttu-id="d8e16-135">Se l'operazione ha esito positivo, restituire **S \_ OK** .</span><span class="sxs-lookup"><span data-stu-id="d8e16-135">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="d8e16-136">Commenti</span><span class="sxs-lookup"><span data-stu-id="d8e16-136">Remarks</span></span>

<span data-ttu-id="d8e16-137">Il metodo **SendKeys** non combina le sequenze di tasti eseguite dall'utente locale con le sequenze di tasti inviate dal metodo.</span><span class="sxs-lookup"><span data-stu-id="d8e16-137">The **SendKeys** method does not mix keystrokes made by the local user with keystrokes that the method is sending.</span></span> <span data-ttu-id="d8e16-138">Tutte le sequenze di tasti passate al metodo vengono inviate alla sessione remota in un'unica sequenza atomica.</span><span class="sxs-lookup"><span data-stu-id="d8e16-138">All keystrokes passed to the method are sent to the remote session in a single atomic sequence.</span></span>

<span data-ttu-id="d8e16-139">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="d8e16-139">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d8e16-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d8e16-140">Requirements</span></span>



| <span data-ttu-id="d8e16-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="d8e16-141">Requirement</span></span> | <span data-ttu-id="d8e16-142">Valore</span><span class="sxs-lookup"><span data-stu-id="d8e16-142">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8e16-143">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d8e16-143">Minimum supported client</span></span><br/> | <span data-ttu-id="d8e16-144">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d8e16-144">Windows Vista</span></span><br/>                                                                     |
| <span data-ttu-id="d8e16-145">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d8e16-145">Minimum supported server</span></span><br/> | <span data-ttu-id="d8e16-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d8e16-146">Windows Server 2008</span></span><br/>                                                               |
| <span data-ttu-id="d8e16-147">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="d8e16-147">Type library</span></span><br/>             | <dl> <span data-ttu-id="d8e16-148"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d8e16-148"><dt>MsTscAx.dll</dt></span></span> </dl>       |
| <span data-ttu-id="d8e16-149">DLL</span><span class="sxs-lookup"><span data-stu-id="d8e16-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d8e16-150"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d8e16-150"><dt>MsTscAx.dll</dt></span></span> </dl>       |
| <span data-ttu-id="d8e16-151">IID</span><span class="sxs-lookup"><span data-stu-id="d8e16-151">IID</span></span><br/>                      | <span data-ttu-id="d8e16-152">IID \_ IMsRdpClientNonScriptable è definito come 2f079c4c-87B2-4afd-97AB-20cdb43038ae</span><span class="sxs-lookup"><span data-stu-id="d8e16-152">IID\_IMsRdpClientNonScriptable is defined as 2f079c4c-87b2-4afd-97ab-20cdb43038ae</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d8e16-153">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d8e16-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8e16-154">**IMsRdpClientNonScriptable2**</span><span class="sxs-lookup"><span data-stu-id="d8e16-154">**IMsRdpClientNonScriptable2**</span></span>](imsrdpclientnonscriptable2.md)
</dt> <dt>

[<span data-ttu-id="d8e16-155">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="d8e16-155">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> <dt>

[<span data-ttu-id="d8e16-156">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="d8e16-156">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="d8e16-157">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="d8e16-157">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="d8e16-158">**IMsRdpClientNonScriptable**</span><span class="sxs-lookup"><span data-stu-id="d8e16-158">**IMsRdpClientNonScriptable**</span></span>](imsrdpclientnonscriptable-interface.md)
</dt> <dt>

[<span data-ttu-id="d8e16-159">KeyDown di WM \_</span><span class="sxs-lookup"><span data-stu-id="d8e16-159">WM\_KEYDOWN</span></span>](../inputdev/wm-keydown.md)
</dt> </dl>

 

