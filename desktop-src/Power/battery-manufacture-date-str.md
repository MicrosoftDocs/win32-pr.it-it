---
description: Contiene la data di produzione di una batteria.
ms.assetid: 0cda66fc-bf4a-4a38-b43c-6eecde46c414
title: BATTERY_MANUFACTURE_DATE struttura (Poclass.h)
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
ms.openlocfilehash: 30a70fed151304d189fa91b20106e1154ca0e9f4ea5225c52bf1023dbd218346
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032971"
---
# <a name="battery_manufacture_date-structure"></a>Struttura \_ BATTERY MANUFACTURE \_ DATE

Contiene la data di produzione di una batteria. Questa struttura viene usata dalla struttura [**BATTERY \_ QUERY \_ INFORMATION**](battery-query-information-str.md) quando viene richiesto il livello di informazioni BatteryManufactureDate.

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

**Month**
</dt> <dd>

Mese di produzione, compreso tra 1 (gennaio) e 12 (dicembre). Nonostante il tipo di dati, non si tratta di un valore con codifica ASCII. Si tratta di un byte senza segno.

</dd> <dt>

**Year**
</dt> <dd>

Anno di produzione. In genere sarà compreso nell'intervallo 1900-2100.

</dd> </dl>

## <a name="remarks"></a>Commenti

La data è codificata nel formato calendario gregoriano o occidentale.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                                                                                                                                                                                                         |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                                                                                                                                                                                                |
| Intestazione<br/>                   | <dl> <dt>Poclass.h;</dt> <dt>Batclass.h in Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 e Windows XP</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**INFORMAZIONI \_ SULLE QUERY SULLA \_ BATTERIA**](battery-query-information-str.md)
</dt> <dt>

[**INFORMAZIONI SULLE \_ QUERY SULLA \_ BATTERIA IOCTL \_**](ioctl-battery-query-information.md)
</dt> </dl>

 

 




