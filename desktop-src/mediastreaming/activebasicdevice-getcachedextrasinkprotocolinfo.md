---
title: Metodo ActiveBasicDevice GetCachedExtraSinkProtocolInfo (PlayToDevice. h)
description: Ottiene informazioni aggiuntive sul protocollo sink memorizzato nella cache per il dispositivo.
ms.assetid: 97112921-1C1D-4FC9-8FE6-1381F3773351
keywords:
- API di streaming multimediale del metodo GetCachedExtraSinkProtocolInfo
- API di streaming multimediale del metodo GetCachedExtraSinkProtocolInfo, interfaccia ActiveBasicDevice
- API di streaming multimediale dell'interfaccia ActiveBasicDevice, metodo GetCachedExtraSinkProtocolInfo
topic_type:
- apiref
api_name:
- ActiveBasicDevice.GetCachedExtraSinkProtocolInfo
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be5bb013d1356d5ff02e709a92f01eceff6c2e0f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400720"
---
# <a name="activebasicdevicegetcachedextrasinkprotocolinfo-method"></a><span data-ttu-id="5f61a-106">Metodo ActiveBasicDevice:: GetCachedExtraSinkProtocolInfo</span><span class="sxs-lookup"><span data-stu-id="5f61a-106">ActiveBasicDevice::GetCachedExtraSinkProtocolInfo method</span></span>

<span data-ttu-id="5f61a-107">Ottiene informazioni aggiuntive sul protocollo sink memorizzato nella cache per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5f61a-107">Gets additional cached sink protocol info for the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f61a-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5f61a-108">Syntax</span></span>


```C++
HRESULT GetCachedExtraSinkProtocolInfo(
  [out, retval] HSTRING *value
);
```



## <a name="parameters"></a><span data-ttu-id="5f61a-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="5f61a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f61a-110">*valore* \[ di out, retval\]</span><span class="sxs-lookup"><span data-stu-id="5f61a-110">*value* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="5f61a-111">Informazioni aggiuntive sul protocollo sink memorizzato nella cache per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5f61a-111">The extra cached sink protocol info for the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f61a-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5f61a-112">Return value</span></span>

<span data-ttu-id="5f61a-113">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="5f61a-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5f61a-114">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5f61a-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f61a-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5f61a-115">Requirements</span></span>



| <span data-ttu-id="5f61a-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f61a-116">Requirement</span></span> | <span data-ttu-id="5f61a-117">Valore</span><span class="sxs-lookup"><span data-stu-id="5f61a-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f61a-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5f61a-118">Minimum supported client</span></span><br/> | <span data-ttu-id="5f61a-119">Windows 8.1 \[ solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5f61a-119">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="5f61a-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5f61a-120">Minimum supported server</span></span><br/> | <span data-ttu-id="5f61a-121">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="5f61a-121">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="5f61a-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5f61a-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="5f61a-123"><dt>PlayToDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="5f61a-123"><dt>PlayToDevice.h</dt></span></span> </dl>   |
| <span data-ttu-id="5f61a-124">IDL</span><span class="sxs-lookup"><span data-stu-id="5f61a-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5f61a-125"><dt>PlayToDevice. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5f61a-125"><dt>PlayToDevice.idl</dt></span></span> </dl> |
| <span data-ttu-id="5f61a-126">DLL</span><span class="sxs-lookup"><span data-stu-id="5f61a-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5f61a-127"><dt>Playtodevice.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5f61a-127"><dt>Playtodevice.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f61a-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5f61a-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="5f61a-129">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5f61a-129">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span></span>
</dt> </dl>

 

