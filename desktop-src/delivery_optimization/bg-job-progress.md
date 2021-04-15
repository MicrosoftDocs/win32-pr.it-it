---
title: Struttura BG_JOB_PROGRESS (Deliveryoptimization. h)
description: La struttura BG_JOB_PROGRESS fornisce informazioni sullo stato di avanzamento correlate al processo, ad esempio il numero di byte e i file trasferiti. Per i processi di caricamento, lo stato di avanzamento si applica al file di caricamento, non al file di risposta.
ms.assetid: F07BBDDE-FD34-4779-9E17-3789A8098616
keywords:
- Struttura BG_JOB_PROGRESS
topic_type:
- apiref
api_name:
- BG_JOB_PROGRESS
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5e45c4a2833f80644ff763fc85a6846f9858fb3d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518549"
---
# <a name="bg_job_progress-structure"></a>Struttura BG_JOB_PROGRESS

La struttura **BG_JOB_PROGRESS** fornisce informazioni sullo stato di avanzamento correlate al processo, ad esempio il numero di byte e i file trasferiti. Per i processi di caricamento, lo stato di avanzamento si applica al file di caricamento, non al file di risposta.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _BG_JOB_PROGRESS {
  UINT64 BytesTotal;
  UINT64 BytesTransferred;
  ULONG  FilesTotal;
  ULONG  FilesTransferred;
} BG_JOB_PROGRESS;
```



## <a name="members"></a>Members

<dl> <dt>

**BytesTotal**
</dt> <dd>

Numero totale di byte da trasferire per tutti i file nel processo. Se il valore è BG_SIZE_UNKNOWN, non è stata determinata la dimensione totale di tutti i file nel processo. DO non imposta questo valore se non è in grado di determinare le dimensioni di uno dei file. Se, ad esempio, il file o il server specificato non esiste, non è possibile determinare le dimensioni del file.

Se si scaricano gli intervalli dal file, **bytesTotal** include il numero totale di byte che si vuole scaricare dal file.

</dd> <dt>

**Byte trasferiti**
</dt> <dd>

Numero di byte trasferiti.

</dd> <dt>

**FilesTotal**
</dt> <dd>

Numero totale di file da trasferire per questo processo.

</dd> <dt>

**FilesTransferred**
</dt> <dd>

Numero di file trasferiti.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows 10 versione 1709 \[\]<br/>                                         |
| Server minimo supportato<br/> | Windows Server, versione 1709 \[ solo per le app desktop\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**BG_FILE_PROGRESS**](bg-file-progress.md)
</dt> <dt>

[**Metodo ibackgroundcopyjob:: getProgress**](ibackgroundcopyjob-getprogress.md)
</dt> </dl>

 

 





