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
# <a name="wpd_stream_units-enumeration"></a><span data-ttu-id="df132-103">\_Enumerazione unità di flusso WPD \_</span><span class="sxs-lookup"><span data-stu-id="df132-103">WPD\_STREAM\_UNITS enumeration</span></span>

<span data-ttu-id="df132-104">L'enumerazione **WPD \_ Stream \_ Units** specifica i tipi di unità da usare per le operazioni di [**IPortableDeviceUnitsStream**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceunitsstream) .</span><span class="sxs-lookup"><span data-stu-id="df132-104">The **WPD\_STREAM\_UNITS** enumeration specifies the unit types to be used for [**IPortableDeviceUnitsStream**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceunitsstream) operations.</span></span>

## <a name="syntax"></a><span data-ttu-id="df132-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="df132-105">Syntax</span></span>


```C++
typedef enum _WPD_STREAM_UNITS { 
  WPD_STREAM_UNITS_BYTES         = 0,
  WPD_STREAM_UNITS_FRAMES        = 1,
  WPD_STREAM_UNITS_ROWS          = 2,
  WPD_STREAM_UNITS_MILLISECONDS  = 3,
  WPD_STREAM_UNITS_MICROSECONDS  = 4
} WPD_STREAM_UNITS;
```



## <a name="constants"></a><span data-ttu-id="df132-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="df132-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="df132-107"><span id="WPD_STREAM_UNITS_BYTES"></span><span id="wpd_stream_units_bytes"></span>**\_ \_ byte unità di flusso WPD \_**</span><span class="sxs-lookup"><span data-stu-id="df132-107"><span id="WPD_STREAM_UNITS_BYTES"></span><span id="wpd_stream_units_bytes"></span>**WPD\_STREAM\_UNITS\_BYTES**</span></span>
</dt> <dd>

<span data-ttu-id="df132-108">Le unità di flusso vengono specificate in byte.</span><span class="sxs-lookup"><span data-stu-id="df132-108">The stream units are specified in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="df132-109"><span id="WPD_STREAM_UNITS_FRAMES"></span><span id="wpd_stream_units_frames"></span>**\_ \_ frame unità di flusso WPD \_**</span><span class="sxs-lookup"><span data-stu-id="df132-109"><span id="WPD_STREAM_UNITS_FRAMES"></span><span id="wpd_stream_units_frames"></span>**WPD\_STREAM\_UNITS\_FRAMES**</span></span>
</dt> <dd>

<span data-ttu-id="df132-110">Le unità di flusso vengono specificate in frame.</span><span class="sxs-lookup"><span data-stu-id="df132-110">The stream units are specified in frames.</span></span>

</dd> <dt>

<span data-ttu-id="df132-111"><span id="WPD_STREAM_UNITS_ROWS"></span><span id="wpd_stream_units_rows"></span>**\_ \_ righe unità flusso \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="df132-111"><span id="WPD_STREAM_UNITS_ROWS"></span><span id="wpd_stream_units_rows"></span>**WPD\_STREAM\_UNITS\_ROWS**</span></span>
</dt> <dd>

<span data-ttu-id="df132-112">Le unità di flusso vengono specificate in righe.</span><span class="sxs-lookup"><span data-stu-id="df132-112">The stream units are specified in rows.</span></span>

</dd> <dt>

<span data-ttu-id="df132-113"><span id="WPD_STREAM_UNITS_MILLISECONDS"></span><span id="wpd_stream_units_milliseconds"></span>**WPD \_ unità di flusso in \_ \_ millisecondi**</span><span class="sxs-lookup"><span data-stu-id="df132-113"><span id="WPD_STREAM_UNITS_MILLISECONDS"></span><span id="wpd_stream_units_milliseconds"></span>**WPD\_STREAM\_UNITS\_MILLISECONDS**</span></span>
</dt> <dd>

<span data-ttu-id="df132-114">Le unità di flusso sono specificate in millisecondi.</span><span class="sxs-lookup"><span data-stu-id="df132-114">The stream units are specified in milliseconds.</span></span>

</dd> <dt>

<span data-ttu-id="df132-115"><span id="WPD_STREAM_UNITS_MICROSECONDS"></span><span id="wpd_stream_units_microseconds"></span>**\_microsecondi unità di flusso WPD \_ \_**</span><span class="sxs-lookup"><span data-stu-id="df132-115"><span id="WPD_STREAM_UNITS_MICROSECONDS"></span><span id="wpd_stream_units_microseconds"></span>**WPD\_STREAM\_UNITS\_MICROSECONDS**</span></span>
</dt> <dd>

<span data-ttu-id="df132-116">Le unità di flusso vengono specificate in microsecondi.</span><span class="sxs-lookup"><span data-stu-id="df132-116">The stream units are specified in microseconds.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="df132-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="df132-117">Requirements</span></span>



| <span data-ttu-id="df132-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="df132-118">Requirement</span></span> | <span data-ttu-id="df132-119">Valore</span><span class="sxs-lookup"><span data-stu-id="df132-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df132-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="df132-120">Minimum supported client</span></span><br/> | <span data-ttu-id="df132-121">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="df132-121">Windows 8 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="df132-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="df132-122">Minimum supported server</span></span><br/> | <span data-ttu-id="df132-123">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="df132-123">None supported</span></span><br/>                                                                        |
| <span data-ttu-id="df132-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="df132-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="df132-125"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="df132-125"><dt>PortableDeviceTypes.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df132-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="df132-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df132-127">**IPortableDeviceUnitsStream**</span><span class="sxs-lookup"><span data-stu-id="df132-127">**IPortableDeviceUnitsStream**</span></span>](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceunitsstream)
</dt> <dt>

[<span data-ttu-id="df132-128">**IPortableDeviceUnitsStream::SeekInUnits**</span><span class="sxs-lookup"><span data-stu-id="df132-128">**IPortableDeviceUnitsStream::SeekInUnits**</span></span>](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceunitsstream-seekinunits)
</dt> </dl>

 

 




