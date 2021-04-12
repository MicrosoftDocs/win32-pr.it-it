---
title: Metodo IMsRdpDeviceCollection2 RedirectNow
description: Impone il reindirizzamento o la rimozione dei dispositivi selezionati o deselezionati dalla raccolta.
ms.assetid: 9cd5849d-a589-43f3-b904-6b2e15ca033d
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo RedirectNow
- Metodo RedirectNow Servizi Desktop remoto, interfaccia IMsRdpDeviceCollection2
- Interfaccia IMsRdpDeviceCollection2 Servizi Desktop remoto, metodo RedirectNow
topic_type:
- apiref
api_name:
- IMsRdpDeviceCollection2.RedirectNow
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 893d1e26f504d5aeb45f795ea7425eeefc3a6232
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963773"
---
# <a name="imsrdpdevicecollection2redirectnow-method"></a><span data-ttu-id="e3061-106">Metodo IMsRdpDeviceCollection2:: RedirectNow</span><span class="sxs-lookup"><span data-stu-id="e3061-106">IMsRdpDeviceCollection2::RedirectNow method</span></span>

<span data-ttu-id="e3061-107">Impone il reindirizzamento o la rimozione dei dispositivi selezionati o deselezionati dalla raccolta.</span><span class="sxs-lookup"><span data-stu-id="e3061-107">Forces devices that were selected or unselected from the collection to be redirected or removed.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3061-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e3061-108">Syntax</span></span>


```C++
HRESULT RedirectNow(
  [in] RedirectDeviceType Type
);
```



## <a name="parameters"></a><span data-ttu-id="e3061-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="e3061-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3061-110">*Tipo* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="e3061-110">*Type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3061-111">Tipo: **[ **RedirectDeviceType**](redirectdevicetype.md)**</span><span class="sxs-lookup"><span data-stu-id="e3061-111">Type: **[**RedirectDeviceType**](redirectdevicetype.md)**</span></span>

<span data-ttu-id="e3061-112">Valore dell'enumerazione [**RedirectDeviceType**](redirectdevicetype.md) che specifica il tipo di dispositivo da reindirizzare.</span><span class="sxs-lookup"><span data-stu-id="e3061-112">A value of the [**RedirectDeviceType**](redirectdevicetype.md) enumeration that specifies the type of device to be redirected.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3061-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e3061-113">Return value</span></span>

<span data-ttu-id="e3061-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="e3061-114">Type: **HRESULT**</span></span>

<span data-ttu-id="e3061-115">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="e3061-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e3061-116">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e3061-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3061-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e3061-117">Requirements</span></span>



| <span data-ttu-id="e3061-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3061-118">Requirement</span></span> | <span data-ttu-id="e3061-119">Valore</span><span class="sxs-lookup"><span data-stu-id="e3061-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e3061-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e3061-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e3061-121">Windows 8</span><span class="sxs-lookup"><span data-stu-id="e3061-121">Windows 8</span></span><br/>                                                                   |
| <span data-ttu-id="e3061-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e3061-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e3061-123">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e3061-123">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="e3061-124">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="e3061-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="e3061-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e3061-125"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="e3061-126">DLL</span><span class="sxs-lookup"><span data-stu-id="e3061-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e3061-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e3061-127"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3061-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e3061-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3061-129">**RedirectDeviceType**</span><span class="sxs-lookup"><span data-stu-id="e3061-129">**RedirectDeviceType**</span></span>](redirectdevicetype.md)
</dt> <dt>

[<span data-ttu-id="e3061-130">**IMsRdpDeviceCollection2**</span><span class="sxs-lookup"><span data-stu-id="e3061-130">**IMsRdpDeviceCollection2**</span></span>](imsrdpdevicecollection2.md)
</dt> </dl>

 

 





