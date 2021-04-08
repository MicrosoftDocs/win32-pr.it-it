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
# <a name="systemaudiochannelcount"></a><span data-ttu-id="87287-104">System. audio. ChannelCount</span><span class="sxs-lookup"><span data-stu-id="87287-104">System.Audio.ChannelCount</span></span>

<span data-ttu-id="87287-105">Indica il numero di canali per il file audio.</span><span class="sxs-lookup"><span data-stu-id="87287-105">Indicates the channel count for the audio file.</span></span> <span data-ttu-id="87287-106">I valori possibili sono 1 per mono e 2 per stereo.</span><span class="sxs-lookup"><span data-stu-id="87287-106">Possible values are 1 for mono and 2 for stereo.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="87287-107">Windows 10, versione 1703, Windows 10, versione 1607, Windows 10, versione 1511, Windows 10, versione 1507, Windows 8.1, Windows 8, Windows 7</span><span class="sxs-lookup"><span data-stu-id="87287-107">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

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

## <a name="windows-vista"></a><span data-ttu-id="87287-108">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="87287-108">Windows Vista</span></span>

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

## <a name="remarks"></a><span data-ttu-id="87287-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="87287-109">Remarks</span></span>

<span data-ttu-id="87287-110">I valori PKEY sono definiti in Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="87287-110">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="87287-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="87287-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="87287-112">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="87287-112">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="87287-113">searchInfo</span><span class="sxs-lookup"><span data-stu-id="87287-113">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="87287-114">labelInfo</span><span class="sxs-lookup"><span data-stu-id="87287-114">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="87287-115">typeInfo</span><span class="sxs-lookup"><span data-stu-id="87287-115">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="87287-116">displayInfo</span><span class="sxs-lookup"><span data-stu-id="87287-116">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="87287-117">stringFormat</span><span class="sxs-lookup"><span data-stu-id="87287-117">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="87287-118">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="87287-118">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="87287-119">numberFormat</span><span class="sxs-lookup"><span data-stu-id="87287-119">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="87287-120">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="87287-120">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="87287-121">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="87287-121">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="87287-122">drawControl</span><span class="sxs-lookup"><span data-stu-id="87287-122">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="87287-123">editControl</span><span class="sxs-lookup"><span data-stu-id="87287-123">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="87287-124">filterControl</span><span class="sxs-lookup"><span data-stu-id="87287-124">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="87287-125">queryControl</span><span class="sxs-lookup"><span data-stu-id="87287-125">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
