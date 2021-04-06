---
description: La \_ \_ struttura di monitoraggio info 2 identifica un monitoraggio.
ms.assetid: 4dd1ca15-6983-403e-8159-1a6d35a88162
title: Struttura MONITOR_INFO_2 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MONITOR_INFO_2
- _MONITOR_INFO_2A
- _MONITOR_INFO_2W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 9d3ad70a0728ca6e73c4dbefb248df58e858a996
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759656"
---
# <a name="monitor_info_2-structure"></a>Struttura di monitoraggio \_ info \_ 2

La struttura di **monitoraggio \_ info \_ 2** identifica un monitoraggio.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _MONITOR_INFO_2 {
  LPTSTR pName;
  LPTSTR pEnvironment;
  LPTSTR pDLLName;
} MONITOR_INFO_2, *PMONITOR_INFO_2;
```



## <a name="members"></a>Members

<dl> <dt>

**pName**
</dt> <dd>

Puntatore a una stringa con terminazione null che rappresenta il nome del monitoraggio.

</dd> <dt>

**pEnvironment**
</dt> <dd>

Puntatore a una stringa con terminazione null che specifica l'ambiente per il quale è stato scritto il monitoraggio (ad esempio, Windows NT x86, Windows IA64, Windows x64).

</dd> <dt>

**pDLLName**
</dt> <dd>

Puntatore a una stringa con terminazione null che rappresenta il nome della DLL di monitoraggio.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool. h (include Windows. h)</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **\_ Monitorare le \_ informazioni \_ 2W** (Unicode) e le **\_ informazioni di monitoraggio \_ \_ 2a** (ANSI)<br/>                           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Strutture dell'API spooler di stampa](printing-and-print-spooler-structures.md)
</dt> <dt>

[**AddMonitor**](addmonitor.md)
</dt> <dt>

[**EnumMonitors**](enummonitors.md)
</dt> <dt>

[**Informazioni di monitoraggio \_ \_ 1**](monitor-info-1.md)
</dt> </dl>

 

 




