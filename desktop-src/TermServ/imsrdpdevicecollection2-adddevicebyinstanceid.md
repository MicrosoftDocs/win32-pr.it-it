---
title: Metodo IMsRdpDeviceCollection2 AddDeviceByInstanceId
description: Aggiunge un dispositivo non in elenco alla raccolta di dispositivi.
ms.assetid: 7ef200c5-b99e-40c9-80e1-0758ddfa0902
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo AddDeviceByInstanceId
- Metodo AddDeviceByInstanceId Servizi Desktop remoto, interfaccia IMsRdpDeviceCollection2
- Interfaccia IMsRdpDeviceCollection2 Servizi Desktop remoto, metodo AddDeviceByInstanceId
topic_type:
- apiref
api_name:
- IMsRdpDeviceCollection2.AddDeviceByInstanceId
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97f817a5beb4d8762787c4bf2f8a3995d3918e8e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047880"
---
# <a name="imsrdpdevicecollection2adddevicebyinstanceid-method"></a><span data-ttu-id="cd98c-106">Metodo IMsRdpDeviceCollection2:: AddDeviceByInstanceId</span><span class="sxs-lookup"><span data-stu-id="cd98c-106">IMsRdpDeviceCollection2::AddDeviceByInstanceId method</span></span>

<span data-ttu-id="cd98c-107">Aggiunge un dispositivo non in elenco alla raccolta di dispositivi.</span><span class="sxs-lookup"><span data-stu-id="cd98c-107">Adds an unlisted device to the device collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd98c-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cd98c-108">Syntax</span></span>


```C++
HRESULT AddDeviceByInstanceId(
  [in] RedirectDeviceType Type,
  [in] BSTR               InstanceId
);
```



## <a name="parameters"></a><span data-ttu-id="cd98c-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="cd98c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd98c-110">*Tipo* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="cd98c-110">*Type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd98c-111">Tipo: **[ **RedirectDeviceType**](redirectdevicetype.md)**</span><span class="sxs-lookup"><span data-stu-id="cd98c-111">Type: **[**RedirectDeviceType**](redirectdevicetype.md)**</span></span>

<span data-ttu-id="cd98c-112">Valore dell'enumerazione [**RedirectDeviceType**](redirectdevicetype.md) che specifica il tipo di dispositivo da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="cd98c-112">A value of the [**RedirectDeviceType**](redirectdevicetype.md) enumeration that specifies the type of device being added.</span></span>

</dd> <dt>

<span data-ttu-id="cd98c-113">*ID* \[ istanza in\]</span><span class="sxs-lookup"><span data-stu-id="cd98c-113">*InstanceId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd98c-114">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="cd98c-114">Type: **BSTR**</span></span>

<span data-ttu-id="cd98c-115">Identificatore dell'istanza del dispositivo da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="cd98c-115">The instance identifier of the device to add.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd98c-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cd98c-116">Return value</span></span>

<span data-ttu-id="cd98c-117">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="cd98c-117">Type: **HRESULT**</span></span>

<span data-ttu-id="cd98c-118">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="cd98c-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="cd98c-119">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="cd98c-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd98c-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cd98c-120">Requirements</span></span>



| <span data-ttu-id="cd98c-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd98c-121">Requirement</span></span> | <span data-ttu-id="cd98c-122">Valore</span><span class="sxs-lookup"><span data-stu-id="cd98c-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cd98c-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cd98c-123">Minimum supported client</span></span><br/> | <span data-ttu-id="cd98c-124">Windows 8</span><span class="sxs-lookup"><span data-stu-id="cd98c-124">Windows 8</span></span><br/>                                                                   |
| <span data-ttu-id="cd98c-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cd98c-125">Minimum supported server</span></span><br/> | <span data-ttu-id="cd98c-126">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="cd98c-126">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="cd98c-127">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="cd98c-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="cd98c-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cd98c-128"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="cd98c-129">DLL</span><span class="sxs-lookup"><span data-stu-id="cd98c-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cd98c-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cd98c-130"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd98c-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cd98c-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd98c-132">**RedirectDeviceType**</span><span class="sxs-lookup"><span data-stu-id="cd98c-132">**RedirectDeviceType**</span></span>](redirectdevicetype.md)
</dt> <dt>

[<span data-ttu-id="cd98c-133">**IMsRdpDeviceCollection2**</span><span class="sxs-lookup"><span data-stu-id="cd98c-133">**IMsRdpDeviceCollection2**</span></span>](imsrdpdevicecollection2.md)
</dt> </dl>

 

 





