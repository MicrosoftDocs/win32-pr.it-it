---
title: MPTHREAT_DATA (MpClient.h)
description: I dati di notifica sono stati passati a causa del rilevamento o della modifica delle minacce.
ms.assetid: 07A2F88B-9D58-44EC-86D0-BDCC1DF44B94
keywords:
- MPTHREAT_DATA funzionalità dell'ambiente Windows legacy
- PMPTHREAT_DATA puntatore alla struttura Legacy Windows Environment Features
topic_type:
- apiref
api_name:
- MPTHREAT_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bd6338a027e3b03971f357950bbc351acef0d3fcdca83b72130e0ea475164d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117883231"
---
# <a name="mpthreat_data-structure"></a>Struttura MPTHREAT \_ DATA

I dati di notifica sono stati passati a causa del rilevamento o della modifica delle minacce.

## <a name="syntax"></a>Sintassi


```C++
typedef struct tagMPTHREAT_DATA {
  MPTHREAT_ID     ThreatID;
  DWORD           dwSessionID;
  MPTHREAT_ACTION ThreatAction;
  DWORD           dwStatus;
} MPTHREAT_DATA, *PMPTHREAT_DATA;
```



## <a name="members"></a>Members

<dl> <dt>

**ThreatID**
</dt> <dd>

Tipo: **MPTHREAT \_ ID**

</dd> <dd>

Identificatore della minaccia. Il bit superiore è impostato per identificare le minacce correlate all'antivirus.

</dd> <dt>

**dwSessionID**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Sessione associata alla minaccia. Impostare su -1 se non sono disponibili informazioni specifiche della sessione.

</dd> <dt>

**ThreatAction**
</dt> <dd>

Tipo: **[ **MPTHREAT \_ ACTION**](mpthreat-action.md)**

</dd> <dd>

È stata tentata l'azione di minaccia per gli eventi **MPNOTIFY \_ THREAT \_ CLEAN \_ SUCCEEDED** / **MPNOTIFY \_ THREAT CLEAN \_ \_ FAILED.**

</dd> <dt>

**dwStatus**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Stato o azioni aggiuntive associate all'azione eseguita. Si tratta di una combinazione di flag di bit di [**MPSTATUS \_ FLAG**](mpstatus-flag.md).

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                            |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MPSTATUS \_ FLAG**](mpstatus-flag.md)
</dt> <dt>

[**AZIONE \_ MPTHREAT**](mpthreat-action.md)
</dt> </dl>

 

 





