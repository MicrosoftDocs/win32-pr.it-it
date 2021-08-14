---
title: MPDETECTION_STATE enumerazione (MpClient.h)
description: Stato della minaccia attualmente rilevata.
ms.assetid: 293771FF-A210-41D0-88A5-3B52ACAA9295
keywords:
- MPDETECTION_STATE funzionalità dell'ambiente Windows legacy
- PMPDETECTION_STATE puntatore di enumerazione Legacy Windows Environment Features
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
ms.openlocfilehash: 0443e0c47eef4d4943d39bd671c28c19db0ff5e1fbe79e5af8d034603b1ab78d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117883518"
---
# <a name="mpdetection_state-enumeration"></a>Enumerazione MPDETECTION \_ STATE

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

<span id="MPDETECTION_STATE_UNKNOWN"></span><span id="mpdetection_state_unknown"></span>**STATO MPDETECTION \_ \_ SCONOSCIUTO**
</dt> <dd>

In uno stato di errore.

</dd> <dt>

<span id="MPDETECTION_STATE_ACTIVE"></span><span id="mpdetection_state_active"></span>**MPDETECTION \_ STATE \_ ACTIVE**
</dt> <dd>

Minaccia attiva.

</dd> <dt>

<span id="MPDETECTION_STATE_FINISHED"></span><span id="mpdetection_state_finished"></span>**MPDETECTION \_ STATE \_ FINISHED**
</dt> <dd>

In attesa di 24 ore per lo spostamento a cancellato.

</dd> <dt>

<span id="MPDETECTION_STATE_ADDITIONAL_ACTIONS"></span><span id="mpdetection_state_additional_actions"></span>**AZIONI AGGIUNTIVE SULLO \_ STATO \_ MPDETECTION \_**
</dt> <dd>

Sono necessarie azioni aggiuntive.

</dd> <dt>

<span id="MPDETECTION_STATE_FAILED"></span><span id="mpdetection_state_failed"></span>**MPDETECTION \_ STATE \_ FAILED**
</dt> <dd>

Errore di correzione non critico.

</dd> <dt>

<span id="MPDETECTION_STATE_CRITICALLY_FAILED"></span><span id="mpdetection_state_critically_failed"></span>**MPDETECTION \_ STATE \_ CRITICALLY \_ FAILED**
</dt> <dd>

Errore di correzione critico.

</dd> <dt>

<span id="MPDETECTION_STATE_CLEARED"></span><span id="mpdetection_state_cleared"></span>**STATO MPDETECTION \_ \_ DESELEZIONATO**
</dt> <dd>

La minaccia non viene mostrata nella query di stato, ma solo nella cronologia.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                            |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



 

 





