---
title: Struttura BG_FILE_PROGRESS (Deliveryoptimization. h)
description: La struttura BG_FILE_PROGRESS fornisce informazioni sullo stato di avanzamento correlate ai file, ad esempio il numero di byte trasferiti.
ms.assetid: 49BDFEEE-D7BF-489A-8BC1-951549B06252
keywords:
- Struttura BG_FILE_PROGRESS
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
ms.openlocfilehash: 93507b8aeefa9c0ea16f70f67e221ecc4218427f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742866"
---
# <a name="bg_file_progress-structure"></a>Struttura BG_FILE_PROGRESS

La struttura **BG_FILE_PROGRESS** fornisce informazioni sullo stato di avanzamento correlate ai file, ad esempio il numero di byte trasferiti.

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

Dimensioni del file, in byte. Se non è in grado di determinare le dimensioni del file (ad esempio, se il file o il server non esiste), il valore viene DO_UNKNOWN_FILE_SIZE.

Se si scaricano intervalli da un file, **bytesTotal** riflette il numero totale di byte che si vuole scaricare dal file.

</dd> <dt>

**Byte trasferiti**
</dt> <dd>

Numero di byte trasferiti.

</dd> <dt>

**Operazione completata**
</dt> <dd>

Per i download, il valore è **true** se il file è disponibile per l'utente; in caso contrario, il valore è **false**. I file sono disponibili per l'utente dopo la chiamata al metodo [**Metodo ibackgroundcopyjob:: complete**](ibackgroundcopyjob-complete.md) . Se il metodo **complete** genera un errore temporaneo, i file elaborati prima dell'errore sono disponibili per l'utente. gli altri non lo sono. Utilizzare il membro **completato** per determinare se il file è disponibile per l'utente quando il **completamento** ha esito negativo.

</dd> </dl>

## <a name="remarks"></a>Commenti

Per determinare se il file è stato trasferito, è possibile:

-   Confrontare **byte trasferiti** con **bytesTotal**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows 10 versione 1709 \[\]<br/>                                         |
| Server minimo supportato<br/> | Windows Server, versione 1709 \[ solo per le app desktop\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**BG_JOB_PROGRESS**](bg-job-progress.md)
</dt> <dt>

[**IBackgroundCopyFile:: getProgress**](ibackgroundcopyfile-getprogress-method.md)
</dt> </dl>

 

 





