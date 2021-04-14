---
title: Metodo ActiveBasicDevice SetCachedBitrateMeasurement (PlayToDevice. h)
description: Imposta la velocità in bit memorizzata nella cache.
ms.assetid: 53530217-CFF7-4376-B155-E11044621E2D
keywords:
- API di streaming multimediale del metodo SetCachedBitrateMeasurement
- API di streaming multimediale del metodo SetCachedBitrateMeasurement, interfaccia ActiveBasicDevice
- API di streaming multimediale dell'interfaccia ActiveBasicDevice, metodo SetCachedBitrateMeasurement
topic_type:
- apiref
api_name:
- ActiveBasicDevice.SetCachedBitrateMeasurement
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c681776b00eb9d911a4fa75a9d360b39a3d2b8c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478976"
---
# <a name="activebasicdevicesetcachedbitratemeasurement-method"></a><span data-ttu-id="bc353-106">Metodo ActiveBasicDevice:: SetCachedBitrateMeasurement</span><span class="sxs-lookup"><span data-stu-id="bc353-106">ActiveBasicDevice::SetCachedBitrateMeasurement method</span></span>

<span data-ttu-id="bc353-107">Imposta la velocità in bit memorizzata nella cache.</span><span class="sxs-lookup"><span data-stu-id="bc353-107">Sets the cached bitrate.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc353-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bc353-108">Syntax</span></span>


```C++
HRESULT SetCachedBitrateMeasurement(
  [in] GUID   physicalNetworkInterface,
  [in] UINT64 bitrate
);
```



## <a name="parameters"></a><span data-ttu-id="bc353-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="bc353-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc353-110">*physicalNetworkInterface* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bc353-110">*physicalNetworkInterface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc353-111">Specifica l'interfaccia di rete fisica.</span><span class="sxs-lookup"><span data-stu-id="bc353-111">Specifies the physical network interface.</span></span>

</dd> <dt>

<span data-ttu-id="bc353-112">*velocità in bit* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bc353-112">*bitrate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc353-113">Valore a cui impostare la velocità in bit.</span><span class="sxs-lookup"><span data-stu-id="bc353-113">The value to set the bitrate to.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc353-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bc353-114">Return value</span></span>

<span data-ttu-id="bc353-115">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="bc353-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="bc353-116">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="bc353-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc353-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bc353-117">Requirements</span></span>



| <span data-ttu-id="bc353-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="bc353-118">Requirement</span></span> | <span data-ttu-id="bc353-119">Valore</span><span class="sxs-lookup"><span data-stu-id="bc353-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc353-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bc353-120">Minimum supported client</span></span><br/> | <span data-ttu-id="bc353-121">Windows 8.1 \[ solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="bc353-121">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="bc353-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bc353-122">Minimum supported server</span></span><br/> | <span data-ttu-id="bc353-123">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="bc353-123">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="bc353-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bc353-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="bc353-125"><dt>PlayToDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="bc353-125"><dt>PlayToDevice.h</dt></span></span> </dl>   |
| <span data-ttu-id="bc353-126">IDL</span><span class="sxs-lookup"><span data-stu-id="bc353-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="bc353-127"><dt>PlayToDevice. idl</dt></span><span class="sxs-lookup"><span data-stu-id="bc353-127"><dt>PlayToDevice.idl</dt></span></span> </dl> |
| <span data-ttu-id="bc353-128">DLL</span><span class="sxs-lookup"><span data-stu-id="bc353-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bc353-129"><dt>Playtodevice.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bc353-129"><dt>Playtodevice.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc353-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bc353-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="bc353-131">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="bc353-131">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span></span>
</dt> </dl>

 

