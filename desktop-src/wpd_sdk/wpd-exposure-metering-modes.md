---
description: Il \_ \_ \_ tipo di enumerazione modalità di misurazione dell'esposizione WPD descrive la modalità di misurazione da usare quando si stima l'esposizione per l'acquisizione di immagini ancora da parte di un dispositivo.
ms.assetid: 5e92013c-600d-4128-ab59-1cfa8953db67
title: Enumerazione WPD_EXPOSURE_METERING_MODES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_EXPOSURE_METERING_MODES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 76c2594339c6fa4997e4d646fc89e8c30dcdf8fa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328970"
---
# <a name="wpd_exposure_metering_modes-enumeration"></a><span data-ttu-id="c8848-103">\_Enumerazione delle \_ modalità di misurazione dell'esposizione WPD \_</span><span class="sxs-lookup"><span data-stu-id="c8848-103">WPD\_EXPOSURE\_METERING\_MODES enumeration</span></span>

<span data-ttu-id="c8848-104">Il tipo di enumerazione **\_ modalità di \_ misurazione \_ dell'esposizione WPD** descrive la modalità di misurazione da usare quando si stima l'esposizione per l'acquisizione di immagini ancora da parte di un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c8848-104">The **WPD\_EXPOSURE\_METERING\_MODES** enumeration type describes the metering mode to use when estimating exposure for still image capture by a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8848-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c8848-105">Syntax</span></span>


```C++
typedef enum WPD_EXPOSURE_METERING_MODES { 
  WPD_EXPOSURE_METERING_MODE_UNDEFINED                = 0,
  WPD_EXPOSURE_METERING_MODE_AVERAGE                  = 1,
  WPD_EXPOSURE_METERING_MODE_CENTER_WEIGHTED_AVERAGE  = 2,
  WPD_EXPOSURE_METERING_MODE_MULTI_SPOT               = 3,
  WPD_EXPOSURE_METERING_MODE_CENTER_SPOT              = 4
} ;
```



## <a name="constants"></a><span data-ttu-id="c8848-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="c8848-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="c8848-107"><span id="WPD_EXPOSURE_METERING_MODE_UNDEFINED"></span><span id="wpd_exposure_metering_mode_undefined"></span>**modalità di misurazione dell'esposizione WPD non \_ \_ \_ \_ definita**</span><span class="sxs-lookup"><span data-stu-id="c8848-107"><span id="WPD_EXPOSURE_METERING_MODE_UNDEFINED"></span><span id="wpd_exposure_metering_mode_undefined"></span>**WPD\_EXPOSURE\_METERING\_MODE\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="c8848-108">La modalità di misurazione non è definita.</span><span class="sxs-lookup"><span data-stu-id="c8848-108">The metering mode is undefined.</span></span>

</dd> <dt>

<span data-ttu-id="c8848-109"><span id="WPD_EXPOSURE_METERING_MODE_AVERAGE"></span><span id="wpd_exposure_metering_mode_average"></span>**\_ \_ media modalità di misurazione dell'esposizione \_ WPD \_**</span><span class="sxs-lookup"><span data-stu-id="c8848-109"><span id="WPD_EXPOSURE_METERING_MODE_AVERAGE"></span><span id="wpd_exposure_metering_mode_average"></span>**WPD\_EXPOSURE\_METERING\_MODE\_AVERAGE**</span></span>
</dt> <dd>

<span data-ttu-id="c8848-110">Usare l'esposizione media nell'immagine completa.</span><span class="sxs-lookup"><span data-stu-id="c8848-110">Use averaged exposure across the full image.</span></span>

</dd> <dt>

<span data-ttu-id="c8848-111"><span id="WPD_EXPOSURE_METERING_MODE_CENTER_WEIGHTED_AVERAGE"></span><span id="wpd_exposure_metering_mode_center_weighted_average"></span>**\_ \_ \_ \_ \_ media ponderata del centro modalità di misurazione dell'esposizione \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="c8848-111"><span id="WPD_EXPOSURE_METERING_MODE_CENTER_WEIGHTED_AVERAGE"></span><span id="wpd_exposure_metering_mode_center_weighted_average"></span>**WPD\_EXPOSURE\_METERING\_MODE\_CENTER\_WEIGHTED\_AVERAGE**</span></span>
</dt> <dd>

<span data-ttu-id="c8848-112">Utilizzare un'esposizione media, con il centro dell'immagine in base a un peso maggiore.</span><span class="sxs-lookup"><span data-stu-id="c8848-112">Use an averaged exposure, with the center of the image given more weight.</span></span>

</dd> <dt>

<span data-ttu-id="c8848-113"><span id="WPD_EXPOSURE_METERING_MODE_MULTI_SPOT"></span><span id="wpd_exposure_metering_mode_multi_spot"></span>**\_modalità di misurazione dell'esposizione WPD \_ \_ \_ \_ multispot**</span><span class="sxs-lookup"><span data-stu-id="c8848-113"><span id="WPD_EXPOSURE_METERING_MODE_MULTI_SPOT"></span><span id="wpd_exposure_metering_mode_multi_spot"></span>**WPD\_EXPOSURE\_METERING\_MODE\_MULTI\_SPOT**</span></span>
</dt> <dd>

<span data-ttu-id="c8848-114">Usare una tecnica di media multispot.</span><span class="sxs-lookup"><span data-stu-id="c8848-114">Use a multi-spot averaging technique.</span></span>

</dd> <dt>

<span data-ttu-id="c8848-115"><span id="WPD_EXPOSURE_METERING_MODE_CENTER_SPOT"></span><span id="wpd_exposure_metering_mode_center_spot"></span>**\_ \_ \_ punto centrale della modalità di misurazione dell' \_ esposizione WPD \_**</span><span class="sxs-lookup"><span data-stu-id="c8848-115"><span id="WPD_EXPOSURE_METERING_MODE_CENTER_SPOT"></span><span id="wpd_exposure_metering_mode_center_spot"></span>**WPD\_EXPOSURE\_METERING\_MODE\_CENTER\_SPOT**</span></span>
</dt> <dd>

<span data-ttu-id="c8848-116">Usare una tecnica per la media di punti centrali.</span><span class="sxs-lookup"><span data-stu-id="c8848-116">Use a center-spot averaging technique.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c8848-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="c8848-117">Remarks</span></span>

<span data-ttu-id="c8848-118">Indica la modalità di misurazione del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c8848-118">Indicates the metering mode of the device.</span></span> <span data-ttu-id="c8848-119">Questa enumerazione viene utilizzata dalla proprietà [della \_ \_ modalità di \_ \_ misurazione \_ dell'esposizione dell'immagine di WPD](still-image-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="c8848-119">This enumeration is used by the [WPD\_STILL\_IMAGE\_EXPOSURE\_METERING\_MODE](still-image-properties.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8848-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c8848-120">Requirements</span></span>



| <span data-ttu-id="c8848-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8848-121">Requirement</span></span> | <span data-ttu-id="c8848-122">Valore</span><span class="sxs-lookup"><span data-stu-id="c8848-122">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8848-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c8848-123">Header</span></span><br/> | <dl> <span data-ttu-id="c8848-124"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="c8848-124"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8848-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c8848-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8848-126">**Strutture e tipi di enumerazione**</span><span class="sxs-lookup"><span data-stu-id="c8848-126">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




