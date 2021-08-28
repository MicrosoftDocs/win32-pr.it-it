---
title: Enumerazione TransportState
description: Definisce gli stati di trasporto disponibili in base alle linee guida UPnP.
ms.assetid: 2F942EAC-514B-4E65-A12F-85558E9A96A0
keywords:
- ENUMERAZIONE TransportState API Streaming multimediale
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
ms.openlocfilehash: a21fc8d0f2799cfba734d605d0c4d2835744ddeb130327ea39a22090d13464f0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119663091"
---
# <a name="transportstate-enumeration"></a>Enumerazione TransportState

Definisce gli stati di trasporto disponibili in base alle linee guida UPnP.

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

Stato errroneo del dispositivo.

</dd> <dt>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Fermato**
</dt> <dd>

Il trasporto del dispositivo è in stato arrestato.

</dd> <dt>

<span id="Playing"></span><span id="playing"></span><span id="PLAYING"></span>**Giocare**
</dt> <dd>

Il trasporto del dispositivo è in stato di riproduzione.

</dd> <dt>

<span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transizione**
</dt> <dd>

Il trasporto del dispositivo è in uno stato di transizione che comporta un altro valore di stato.

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Pausa**
</dt> <dd>

Il trasporto del dispositivo è in stato di sospensione.

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

Stato precedente del dispositivo allo stato di trasporto corrente.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| Idl<br/> | <dl> <dt>Windows. Media.Streaming.idl (riferimento Windows. Media.Streaming.idl)</dt> </dl> |



 

 





