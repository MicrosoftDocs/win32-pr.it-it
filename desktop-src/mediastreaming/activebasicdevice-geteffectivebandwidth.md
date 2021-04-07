---
title: Metodo ActiveBasicDevice GetEffectiveBandwidth (PlayToDevice. h)
description: Ottiene la larghezza di banda effettiva corrente per il dispositivo.
ms.assetid: 88CE03AB-6F87-4E43-B673-2C693D351F10
keywords:
- API di streaming multimediale del metodo GetEffectiveBandwidth
- API di streaming multimediale del metodo GetEffectiveBandwidth, interfaccia ActiveBasicDevice
- API di streaming multimediale dell'interfaccia ActiveBasicDevice, metodo GetEffectiveBandwidth
topic_type:
- apiref
api_name:
- ActiveBasicDevice.GetEffectiveBandwidth
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05a97e9f1dc77040d4f55bc8997e553e0cdc5239
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048715"
---
# <a name="activebasicdevicegeteffectivebandwidth-method"></a><span data-ttu-id="64d46-106">Metodo ActiveBasicDevice:: GetEffectiveBandwidth</span><span class="sxs-lookup"><span data-stu-id="64d46-106">ActiveBasicDevice::GetEffectiveBandwidth method</span></span>

<span data-ttu-id="64d46-107">Ottiene la larghezza di banda effettiva corrente per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="64d46-107">Gets the current effective bandwidth for the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="64d46-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="64d46-108">Syntax</span></span>


```C++
HRESULT GetEffectiveBandwidth(
  [in, retval] boolean transmitSpeed,
  [out]        ULONG64 *currentSpeed
);
```



## <a name="parameters"></a><span data-ttu-id="64d46-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="64d46-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64d46-110">*transmitSpeed* \[ in, retval\]</span><span class="sxs-lookup"><span data-stu-id="64d46-110">*transmitSpeed* \[in, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="64d46-111">Specifica se viene recuperata la velocità di trasmissione o se viene recuperata la velocità di ricezione.</span><span class="sxs-lookup"><span data-stu-id="64d46-111">Specifies whether the transmit speed is retrieved or the receive speed is retrieved.</span></span>

<span data-ttu-id="64d46-112">**true** per recuperare la velocità di trasmissione.</span><span class="sxs-lookup"><span data-stu-id="64d46-112">**true** to retrieve the transmit speed.</span></span> <span data-ttu-id="64d46-113">**false** per recuperare la velocità di ricezione.</span><span class="sxs-lookup"><span data-stu-id="64d46-113">**false** to retrieve the receive speed.</span></span>

</dd> <dt>

<span data-ttu-id="64d46-114">*currentSpeed* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="64d46-114">*currentSpeed* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="64d46-115">Riceve la larghezza di banda effettiva corrente.</span><span class="sxs-lookup"><span data-stu-id="64d46-115">Receives the current effective bandwidth.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64d46-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="64d46-116">Return value</span></span>

<span data-ttu-id="64d46-117">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="64d46-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="64d46-118">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="64d46-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="64d46-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="64d46-119">Requirements</span></span>



| <span data-ttu-id="64d46-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="64d46-120">Requirement</span></span> | <span data-ttu-id="64d46-121">Valore</span><span class="sxs-lookup"><span data-stu-id="64d46-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="64d46-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="64d46-122">Minimum supported client</span></span><br/> | <span data-ttu-id="64d46-123">Windows 8.1 \[ solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="64d46-123">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="64d46-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="64d46-124">Minimum supported server</span></span><br/> | <span data-ttu-id="64d46-125">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="64d46-125">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="64d46-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="64d46-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="64d46-127"><dt>PlayToDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="64d46-127"><dt>PlayToDevice.h</dt></span></span> </dl>   |
| <span data-ttu-id="64d46-128">IDL</span><span class="sxs-lookup"><span data-stu-id="64d46-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="64d46-129"><dt>PlayToDevice. idl</dt></span><span class="sxs-lookup"><span data-stu-id="64d46-129"><dt>PlayToDevice.idl</dt></span></span> </dl> |
| <span data-ttu-id="64d46-130">DLL</span><span class="sxs-lookup"><span data-stu-id="64d46-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="64d46-131"><dt>Playtodevice.dll</dt></span><span class="sxs-lookup"><span data-stu-id="64d46-131"><dt>Playtodevice.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64d46-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="64d46-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="64d46-133">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="64d46-133">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span></span>
</dt> </dl>

 

