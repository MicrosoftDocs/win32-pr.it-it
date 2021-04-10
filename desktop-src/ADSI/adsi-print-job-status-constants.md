---
title: Costanti di stato del processo di stampa ADSI (Adssts. h)
description: Le costanti seguenti vengono utilizzate con la proprietà IADsPrintJobOperations. status per indicare lo stato di un processo di stampa.
ms.assetid: 44a981cc-1098-4b6d-8332-e678953c9112
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- ADS_JOB_PAUSED
- ADS_JOB_ERROR
- ADS_JOB_DELETING
- ADS_JOB_SPOOLING
- ADS_JOB_PRINTING
- ADS_JOB_OFFLINE
- ADS_JOB_PAPEROUT
- ADS_JOB_PRINTED
- ADS_JOB_DELETED
api_location:
- Adssts.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c51e83393aa0322ef142ee45b4a893f980293ded
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964666"
---
# <a name="adsi-print-job-status-constants"></a>Costanti di stato del processo di stampa ADSI

Le costanti seguenti vengono utilizzate con la proprietà [**IADsPrintJobOperations. status**](iadsprintjoboperations-property-methods.md) per indicare lo stato di un processo di stampa.

<dl> <dt>

<span id="ADS_JOB_PAUSED"></span><span id="ads_job_paused"></span>**\_processo ads \_ sospeso**
</dt> <dd> <dl> <dt>

1 (0x1)
</dt> <dt>



Il processo di stampa è in pausa.


</dt> </dl> </dd> <dt>

<span id="ADS_JOB_ERROR"></span><span id="ads_job_error"></span>**\_errore del processo ads \_**
</dt> <dd> <dl> <dt>

2 (0x2)
</dt> <dt>



Si è verificato un errore.


</dt> </dl> </dd> <dt>

<span id="ADS_JOB_DELETING"></span><span id="ads_job_deleting"></span>**\_eliminazione del processo ads \_**
</dt> <dd> <dl> <dt>

4 (0x4)
</dt> <dt>



È in corso l'eliminazione del processo di stampa.


</dt> </dl> </dd> <dt>

<span id="ADS_JOB_SPOOLING"></span><span id="ads_job_spooling"></span>**\_spooling del processo ads \_**
</dt> <dd> <dl> <dt>

8 (0x8)
</dt> <dt>



È in corso lo spooling del processo di stampa.


</dt> </dl> </dd> <dt>

<span id="ADS_JOB_PRINTING"></span><span id="ads_job_printing"></span>**\_stampa del processo ads \_**
</dt> <dd> <dl> <dt>

16 (0x10)
</dt> <dt>



È in corso la stampa del processo di stampa.


</dt> </dl> </dd> <dt>

<span id="ADS_JOB_OFFLINE"></span><span id="ads_job_offline"></span>**\_processo ads \_ offline**
</dt> <dd> <dl> <dt>

32 (0x20)
</dt> <dt>



La stampante non è in linea.


</dt> </dl> </dd> <dt>

<span id="ADS_JOB_PAPEROUT"></span><span id="ads_job_paperout"></span>**\_stampa del processo ads \_**
</dt> <dd> <dl> <dt>

64 (0x40)
</dt> <dt>



La stampante ha esaurito la carta.


</dt> </dl> </dd> <dt>

<span id="ADS_JOB_PRINTED"></span><span id="ads_job_printed"></span>**\_processo ads \_ stampato**
</dt> <dd> <dl> <dt>

128 (0x80)
</dt> <dt>



Il processo di stampa è stato stampato.


</dt> </dl> </dd> <dt>

<span id="ADS_JOB_DELETED"></span><span id="ads_job_deleted"></span>**\_processo ads \_ eliminato**
</dt> <dd> <dl> <dt>

256 (0x100)
</dt> <dt>



Il processo di stampa è stato eliminato.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                            |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Adssts. h</dt> </dl> |



 

 





