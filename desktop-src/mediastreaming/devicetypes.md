---
title: Enumerazione DeviceTypes
description: Descrive i tipi di dispositivo DLNA supportati dall'API Streaming multimediale.
ms.assetid: ec6bbc1f-653a-414c-b458-1a5e1b101781
keywords:
- Api Streaming multimediale dell'enumerazione DeviceTypes
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
ms.openlocfilehash: 969eb389a1216ec0e30f27a938ca4f5382397ac5489f87add87731b69824b87f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119100655"
---
# <a name="devicetypes-enumeration"></a>Enumerazione DeviceTypes

Descrive i tipi di dispositivo DLNA supportati dall'API Streaming multimediale.

## <a name="syntax"></a>Sintassi


```C++
typedef enum DeviceTypes { 
  Unknown               = 0x0,
  DigitalMediaRenderer  = 0x1,
  DigitalMediaServer    = 0x2,
  DigitalMediaPlayer    = 0x4
} DeviceTypes;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto**
</dt> <dd>

Tipo di dispositivo sconosciuto.

</dd> <dt>

<span id="DigitalMediaRenderer"></span><span id="digitalmediarenderer"></span><span id="DIGITALMEDIARENDERER"></span>**DigitalMediaRenderer**
</dt> <dd>

DLNA Digital Media Renderer (DMR). Il valore è equivalente al tipo di dispositivo **urn:schemas-upnp-org:device:MediaRenderer:1**.

</dd> <dt>

<span id="DigitalMediaServer"></span><span id="digitalmediaserver"></span><span id="DIGITALMEDIASERVER"></span>**DigitalMediaServer**
</dt> <dd>

DLNA Digital Media Server (DMS). Il valore è equivalente al tipo di **dispositivo urn:schemas-upnp-org:device:MediaServer:1**.

</dd> <dt>

<span id="DigitalMediaPlayer"></span><span id="digitalmediaplayer"></span><span id="DIGITALMEDIAPLAYER"></span>**DigitalMediaPlayer**
</dt> <dd>

DLNA Digital Media Player

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| Idl<br/> | <dl> <dt>Windows. Media.Streaming.idl (riferimento Windows. Media.Streaming.idl)</dt> </dl> |



 

 





