---
title: Enumerazione DeviceTypes
description: Descrive i tipi di dispositivo DLNA supportati dall'API di streaming multimediale.
ms.assetid: ec6bbc1f-653a-414c-b458-1a5e1b101781
keywords:
- API di streaming multimediale dell'enumerazione DeviceTypes
topic_type:
- apiref
api_name:
- DeviceTypes
api_location:
- Windows.Media.Streaming.idl
api_type:
- IDLDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9caf60fa5736f9db442da5787746a49f71c61c89
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106323909"
---
# <a name="devicetypes-enumeration"></a><span data-ttu-id="f89f2-104">Enumerazione DeviceTypes</span><span class="sxs-lookup"><span data-stu-id="f89f2-104">DeviceTypes enumeration</span></span>

<span data-ttu-id="f89f2-105">Descrive i tipi di dispositivo DLNA supportati dall'API di streaming multimediale.</span><span class="sxs-lookup"><span data-stu-id="f89f2-105">Describes the DLNA device types that are supported by the Media Streaming API.</span></span>

## <a name="syntax"></a><span data-ttu-id="f89f2-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f89f2-106">Syntax</span></span>


```C++
typedef enum DeviceTypes { 
  Unknown               = 0x0,
  DigitalMediaRenderer  = 0x1,
  DigitalMediaServer    = 0x2,
  DigitalMediaPlayer    = 0x4
} DeviceTypes;
```



## <a name="constants"></a><span data-ttu-id="f89f2-107">Costanti</span><span class="sxs-lookup"><span data-stu-id="f89f2-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="f89f2-108"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto**</span><span class="sxs-lookup"><span data-stu-id="f89f2-108"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown**</span></span>
</dt> <dd>

<span data-ttu-id="f89f2-109">Tipo di dispositivo sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="f89f2-109">Unknown device type.</span></span>

</dd> <dt>

<span data-ttu-id="f89f2-110"><span id="DigitalMediaRenderer"></span><span id="digitalmediarenderer"></span><span id="DIGITALMEDIARENDERER"></span>**DigitalMediaRenderer**</span><span class="sxs-lookup"><span data-stu-id="f89f2-110"><span id="DigitalMediaRenderer"></span><span id="digitalmediarenderer"></span><span id="DIGITALMEDIARENDERER"></span>**DigitalMediaRenderer**</span></span>
</dt> <dd>

<span data-ttu-id="f89f2-111">Renderer digitale multimediale DLNA (ricevitore).</span><span class="sxs-lookup"><span data-stu-id="f89f2-111">DLNA Digital Media Renderer (DMR).</span></span> <span data-ttu-id="f89f2-112">Il valore è equivalente al tipo di dispositivo **urn: schemas-UPnP-org: Device: MediaRenderer: 1**.</span><span class="sxs-lookup"><span data-stu-id="f89f2-112">The value is equivalent to the device type **urn:schemas-upnp-org:device:MediaRenderer:1**.</span></span>

</dd> <dt>

<span data-ttu-id="f89f2-113"><span id="DigitalMediaServer"></span><span id="digitalmediaserver"></span><span id="DIGITALMEDIASERVER"></span>**DigitalMediaServer**</span><span class="sxs-lookup"><span data-stu-id="f89f2-113"><span id="DigitalMediaServer"></span><span id="digitalmediaserver"></span><span id="DIGITALMEDIASERVER"></span>**DigitalMediaServer**</span></span>
</dt> <dd>

<span data-ttu-id="f89f2-114">Server multimediale digitale DLNA (DMS).</span><span class="sxs-lookup"><span data-stu-id="f89f2-114">DLNA Digital Media Server (DMS).</span></span> <span data-ttu-id="f89f2-115">Il valore è equivalente al tipo di dispositivo **urn: schemas-UPnP-org: Device: MediaServer: 1**.</span><span class="sxs-lookup"><span data-stu-id="f89f2-115">The value is equivalent to the device type **urn:schemas-upnp-org:device:MediaServer:1**.</span></span>

</dd> <dt>

<span data-ttu-id="f89f2-116"><span id="DigitalMediaPlayer"></span><span id="digitalmediaplayer"></span><span id="DIGITALMEDIAPLAYER"></span>**DigitalMediaPlayer**</span><span class="sxs-lookup"><span data-stu-id="f89f2-116"><span id="DigitalMediaPlayer"></span><span id="digitalmediaplayer"></span><span id="DIGITALMEDIAPLAYER"></span>**DigitalMediaPlayer**</span></span>
</dt> <dd>

<span data-ttu-id="f89f2-117">Media Player digitali DLNA</span><span class="sxs-lookup"><span data-stu-id="f89f2-117">DLNA Digital Media Player</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f89f2-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f89f2-118">Requirements</span></span>



| <span data-ttu-id="f89f2-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="f89f2-119">Requirement</span></span> | <span data-ttu-id="f89f2-120">Valore</span><span class="sxs-lookup"><span data-stu-id="f89f2-120">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f89f2-121">IDL</span><span class="sxs-lookup"><span data-stu-id="f89f2-121">IDL</span></span><br/> | <dl> <span data-ttu-id="f89f2-122"><dt>Windows. Media. streaming. IDL (riferimento a Windows. Media. streaming. idl)</dt></span><span class="sxs-lookup"><span data-stu-id="f89f2-122"><dt>Windows.Media.Streaming.idl (reference Windows.Media.Streaming.idl)</dt></span></span> </dl> |



 

 





