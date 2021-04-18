---
description: Contiene la data di produzione di una batteria.
ms.assetid: 0cda66fc-bf4a-4a38-b43c-6eecde46c414
title: Struttura BATTERY_MANUFACTURE_DATE (Poclass. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BATTERY_MANUFACTURE_DATE
api_type:
- HeaderDef
api_location:
- Poclass.h
- Batclass.h
ms.openlocfilehash: cdd3f067bc3ed2e3339710e0a5bd48c8f42e6525
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312060"
---
# <a name="battery_manufacture_date-structure"></a>Struttura della data di \_ produzione della batteria \_

Contiene la data di produzione di una batteria. Questa struttura viene utilizzata dalla struttura [**di \_ \_ informazioni sulle query della batteria**](battery-query-information-str.md) quando è richiesto il livello di informazioni BatteryManufactureDate.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _BATTERY_MANUFACTURE_DATE {
  UCHAR  Day;
  UCHAR  Month;
  USHORT Year;
} BATTERY_MANUFACTURE_DATE, *PBATTERY_MANUFACTURE_DATE;
```



## <a name="members"></a>Members

<dl> <dt>

**Day**
</dt> <dd>

Giorno del mese di produzione, compreso tra 1 e 31. Nonostante il tipo di dati, non si tratta di un valore con codifica ASCII. Si tratta di un byte senza segno.

</dd> <dt>

**Mese**
</dt> <dd>

Mese di produzione, compreso tra 1 (gennaio) e 12 (dicembre). Nonostante il tipo di dati, non si tratta di un valore con codifica ASCII. Si tratta di un byte senza segno.

</dd> <dt>

**Anno**
</dt> <dd>

Anno di produzione. Questo sarà in genere compreso nell'intervallo 1900-2100.

</dd> </dl>

## <a name="remarks"></a>Commenti

La data è codificata nel formato calendario gregoriano o occidentale.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                                                                                                                                                                                                         |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                                                                                                                                                                                |
| Intestazione<br/>                   | <dl> <dt>Poclass. h; </dt> <dt>Batclass. h in Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows server 2003 e Windows XP</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_informazioni sulle query della batteria \_**](battery-query-information-str.md)
</dt> <dt>

[**\_ \_ informazioni sulle query della batteria IOCTL \_**](ioctl-battery-query-information.md)
</dt> </dl>

 

 




