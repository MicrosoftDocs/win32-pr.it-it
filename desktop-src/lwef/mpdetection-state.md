---
title: Enumerazione MPDETECTION_STATE (MpClient. h)
description: Stato della minaccia attualmente rilevata.
ms.assetid: 293771FF-A210-41D0-88A5-3B52ACAA9295
keywords:
- Funzionalità dell'ambiente Windows legacy dell'enumerazione MPDETECTION_STATE
- Caratteristiche dell'ambiente Windows legacy del puntatore di enumerazione PMPDETECTION_STATE
topic_type:
- apiref
api_name:
- MPDETECTION_STATE
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9265a15641d2072d87b33af2782f17974bf07be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476114"
---
# <a name="mpdetection_state-enumeration"></a>\_Enumerazione dello stato MPDETECTION

Stato della minaccia attualmente rilevata.

## <a name="syntax"></a>Sintassi


```C++
typedef enum tagMPDETECTION_STATE { 
  MPDETECTION_STATE_UNKNOWN             = 0,
  MPDETECTION_STATE_ACTIVE              = 1,
  MPDETECTION_STATE_FINISHED            = 2,
  MPDETECTION_STATE_ADDITIONAL_ACTIONS  = 3,
  MPDETECTION_STATE_FAILED              = 4,
  MPDETECTION_STATE_CRITICALLY_FAILED   = 5,
  MPDETECTION_STATE_CLEARED             = 6
} MPDETECTION_STATE, *PMPDETECTION_STATE;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="MPDETECTION_STATE_UNKNOWN"></span><span id="mpdetection_state_unknown"></span>**stato di MPDETECTION \_ \_ sconosciuto**
</dt> <dd>

In uno stato di errore.

</dd> <dt>

<span id="MPDETECTION_STATE_ACTIVE"></span><span id="mpdetection_state_active"></span>**\_stato MPDETECTION \_ attivo**
</dt> <dd>

Minaccia attiva.

</dd> <dt>

<span id="MPDETECTION_STATE_FINISHED"></span><span id="mpdetection_state_finished"></span>**\_stato MPDETECTION \_ terminato**
</dt> <dd>

In sospeso 24 ore su uno spostamento da cancellare.

</dd> <dt>

<span id="MPDETECTION_STATE_ADDITIONAL_ACTIONS"></span><span id="mpdetection_state_additional_actions"></span>**\_azioni aggiuntive sullo stato MPDETECTION \_ \_**
</dt> <dd>

Sono necessarie azioni aggiuntive.

</dd> <dt>

<span id="MPDETECTION_STATE_FAILED"></span><span id="mpdetection_state_failed"></span>**\_stato MPDETECTION \_ non riuscito**
</dt> <dd>

Errore di correzione non critico.

</dd> <dt>

<span id="MPDETECTION_STATE_CRITICALLY_FAILED"></span><span id="mpdetection_state_critically_failed"></span>**stato di MPDETECTION \_ \_ \_ non riuscito**
</dt> <dd>

Errore critico di correzione.

</dd> <dt>

<span id="MPDETECTION_STATE_CLEARED"></span><span id="mpdetection_state_cleared"></span>**\_stato MPDETECTION \_ cancellato**
</dt> <dd>

La minaccia non viene visualizzata nella query di stato, ma solo nella cronologia.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





