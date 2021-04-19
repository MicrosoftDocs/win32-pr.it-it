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
# <a name="devicetypes-enumeration"></a>Enumerazione DeviceTypes

Descrive i tipi di dispositivo DLNA supportati dall'API di streaming multimediale.

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

Renderer digitale multimediale DLNA (ricevitore). Il valore è equivalente al tipo di dispositivo **urn: schemas-UPnP-org: Device: MediaRenderer: 1**.

</dd> <dt>

<span id="DigitalMediaServer"></span><span id="digitalmediaserver"></span><span id="DIGITALMEDIASERVER"></span>**DigitalMediaServer**
</dt> <dd>

Server multimediale digitale DLNA (DMS). Il valore è equivalente al tipo di dispositivo **urn: schemas-UPnP-org: Device: MediaServer: 1**.

</dd> <dt>

<span id="DigitalMediaPlayer"></span><span id="digitalmediaplayer"></span><span id="DIGITALMEDIAPLAYER"></span>**DigitalMediaPlayer**
</dt> <dd>

Media Player digitali DLNA

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| IDL<br/> | <dl> <dt>Windows. Media. streaming. IDL (riferimento a Windows. Media. streaming. idl)</dt> </dl> |



 

 





