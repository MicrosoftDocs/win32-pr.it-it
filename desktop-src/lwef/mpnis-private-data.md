---
title: Struttura MPNIS_PRIVATE_DATA (MpClient. h)
description: Notifiche NIS private.
ms.assetid: 19B4928F-BC78-4DEA-A563-1516B6454465
keywords:
- Struttura MPNIS_PRIVATE_DATA le funzionalità legacy dell'ambiente Windows
- Funzionalità dell'ambiente Windows legacy del puntatore della struttura di PMPNIS_PRIVATE_DATA
topic_type:
- apiref
api_name:
- MPNIS_PRIVATE_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21340665a32b619c42d7909e8cd1b72ca6d09fb7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740138"
---
# <a name="mpnis_private_data-structure"></a>\_Struttura di \_ dati privati MPNIS

Notifiche NIS private.

## <a name="syntax"></a>Sintassi


```C++
typedef struct tagMPNIS_PRIVATE_DATA {
  DWORD dwNotificationType;
  DWORD cbDataSize;
  BYTE  *pbData;
} MPNIS_PRIVATE_DATA, *PMPNIS_PRIVATE_DATA;
```



## <a name="members"></a>Members

<dl> <dt>

**dwNotificationType**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Tipo di notifica.

</dd> <dt>

**cbDataSize**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Dimensioni in byte dei dati riservati.

</dd> <dt>

**pbData**
</dt> <dd>

Tipo: **byte \***

</dd> <dd>

Puntatore ai dati riservati.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





