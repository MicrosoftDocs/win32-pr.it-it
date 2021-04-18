---
title: Metodo ActiveBasicDevice SetCachedSinkProtocolInfo (PlayToDevice. h)
description: Ottiene le informazioni sul protocollo sink memorizzato nella cache per il dispositivo. | Metodo ActiveBasicDevice SetCachedSinkProtocolInfo (PlayToDevice. h)
ms.assetid: C4856B97-89F9-43EC-B778-9E0CDAAF2C47
keywords:
- API di streaming multimediale del metodo SetCachedSinkProtocolInfo
- API di streaming multimediale del metodo SetCachedSinkProtocolInfo, interfaccia ActiveBasicDevice
- API di streaming multimediale dell'interfaccia ActiveBasicDevice, metodo SetCachedSinkProtocolInfo
topic_type:
- apiref
api_name:
- ActiveBasicDevice.SetCachedSinkProtocolInfo
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9100cb8faeb685a0cc7a8b7b73deb11afca29a3e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321899"
---
# <a name="activebasicdevicesetcachedsinkprotocolinfo-method"></a><span data-ttu-id="845f5-107">Metodo ActiveBasicDevice:: SetCachedSinkProtocolInfo</span><span class="sxs-lookup"><span data-stu-id="845f5-107">ActiveBasicDevice::SetCachedSinkProtocolInfo method</span></span>

<span data-ttu-id="845f5-108">Ottiene le informazioni sul protocollo sink memorizzato nella cache per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="845f5-108">Gets the cached sink protocol info for the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="845f5-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="845f5-109">Syntax</span></span>


```C++
HRESULT SetCachedSinkProtocolInfo(
  [in] GUID   physicalNetworkInterface,
  [in] UINT64 bitrate
);
```



## <a name="parameters"></a><span data-ttu-id="845f5-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="845f5-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="845f5-111">*physicalNetworkInterface* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="845f5-111">*physicalNetworkInterface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="845f5-112">Specifica l'interfaccia di rete fisica.</span><span class="sxs-lookup"><span data-stu-id="845f5-112">Specifies the physical network interface.</span></span>

</dd> <dt>

<span data-ttu-id="845f5-113">*velocità in bit* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="845f5-113">*bitrate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="845f5-114">Valore della velocità in bit.</span><span class="sxs-lookup"><span data-stu-id="845f5-114">The bitrate value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="845f5-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="845f5-115">Return value</span></span>

<span data-ttu-id="845f5-116">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="845f5-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="845f5-117">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="845f5-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="845f5-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="845f5-118">Requirements</span></span>



| <span data-ttu-id="845f5-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="845f5-119">Requirement</span></span> | <span data-ttu-id="845f5-120">Valore</span><span class="sxs-lookup"><span data-stu-id="845f5-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="845f5-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="845f5-121">Minimum supported client</span></span><br/> | <span data-ttu-id="845f5-122">Windows 8.1 \[ solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="845f5-122">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="845f5-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="845f5-123">Minimum supported server</span></span><br/> | <span data-ttu-id="845f5-124">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="845f5-124">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="845f5-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="845f5-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="845f5-126"><dt>PlayToDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="845f5-126"><dt>PlayToDevice.h</dt></span></span> </dl>   |
| <span data-ttu-id="845f5-127">IDL</span><span class="sxs-lookup"><span data-stu-id="845f5-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="845f5-128"><dt>PlayToDevice. idl</dt></span><span class="sxs-lookup"><span data-stu-id="845f5-128"><dt>PlayToDevice.idl</dt></span></span> </dl> |
| <span data-ttu-id="845f5-129">DLL</span><span class="sxs-lookup"><span data-stu-id="845f5-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="845f5-130"><dt>Playtodevice.dll</dt></span><span class="sxs-lookup"><span data-stu-id="845f5-130"><dt>Playtodevice.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="845f5-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="845f5-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="845f5-132">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="845f5-132">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span></span>
</dt> </dl>

 

