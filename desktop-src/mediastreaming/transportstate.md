---
title: Enumerazione TransportState
description: Definisce gli Stati di trasporto disponibili come definito dalle linee guida di UPnP.
ms.assetid: 2F942EAC-514B-4E65-A12F-85558E9A96A0
keywords:
- API di streaming multimediale dell'enumerazione TransportState
topic_type:
- apiref
api_name:
- TransportState
api_location:
- Windows.Media.Streaming.idl
api_type:
- IDLDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 865d7e0f6a96727915833bb402860cde661162f9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332882"
---
# <a name="transportstate-enumeration"></a>Enumerazione TransportState

Definisce gli Stati di trasporto disponibili come definito dalle linee guida di UPnP.

## <a name="syntax"></a>Sintassi


```C++
typedef enum _TransportState { 
  Unknown         = 0,
  Stopped         = 1,
  Playing         = 2,
  Transitioning   = 3,
  Paused          = 4,
  Recording       = 5,
  NoMediaPresent  = 6,
  Last            = 7
} TransportState;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto**
</dt> <dd>

Stato del dispositivo errato.

</dd> <dt>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Fermato**
</dt> <dd>

Il trasporto del dispositivo è in stato interrotto.

</dd> <dt>

<span id="Playing"></span><span id="playing"></span><span id="PLAYING"></span>**Riproduzione**
</dt> <dd>

Il trasporto del dispositivo è in uno stato di riproduzione.

</dd> <dt>

<span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transizione**
</dt> <dd>

Il trasporto del dispositivo è in uno stato di transizione che comporterà un altro valore di stato.

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Pausa**
</dt> <dd>

Il trasporto del dispositivo è in uno stato di sospensione.

</dd> <dt>

<span id="Recording"></span><span id="recording"></span><span id="RECORDING"></span>**Registrazione**
</dt> <dd>

Il trasporto del dispositivo è in uno stato di registrazione.

</dd> <dt>

<span id="NoMediaPresent"></span><span id="nomediapresent"></span><span id="NOMEDIAPRESENT"></span>**NoMediaPresent**
</dt> <dd>

Per il trasporto del dispositivo non è impostato un URI per la riproduzione.

</dd> <dt>

<span id="Last"></span><span id="last"></span><span id="LAST"></span>**Ultima**
</dt> <dd>

Stato precedente del dispositivo allo stato del trasporto corrente.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| IDL<br/> | <dl> <dt>Windows. Media. streaming. IDL (riferimento a Windows. Media. streaming. idl)</dt> </dl> |



 

 





