---
description: La \_ struttura ADDJOB info \_ 1 identifica un processo di stampa, nonché la directory e il file in cui un'applicazione può archiviare il processo.
ms.assetid: de915932-11a7-47e8-9be9-edab76d94189
title: Struttura ADDJOB_INFO_1 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ADDJOB_INFO_1
- _ADDJOB_INFO_1A
- _ADDJOB_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 08197a6a72da7e38a349014e08d2d2c2c946f6e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233732"
---
# <a name="addjob_info_1-structure"></a>\_Struttura ADDJOB info \_ 1

La struttura **ADDJOB \_ info \_ 1** identifica un processo di stampa, nonché la directory e il file in cui un'applicazione può archiviare il processo.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _ADDJOB_INFO_1 {
  LPTSTR Path;
  DWORD  JobId;
} ADDJOB_INFO_1, *PADDJOB_INFO_1;
```



## <a name="members"></a>Members

<dl> <dt>

**Percorso**
</dt> <dd>

Puntatore a una stringa con terminazione null che contiene il percorso e il nome del file che l'applicazione può utilizzare per archiviare il processo di stampa.

</dd> <dt>

**JobId**
</dt> <dd>

Handle per il processo di stampa.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool. h (include Windows. h)</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **\_ ADDJOB \_ info \_ 1W** (Unicode) e **\_ ADDJOB \_ info \_ 1a** (ANSI)<br/>                             |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Strutture dell'API spooler di stampa](printing-and-print-spooler-structures.md)
</dt> <dt>

[**AddJob**](addjob.md)
</dt> </dl>

 

 




