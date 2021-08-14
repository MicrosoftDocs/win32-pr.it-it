---
title: MPENDOFLIFE_DATA struttura (MpClient.h)
description: '\ 0034; Fine del ciclo di vita \ 0034; dati di notifica.'
ms.assetid: 00C2E707-9034-4BBC-99CF-3DFA4B8C08D9
keywords:
- MPENDOFLIFE_DATA struttura Legacy Windows Environment Features
- PMPENDOFLIFE_DATA puntatore alla struttura Legacy Windows Environment Features
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
ms.openlocfilehash: 532ee5f80e76de49c2c20bb01958e95fc13603b8f4b65666639834c5cad0fa72
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118476283"
---
# <a name="mpendoflife_data-structure"></a>Struttura MPENDOFLIFE \_ DATA

Dati di notifica "Fine vita".

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

Tipo: **FILETIME**

</dd> <dd>

Ora di scadenza della firma.

</dd> <dt>

**ftPlatformExpiry**
</dt> <dd>

Tipo: **FILETIME**

</dd> <dd>

Ora di scadenza della piattaforma.

</dd> <dt>

**fAdminControlled**
</dt> <dd>

Tipo: **BOOL**

</dd> <dd>

True se l'amministratore controlla i criteri per la visualizzazione della notifica. Se impostato, indica all'interfaccia utente di non visualizzare la notifica EOL.

</dd> <dt>

**fEndOfLifeImpendingOrPast**
</dt> <dd>

Tipo: **BOOL**

</dd> <dd>

True se "End of Life" è in sospeso o passato. Se false, l'interfaccia utente e i client possono cancellare tutti gli stati correlati a EOL.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                            |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



 

 





