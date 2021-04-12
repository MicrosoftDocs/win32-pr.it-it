---
title: Metodo IMsRdpClient5 GetErrorDescription
description: Recupera la descrizione dell'errore per gli eventi di disconnessione della sessione.
ms.assetid: 8c8f7b10-7f79-4586-845e-e99f5ca81905
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo GetErrorDescription
- Metodo GetErrorDescription Servizi Desktop remoto, interfaccia IMsRdpClient5
- Interfaccia IMsRdpClient5 Servizi Desktop remoto, metodo GetErrorDescription
- Metodo GetErrorDescription Servizi Desktop remoto, interfaccia IMsRdpClient6
- Interfaccia IMsRdpClient6 Servizi Desktop remoto, metodo GetErrorDescription
- Metodo GetErrorDescription Servizi Desktop remoto, interfaccia IMsRdpClient7
- Interfaccia IMsRdpClient7 Servizi Desktop remoto, metodo GetErrorDescription
- Metodo GetErrorDescription Servizi Desktop remoto, interfaccia IMsRdpClient8
- Interfaccia IMsRdpClient8 Servizi Desktop remoto, metodo GetErrorDescription
- Metodo GetErrorDescription Servizi Desktop remoto, interfaccia IMsRdpClient9
- Interfaccia IMsRdpClient9 Servizi Desktop remoto, metodo GetErrorDescription
- Metodo GetErrorDescription Servizi Desktop remoto, interfaccia IMsRdpClient10
- Interfaccia IMsRdpClient10 Servizi Desktop remoto, metodo GetErrorDescription
topic_type:
- apiref
api_name:
- IMsRdpClient5.GetErrorDescription
- IMsRdpClient6.GetErrorDescription
- IMsRdpClient7.GetErrorDescription
- IMsRdpClient8.GetErrorDescription
- IMsRdpClient9.GetErrorDescription
- IMsRdpClient10.GetErrorDescription
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c402a0128286964ddeb1c53cd805e4ef6414bfb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400882"
---
# <a name="imsrdpclient5geterrordescription-method"></a><span data-ttu-id="a0043-116">Metodo IMsRdpClient5:: GetErrorDescription</span><span class="sxs-lookup"><span data-stu-id="a0043-116">IMsRdpClient5::GetErrorDescription method</span></span>

<span data-ttu-id="a0043-117">Recupera la descrizione dell'errore per gli eventi di disconnessione della sessione.</span><span class="sxs-lookup"><span data-stu-id="a0043-117">Retrieves the error description for the session disconnect events.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0043-118">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a0043-118">Syntax</span></span>


```C++
HRESULT GetErrorDescription(
  [in]  UINT disconnectReason,
  [in]  UINT extendedDisconnectReason,
  [out] BSTR *pBstrErrorMsg
);
```



## <a name="parameters"></a><span data-ttu-id="a0043-119">Parametri</span><span class="sxs-lookup"><span data-stu-id="a0043-119">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0043-120">*disconnectReason* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a0043-120">*disconnectReason* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0043-121">Motivo della disconnessione.</span><span class="sxs-lookup"><span data-stu-id="a0043-121">The disconnect reason.</span></span>

</dd> <dt>

<span data-ttu-id="a0043-122">*extendedDisconnectReason* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a0043-122">*extendedDisconnectReason* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0043-123">Fornisce informazioni dettagliate sul motivo per cui è stata avviata una disconnessione.</span><span class="sxs-lookup"><span data-stu-id="a0043-123">Provides detailed information about why a disconnect was initiated.</span></span>

</dd> <dt>

<span data-ttu-id="a0043-124">*pBstrErrorMsg* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="a0043-124">*pBstrErrorMsg* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a0043-125">Puntatore a una variabile **BSTR** che riceve il testo del messaggio di errore.</span><span class="sxs-lookup"><span data-stu-id="a0043-125">A pointer to a **BSTR** variable that receives the error message text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0043-126">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a0043-126">Return value</span></span>

<span data-ttu-id="a0043-127">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="a0043-127">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0043-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a0043-128">Requirements</span></span>



| <span data-ttu-id="a0043-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0043-129">Requirement</span></span> | <span data-ttu-id="a0043-130">Valore</span><span class="sxs-lookup"><span data-stu-id="a0043-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a0043-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a0043-131">Minimum supported client</span></span><br/> | <span data-ttu-id="a0043-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a0043-132">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="a0043-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a0043-133">Minimum supported server</span></span><br/> | <span data-ttu-id="a0043-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a0043-134">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="a0043-135">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="a0043-135">Type library</span></span><br/>             | <dl> <span data-ttu-id="a0043-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a0043-136"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="a0043-137">DLL</span><span class="sxs-lookup"><span data-stu-id="a0043-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a0043-138"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a0043-138"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="a0043-139">IID</span><span class="sxs-lookup"><span data-stu-id="a0043-139">IID</span></span><br/>                      | <span data-ttu-id="a0043-140">IID \_ IMsRdpClient5 è definito come 4eb5335b-6429-477d-B922-e06a28ecd8bf</span><span class="sxs-lookup"><span data-stu-id="a0043-140">IID\_IMsRdpClient5 is defined as 4eb5335b-6429-477d-b922-e06a28ecd8bf</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="a0043-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a0043-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0043-142">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="a0043-142">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="a0043-143">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="a0043-143">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="a0043-144">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="a0043-144">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="a0043-145">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="a0043-145">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="a0043-146">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="a0043-146">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="a0043-147">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="a0043-147">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





