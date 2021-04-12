---
description: La \_ struttura info processo \_ 3 viene utilizzata per collegare insieme un set di processi di stampa.
ms.assetid: a110f555-dc33-450c-ae77-ea26f0f69448
title: Struttura JOB_INFO_3 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- JOB_INFO_3
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: c76cbb6c019878d9c392d21caa40c604df3a5f12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233722"
---
# <a name="job_info_3-structure"></a>\_Struttura info processo \_ 3

La **struttura \_ info processo \_ 3** viene utilizzata per collegare insieme un set di processi di stampa.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _JOB_INFO_3 {
  DWORD JobId;
  DWORD NextJobId;
  DWORD Reserved;
} JOB_INFO_3, *PJOB_INFO_3;
```



## <a name="members"></a>Members

<dl> <dt>

**JobId**
</dt> <dd>

Identificatore del processo di stampa.

</dd> <dt>

**NextJobId**
</dt> <dd>

Identificatore del processo di stampa per il processo di stampa successivo nel set collegato di processi di stampa.

</dd> <dt>

**Reserved**
</dt> <dd>

Questo valore è riservato per l'uso futuro. È necessario impostarlo su zero.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Strutture dell'API spooler di stampa](printing-and-print-spooler-structures.md)
</dt> <dt>

[**EnumJobs**](enumjobs.md)
</dt> <dt>

[**GetJob**](getjob.md)
</dt> <dt>

[**SetJob**](setjob.md)
</dt> </dl>

 

 




