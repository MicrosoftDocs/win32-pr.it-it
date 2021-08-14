---
title: Enumerazione TransportStatus
description: Definisce lo stato del trasporto disponibile in base alle linee guida UPnP.
ms.assetid: 6fde82f0-9bc4-4abb-9d10-0000501c2b24
keywords:
- ENUMERAZIONE TransportStatus API Streaming multimediale
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
ms.openlocfilehash: e96b7d3892d0344b166665426c66313da370aed1abbdb80c17037ea6aeb44e46
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118472997"
---
# <a name="transportstatus-enumeration"></a>Enumerazione TransportStatus

Definisce lo stato del trasporto disponibile in base alle linee guida UPnP.

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

Stato del dispositivo erro.

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

Stato precedente del dispositivo allo stato di trasporto corrente.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| Idl<br/> | <dl> <dt>Windows. Media.Streaming.idl (riferimento Windows. Media.Streaming.idl)</dt> </dl> |



 

 





