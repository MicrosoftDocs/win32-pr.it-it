---
description: Il tipo di enumerazione WPD VIDEO SCAN TYPES descrive come vengono codificati \_ i campi in un file \_ \_ video.
ms.assetid: ea0dab57-6783-4d02-a43c-414e313f1e80
title: WPD_VIDEO_SCAN_TYPES enumerazione (PortableDevice.h)
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
ms.openlocfilehash: 5f2c6f8a5707780bae6c8a135e3ca940fb4a77408c3df835b321b5b190644fcc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119703721"
---
# <a name="wpd_video_scan_types-enumeration"></a>Enumerazione WPD \_ VIDEO \_ SCAN \_ TYPES

Il **tipo di enumerazione WPD VIDEO SCAN \_ \_ \_ TYPES** descrive come vengono codificati i campi in un file video.

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

<span id="WPD_VIDEO_SCAN_TYPE_UNUSED"></span><span id="wpd_video_scan_type_unused"></span>**TIPO DI \_ ANALISI VIDEO WPD NON \_ \_ \_ USATO**
</dt> <dd>

Il tipo di analisi non è stato definito per questo file video o non è applicabile.

</dd> <dt>

<span id="WPD_VIDEO_SCAN_TYPE_PROGRESSIVE"></span><span id="wpd_video_scan_type_progressive"></span>**TIPO DI \_ ANALISI VIDEO WPD \_ \_ \_ PROGRESSIVO**
</dt> <dd>

Un file video di analisi progressiva.

</dd> <dt>

<span id="WPD_VIDEO_SCAN_TYPE_FIELD_INTERLEAVED_UPPER_FIRST"></span><span id="wpd_video_scan_type_field_interleaved_upper_first"></span>**CAMPO DEL TIPO DI ANALISI VIDEO WPD \_ \_ \_ \_ \_ INTERLEAVED \_ UPPER \_ FIRST**
</dt> <dd>

Un file video interleaved in cui i campi sono alternativi e il campo superiore (con riga 1) viene disegnato per primo. Per altre informazioni, vedere la sezione Osservazioni.

</dd> <dt>

<span id="WPD_VIDEO_SCAN_TYPE_FIELD_INTERLEAVED_LOWER_FIRST"></span><span id="wpd_video_scan_type_field_interleaved_lower_first"></span>**CAMPO DEL TIPO DI ANALISI VIDEO WPD \_ \_ \_ \_ \_ INTERLEAVED \_ LOWER \_ FIRST**
</dt> <dd>

Un file video interleaved in cui i campi sono alternativi e il campo inferiore (con riga 2) viene disegnato per primo. Per altre informazioni, vedere La sezione Osservazioni riportata di seguito.

</dd> <dt>

<span id="WPD_VIDEO_SCAN_TYPE_FIELD_SINGLE_UPPER_FIRST"></span><span id="wpd_video_scan_type_field_single_upper_first"></span>**CAMPO WPD \_ VIDEO SCAN TYPE SINGLE UPPER \_ \_ \_ \_ \_ \_ FIRST**
</dt> <dd>

File video interleaved in cui i campi vengono inviati come campioni contigui e il campo superiore (con riga 1) viene disegnato per primo. Per altre informazioni, vedere La sezione Osservazioni riportata di seguito.

</dd> <dt>

<span id="WPD_VIDEO_SCAN_TYPE_FIELD_SINGLE_LOWER_FIRST"></span><span id="wpd_video_scan_type_field_single_lower_first"></span>**CAMPO WPD \_ VIDEO SCAN TYPE SINGLE LOWER \_ \_ \_ \_ \_ \_ FIRST**
</dt> <dd>

Un file video interleaved in cui i campi vengono inviati come campioni contigui e il campo inferiore (con la riga 2) viene inviato per primo.

</dd> <dt>

<span id="WPD_VIDEO_SCAN_TYPE_MIXED_INTERLACE"></span><span id="wpd_video_scan_type_mixed_interlace"></span>**\_INTERLACE MISTO \_ TIPO DI \_ ANALISI \_ VIDEO WPD \_**
</dt> <dd>

Un file video con una combinazione di modalità di interlacciamento.

</dd> <dt>

<span id="WPD_VIDEO_SCAN_TYPE_MIXED_INTERLACE_AND_PROGRESSIVE"></span><span id="wpd_video_scan_type_mixed_interlace_and_progressive"></span>**WPD \_ VIDEO \_ SCAN \_ TYPE \_ MIXED \_ INTERLACE \_ AND \_ PROGRESSIVE**
</dt> <dd>

Un file video con una combinazione di modalità interlacciata e progressiva.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa enumerazione viene usata dalla [proprietà WPD \_ VIDEO SCAN \_ \_ TYPE.](properties-and-attributes.md)

Esistono due tipi di formati di file interleaved specificati da questa enumerazione. **WPD \_ VIDEO \_ SCAN TYPE FIELD \_ \_ \_ INTERLEAVED** fa riferimento a un formato di file in cui i fotogrammi vengono recapitati quando sono stati analizzati campi alternativi e i dati passano riga per riga, come illustrato di seguito:

**Fotogramma 1**

Campo 1: Riga 1

Campo 2: Riga 1

Campo 1: Riga 2

Campo 2: Riga 2

Campo 1: Riga 3

Campo 2: Riga 3

...

**WPD \_ VIDEO \_ SCAN TYPE FIELD \_ \_ \_ SINGLE** fa riferimento a un formato di file in cui ogni campo viene archiviato in un singolo blocco di righe di analisi e i campi vengono archiviati in sequenza, come illustrato di seguito:

**Fotogramma 1**

Campo 1: Riga 1

Campo 1: Riga 2

Campo 1: Riga 3

...

Seguito da

Campo 2: Riga 1

Campo 2: Riga 2

Campo 2: Riga 3

...

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Strutture e tipi di enumerazione**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




