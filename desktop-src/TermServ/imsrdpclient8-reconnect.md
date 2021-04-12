---
title: Metodo di riconnessione IMsRdpClient8
description: Si riconnette alla sessione remota con la nuova larghezza e altezza del desktop.
ms.assetid: A2C4101D-780A-4973-B87C-025D9140C4BC
ms.tgt_platform: multiple
keywords:
- Metodo di riconnessione Servizi Desktop remoto
- Metodo di riconnessione Servizi Desktop remoto, interfaccia IMsRdpClient8
- Interfaccia IMsRdpClient8 Servizi Desktop remoto, metodo di riconnessione
- Metodo di riconnessione Servizi Desktop remoto, interfaccia IMsRdpClient9
- Interfaccia IMsRdpClient9 Servizi Desktop remoto, metodo di riconnessione
- Metodo di riconnessione Servizi Desktop remoto, interfaccia IMsRdpClient10
- Interfaccia IMsRdpClient10 Servizi Desktop remoto, metodo di riconnessione
topic_type:
- apiref
api_name:
- IMsRdpClient8.Reconnect
- IMsRdpClient9.Reconnect
- IMsRdpClient10.Reconnect
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d62072c56852af6be2965ce63aecf4634de87d11
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519246"
---
# <a name="imsrdpclient8reconnect-method"></a><span data-ttu-id="1c940-110">Metodo IMsRdpClient8:: Reconnect</span><span class="sxs-lookup"><span data-stu-id="1c940-110">IMsRdpClient8::Reconnect method</span></span>

<span data-ttu-id="1c940-111">Si riconnette alla sessione remota con la nuova larghezza e altezza del desktop.</span><span class="sxs-lookup"><span data-stu-id="1c940-111">Reconnects to the remote session with the new desktop width and height.</span></span> <span data-ttu-id="1c940-112">Il controllo deve essere già connesso a una sessione remota affinché questo metodo abbia esito positivo.</span><span class="sxs-lookup"><span data-stu-id="1c940-112">The control must already be connected to a remote session for this method to succeed.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c940-113">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1c940-113">Syntax</span></span>


```C++
HRESULT Reconnect(
  [in]          ULONG                  ulWidth,
  [in]          ULONG                  ulHeight,
  [out, retval] ControlReconnectStatus *pReconnectStatus
);
```



## <a name="parameters"></a><span data-ttu-id="1c940-114">Parametri</span><span class="sxs-lookup"><span data-stu-id="1c940-114">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c940-115">*ulWidth* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1c940-115">*ulWidth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c940-116">Tipo: **ULONG**</span><span class="sxs-lookup"><span data-stu-id="1c940-116">Type: **ULONG**</span></span>

<span data-ttu-id="1c940-117">La nuova larghezza del desktop, in pixel.</span><span class="sxs-lookup"><span data-stu-id="1c940-117">The new desktop width, in pixels.</span></span> <span data-ttu-id="1c940-118">Per le restrizioni relative ai valori, vedere la proprietà [**DesktopWidth**](imstscax-desktopwidth.md) .</span><span class="sxs-lookup"><span data-stu-id="1c940-118">See the [**DesktopWidth**](imstscax-desktopwidth.md) property for value restrictions.</span></span>

</dd> <dt>

<span data-ttu-id="1c940-119">*ulHeight* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1c940-119">*ulHeight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c940-120">Tipo: **ULONG**</span><span class="sxs-lookup"><span data-stu-id="1c940-120">Type: **ULONG**</span></span>

<span data-ttu-id="1c940-121">Nuova altezza del desktop, in pixel.</span><span class="sxs-lookup"><span data-stu-id="1c940-121">The new desktop height, in pixels.</span></span> <span data-ttu-id="1c940-122">Per le restrizioni relative ai valori, vedere la proprietà [**DesktopHeight**](imstscax-desktopheight.md) .</span><span class="sxs-lookup"><span data-stu-id="1c940-122">See the [**DesktopHeight**](imstscax-desktopheight.md) property for value restrictions.</span></span>

</dd> <dt>

<span data-ttu-id="1c940-123">*pReconnectStatus* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="1c940-123">*pReconnectStatus* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="1c940-124">Tipo: \**[**ControlReconnectStatus**](controlreconnectstatus.md) \** _</span><span class="sxs-lookup"><span data-stu-id="1c940-124">Type: \**[**ControlReconnectStatus**](controlreconnectstatus.md)\** _</span></span>

<span data-ttu-id="1c940-125">Puntatore a una variabile [_ *ControlReconnectStatus* \*](controlreconnectstatus.md) che riceve lo stato dell'operazione di riconnessione.</span><span class="sxs-lookup"><span data-stu-id="1c940-125">A pointer to a [_ *ControlReconnectStatus*\*](controlreconnectstatus.md) variable that receives the status of the reconnect operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c940-126">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1c940-126">Return value</span></span>

<span data-ttu-id="1c940-127">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="1c940-127">Type: **HRESULT**</span></span>

<span data-ttu-id="1c940-128">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="1c940-128">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1c940-129">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1c940-129">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c940-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1c940-130">Requirements</span></span>



| <span data-ttu-id="1c940-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="1c940-131">Requirement</span></span> | <span data-ttu-id="1c940-132">Valore</span><span class="sxs-lookup"><span data-stu-id="1c940-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1c940-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1c940-133">Minimum supported client</span></span><br/> | <span data-ttu-id="1c940-134">Windows 8</span><span class="sxs-lookup"><span data-stu-id="1c940-134">Windows 8</span></span><br/>                                                                   |
| <span data-ttu-id="1c940-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1c940-135">Minimum supported server</span></span><br/> | <span data-ttu-id="1c940-136">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1c940-136">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="1c940-137">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="1c940-137">Type library</span></span><br/>             | <dl> <span data-ttu-id="1c940-138"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1c940-138"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="1c940-139">DLL</span><span class="sxs-lookup"><span data-stu-id="1c940-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1c940-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1c940-140"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="1c940-141">IID</span><span class="sxs-lookup"><span data-stu-id="1c940-141">IID</span></span><br/>                      | <span data-ttu-id="1c940-142">IID \_ IMsRdpClient8 è definito come 4247E044-9271-43a9-BC49-E2AD9E855D62</span><span class="sxs-lookup"><span data-stu-id="1c940-142">IID\_IMsRdpClient8 is defined as 4247E044-9271-43A9-BC49-E2AD9E855D62</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="1c940-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1c940-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c940-144">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="1c940-144">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="1c940-145">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="1c940-145">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="1c940-146">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="1c940-146">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> <dt>

[<span data-ttu-id="1c940-147">**ControlReconnectStatus**</span><span class="sxs-lookup"><span data-stu-id="1c940-147">**ControlReconnectStatus**</span></span>](controlreconnectstatus.md)
</dt> </dl>

 

 





