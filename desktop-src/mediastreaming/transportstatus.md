---
title: Enumerazione TransportStatus
description: Definisce lo stato del trasporto disponibile come definito dalle linee guida di UPnP.
ms.assetid: 6fde82f0-9bc4-4abb-9d10-0000501c2b24
keywords:
- API di streaming multimediale dell'enumerazione TransportStatus
topic_type:
- apiref
api_name:
- TransportStatus
api_location:
- Windows.Media.Streaming.idl
api_type:
- IDLDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb4a9de34f358db96b468dbd3329483a8e09b6b7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332881"
---
# <a name="transportstatus-enumeration"></a>Enumerazione TransportStatus

Definisce lo stato del trasporto disponibile come definito dalle linee guida di UPnP.

## <a name="syntax"></a>Sintassi


```C++
typedef enum TransportStatus { 
  Unknown        = 0,
  Ok             = 1,
  ErrorOccurred  = 2,
  Last           = 3
} TransportStatus;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto**
</dt> <dd>

Stato del dispositivo errato.

</dd> <dt>

<span id="Ok"></span><span id="ok"></span><span id="OK"></span>**Ok**
</dt> <dd>

Il dispositivo è in uno stato valido.

</dd> <dt>

<span id="ErrorOccurred"></span><span id="erroroccurred"></span><span id="ERROROCCURRED"></span>**ErrorOccurred**
</dt> <dd>

Si è verificato un errore nel dispositivo.

</dd> <dt>

<span id="Last"></span><span id="last"></span><span id="LAST"></span>**Ultima**
</dt> <dd>

Stato precedente del dispositivo allo stato del trasporto corrente.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| IDL<br/> | <dl> <dt>Windows. Media. streaming. IDL (riferimento a Windows. Media. streaming. idl)</dt> </dl> |



 

 





