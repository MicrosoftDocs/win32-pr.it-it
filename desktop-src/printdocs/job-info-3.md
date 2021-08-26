---
description: La struttura JOB \_ INFO \_ 3 viene usata per collegare un set di processi di stampa.
ms.assetid: a110f555-dc33-450c-ae77-ea26f0f69448
title: JOB_INFO_3 struttura (Winspool.h)
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
ms.openlocfilehash: 111b292c5f355aceefa95fb01bafc2cb9220757618d39d4b3ca29bbf77ca4570
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119948681"
---
# <a name="job_info_3-structure"></a>Struttura JOB \_ INFO \_ 3

La **struttura JOB INFO \_ \_ 3** viene usata per collegare un set di processi di stampa.

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

**Jobid**
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
| Intestazione<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Stampa](printdocs-printing.md)
</dt> <dt>

[Strutture dell'API Spooler di stampa](printing-and-print-spooler-structures.md)
</dt> <dt>

[**EnumJobs**](enumjobs.md)
</dt> <dt>

[**GetJob**](getjob.md)
</dt> <dt>

[**SetJob**](setjob.md)
</dt> </dl>

 

 




