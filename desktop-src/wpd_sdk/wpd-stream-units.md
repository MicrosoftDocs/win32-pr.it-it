---
description: L'enumerazione WPD STREAM UNITS specifica i tipi di \_ unità da usare per le operazioni \_ IPortableDeviceUnitsStream.
ms.assetid: BE668696-7AF3-44AA-891A-9BFF67FB5544
title: WPD_STREAM_UNITS enumerazione (PortableDeviceTypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_STREAM_UNITS
api_type:
- HeaderDef
api_location:
- PortableDeviceTypes.h
ms.openlocfilehash: d2419453beac6b493ddd1bbbe1281b1596ce00456599074b3872fecb003550c5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119440761"
---
# <a name="wpd_stream_units-enumeration"></a>Enumerazione WPD \_ STREAM \_ UNITS

**L'enumerazione WPD \_ STREAM \_ UNITS** specifica i tipi di unità da usare per [**le operazioni IPortableDeviceUnitsStream.**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceunitsstream)

## <a name="syntax"></a>Sintassi


```C++
typedef enum _WPD_STREAM_UNITS { 
  WPD_STREAM_UNITS_BYTES         = 0,
  WPD_STREAM_UNITS_FRAMES        = 1,
  WPD_STREAM_UNITS_ROWS          = 2,
  WPD_STREAM_UNITS_MILLISECONDS  = 3,
  WPD_STREAM_UNITS_MICROSECONDS  = 4
} WPD_STREAM_UNITS;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="WPD_STREAM_UNITS_BYTES"></span><span id="wpd_stream_units_bytes"></span>**BYTE DELLE UNITÀ \_ DI \_ FLUSSO WPD \_**
</dt> <dd>

Le unità di flusso sono specificate in byte.

</dd> <dt>

<span id="WPD_STREAM_UNITS_FRAMES"></span><span id="wpd_stream_units_frames"></span>**FOTOGRAMMI DI \_ UNITÀ \_ DI FLUSSO WPD \_**
</dt> <dd>

Le unità di flusso sono specificate in fotogrammi.

</dd> <dt>

<span id="WPD_STREAM_UNITS_ROWS"></span><span id="wpd_stream_units_rows"></span>**RIGHE DI \_ UNITÀ DI FLUSSO \_ WPD \_**
</dt> <dd>

Le unità di flusso sono specificate in righe.

</dd> <dt>

<span id="WPD_STREAM_UNITS_MILLISECONDS"></span><span id="wpd_stream_units_milliseconds"></span>**UNITÀ DI FLUSSO WPD \_ \_ \_ MILLISECONDI**
</dt> <dd>

Le unità di flusso sono specificate in millisecondi.

</dd> <dt>

<span id="WPD_STREAM_UNITS_MICROSECONDS"></span><span id="wpd_stream_units_microseconds"></span>**\_MICROSECONDI DELLE UNITÀ DI FLUSSO \_ \_ WPD**
</dt> <dd>

Le unità di flusso sono specificate in microsecondi.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                                       |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                        |
| Intestazione<br/>                   | <dl> <dt>PortableDeviceTypes.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IPortableDeviceUnitsStream**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceunitsstream)
</dt> <dt>

[**IPortableDeviceUnitsStream::SeekInUnits**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceunitsstream-seekinunits)
</dt> </dl>

 

 




