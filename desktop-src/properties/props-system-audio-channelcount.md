---
description: Indica il numero di canali per il file audio. I valori possibili sono 1 per mono e 2 per stereo.
ms.assetid: 8a028167-dc0f-4ed9-a710-568caf1b9a47
title: System. audio. ChannelCount
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b9a370e517f8c3552e27bf034c4873b5e1cb593
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880542"
---
# <a name="systemaudiochannelcount"></a>System. audio. ChannelCount

Indica il numero di canali per il file audio. I valori possibili sono 1 per mono e 2 per stereo.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a>Windows 10, versione 1703, Windows 10, versione 1607, Windows 10, versione 1511, Windows 10, versione 1507, Windows 8.1, Windows 8, Windows 7

```
propertyDescription
   name = System.Audio.ChannelCount
   shellPKey = PKEY_Audio_ChannelCount
   formatID = 64440490-4C8B-11D1-8B70-080036B11A03
   propID = 7
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = UInt32
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enum
            name = Mono
            value = 1
            text = 1 (mono)
            defineToken = AUDIO_CHANNELCOUNT_MONO
         enum
            name = Stereo
            value = 2
            text = 2 (stereo)
            defineToken = AUDIO_CHANNELCOUNT_STEREO
```

## <a name="windows-vista"></a>Windows Vista

```
propertyDescription
   name = System.Audio.ChannelCount
   shellPKey = PKEY_Audio_ChannelCount
   formatID = 64440490-4C8B-11D1-8B70-080036B11A03
   propID = 7
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = UInt32
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enum
            value = 1
            text = 1 (mono)
            defineName = AUDIO_CHANNELCOUNT_MONO
         enum
            value = 2
            text = 2 (stereo)
            defineName = AUDIO_CHANNELCOUNT_STEREO
```

## <a name="remarks"></a>Commenti

I valori PKEY sono definiti in Propkey. h.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[propertyDescription](./propdesc-schema-propertydescription.md)
</dt> <dt>

[searchInfo](./propdesc-schema-searchinfo.md)
</dt> <dt>

[labelInfo](./propdesc-schema-labelinfo.md)
</dt> <dt>

[typeInfo](./propdesc-schema-typeinfo.md)
</dt> <dt>

[displayInfo](./propdesc-schema-displayinfo.md)
</dt> <dt>

[stringFormat](./propdesc-schema-stringformat.md)
</dt> <dt>

[booleanFormat](./propdesc-schema-booleanformat.md)
</dt> <dt>

[numberFormat](./propdesc-schema-numberformat.md)
</dt> <dt>

[dateTimeFormat](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[enumeratedList](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[drawControl](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[editControl](./propdesc-schema-editcontrol.md)
</dt> <dt>

[filterControl](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[queryControl](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
