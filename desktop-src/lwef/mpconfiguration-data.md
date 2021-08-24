---
title: MPCONFIGURATION_DATA struttura (MpClient.h)
description: Contiene i dati sulle modifiche di configurazione, inclusi i valori vecchi e nuovi.
ms.assetid: AB70B1C0-C148-44BC-8C0E-CC5D2A66BCA5
keywords:
- MPCONFIGURATION_DATA struttura Legacy Windows Environment Features
- PMPCONFIGURATION_DATA puntatore alla struttura Legacy Windows Environment Features
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
ms.openlocfilehash: 192cb4d2e35d1b471ef92fb976535bb1e6ed733e2f29ebf86d357f722904514c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120114581"
---
# <a name="mpconfiguration_data-structure"></a>Struttura MPCONFIGURATION \_ DATA

Contiene i dati sulle modifiche di configurazione, inclusi i valori vecchi e nuovi.

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

Tipo: **MP \_ MIDL STRING \_ LPWSTR**

</dd> <dd>

Nome della configurazione modificata.

</dd> <dt>

**DataType**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Tipo di dati utilizzato.

</dd> <dt>

**PreviousDataSize**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Dimensioni dei dati precedenti, in byte.

</dd> <dt>

**pPreviousData**
</dt> <dd>

Tipo: **\* BYTE**

</dd> <dd>

Puntatore ai dati precedenti.

</dd> <dt>

**CurrentDataSize**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Dimensioni dei nuovi dati, in byte.

</dd> <dt>

**pCurrentData**
</dt> <dd>

Tipo: **\* BYTE**

</dd> <dd>

Puntatore ai nuovi dati.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                            |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



 

 





