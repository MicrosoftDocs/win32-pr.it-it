---
description: Il \_ \_ \_ tipo di enumerazione WPD video Scan types descrive il modo in cui vengono codificati i campi di un file video.
ms.assetid: ea0dab57-6783-4d02-a43c-414e313f1e80
title: Enumerazione WPD_VIDEO_SCAN_TYPES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_VIDEO_SCAN_TYPES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: a636bc95fd3d25de20c2df413576a504c4fa1b96
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324865"
---
# <a name="wpd_video_scan_types-enumeration"></a>\_Enumerazione dei \_ tipi di analisi video WPD \_

Il tipo di enumerazione **WPD \_ video \_ Scan \_ types** descrive il modo in cui vengono codificati i campi di un file video.

## <a name="syntax"></a>Sintassi


```C++
typedef enum WPD_VIDEO_SCAN_TYPES { 
  WPD_VIDEO_SCAN_TYPE_UNUSED                           = 0,
  WPD_VIDEO_SCAN_TYPE_PROGRESSIVE                      = 1,
  WPD_VIDEO_SCAN_TYPE_FIELD_INTERLEAVED_UPPER_FIRST    = 2,
  WPD_VIDEO_SCAN_TYPE_FIELD_INTERLEAVED_LOWER_FIRST    = 3,
  WPD_VIDEO_SCAN_TYPE_FIELD_SINGLE_UPPER_FIRST         = 4,
  WPD_VIDEO_SCAN_TYPE_FIELD_SINGLE_LOWER_FIRST         = 5,
  WPD_VIDEO_SCAN_TYPE_MIXED_INTERLACE                  = 6,
  WPD_VIDEO_SCAN_TYPE_MIXED_INTERLACE_AND_PROGRESSIVE  = 7
} ;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="WPD_VIDEO_SCAN_TYPE_UNUSED"></span><span id="wpd_video_scan_type_unused"></span>**\_tipo di analisi video WPD non \_ \_ \_ usato**
</dt> <dd>

Il tipo di analisi non è stato definito per questo file video o non è applicabile.

</dd> <dt>

<span id="WPD_VIDEO_SCAN_TYPE_PROGRESSIVE"></span><span id="wpd_video_scan_type_progressive"></span>**\_tipo di \_ analisi video WPD \_ \_ progressivo**
</dt> <dd>

Un file video di analisi progressiva.

</dd> <dt>

<span id="WPD_VIDEO_SCAN_TYPE_FIELD_INTERLEAVED_UPPER_FIRST"></span><span id="wpd_video_scan_type_field_interleaved_upper_first"></span>**WPD \_ il \_ campo tipo di analisi video \_ \_ \_ Interleaved \_ superiore \_**
</dt> <dd>

Un file video con interfoliazione in cui i campi alternativi e il campo superiore (con riga 1) vengono disegnati per primi. Per altre informazioni, vedere la sezione Osservazioni.

</dd> <dt>

<span id="WPD_VIDEO_SCAN_TYPE_FIELD_INTERLEAVED_LOWER_FIRST"></span><span id="wpd_video_scan_type_field_interleaved_lower_first"></span>**WPD \_ il \_ campo tipo di analisi video con \_ \_ \_ interfoliazione \_ più basso \_ prima**
</dt> <dd>

Un file video con interfoliazione in cui i campi alternativi e il campo inferiore (con riga 2) vengono disegnati per primi. Per ulteriori informazioni, vedere la sezione Osservazioni di seguito.

</dd> <dt>

<span id="WPD_VIDEO_SCAN_TYPE_FIELD_SINGLE_UPPER_FIRST"></span><span id="wpd_video_scan_type_field_single_upper_first"></span>**WPD \_ il \_ campo tipo di analisi video \_ \_ singolo in \_ \_ \_ primo piano**
</dt> <dd>

Un file video con interfoliazione in cui i campi vengono inviati come campioni contigui e viene disegnato per primo il campo superiore (con riga 1). Per ulteriori informazioni, vedere la sezione Osservazioni di seguito.

</dd> <dt>

<span id="WPD_VIDEO_SCAN_TYPE_FIELD_SINGLE_LOWER_FIRST"></span><span id="wpd_video_scan_type_field_single_lower_first"></span>**WPD \_ \_ campo tipo di analisi video \_ singolo in \_ basso per \_ \_ \_ primo**
</dt> <dd>

Un file video con interfoliazione in cui i campi vengono inviati come campioni contigui e viene inviato per primo il campo inferiore (con riga 2).

</dd> <dt>

<span id="WPD_VIDEO_SCAN_TYPE_MIXED_INTERLACE"></span><span id="wpd_video_scan_type_mixed_interlace"></span>**\_tipo di \_ analisi video WPD \_ \_ mixed \_ Interlace**
</dt> <dd>

Un file video con una combinazione di modalità di interlacciamento.

</dd> <dt>

<span id="WPD_VIDEO_SCAN_TYPE_MIXED_INTERLACE_AND_PROGRESSIVE"></span><span id="wpd_video_scan_type_mixed_interlace_and_progressive"></span>**\_ \_ tipo di analisi video WPD \_ \_ misto \_ interlacciato \_ e \_ progressivo**
</dt> <dd>

Un file video con una combinazione di modalità interlacciata e progressiva.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa enumerazione viene utilizzata dalla proprietà [del \_ \_ \_ tipo di analisi video WPD](properties-and-attributes.md) .

Esistono due tipi di formati di file con interfoliazione specificati da questa enumerazione. **WPD \_ Il \_ campo tipo di analisi video con \_ \_ \_ interfoliazione** si riferisce a un formato di file in cui i frame vengono recapitati in base ai campi analizzati alternativi e i dati passano riga per riga, come illustrato di seguito:

**Fotogramma 1**

Campo 1: riga 1

Campo 2: riga 1

Campo 1: riga 2

Campo 2: riga 2

Campo 1: riga 3

Campo 2: riga 3

...

**WPD \_ Il \_ campo tipo di analisi video \_ \_ \_ singolo** fa riferimento a un formato di file in cui ogni campo viene archiviato in un singolo blocco di righe di analisi e i campi vengono archiviati in sequenza, come illustrato di seguito:

**Fotogramma 1**

Campo 1: riga 1

Campo 1: riga 2

Campo 1: riga 3

...

Seguito da

Campo 2: riga 1

Campo 2: riga 2

Campo 2: riga 3

...

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Strutture e tipi di enumerazione**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




