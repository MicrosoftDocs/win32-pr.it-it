---
title: Metodo IMsRdpClient9 detachEvent
description: Scollega un evento.
ms.assetid: 6a3ca713-1d5c-4070-a527-ad4f532a4cbf
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo detachEvent
- Metodo detachEvent Servizi Desktop remoto, interfaccia IMsRdpClient9
- Interfaccia IMsRdpClient9 Servizi Desktop remoto, metodo detachEvent
- Metodo detachEvent Servizi Desktop remoto, interfaccia IMsRdpClient10
- Interfaccia IMsRdpClient10 Servizi Desktop remoto, metodo detachEvent
topic_type:
- apiref
api_name:
- IMsRdpClient9.detachEvent
- IMsRdpClient10.detachEvent
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 399611ea526338f4cfe40ef3a4d6543bf27f134a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119046"
---
# <a name="imsrdpclient9detachevent-method"></a><span data-ttu-id="b5904-108">IMsRdpClient9::d metodo etachEvent</span><span class="sxs-lookup"><span data-stu-id="b5904-108">IMsRdpClient9::detachEvent method</span></span>

<span data-ttu-id="b5904-109">Scollega un evento.</span><span class="sxs-lookup"><span data-stu-id="b5904-109">Detaches an event.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5904-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b5904-110">Syntax</span></span>


```C++
HRESULT detachEvent(
  [in] BSTR      eventName,
  [in] IDispatch *callback
);
```



## <a name="parameters"></a><span data-ttu-id="b5904-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="b5904-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5904-112">*EventName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b5904-112">*eventName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5904-113">Nome dell'evento.</span><span class="sxs-lookup"><span data-stu-id="b5904-113">Name of the event.</span></span>

</dd> <dt>

<span data-ttu-id="b5904-114">*callback* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="b5904-114">*callback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5904-115">Callback associato all'evento.</span><span class="sxs-lookup"><span data-stu-id="b5904-115">The callback associated with the event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5904-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b5904-116">Return value</span></span>

<span data-ttu-id="b5904-117">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="b5904-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b5904-118">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b5904-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5904-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b5904-119">Requirements</span></span>



| <span data-ttu-id="b5904-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5904-120">Requirement</span></span> | <span data-ttu-id="b5904-121">Valore</span><span class="sxs-lookup"><span data-stu-id="b5904-121">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5904-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b5904-122">Minimum supported client</span></span><br/> | <span data-ttu-id="b5904-123">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="b5904-123">Windows 8.1</span></span><br/>                                                                                                                                                                                                                                                  |
| <span data-ttu-id="b5904-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b5904-124">Minimum supported server</span></span><br/> | <span data-ttu-id="b5904-125">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="b5904-125">Windows Server 2012 R2</span></span><br/>                                                                                                                                                                                                                                       |
| <span data-ttu-id="b5904-126">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="b5904-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="b5904-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b5904-127"><dt>MsTscAx.dll</dt></span></span> </dl>                                                                                                                                                                                  |
| <span data-ttu-id="b5904-128">DLL</span><span class="sxs-lookup"><span data-stu-id="b5904-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b5904-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b5904-129"><dt>MsTscAx.dll</dt></span></span> </dl>                                                                                                                                                                                  |
| <span data-ttu-id="b5904-130">IID</span><span class="sxs-lookup"><span data-stu-id="b5904-130">IID</span></span><br/>                      | <span data-ttu-id="b5904-131">CLSID \_ MsRdpClient9 è definito come 301B94BA-5D25-4A12-BFFE-3B6E7A616585</span><span class="sxs-lookup"><span data-stu-id="b5904-131">CLSID\_MsRdpClient9 is defined as 301B94BA-5D25-4A12-BFFE-3B6E7A616585</span></span><br/> <span data-ttu-id="b5904-132">CLSID \_ MsRdpClient9NotSafeForScripting è definito come 8B918B82-7985-4c24-89DF-C33AD2BBFBCD</span><span class="sxs-lookup"><span data-stu-id="b5904-132">CLSID\_MsRdpClient9NotSafeForScripting is defined as 8B918B82-7985-4C24-89DF-C33AD2BBFBCD</span></span><br/> <span data-ttu-id="b5904-133">IID \_ IMsRdpClient9 è definito come 28904001-04B6-436c-A55B-0AF1A0883DC9</span><span class="sxs-lookup"><span data-stu-id="b5904-133">IID\_IMsRdpClient9 is defined as 28904001-04B6-436C-A55B-0AF1A0883DC9</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b5904-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b5904-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5904-135">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="b5904-135">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> <dt>

[<span data-ttu-id="b5904-136">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="b5904-136">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> </dl>

 

 





