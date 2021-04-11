---
title: Struttura BITS_JOB_PROPERTY_VALUE (Deliveryoptimization. h)
description: Il BITS_JOB_PROPERTY_VALUE Unione fornisce il valore della proprietà del processo DO in base al valore dell'enumerazione BITS_JOB_PROPERTY_ID.
ms.assetid: C24D9EA1-2E72-4403-939A-7B01D7133FE7
keywords:
- Struttura BITS_JOB_PROPERTY_VALUE
- Struttura BITS_JOB_PROPERTY_VALUE
topic_type:
- apiref
api_name:
- BITS_JOB_PROPERTY_VALUE
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c48c1fe550db51b6b838379d44df21c95fa95e41
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119759"
---
# <a name="bits_job_property_value-structure"></a>Struttura BITS_JOB_PROPERTY_VALUE

Il **BITS_JOB_PROPERTY_VALUE** Unione fornisce il valore della proprietà del processo do in base al valore dell'enumerazione [**BITS_JOB_PROPERTY_ID**](bits-job-property-id.md) .

## <a name="syntax"></a>Sintassi


```C++
typedef struct {
  DWORD          Dword;
  GUID           ClsID;
  BOOL           Enable;
  UINT64         Uint64;
  BG_AUTH_TARGET Target;
} BITS_JOB_PROPERTY_VALUE;
```



## <a name="members"></a>Members

<dl> <dt>

**DWORD**
</dt> <dd>

Questo valore viene restituito quando si usa l'ID della proprietà enum **BITS_JOB_PROPERTY_ID_COST_FLAGS** e viene applicato come [criterio di trasferimento](https://www.bing.com/search?q=transfer+policy) nel processo do.

</dd> <dt>

**ClsID**
</dt> <dd>

Questo valore viene restituito quando si usa l'ID della proprietà enum **BITS_JOB_PROPERTY_NOTIFICATION_CLSID** e rappresenta il CLSID dell'oggetto callback da registrare con il processo do.

</dd> <dt>

**Attiva**
</dt> <dd>

Non supportata.

</dd> <dt>

**UInt64**
</dt> <dd>

Non supportata.

</dd> <dt>

**Destinazione**
</dt> <dd>

Non supportata.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows 10 versione 1709 \[\]<br/>                                         |
| Server minimo supportato<br/> | Windows Server, versione 1709 \[ solo per le app desktop\]<br/>                                     |
| Intestazione<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**BITS_JOB_PROPERTY_ID**](bits-job-property-id.md)
</dt> <dt>

[**BITS_JOB_TRANSFER_POLICY**](bits-job-transfer-policy-.md)
</dt> </dl>

 

 





