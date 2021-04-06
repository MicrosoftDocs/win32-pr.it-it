---
title: Metodo IMsRdpClient7 GetStatusText (OpenService. h)
description: Recupera il testo di stato per il codice di stato specificato.
ms.assetid: 1da2280a-c26d-4caa-b227-c289055f3aa9
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo GetStatusText
- Metodo GetStatusText Servizi Desktop remoto, interfaccia IMsRdpClient7
- Interfaccia IMsRdpClient7 Servizi Desktop remoto, metodo GetStatusText
- Metodo GetStatusText Servizi Desktop remoto, interfaccia IMsRdpClient8
- Interfaccia IMsRdpClient8 Servizi Desktop remoto, metodo GetStatusText
- Metodo GetStatusText Servizi Desktop remoto, interfaccia IMsRdpClient9
- Interfaccia IMsRdpClient9 Servizi Desktop remoto, metodo GetStatusText
- Metodo GetStatusText Servizi Desktop remoto, interfaccia IMsRdpClient10
- Interfaccia IMsRdpClient10 Servizi Desktop remoto, metodo GetStatusText
topic_type:
- apiref
api_name:
- IMsRdpClient7.GetStatusText
- IMsRdpClient8.GetStatusText
- IMsRdpClient9.GetStatusText
- IMsRdpClient10.GetStatusText
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 820628bfba59ec980e5128b9d9df3ee21b49a064
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742143"
---
# <a name="imsrdpclient7getstatustext-method"></a><span data-ttu-id="930d3-112">Metodo IMsRdpClient7:: GetStatusText</span><span class="sxs-lookup"><span data-stu-id="930d3-112">IMsRdpClient7::GetStatusText method</span></span>

<span data-ttu-id="930d3-113">Recupera il testo di stato per il codice di stato specificato.</span><span class="sxs-lookup"><span data-stu-id="930d3-113">Retrieves the status text for the specified status code.</span></span>

## <a name="syntax"></a><span data-ttu-id="930d3-114">Sintassi</span><span class="sxs-lookup"><span data-stu-id="930d3-114">Syntax</span></span>


```C++
HRESULT GetStatusText(
  [in]          UINT statusCode,
  [out, retval] BSTR *pBstrStatusText
);
```



## <a name="parameters"></a><span data-ttu-id="930d3-115">Parametri</span><span class="sxs-lookup"><span data-stu-id="930d3-115">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="930d3-116">*statusCode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="930d3-116">*statusCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="930d3-117">**Uint** che specifica il codice di stato per il quale recuperare il testo.</span><span class="sxs-lookup"><span data-stu-id="930d3-117">A **UINT** that specifies the status code to retrieve the text for.</span></span>

</dd> <dt>

<span data-ttu-id="930d3-118">*pBstrStatusText* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="930d3-118">*pBstrStatusText* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="930d3-119">Indirizzo di un **BSTR** che riceve il testo dello stato.</span><span class="sxs-lookup"><span data-stu-id="930d3-119">The address of a **BSTR** that receives the status text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="930d3-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="930d3-120">Return value</span></span>

<span data-ttu-id="930d3-121">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="930d3-121">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="930d3-122">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="930d3-122">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="930d3-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="930d3-123">Requirements</span></span>



| <span data-ttu-id="930d3-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="930d3-124">Requirement</span></span> | <span data-ttu-id="930d3-125">Valore</span><span class="sxs-lookup"><span data-stu-id="930d3-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="930d3-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="930d3-126">Minimum supported client</span></span><br/> | <span data-ttu-id="930d3-127">Windows 7</span><span class="sxs-lookup"><span data-stu-id="930d3-127">Windows 7</span></span><br/>                                                                     |
| <span data-ttu-id="930d3-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="930d3-128">Minimum supported server</span></span><br/> | <span data-ttu-id="930d3-129">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="930d3-129">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="930d3-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="930d3-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="930d3-131"><dt>OpenService. h</dt></span><span class="sxs-lookup"><span data-stu-id="930d3-131"><dt>Openservice.h</dt></span></span> </dl> |
| <span data-ttu-id="930d3-132">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="930d3-132">Type library</span></span><br/>             | <dl> <span data-ttu-id="930d3-133"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="930d3-133"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="930d3-134">DLL</span><span class="sxs-lookup"><span data-stu-id="930d3-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="930d3-135"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="930d3-135"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="930d3-136">IID</span><span class="sxs-lookup"><span data-stu-id="930d3-136">IID</span></span><br/>                      | <span data-ttu-id="930d3-137">IID \_ IMsRdpClient7 è definito come b2a5b5ce-3461-444A-91D4-add26d070638</span><span class="sxs-lookup"><span data-stu-id="930d3-137">IID\_IMsRdpClient7 is defined as b2a5b5ce-3461-444a-91d4-add26d070638</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="930d3-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="930d3-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="930d3-139">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="930d3-139">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="930d3-140">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="930d3-140">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="930d3-141">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="930d3-141">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="930d3-142">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="930d3-142">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





