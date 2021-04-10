---
description: La struttura CONFIGUREDEXPERT associa un esperto ai dati di configurazione.
ms.assetid: 96a6650b-6d6f-495e-83bb-385d44ff015d
title: Struttura CONFIGUREDEXPERT (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CONFIGUREDEXPERT
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 3f3d40bf5d38c6b5151691a7d15bd93bef01eee5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231723"
---
# <a name="configuredexpert-structure"></a>Struttura CONFIGUREDEXPERT

La struttura **CONFIGUREDEXPERT** associa un esperto ai dati di configurazione.

## <a name="syntax"></a>Sintassi


```C++
typedef struct {
  HEXPERT       hExpert;
  DWORD         StartupFlags;
  PEXPERTCONFIG pConfig;
} CONFIGUREDEXPERT, *PCONFIGUREDEXPERT;
```



## <a name="members"></a>Members

<dl> <dt>

**hExpert**
</dt> <dd>

Handle per un esperto.

</dd> <dt>

**StartupFlags**
</dt> <dd>

Valori dei flag di avvio dell'esperto.

</dd> <dt>

**pConfig**
</dt> <dd>

Puntatore a una struttura [**EXPERTCONFIG**](expertconfig.md) .

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




