---
description: Durata della batteria rimanente del dispositivo e relativo stato di ricarica.
ms.assetid: 9c6800ed-ca55-4202-8dfb-6e430121d6b7
title: System.Devices.BatteryPlusCharging
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f249b65afe57b1e9959bd180f7bd3dc9342c85f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231592"
---
# <a name="systemdevicesbatterypluscharging"></a><span data-ttu-id="60f24-103">System.Devices.BatteryPlusCharging</span><span class="sxs-lookup"><span data-stu-id="60f24-103">System.Devices.BatteryPlusCharging</span></span>

<span data-ttu-id="60f24-104">Durata della batteria rimanente del dispositivo e relativo stato di ricarica.</span><span class="sxs-lookup"><span data-stu-id="60f24-104">Remaining battery life of the device and its charging state.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="60f24-105">Windows 10, versione 1703, Windows 10, versione 1607, Windows 10, versione 1511, Windows 10, versione 1507, Windows 8.1, Windows 8, Windows 7</span><span class="sxs-lookup"><span data-stu-id="60f24-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.Devices.BatteryPlusCharging
   shellPKey = PKEY_Devices_BatteryPlusCharging
   formatID = 49CD1F76-5626-4B17-A4E8-18B4AA1A2213
   propID = 22
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Byte
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enumRange
            name = CriticallyLow
            minValue = 0
            setValue = 5
            text = Critically low battery
            defineToken = BATTERYPLUSCHARGING_CRITICALLY_LOW
         enumRange
            name = Low
            minValue = 11
            setValue = 18
            text = Low battery
            defineToken = BATTERYPLUSCHARGING_LOW
         enumRange
            name = Average
            minValue = 26
            setValue = 60
            text = Average battery
            defineToken = BATTERYPLUSCHARGING_AVERAGE
         enumRange
            name = Full
            minValue = 90
            setValue = 95
            text = Full battery
            defineToken = BATTERYPLUSCHARGING_FULL
         enumRange
            name = CriticallyLow
            minValue = 101
            setValue = 5
            text = Critically low battery (charging)
            defineToken = BATTERYPLUSCHARGING_CHARGING_CRITICALLY_LOW
         enumRange
            name = Low
            minValue = 111
            setValue = 18
            text = Low battery (charging)
            defineToken = BATTERYPLUSCHARGING_CHARGING_LOW
         enumRange
            name = Average
            minValue = 126
            setValue = 60
            text = Average battery (charging)
            defineToken = BATTERYPLUSCHARGING_CHARGING_AVERAGE
         enumRange
            name = Full
            minValue = 190
            setValue = 95
            text = Full battery (charging)
            defineToken = BATTERYPLUSCHARGING_CHARGING_FULL
         enumRange
            name = UnknownStatus
            minValue = 201
            setValue = 201
            text = Unknown battery and charging status
            defineToken = BATTERYPLUSCHARGING_UNKNOWN_STATUS
```

## <a name="remarks"></a><span data-ttu-id="60f24-106">Commenti</span><span class="sxs-lookup"><span data-stu-id="60f24-106">Remarks</span></span>

<span data-ttu-id="60f24-107">I valori PKEY sono definiti in Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="60f24-107">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="60f24-108">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="60f24-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="60f24-109">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="60f24-109">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="60f24-110">searchInfo</span><span class="sxs-lookup"><span data-stu-id="60f24-110">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="60f24-111">labelInfo</span><span class="sxs-lookup"><span data-stu-id="60f24-111">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="60f24-112">typeInfo</span><span class="sxs-lookup"><span data-stu-id="60f24-112">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="60f24-113">displayInfo</span><span class="sxs-lookup"><span data-stu-id="60f24-113">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="60f24-114">stringFormat</span><span class="sxs-lookup"><span data-stu-id="60f24-114">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="60f24-115">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="60f24-115">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="60f24-116">numberFormat</span><span class="sxs-lookup"><span data-stu-id="60f24-116">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="60f24-117">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="60f24-117">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="60f24-118">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="60f24-118">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="60f24-119">drawControl</span><span class="sxs-lookup"><span data-stu-id="60f24-119">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="60f24-120">editControl</span><span class="sxs-lookup"><span data-stu-id="60f24-120">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="60f24-121">filterControl</span><span class="sxs-lookup"><span data-stu-id="60f24-121">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="60f24-122">queryControl</span><span class="sxs-lookup"><span data-stu-id="60f24-122">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
