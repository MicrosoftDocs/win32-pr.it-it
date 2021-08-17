---
title: MPRESERVED_DATA (MpClient.h)
description: Dati di notifica riservati.
ms.assetid: C92206BD-6E56-4B7D-ABB1-DC1149AE141D
keywords:
- MPRESERVED_DATA funzionalità dell'ambiente Windows legacy
- PMPRESERVED_DATA puntatore alla struttura Legacy Windows Environment Features
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
ms.openlocfilehash: faabacdcfb581f9b4fc7e9d9a42464dd61e152ca533865acfb7231a711f02317
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118747655"
---
# <a name="mpreserved_data-structure"></a>Struttura MPRESERVED \_ DATA

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

Dimensioni dei dati riservati, in byte.

</dd> <dt>

**pbReservedData**
</dt> <dd>

Tipo: **\* BYTE**

</dd> <dd>

Puntatore ai dati riservati.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                            |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



 

 





