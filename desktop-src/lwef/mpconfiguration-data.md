---
title: Struttura MPCONFIGURATION_DATA (MpClient. h)
description: Contiene i dati sulle modifiche di configurazione, inclusi i vecchi e i nuovi valori.
ms.assetid: AB70B1C0-C148-44BC-8C0E-CC5D2A66BCA5
keywords:
- Struttura MPCONFIGURATION_DATA le funzionalità legacy dell'ambiente Windows
- Funzionalità dell'ambiente Windows legacy del puntatore della struttura di PMPCONFIGURATION_DATA
topic_type:
- apiref
api_name:
- MPCONFIGURATION_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bb54ae4e323f2144dd25c52005d8484b0a207e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048215"
---
# <a name="mpconfiguration_data-structure"></a>\_Struttura dei dati MPCONFIGURATION

Contiene i dati sulle modifiche di configurazione, inclusi i vecchi e i nuovi valori.

## <a name="syntax"></a>Sintassi


```C++
typedef struct tagMPCONFIGURATION_DATA {
  MP_MIDL_STRING LPWSTR ConfigurationName;
  DWORD                 DataType;
  DWORD                 PreviousDataSize;
  BYTE                  *pPreviousData;
  DWORD                 CurrentDataSize;
  BYTE                  *pCurrentData;
} MPCONFIGURATION_DATA, *PMPCONFIGURATION_DATA;
```



## <a name="members"></a>Members

<dl> <dt>

**ConfigurationName**
</dt> <dd>

Tipo: **\_ \_ LPWSTR stringa MIDL MP**

</dd> <dd>

Nome della configurazione modificata.

</dd> <dt>

**DataType**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Tipo di dati utilizzati.

</dd> <dt>

**PreviousDataSize**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Dimensioni in byte dei dati precedenti.

</dd> <dt>

**pPreviousData**
</dt> <dd>

Tipo: **byte \** _

</dd> <dd>

Puntatore ai dati precedenti.

</dd> <dt>

_ *CurrentDataSize**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Dimensioni dei nuovi dati in byte.

</dd> <dt>

**pCurrentData**
</dt> <dd>

Tipo: **byte \***

</dd> <dd>

Puntatore ai nuovi dati.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





