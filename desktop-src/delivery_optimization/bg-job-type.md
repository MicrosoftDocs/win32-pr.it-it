---
title: Enumerazione BG_JOB_TYPE (Deliveryoptimization. h)
description: L'enumerazione BG_JOB_TYPE definisce valori costanti che specificano il tipo di processo di trasferimento, ad esempio download.
ms.assetid: 696A43C3-1FA2-436D-B34A-3544E7C9A66A
keywords:
- Enumerazione BG_JOB_TYPE
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
ms.openlocfilehash: f1f672bcf2d2538bfaa9b9573fa1dfa71ee7b9cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476174"
---
# <a name="bg_job_type-enumeration"></a>Enumerazione BG_JOB_TYPE

L'enumerazione **BG_JOB_TYPE** definisce valori costanti che specificano il tipo di processo di trasferimento, ad esempio download.

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

Specifica che il processo Scarica i file nel client.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows 10 versione 1709 \[\]<br/>                                         |
| Server minimo supportato<br/> | Windows Server, versione 1709 \[ solo per le app desktop\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Metodo ibackgroundcopyjob:: GetType**](ibackgroundcopyjob-gettype.md)
</dt> <dt>

[**IBackgroundCopyManager:: CreateJob**](ibackgroundcopymanager-createjob.md)
</dt> </dl>

 

 





