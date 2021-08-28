---
description: La struttura MONITOR \_ INFO \_ 2 identifica un monitoraggio.
ms.assetid: 4dd1ca15-6983-403e-8159-1a6d35a88162
title: MONITOR_INFO_2 struttura (Winspool.h)
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
ms.openlocfilehash: c01377740c77ef4cb2be15e785b9ea3e93449944c11f2014ed660d8c3e3245b7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120112331"
---
# <a name="monitor_info_2-structure"></a>Struttura MONITOR \_ INFO \_ 2

La **struttura MONITOR INFO \_ \_ 2** identifica un monitoraggio.

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

**Pname**
</dt> <dd>

Puntatore a una stringa con terminazione Null che rappresenta il nome del monitoraggio.

</dd> <dt>

**pEnvironment**
</dt> <dd>

Puntatore a una stringa con terminazione Null che specifica l'ambiente per cui è stato scritto il monitoraggio, ad esempio Windows NT x86, Windows IA64, Windows x64).

</dd> <dt>

**pDLLName**
</dt> <dd>

Puntatore a una stringa con terminazione Null che rappresenta il nome della DLL di monitoraggio.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **\_ MONITOR \_ INFO \_ 2W** (Unicode) e **\_ MONITOR INFO \_ \_ 2A** (ANSI)<br/>                           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Strutture dell'API Spooler di stampa](printing-and-print-spooler-structures.md)
</dt> <dt>

[**AddMonitor**](addmonitor.md)
</dt> <dt>

[**EnumMonitors**](enummonitors.md)
</dt> <dt>

[**INFORMAZIONI \_ DI \_ MONITORAGGIO 1**](monitor-info-1.md)
</dt> </dl>

 

 




