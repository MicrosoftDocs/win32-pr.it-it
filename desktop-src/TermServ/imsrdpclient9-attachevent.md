---
title: Metodo IMsRdpClient9 attachEvent
description: Connette un evento.
ms.assetid: 3a887aeb-a74f-4477-8cf3-8ac43a31fa26
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo attachEvent
- Metodo attachEvent Servizi Desktop remoto, interfaccia IMsRdpClient9
- Interfaccia IMsRdpClient9 Servizi Desktop remoto, metodo attachEvent
- Metodo attachEvent Servizi Desktop remoto, interfaccia IMsRdpClient10
- Interfaccia IMsRdpClient10 Servizi Desktop remoto, metodo attachEvent
topic_type:
- apiref
api_name:
- IMsRdpClient9.attachEvent
- IMsRdpClient10.attachEvent
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1bd3fd518fba825c209a4170e6b314a7b774a49
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475244"
---
# <a name="imsrdpclient9attachevent-method"></a><span data-ttu-id="44553-108">Metodo IMsRdpClient9:: attachEvent</span><span class="sxs-lookup"><span data-stu-id="44553-108">IMsRdpClient9::attachEvent method</span></span>

<span data-ttu-id="44553-109">Connette un evento.</span><span class="sxs-lookup"><span data-stu-id="44553-109">Attaches an event.</span></span>

## <a name="syntax"></a><span data-ttu-id="44553-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="44553-110">Syntax</span></span>


```C++
HRESULT attachEvent(
  [in] BSTR      eventName,
  [in] IDispatch *callback
);
```



## <a name="parameters"></a><span data-ttu-id="44553-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="44553-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44553-112">*EventName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="44553-112">*eventName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44553-113">Evento da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="44553-113">The event to attach.</span></span>

</dd> <dt>

<span data-ttu-id="44553-114">*callback* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="44553-114">*callback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44553-115">Callback.</span><span class="sxs-lookup"><span data-stu-id="44553-115">The callback.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44553-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="44553-116">Return value</span></span>

<span data-ttu-id="44553-117">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="44553-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="44553-118">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="44553-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="44553-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="44553-119">Requirements</span></span>



| <span data-ttu-id="44553-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="44553-120">Requirement</span></span> | <span data-ttu-id="44553-121">Valore</span><span class="sxs-lookup"><span data-stu-id="44553-121">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="44553-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="44553-122">Minimum supported client</span></span><br/> | <span data-ttu-id="44553-123">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="44553-123">Windows 8.1</span></span><br/>                                                                                                                                                                                                                                                  |
| <span data-ttu-id="44553-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="44553-124">Minimum supported server</span></span><br/> | <span data-ttu-id="44553-125">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="44553-125">Windows Server 2012 R2</span></span><br/>                                                                                                                                                                                                                                       |
| <span data-ttu-id="44553-126">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="44553-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="44553-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="44553-127"><dt>MsTscAx.dll</dt></span></span> </dl>                                                                                                                                                                                  |
| <span data-ttu-id="44553-128">DLL</span><span class="sxs-lookup"><span data-stu-id="44553-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="44553-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="44553-129"><dt>MsTscAx.dll</dt></span></span> </dl>                                                                                                                                                                                  |
| <span data-ttu-id="44553-130">IID</span><span class="sxs-lookup"><span data-stu-id="44553-130">IID</span></span><br/>                      | <span data-ttu-id="44553-131">CLSID \_ MsRdpClient9 è definito come 301B94BA-5D25-4A12-BFFE-3B6E7A616585</span><span class="sxs-lookup"><span data-stu-id="44553-131">CLSID\_MsRdpClient9 is defined as 301B94BA-5D25-4A12-BFFE-3B6E7A616585</span></span><br/> <span data-ttu-id="44553-132">CLSID \_ MsRdpClient9NotSafeForScripting è definito come 8B918B82-7985-4c24-89DF-C33AD2BBFBCD</span><span class="sxs-lookup"><span data-stu-id="44553-132">CLSID\_MsRdpClient9NotSafeForScripting is defined as 8B918B82-7985-4C24-89DF-C33AD2BBFBCD</span></span><br/> <span data-ttu-id="44553-133">IID \_ IMsRdpClient9 è definito come 28904001-04B6-436c-A55B-0AF1A0883DC9</span><span class="sxs-lookup"><span data-stu-id="44553-133">IID\_IMsRdpClient9 is defined as 28904001-04B6-436C-A55B-0AF1A0883DC9</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="44553-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="44553-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44553-135">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="44553-135">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> <dt>

[<span data-ttu-id="44553-136">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="44553-136">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> </dl>

 

 





