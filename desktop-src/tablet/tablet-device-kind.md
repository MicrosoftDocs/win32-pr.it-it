---
description: Indica il tipo di dispositivo tablet, ad esempio una penna, un mouse o un digitalizzatore sensibile al tocco.
ms.assetid: 4cca1e09-99c0-4357-a6ef-159bc8d17d57
title: Enumerazione TABLET_DEVICE_KIND
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TABLET_DEVICE_KIND
api_type:
- NA
api_location: ''
ms.openlocfilehash: 18f691a2fa909ef28059a4788f4f8b4e184a61ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319131"
---
# <a name="tablet_device_kind-enumeration"></a><span data-ttu-id="3d43c-103">Enumerazione del tipo di \_ dispositivo Tablet \_</span><span class="sxs-lookup"><span data-stu-id="3d43c-103">TABLET\_DEVICE\_KIND enumeration</span></span>

<span data-ttu-id="3d43c-104">Indica il tipo di dispositivo tablet, ad esempio una penna, un mouse o un digitalizzatore sensibile al tocco.</span><span class="sxs-lookup"><span data-stu-id="3d43c-104">Indicates the type of tablet device such as a pen, mouse or touch sensitive digitizer.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d43c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3d43c-105">Syntax</span></span>


```C++
typedef enum _TABLET_DEVICE_KIND { 
  TABLET_DEVICE_MOUSE  = 0,
  TABLET_DEVICE_PEN,
  TABLET_DEVICE_TOUCH
} TABLET_DEVICE_KIND;
```



## <a name="constants"></a><span data-ttu-id="3d43c-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="3d43c-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="3d43c-107"><span id="TABLET_DEVICE_MOUSE"></span><span id="tablet_device_mouse"></span>**\_mouse dispositivo \_ Tablet**</span><span class="sxs-lookup"><span data-stu-id="3d43c-107"><span id="TABLET_DEVICE_MOUSE"></span><span id="tablet_device_mouse"></span>**TABLET\_DEVICE\_MOUSE**</span></span>
</dt> <dd>

<span data-ttu-id="3d43c-108">Il tablet è un mouse.</span><span class="sxs-lookup"><span data-stu-id="3d43c-108">The tablet is a mouse.</span></span> <span data-ttu-id="3d43c-109">Sono inclusi i touchpad presenti in molti computer portatili.</span><span class="sxs-lookup"><span data-stu-id="3d43c-109">This includes touchpads found on many laptop computers.</span></span>

</dd> <dt>

<span data-ttu-id="3d43c-110"><span id="TABLET_DEVICE_PEN"></span><span id="tablet_device_pen"></span>**\_penna del dispositivo Tablet \_**</span><span class="sxs-lookup"><span data-stu-id="3d43c-110"><span id="TABLET_DEVICE_PEN"></span><span id="tablet_device_pen"></span>**TABLET\_DEVICE\_PEN**</span></span>
</dt> <dd>

<span data-ttu-id="3d43c-111">Il tablet usa una penna elettromagnetica e un digitalizzatore.</span><span class="sxs-lookup"><span data-stu-id="3d43c-111">The tablet utilizes an electromagnetic pen and digitizer.</span></span>

</dd> <dt>

<span data-ttu-id="3d43c-112"><span id="TABLET_DEVICE_TOUCH"></span><span id="tablet_device_touch"></span>**\_tocco del dispositivo Tablet \_**</span><span class="sxs-lookup"><span data-stu-id="3d43c-112"><span id="TABLET_DEVICE_TOUCH"></span><span id="tablet_device_touch"></span>**TABLET\_DEVICE\_TOUCH**</span></span>
</dt> <dd>

<span data-ttu-id="3d43c-113">Il tablet utilizza un digitalizzatore sensibile al tocco.</span><span class="sxs-lookup"><span data-stu-id="3d43c-113">The tablet utilizes a touch sensitive digitizer.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3d43c-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3d43c-114">Requirements</span></span>



| <span data-ttu-id="3d43c-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="3d43c-115">Requirement</span></span> | <span data-ttu-id="3d43c-116">Valore</span><span class="sxs-lookup"><span data-stu-id="3d43c-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="3d43c-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3d43c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="3d43c-118">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="3d43c-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="3d43c-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3d43c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="3d43c-120">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="3d43c-120">None supported</span></span><br/>                                     |



## <a name="see-also"></a><span data-ttu-id="3d43c-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3d43c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d43c-122">**Metodo ITablet2:: GetDeviceKind**</span><span class="sxs-lookup"><span data-stu-id="3d43c-122">**ITablet2::GetDeviceKind Method**</span></span>](itablet2-getdevicekind.md)
</dt> </dl>

 

 




