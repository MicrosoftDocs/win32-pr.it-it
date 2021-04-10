---
title: Enumerazione MPCOMPONENT_ID (MpClient. h)
description: Componenti possibili per malware Protection Manager.
ms.assetid: 014B400A-880B-419D-9F50-F3354CE945D9
keywords:
- Funzionalità dell'ambiente Windows legacy dell'enumerazione MPCOMPONENT_ID
- Caratteristiche dell'ambiente Windows legacy del puntatore di enumerazione PMPCOMPONENT_ID
topic_type:
- apiref
api_name:
- MPCOMPONENT_ID
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 196eebc5a3bee4968878c376cd7358724c9c55cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119491"
---
# <a name="mpcomponent_id-enumeration"></a>\_Enumerazione ID MPCOMPONENT

Componenti possibili per malware Protection Manager.

## <a name="syntax"></a>Sintassi


```C++
typedef enum tagMPCOMPONENT_ID { 
  MPCOMPONENT_AS_SIGNATURE         = 0,
  MPCOMPONENT_AV_SIGNATURE         = 1,
  MPCOMPONENT_REALTIME_MONITOR     = 2,
  MPCOMPONENT_ONACCESS_PROTECTION  = 3,
  MPCOMPONENT_IOAV_PROTECTION      = 4,
  MPCOMPONENT_BEHAVIOR_MONITOR     = 5,
  MPCOMPONENT_AUTO_SCAN            = 6,
  MPCOMPONENT_AUTO_SIGUPDATE       = 7,
  MPCOMPONENT_IPC                  = 8,
  MPCOMPONENT_NIS                  = 9,
  MPCOMPONENT_ELAM                 = 10,
  MPCOMPONENT_MAXVALUE             = 10
} MPCOMPONENT_ID, *PMPCOMPONENT_ID;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="MPCOMPONENT_AS_SIGNATURE"></span><span id="mpcomponent_as_signature"></span>**MPCOMPONENT \_ come \_ firma**
</dt> <dd></dd> <dt>

<span id="MPCOMPONENT_AV_SIGNATURE"></span><span id="mpcomponent_av_signature"></span>**\_firma AV \_ MPCOMPONENT**
</dt> <dd></dd> <dt>

<span id="MPCOMPONENT_REALTIME_MONITOR"></span><span id="mpcomponent_realtime_monitor"></span>**\_monitoraggio in tempo reale MPCOMPONENT \_**
</dt> <dd></dd> <dt>

<span id="MPCOMPONENT_ONACCESS_PROTECTION"></span><span id="mpcomponent_onaccess_protection"></span>**\_protezione MPCOMPONENT ONaccess \_**
</dt> <dd></dd> <dt>

<span id="MPCOMPONENT_IOAV_PROTECTION"></span><span id="mpcomponent_ioav_protection"></span>**\_protezione MPCOMPONENT IOAV \_**
</dt> <dd></dd> <dt>

<span id="MPCOMPONENT_BEHAVIOR_MONITOR"></span><span id="mpcomponent_behavior_monitor"></span>**\_monitoraggio comportamento \_ MPCOMPONENT**
</dt> <dd></dd> <dt>

<span id="MPCOMPONENT_AUTO_SCAN"></span><span id="mpcomponent_auto_scan"></span>**\_analisi automatica \_ MPCOMPONENT**
</dt> <dd></dd> <dt>

<span id="MPCOMPONENT_AUTO_SIGUPDATE"></span><span id="mpcomponent_auto_sigupdate"></span>**\_SIGUPDATE MPCOMPONENT auto \_**
</dt> <dd></dd> <dt>

<span id="MPCOMPONENT_IPC"></span><span id="mpcomponent_ipc"></span>**\_IPC MPCOMPONENT**
</dt> <dd></dd> <dt>

<span id="MPCOMPONENT_NIS"></span><span id="mpcomponent_nis"></span>**\_NIS MPCOMPONENT**
</dt> <dd></dd> <dt>

<span id="MPCOMPONENT_ELAM"></span><span id="mpcomponent_elam"></span>**\_Elam MPCOMPONENT**
</dt> <dd></dd> <dt>

<span id="MPCOMPONENT_MAXVALUE"></span><span id="mpcomponent_maxvalue"></span>**MPCOMPONENT \_ MaxValue**
</dt> <dd></dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





