---
title: Struttura MPTHREAT_DATA (MpClient. h)
description: Dati di notifica passati a causa di rilevamento o modifica delle minacce.
ms.assetid: 07A2F88B-9D58-44EC-86D0-BDCC1DF44B94
keywords:
- Struttura MPTHREAT_DATA le funzionalità legacy dell'ambiente Windows
- Funzionalità dell'ambiente Windows legacy del puntatore della struttura di PMPTHREAT_DATA
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
ms.openlocfilehash: 5cafbb11dbb3b1a34b38ffd0448db96fd1409efd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302652"
---
# <a name="mpthreat_data-structure"></a>\_Struttura dei dati MPTHREAT

Dati di notifica passati a causa di rilevamento o modifica delle minacce.

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

Identificatore della minaccia. Il bit superiore è impostato in modo da identificare le minacce correlate all'antivirus.

</dd> <dt>

**dwSessionID**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Sessione associata alla minaccia. Impostare su-1 se non sono disponibili informazioni specifiche della sessione.

</dd> <dt>

**ThreatAction**
</dt> <dd>

Tipo: **[ **\_ azione MPTHREAT**](mpthreat-action.md)**

</dd> <dd>

Si è tentato di eseguire un'azione di minaccia per gli eventi di pulizia della minaccia **MPNOTIFY \_ \_ \_ riuscita** / **MPNOTIFY \_ \_ \_**

</dd> <dt>

**dwStatus**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Stato o azioni aggiuntive associate all'azione eseguita. Si tratta di una combinazione di flag di bit del [**\_ flag MPSTATUS**](mpstatus-flag.md).

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_flag MPSTATUS**](mpstatus-flag.md)
</dt> <dt>

[**\_azione MPTHREAT**](mpthreat-action.md)
</dt> </dl>

 

 





