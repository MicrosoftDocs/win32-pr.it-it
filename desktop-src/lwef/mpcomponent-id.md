---
title: MPCOMPONENT_ID enumerazione (MpClient.h)
description: Possibili componenti per Malware Protection Manager.
ms.assetid: 014B400A-880B-419D-9F50-F3354CE945D9
keywords:
- MPCOMPONENT_ID funzionalità dell'ambiente Windows legacy
- PMPCOMPONENT_ID puntatore di enumerazione Legacy Windows Environment Features
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
ms.openlocfilehash: 9fb5acb8d21f7fc947ae83d2b3e6ac9288c5aa38e13c5d4afaa2501b73a3d458
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976081"
---
# <a name="mpcomponent_id-enumeration"></a>Enumerazione MPCOMPONENT \_ ID

Possibili componenti per Malware Protection Manager.

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

<span id="MPCOMPONENT_AS_SIGNATURE"></span><span id="mpcomponent_as_signature"></span>**MPCOMPONENT \_ COME \_ FIRMA**
</dt> <dd></dd> <dt>

<span id="MPCOMPONENT_AV_SIGNATURE"></span><span id="mpcomponent_av_signature"></span>**MPCOMPONENT \_ AV \_ SIGNATURE**
</dt> <dd></dd> <dt>

<span id="MPCOMPONENT_REALTIME_MONITOR"></span><span id="mpcomponent_realtime_monitor"></span>**MONITORAGGIO \_ IN TEMPO REALE MPCOMPONENT \_**
</dt> <dd></dd> <dt>

<span id="MPCOMPONENT_ONACCESS_PROTECTION"></span><span id="mpcomponent_onaccess_protection"></span>**PROTEZIONE MPCOMPONENT \_ ONACCESS \_**
</dt> <dd></dd> <dt>

<span id="MPCOMPONENT_IOAV_PROTECTION"></span><span id="mpcomponent_ioav_protection"></span>**PROTEZIONE \_ IOAV \_ MPCOMPONENT**
</dt> <dd></dd> <dt>

<span id="MPCOMPONENT_BEHAVIOR_MONITOR"></span><span id="mpcomponent_behavior_monitor"></span>**MONITORAGGIO DEL COMPORTAMENTO DI MPCOMPONENT \_ \_**
</dt> <dd></dd> <dt>

<span id="MPCOMPONENT_AUTO_SCAN"></span><span id="mpcomponent_auto_scan"></span>**ANALISI \_ AUTOMATICA MPCOMPONENT \_**
</dt> <dd></dd> <dt>

<span id="MPCOMPONENT_AUTO_SIGUPDATE"></span><span id="mpcomponent_auto_sigupdate"></span>**MPCOMPONENT \_ AUTO \_ SIGUPDATE**
</dt> <dd></dd> <dt>

<span id="MPCOMPONENT_IPC"></span><span id="mpcomponent_ipc"></span>**MPCOMPONENT \_ IPC**
</dt> <dd></dd> <dt>

<span id="MPCOMPONENT_NIS"></span><span id="mpcomponent_nis"></span>**MPCOMPONENT \_ NIS**
</dt> <dd></dd> <dt>

<span id="MPCOMPONENT_ELAM"></span><span id="mpcomponent_elam"></span>**MPCOMPONENT \_ ELAM**
</dt> <dd></dd> <dt>

<span id="MPCOMPONENT_MAXVALUE"></span><span id="mpcomponent_maxvalue"></span>**MPCOMPONENT \_ MAXVALUE**
</dt> <dd></dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                            |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



 

 





