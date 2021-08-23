---
title: BG_JOB_TYPE enumerazione (Deliveryoptimization.h)
description: L BG_JOB_TYPE enumere definisce valori costanti che specificano il tipo di processo di trasferimento, ad esempio il download.
ms.assetid: 696A43C3-1FA2-436D-B34A-3544E7C9A66A
keywords:
- BG_JOB_TYPE enumerazione
topic_type:
- apiref
api_name:
- BG_JOB_TYPE
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9ae722871435af316e045b293f2cf439a07600af1823202b7bfda654bf01d771
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119755821"
---
# <a name="bg_job_type-enumeration"></a>BG_JOB_TYPE enumerazione

L BG_JOB_TYPE enumere definisce valori costanti che specificano il tipo di processo di trasferimento, ad esempio il download. 

## <a name="syntax"></a>Sintassi


```C++
typedef enum  { 
  BG_JOB_TYPE_DOWNLOAD
} BG_JOB_TYPE;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="BG_JOB_TYPE_DOWNLOAD"></span><span id="bg_job_type_download"></span>**BG_JOB_TYPE_DOWNLOAD**
</dt> <dd>

Specifica che il processo scarica i file nel client.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 10, solo app desktop versione 1709 \[\]<br/>                                         |
| Server minimo supportato<br/> | Windows Server, solo app desktop versione 1709 \[\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IBackgroundCopyJob::GetType**](ibackgroundcopyjob-gettype.md)
</dt> <dt>

[**IBackgroundCopyManager::CreateJob**](ibackgroundcopymanager-createjob.md)
</dt> </dl>

 

 





