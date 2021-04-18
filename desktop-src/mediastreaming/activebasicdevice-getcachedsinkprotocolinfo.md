---
title: Metodo ActiveBasicDevice GetCachedSinkProtocolInfo (PlayToDevice. h)
description: Ottiene le informazioni sul protocollo sink memorizzato nella cache per il dispositivo. | Metodo ActiveBasicDevice GetCachedSinkProtocolInfo (PlayToDevice. h)
ms.assetid: C6A3C4B5-1883-4E71-83D2-11E378A4FBCA
keywords:
- API di streaming multimediale del metodo GetCachedSinkProtocolInfo
- API di streaming multimediale del metodo GetCachedSinkProtocolInfo, interfaccia ActiveBasicDevice
- API di streaming multimediale dell'interfaccia ActiveBasicDevice, metodo GetCachedSinkProtocolInfo
topic_type:
- apiref
api_name:
- ActiveBasicDevice.GetCachedSinkProtocolInfo
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 056cc351a1ecd1c8eef07d4e994da8e895aa85f8
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321676"
---
# <a name="activebasicdevicegetcachedsinkprotocolinfo-method"></a><span data-ttu-id="213fe-107">Metodo ActiveBasicDevice:: GetCachedSinkProtocolInfo</span><span class="sxs-lookup"><span data-stu-id="213fe-107">ActiveBasicDevice::GetCachedSinkProtocolInfo method</span></span>

<span data-ttu-id="213fe-108">Ottiene le informazioni sul protocollo sink memorizzato nella cache per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="213fe-108">Gets the cached sink protocol info for the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="213fe-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="213fe-109">Syntax</span></span>


```C++
HRESULT GetCachedSinkProtocolInfo(
  [out, retval] HSTRING *value
);
```



## <a name="parameters"></a><span data-ttu-id="213fe-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="213fe-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="213fe-111">*valore* \[ di out, retval\]</span><span class="sxs-lookup"><span data-stu-id="213fe-111">*value* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="213fe-112">Informazioni sul protocollo sink memorizzato nella cache per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="213fe-112">The cached sink protocol info for the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="213fe-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="213fe-113">Return value</span></span>

<span data-ttu-id="213fe-114">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="213fe-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="213fe-115">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="213fe-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="213fe-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="213fe-116">Requirements</span></span>



| <span data-ttu-id="213fe-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="213fe-117">Requirement</span></span> | <span data-ttu-id="213fe-118">Valore</span><span class="sxs-lookup"><span data-stu-id="213fe-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="213fe-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="213fe-119">Minimum supported client</span></span><br/> | <span data-ttu-id="213fe-120">Windows 8.1 \[ solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="213fe-120">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="213fe-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="213fe-121">Minimum supported server</span></span><br/> | <span data-ttu-id="213fe-122">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="213fe-122">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="213fe-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="213fe-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="213fe-124"><dt>PlayToDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="213fe-124"><dt>PlayToDevice.h</dt></span></span> </dl>   |
| <span data-ttu-id="213fe-125">IDL</span><span class="sxs-lookup"><span data-stu-id="213fe-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="213fe-126"><dt>PlayToDevice. idl</dt></span><span class="sxs-lookup"><span data-stu-id="213fe-126"><dt>PlayToDevice.idl</dt></span></span> </dl> |
| <span data-ttu-id="213fe-127">DLL</span><span class="sxs-lookup"><span data-stu-id="213fe-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="213fe-128"><dt>Playtodevice.dll</dt></span><span class="sxs-lookup"><span data-stu-id="213fe-128"><dt>Playtodevice.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="213fe-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="213fe-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="213fe-130">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="213fe-130">[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))</span></span>
</dt> </dl>

 

