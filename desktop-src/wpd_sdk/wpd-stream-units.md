---
description: L' \_ enumerazione WPD Stream \_ Units specifica i tipi di unità da usare per le operazioni di IPortableDeviceUnitsStream.
ms.assetid: BE668696-7AF3-44AA-891A-9BFF67FB5544
title: Enumerazione WPD_STREAM_UNITS (PortableDeviceTypes. h)
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
ms.openlocfilehash: 8e70455402a49673b574a0c696b6dda30cc6a884
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758837"
---
# <a name="wpd_stream_units-enumeration"></a>\_Enumerazione unità di flusso WPD \_

L'enumerazione **WPD \_ Stream \_ Units** specifica i tipi di unità da usare per le operazioni di [**IPortableDeviceUnitsStream**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceunitsstream) .

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

<span id="WPD_STREAM_UNITS_BYTES"></span><span id="wpd_stream_units_bytes"></span>**\_ \_ byte unità di flusso WPD \_**
</dt> <dd>

Le unità di flusso vengono specificate in byte.

</dd> <dt>

<span id="WPD_STREAM_UNITS_FRAMES"></span><span id="wpd_stream_units_frames"></span>**\_ \_ frame unità di flusso WPD \_**
</dt> <dd>

Le unità di flusso vengono specificate in frame.

</dd> <dt>

<span id="WPD_STREAM_UNITS_ROWS"></span><span id="wpd_stream_units_rows"></span>**\_ \_ righe unità flusso \_ WPD**
</dt> <dd>

Le unità di flusso vengono specificate in righe.

</dd> <dt>

<span id="WPD_STREAM_UNITS_MILLISECONDS"></span><span id="wpd_stream_units_milliseconds"></span>**WPD \_ unità di flusso in \_ \_ millisecondi**
</dt> <dd>

Le unità di flusso sono specificate in millisecondi.

</dd> <dt>

<span id="WPD_STREAM_UNITS_MICROSECONDS"></span><span id="wpd_stream_units_microseconds"></span>**\_microsecondi unità di flusso WPD \_ \_**
</dt> <dd>

Le unità di flusso vengono specificate in microsecondi.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                                       |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                        |
| Intestazione<br/>                   | <dl> <dt>PortableDeviceTypes. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IPortableDeviceUnitsStream**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceunitsstream)
</dt> <dt>

[**IPortableDeviceUnitsStream::SeekInUnits**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceunitsstream-seekinunits)
</dt> </dl>

 

 




