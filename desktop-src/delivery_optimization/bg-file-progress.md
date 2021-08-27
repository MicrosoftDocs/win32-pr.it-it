---
title: BG_FILE_PROGRESS (Deliveryoptimization.h)
description: La BG_FILE_PROGRESS fornisce informazioni sullo stato di avanzamento relative ai file, ad esempio il numero di byte trasferiti.
ms.assetid: 49BDFEEE-D7BF-489A-8BC1-951549B06252
keywords:
- BG_FILE_PROGRESS struttura
topic_type:
- apiref
api_name:
- BG_FILE_PROGRESS
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: dd0bec0f21fb652ccc5c8d543f04816468fff9bc28db74a68a1d05c072a895a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047249"
---
# <a name="bg_file_progress-structure"></a>BG_FILE_PROGRESS struttura

La **BG_FILE_PROGRESS** fornisce informazioni sullo stato di avanzamento relative ai file, ad esempio il numero di byte trasferiti.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _BG_FILE_PROGRESS {
  UINT64 BytesTotal;
  UINT64 BytesTransferred;
  BOOL   Completed;
} BG_FILE_PROGRESS;
```



## <a name="members"></a>Members

<dl> <dt>

**BytesTotal**
</dt> <dd>

Dimensioni del file, in byte. Se DO non è in grado di determinare le dimensioni del file, ad esempio se il file o il server non esiste, il valore viene DO_UNKNOWN_FILE_SIZE.

Se si scaricano intervalli da un file, **BytesTotal** riflette il numero totale di byte da scaricare dal file.

</dd> <dt>

**BytesTransferred**
</dt> <dd>

Numero di byte trasferiti.

</dd> <dt>

**Operazione completata**
</dt> <dd>

Per i download, il valore è **TRUE** se il file è disponibile per l'utente. In caso contrario, il valore è **FALSE.** I file sono disponibili per l'utente dopo la chiamata [**al metodo IBackgroundCopyJob::Complete.**](ibackgroundcopyjob-complete.md) Se il **metodo Complete** genera un errore temporaneo, i file elaborati prima dell'errore sono disponibili per l'utente. gli altri no. Usare il **membro Completed** per determinare se il file è disponibile per l'utente quando **l'operazione non riesce.**

</dd> </dl>

## <a name="remarks"></a>Commenti

Per determinare se DO ha trasferito il file, è possibile:

-   Confrontare **BytesTransferred** con **BytesTotal.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 10, solo app desktop versione 1709 \[\]<br/>                                         |
| Server minimo supportato<br/> | Windows Server, solo app desktop versione 1709 \[\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**BG_JOB_PROGRESS**](bg-job-progress.md)
</dt> <dt>

[**IBackgroundCopyFile::GetProgress**](ibackgroundcopyfile-getprogress-method.md)
</dt> </dl>

 

 





