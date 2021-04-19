---
description: Algoritmo utilizzato per comprimere l'immagine.
ms.assetid: b355351d-b0b4-4f5d-a440-fc408a29e700
title: System. image. Compression
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b33b75d2d291edbc16a8cfd6c0c96c2a3db610e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311351"
---
# <a name="systemimagecompression"></a><span data-ttu-id="69bf2-103">System. image. Compression</span><span class="sxs-lookup"><span data-stu-id="69bf2-103">System.Image.Compression</span></span>

<span data-ttu-id="69bf2-104">Algoritmo utilizzato per comprimere l'immagine.</span><span class="sxs-lookup"><span data-stu-id="69bf2-104">The algorithm used to compress the image.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="69bf2-105">Windows 10, versione 1703, Windows 10, versione 1607, Windows 10, versione 1511, Windows 10, versione 1507, Windows 8.1, Windows 8, Windows 7</span><span class="sxs-lookup"><span data-stu-id="69bf2-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.Image.Compression
   shellPKey = PKEY_Image_Compression
   formatID = 14B81DA1-0135-4D31-96D9-6CBFC9671A99
   propID = 259
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = UInt16
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enum
            name = Uncompressed
            value = 1
            text = Uncompressed
            defineToken = IMAGE_COMPRESSION_UNCOMPRESSED
         enum
            name = CCITT.T3
            value = 2
            text = CCITT T.3
            defineToken = IMAGE_COMPRESSION_CCITT_T3
         enum
            name = CCITT.T4
            value = 3
            text = CCITT T.4
            defineToken = IMAGE_COMPRESSION_CCITT_T4
         enum
            name = CCITT.T6
            value = 4
            text = CCITT T.6
            defineToken = IMAGE_COMPRESSION_CCITT_T6
         enum
            name = LZW
            value = 5
            text = LZW
            defineToken = IMAGE_COMPRESSION_LZW
         enum
            name = JPEG
            value = 6
            text = JPEG
            defineToken = IMAGE_COMPRESSION_JPEG
         enum
            name = PackBits
            value = 32773
            text = PackBits
            defineToken = IMAGE_COMPRESSION_PACKBITS
```

## <a name="windows-vista"></a><span data-ttu-id="69bf2-106">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="69bf2-106">Windows Vista</span></span>

```
propertyDescription
   name = System.Image.Compression
   shellPKey = PKEY_Image_Compression
   formatID = 14B81DA1-0135-4D31-96D9-6CBFC9671A99
   propID = 259
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = UInt16
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enum
            value = 1
            text = Uncompressed
            defineName = IMAGE_COMPRESSION_UNCOMPRESSED
         enum
            value = 2
            text = CCITT T.3
            defineName = IMAGE_COMPRESSION_CCITT_T3
         enum
            value = 3
            text = CCITT T.4
            defineName = IMAGE_COMPRESSION_CCITT_T4
         enum
            value = 4
            text = CCITT T.6
            defineName = IMAGE_COMPRESSION_CCITT_T6
         enum
            value = 5
            text = LZW
            defineName = IMAGE_COMPRESSION_LZW
         enum
            value = 6
            text = JPEG
            defineName = IMAGE_COMPRESSION_JPEG
         enum
            value = 32773
            text = PackBits
            defineName = IMAGE_COMPRESSION_PACKBITS
```

## <a name="remarks"></a><span data-ttu-id="69bf2-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="69bf2-107">Remarks</span></span>

<span data-ttu-id="69bf2-108">I valori PKEY sono definiti in Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="69bf2-108">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="69bf2-109">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="69bf2-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="69bf2-110">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="69bf2-110">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="69bf2-111">searchInfo</span><span class="sxs-lookup"><span data-stu-id="69bf2-111">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="69bf2-112">labelInfo</span><span class="sxs-lookup"><span data-stu-id="69bf2-112">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="69bf2-113">typeInfo</span><span class="sxs-lookup"><span data-stu-id="69bf2-113">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="69bf2-114">displayInfo</span><span class="sxs-lookup"><span data-stu-id="69bf2-114">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="69bf2-115">stringFormat</span><span class="sxs-lookup"><span data-stu-id="69bf2-115">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="69bf2-116">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="69bf2-116">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="69bf2-117">numberFormat</span><span class="sxs-lookup"><span data-stu-id="69bf2-117">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="69bf2-118">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="69bf2-118">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="69bf2-119">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="69bf2-119">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="69bf2-120">drawControl</span><span class="sxs-lookup"><span data-stu-id="69bf2-120">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="69bf2-121">editControl</span><span class="sxs-lookup"><span data-stu-id="69bf2-121">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="69bf2-122">filterControl</span><span class="sxs-lookup"><span data-stu-id="69bf2-122">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="69bf2-123">queryControl</span><span class="sxs-lookup"><span data-stu-id="69bf2-123">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
