---
title: Struttura MPENDOFLIFE_DATA (MpClient. h)
description: '\ 0034; Fine vita \ 0034; dati di notifica.'
ms.assetid: 00C2E707-9034-4BBC-99CF-3DFA4B8C08D9
keywords:
- Struttura MPENDOFLIFE_DATA le funzionalità legacy dell'ambiente Windows
- Funzionalità dell'ambiente Windows legacy del puntatore della struttura di PMPENDOFLIFE_DATA
topic_type:
- apiref
api_name:
- MPENDOFLIFE_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e209b9b35a089523815c353e8a750152bf4af75
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120551"
---
# <a name="mpendoflife_data-structure"></a>\_Struttura dei dati MPENDOFLIFE

Dati di notifica di "fine vita".

## <a name="syntax"></a>Sintassi


```C++
typedef struct tagMPENDOFLIFE_DATA {
  FILETIME ftSignatureExpiry;
  FILETIME ftPlatformExpiry;
  BOOL     fAdminControlled;
  BOOL     fEndOfLifeImpendingOrPast;
} MPENDOFLIFE_DATA, *PMPENDOFLIFE_DATA;
```



## <a name="members"></a>Members

<dl> <dt>

**ftSignatureExpiry**
</dt> <dd>

Tipo: **FILEtime**

</dd> <dd>

Ora di scadenza della firma.

</dd> <dt>

**ftPlatformExpiry**
</dt> <dd>

Tipo: **FILEtime**

</dd> <dd>

Ora di scadenza della piattaforma.

</dd> <dt>

**fAdminControlled**
</dt> <dd>

Tipo: **bool**

</dd> <dd>

True se l'amministratore controlla i criteri per la visualizzazione della notifica. Se impostato, indica all'interfaccia utente di non visualizzare la notifica EOL.

</dd> <dt>

**fEndOfLifeImpendingOrPast**
</dt> <dd>

Tipo: **bool**

</dd> <dd>

True se "End of Life" è in sospeso o passato. Se false, l'interfaccia utente e i client possono cancellare tutti gli stati correlati a EOL.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





