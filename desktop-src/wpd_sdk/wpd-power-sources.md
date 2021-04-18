---
description: Il tipo di enumerazione WPD Power Sources \_ \_ descrive la fonte di alimentazione usata da un dispositivo.
ms.assetid: feebf213-052d-4315-84db-2109cab5f179
title: Enumerazione WPD_POWER_SOURCES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_POWER_SOURCES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: bf9a153d4d41a64b639f796ea2ba0eeb9e567a32
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325801"
---
# <a name="wpd_power_sources-enumeration"></a><span data-ttu-id="8115d-103">\_ \_ Enumerazione origini alimentazione WPD</span><span class="sxs-lookup"><span data-stu-id="8115d-103">WPD\_POWER\_SOURCES enumeration</span></span>

<span data-ttu-id="8115d-104">Il tipo di enumerazione **WPD \_ Power \_** Sources descrive la fonte di alimentazione usata da un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8115d-104">The **WPD\_POWER\_SOURCES** enumeration type describes the power source that a device is using.</span></span>

## <a name="syntax"></a><span data-ttu-id="8115d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8115d-105">Syntax</span></span>


```C++
typedef enum WPD_POWER_SOURCES { 
  WPD_POWER_SOURCE_BATTERY   = 0,
  WPD_POWER_SOURCE_EXTERNAL  = 1
} ;
```



## <a name="constants"></a><span data-ttu-id="8115d-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="8115d-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="8115d-107"><span id="WPD_POWER_SOURCE_BATTERY"></span><span id="wpd_power_source_battery"></span>**\_batteria di \_ origine \_ alimentazione WPD**</span><span class="sxs-lookup"><span data-stu-id="8115d-107"><span id="WPD_POWER_SOURCE_BATTERY"></span><span id="wpd_power_source_battery"></span>**WPD\_POWER\_SOURCE\_BATTERY**</span></span>
</dt> <dd>

<span data-ttu-id="8115d-108">La fonte di alimentazione del dispositivo è una batteria.</span><span class="sxs-lookup"><span data-stu-id="8115d-108">The device power source is a battery.</span></span>

</dd> <dt>

<span data-ttu-id="8115d-109"><span id="WPD_POWER_SOURCE_EXTERNAL"></span><span id="wpd_power_source_external"></span>**\_origine alimentazione \_ \_ esterna WPD**</span><span class="sxs-lookup"><span data-stu-id="8115d-109"><span id="WPD_POWER_SOURCE_EXTERNAL"></span><span id="wpd_power_source_external"></span>**WPD\_POWER\_SOURCE\_EXTERNAL**</span></span>
</dt> <dd>

<span data-ttu-id="8115d-110">Il dispositivo usa una fonte di alimentazione esterna.</span><span class="sxs-lookup"><span data-stu-id="8115d-110">The device uses an external power source.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8115d-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="8115d-111">Remarks</span></span>

<span data-ttu-id="8115d-112">Questa enumerazione viene utilizzata dalla proprietà [di \_ \_ \_ origine dell'alimentazione del dispositivo WPD](device-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="8115d-112">This enumeration is used by the [WPD\_DEVICE\_POWER\_SOURCE](device-properties.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="8115d-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8115d-113">Requirements</span></span>



| <span data-ttu-id="8115d-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="8115d-114">Requirement</span></span> | <span data-ttu-id="8115d-115">Valore</span><span class="sxs-lookup"><span data-stu-id="8115d-115">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="8115d-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8115d-116">Header</span></span><br/> | <dl> <span data-ttu-id="8115d-117"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="8115d-117"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8115d-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8115d-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8115d-119">**Strutture e tipi di enumerazione**</span><span class="sxs-lookup"><span data-stu-id="8115d-119">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




