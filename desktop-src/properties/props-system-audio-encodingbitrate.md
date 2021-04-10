---
description: Indica la velocità media dei dati in Hertz (Hz) per il file audio in bit al secondo.
ms.assetid: 570711c2-ef9b-4b3a-9b5f-94a6601fa3d4
title: System. audio. EncodingBitrate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fd0325ea0e8971e7764346b3dada2784d9209cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226887"
---
# <a name="systemaudioencodingbitrate"></a><span data-ttu-id="7c5fa-103">System. audio. EncodingBitrate</span><span class="sxs-lookup"><span data-stu-id="7c5fa-103">System.Audio.EncodingBitrate</span></span>

<span data-ttu-id="7c5fa-104">Indica la velocità media dei dati in Hertz (Hz) per il file audio in bit al secondo.</span><span class="sxs-lookup"><span data-stu-id="7c5fa-104">Indicates the average data rate in Hertz (Hz) for the audio file in bits per second.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="7c5fa-105">Windows 10, versione 1703, Windows 10, versione 1607, Windows 10, versione 1511, Windows 10, versione 1507, Windows 8.1, Windows 8, Windows 7</span><span class="sxs-lookup"><span data-stu-id="7c5fa-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.Audio.EncodingBitrate
   shellPKey = PKEY_Audio_EncodingBitrate
   formatID = 64440490-4C8B-11D1-8B70-080036B11A03
   propID = 4
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = UInt32
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enumRange
            name = AMBroadcast
            minValue = 0
            setValue = 0
            text = Voice and AM Broadcast (0 - 32 Kbps)
            defineToken = ENCODINGBITRATE_AM_BROADCAST
         enumRange
            name = FMBroadcast
            minValue = 32769
            setValue = 32769
            text = FM Broadcast (32 - 64 Kbps)
            defineToken = ENCODINGBITRATE_FM_BROADCAST
         enumRange
            name = HighQuality
            minValue = 65537
            setValue = 65537
            text = High Quality (64 - 128 Kbps)
            defineToken = ENCODINGBITRATE_HIGH_QUALITY
         enumRange
            name = NearCDQuality
            minValue = 131073
            setValue = 131073
            text = Near CD Quality (over 128 Kbps)
            defineToken = ENCODINGBITRATE_NEAR_CD_QUALITY
         enumRange
            name
            minValue = 4294967295
```

## <a name="windows-vista"></a><span data-ttu-id="7c5fa-106">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7c5fa-106">Windows Vista</span></span>

```
propertyDescription
   name = System.Audio.EncodingBitrate
   shellPKey = PKEY_Audio_EncodingBitrate
   formatID = 64440490-4C8B-11D1-8B70-080036B11A03
   propID = 4
   SearchInfo
      IsColumn = true
   typeInfo
      type = UInt32
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enumRange
            minValue = 0
            setValue = 0
            text = Voice and AM Broadcast (0 - 32 Kbps)
         enumRange
            minValue = 32769
            setValue = 32769
            text = FM Broadcast (32 - 64 Kbps)
         enumRange
            minValue = 65537
            setValue = 65537
            text = High Quality (64 - 128 Kbps)
         enumRange
            minValue = 131073
            setValue = 131073
            text = Near CD Quality (over 128 Kbps)
         enumRange
            minValue = 4294967295
```

## <a name="remarks"></a><span data-ttu-id="7c5fa-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="7c5fa-107">Remarks</span></span>

<span data-ttu-id="7c5fa-108">I valori PKEY sono definiti in Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="7c5fa-108">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7c5fa-109">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7c5fa-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7c5fa-110">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="7c5fa-110">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="7c5fa-111">searchInfo</span><span class="sxs-lookup"><span data-stu-id="7c5fa-111">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="7c5fa-112">labelInfo</span><span class="sxs-lookup"><span data-stu-id="7c5fa-112">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="7c5fa-113">typeInfo</span><span class="sxs-lookup"><span data-stu-id="7c5fa-113">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="7c5fa-114">displayInfo</span><span class="sxs-lookup"><span data-stu-id="7c5fa-114">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="7c5fa-115">stringFormat</span><span class="sxs-lookup"><span data-stu-id="7c5fa-115">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="7c5fa-116">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="7c5fa-116">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="7c5fa-117">numberFormat</span><span class="sxs-lookup"><span data-stu-id="7c5fa-117">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="7c5fa-118">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="7c5fa-118">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="7c5fa-119">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="7c5fa-119">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="7c5fa-120">drawControl</span><span class="sxs-lookup"><span data-stu-id="7c5fa-120">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="7c5fa-121">editControl</span><span class="sxs-lookup"><span data-stu-id="7c5fa-121">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="7c5fa-122">filterControl</span><span class="sxs-lookup"><span data-stu-id="7c5fa-122">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="7c5fa-123">queryControl</span><span class="sxs-lookup"><span data-stu-id="7c5fa-123">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
