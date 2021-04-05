---
title: Struttura MPTHREAT_INFOEX_UNUSED (MpClient. h)
description: Struttura fittizia per le minacce del tipo di modifica non del comportamento.
ms.assetid: 3C5305CD-D533-47B5-ADD3-BD8DA05F2046
keywords:
- Struttura MPTHREAT_INFOEX_UNUSED le funzionalità legacy dell'ambiente Windows
- Funzionalità dell'ambiente Windows legacy del puntatore della struttura di PMPTHREAT_INFOEX_UNUSED
topic_type:
- apiref
api_name:
- MPTHREAT_INFOEX_UNUSED
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fed78d904bd03fee17676dced7c828aaea8d319d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120342"
---
# <a name="mpthreat_infoex_unused-structure"></a>\_Struttura MPTHREAT INFOEX \_ inutilizzata

Struttura fittizia per le minacce del tipo di modifica non del comportamento.

## <a name="syntax"></a>Sintassi


```C++
typedef struct tagMPTHREAT_INFOEX_UNUSED {
  DWORD dwNone;
} MPTHREAT_INFOEX_UNUSED, *PMPTHREAT_INFOEX_UNUSED;
```



## <a name="members"></a>Members

<dl> <dt>

**dwNone**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd></dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





