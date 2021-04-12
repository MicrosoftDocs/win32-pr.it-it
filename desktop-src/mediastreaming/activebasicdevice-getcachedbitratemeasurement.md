---
title: Metodo ActiveBasicDevice GetCachedBitrateMeasurement (PlayToDevice. h)
description: Ottiene la velocità in bit memorizzata nella cache.
ms.assetid: 78C3C5D7-C46B-413D-BC18-C3861E5FDAA5
keywords:
- API di streaming multimediale del metodo GetCachedBitrateMeasurement
- API di streaming multimediale del metodo GetCachedBitrateMeasurement, interfaccia ActiveBasicDevice
- API di streaming multimediale dell'interfaccia ActiveBasicDevice, metodo GetCachedBitrateMeasurement
topic_type:
- apiref
api_name:
- ActiveBasicDevice.GetCachedBitrateMeasurement
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d15b38ba2730d2023b09c2fa0352ade1f1532724
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518700"
---
# <a name="activebasicdevicegetcachedbitratemeasurement-method"></a><span data-ttu-id="ff88a-106">Metodo ActiveBasicDevice:: GetCachedBitrateMeasurement</span><span class="sxs-lookup"><span data-stu-id="ff88a-106">ActiveBasicDevice::GetCachedBitrateMeasurement method</span></span>

<span data-ttu-id="ff88a-107">Ottiene la velocità in bit memorizzata nella cache.</span><span class="sxs-lookup"><span data-stu-id="ff88a-107">Gets the cached bitrate.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff88a-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ff88a-108">Syntax</span></span>


```C++
HRESULT GetCachedBitrateMeasurement(
  [in]          GUID   physicalNetworkInterface,
  [out, retval] UINT64 *bitrate
);
```



## <a name="parameters"></a><span data-ttu-id="ff88a-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="ff88a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff88a-110">*physicalNetworkInterface* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ff88a-110">*physicalNetworkInterface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff88a-111">Specifica l'interfaccia di rete fisica.</span><span class="sxs-lookup"><span data-stu-id="ff88a-111">Specifies the physical network interface.</span></span>

</dd> <dt>

<span data-ttu-id="ff88a-112">*velocità in bit* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="ff88a-112">*bitrate* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="ff88a-113">Riceve il valore di velocità in bit.</span><span class="sxs-lookup"><span data-stu-id="ff88a-113">Receives the bitrate value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff88a-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ff88a-114">Return value</span></span>

<span data-ttu-id="ff88a-115">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="ff88a-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ff88a-116">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ff88a-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff88a-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ff88a-117">Requirements</span></span>



| <span data-ttu-id="ff88a-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="ff88a-118">Requirement</span></span> | <span data-ttu-id="ff88a-119">Valore</span><span class="sxs-lookup"><span data-stu-id="ff88a-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff88a-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ff88a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ff88a-121">Windows 8.1 \[ solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ff88a-121">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="ff88a-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ff88a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ff88a-123">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="ff88a-123">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="ff88a-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ff88a-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="ff88a-125"><dt>PlayToDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="ff88a-125"><dt>PlayToDevice.h</dt></span></span> </dl>   |
| <span data-ttu-id="ff88a-126">IDL</span><span class="sxs-lookup"><span data-stu-id="ff88a-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ff88a-127"><dt>PlayToDevice. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ff88a-127"><dt>PlayToDevice.idl</dt></span></span> </dl> |
| <span data-ttu-id="ff88a-128">DLL</span><span class="sxs-lookup"><span data-stu-id="ff88a-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ff88a-129"><dt>Playtodevice.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ff88a-129"><dt>Playtodevice.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff88a-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ff88a-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="ff88a-131">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ff88a-131">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span></span>
</dt> </dl>

 

