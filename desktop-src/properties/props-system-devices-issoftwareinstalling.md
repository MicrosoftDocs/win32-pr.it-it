---
description: Se VARIANT \_ true, il programma di installazione del dispositivo sta attualmente installando il software.
ms.assetid: 7C62C1E3-D3F3-49ce-A19D-B3A1C14E24D6
title: System. Devices. IsSoftwareInstalling
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06ba8b61b2c2a11c6e35efb9bafaae69aeb3d01d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049946"
---
# <a name="systemdevicesissoftwareinstalling"></a><span data-ttu-id="a0f92-103">System. Devices. IsSoftwareInstalling</span><span class="sxs-lookup"><span data-stu-id="a0f92-103">System.Devices.IsSoftwareInstalling</span></span>

<span data-ttu-id="a0f92-104">Se VARIANT \_ true, il programma di installazione del dispositivo sta attualmente installando il software.</span><span class="sxs-lookup"><span data-stu-id="a0f92-104">If VARIANT\_TRUE, the device installer is currently installing software.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8"></a><span data-ttu-id="a0f92-105">Windows 10, versione 1703, Windows 10, versione 1607, Windows 10, versione 1511, Windows 10, versione 1507, Windows 8.1, Windows 8</span><span class="sxs-lookup"><span data-stu-id="a0f92-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8</span></span>

```
propertyDescription
   name = System.Devices.IsSoftwareInstalling
   shellPKey = PKEY_Devices_IsSoftwareInstalling
   formatID = 83DA6326-97A6-4088-9453-A1923F573B29
   propID = 9
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Boolean
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enum
            name = SoftwareInstalling
            value = #TRUE#
            text = Device setup in progress
            defineToken = ISSOFTWAREINSTALLING_INSTALLING
```

## <a name="windows-7"></a><span data-ttu-id="a0f92-106">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a0f92-106">Windows 7</span></span>

```
propertyDescription
   name = System.Devices.IsSoftwareInstalling
   shellPKey = PKEY_Devices_IsSoftwareInstalling
   formatID = 83DA6326-97A6-4088-9453-A1923F573B29
   propID = 9
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Boolean
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enum
            name = SoftwareInstalling
            value = #TRUE#
            text = Software is installing for this device
            defineToken = ISSOFTWAREINSTALLING_INSTALLING
```

## <a name="remarks"></a><span data-ttu-id="a0f92-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="a0f92-107">Remarks</span></span>

<span data-ttu-id="a0f92-108">I valori PKEY sono definiti in Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="a0f92-108">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a0f92-109">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a0f92-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a0f92-110">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="a0f92-110">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="a0f92-111">searchInfo</span><span class="sxs-lookup"><span data-stu-id="a0f92-111">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="a0f92-112">labelInfo</span><span class="sxs-lookup"><span data-stu-id="a0f92-112">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="a0f92-113">typeInfo</span><span class="sxs-lookup"><span data-stu-id="a0f92-113">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="a0f92-114">displayInfo</span><span class="sxs-lookup"><span data-stu-id="a0f92-114">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="a0f92-115">stringFormat</span><span class="sxs-lookup"><span data-stu-id="a0f92-115">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="a0f92-116">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="a0f92-116">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="a0f92-117">numberFormat</span><span class="sxs-lookup"><span data-stu-id="a0f92-117">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="a0f92-118">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="a0f92-118">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="a0f92-119">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="a0f92-119">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="a0f92-120">drawControl</span><span class="sxs-lookup"><span data-stu-id="a0f92-120">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="a0f92-121">editControl</span><span class="sxs-lookup"><span data-stu-id="a0f92-121">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="a0f92-122">filterControl</span><span class="sxs-lookup"><span data-stu-id="a0f92-122">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="a0f92-123">queryControl</span><span class="sxs-lookup"><span data-stu-id="a0f92-123">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
