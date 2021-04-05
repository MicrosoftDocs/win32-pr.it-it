---
title: Struttura BG_JOB_TIMES (Deliveryoptimization. h)
description: La struttura BG_JOB_TIMES fornisce timestamp relativi ai processi.
ms.assetid: 0147478F-C850-4B66-AB15-042C1A81D6B5
keywords:
- Struttura BG_JOB_TIMES
topic_type:
- apiref
api_name:
- BG_JOB_TIMES
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0a2d4e56bb616254537e26fc1ba0fdf5b9e251a4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740322"
---
# <a name="bg_job_times-structure"></a>Struttura BG_JOB_TIMES

La struttura **BG_JOB_TIMES** fornisce timestamp relativi ai processi.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _BG_JOB_TIMES {
  FILETIME CreationTime;
  FILETIME ModificationTime;
  FILETIME TransferCompletionTime;
} BG_JOB_TIMES;
```



## <a name="members"></a>Members

<dl> <dt>

**CreationTime**
</dt> <dd>

Ora di creazione del processo. L'ora viene specificata come [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime).

</dd> <dt>

**ModificationTime**
</dt> <dd>

Ora dell'Ultima modifica apportata al processo oppure byte trasferiti. L'aggiunta di file o la chiamata di uno dei metodi set nelle interfacce [ * *Metodo ibackgroundcopyjob \** _](/previous-versions//mt811348(v=vs.85)) modifica questo valore. Inoltre, le modifiche allo stato del processo e alla chiamata dei metodi [_ *Suspend* *](ibackgroundcopyjob-suspend.md), [**Resume**](ibackgroundcopyjob-resume.md), [**Cancel**](ibackgroundcopyjob-cancel.md)e [**complete**](ibackgroundcopyjob-complete.md) cambiano questo valore. L'ora viene specificata come [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime).

</dd> <dt>

**TransferCompletionTime**
</dt> <dd>

Ora in cui il processo è entrato nello stato BG_JOB_STATE_TRANSFERRED. L'ora viene specificata come [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime).

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows 10 versione 1709 \[\]<br/>                                         |
| Server minimo supportato<br/> | Windows Server, versione 1709 \[ solo per le app desktop\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Metodo ibackgroundcopyjob:: gettimes**](ibackgroundcopyjob-gettimes.md)
</dt> </dl>

 

