---
title: Struttura MPRESERVED_DATA (MpClient. h)
description: Dati di notifica riservati.
ms.assetid: C92206BD-6E56-4B7D-ABB1-DC1149AE141D
keywords:
- Struttura MPRESERVED_DATA le funzionalità legacy dell'ambiente Windows
- Funzionalità dell'ambiente Windows legacy del puntatore della struttura di PMPRESERVED_DATA
topic_type:
- apiref
api_name:
- MPRESERVED_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b1e08184da71fe857cb412ef986c986a0c59baa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120350"
---
# <a name="mpreserved_data-structure"></a>\_Struttura dei dati MPRESERVED

Dati di notifica riservati.

## <a name="syntax"></a>Sintassi


```C++
typedef struct tagMPRESERVED_DATA {
  DWORD cbReservedData;
  BYTE  *pbReservedData;
} MPRESERVED_DATA, *PMPRESERVED_DATA;
```



## <a name="members"></a>Members

<dl> <dt>

**cbReservedData**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Dimensioni in byte dei dati riservati.

</dd> <dt>

**pbReservedData**
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



 

 





