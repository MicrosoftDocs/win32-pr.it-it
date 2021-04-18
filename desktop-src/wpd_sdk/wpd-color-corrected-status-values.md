---
description: Il \_ \_ \_ tipo di enumerazione dei valori di stato con correzione del colore WPD \_ descrive lo stato di correzione dei colori di un'immagine o un file video.
ms.assetid: af129a1b-7760-4339-adf7-3f3c17cebde2
title: Enumerazione WPD_COLOR_CORRECTED_STATUS_VALUES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_COLOR_CORRECTED_STATUS_VALUES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: ec6bfcaa3933bb70c3064f829e701509e3ff32f7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330581"
---
# <a name="wpd_color_corrected_status_values-enumeration"></a><span data-ttu-id="6b123-103">\_ \_ \_ Enumerazione dei valori di stato con correzione del colore WPD \_</span><span class="sxs-lookup"><span data-stu-id="6b123-103">WPD\_COLOR\_CORRECTED\_STATUS\_VALUES enumeration</span></span>

<span data-ttu-id="6b123-104">Il tipo di enumerazione dei **valori di stato con \_ correzione del colore \_ \_ \_ WPD** descrive lo stato di correzione dei colori di un'immagine o un file video.</span><span class="sxs-lookup"><span data-stu-id="6b123-104">The **WPD\_COLOR\_CORRECTED\_STATUS\_VALUES** enumeration type describes the color correction status of an image or video file.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b123-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6b123-105">Syntax</span></span>


```C++
typedef enum WPD_COLOR_CORRECTED_STATUS_VALUES { 
  WPD_COLOR_CORRECTED_STATUS_NOT_CORRECTED            = 0,
  WPD_COLOR_CORRECTED_STATUS_CORRECTED                = 1,
  WPD_COLOR_CORRECTED_STATUS_SHOULD_NOT_BE_CORRECTED  = 2
} ;
```



## <a name="constants"></a><span data-ttu-id="6b123-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="6b123-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="6b123-107"><span id="WPD_COLOR_CORRECTED_STATUS_NOT_CORRECTED"></span><span id="wpd_color_corrected_status_not_corrected"></span>**\_stato correzione colore WPD \_ \_ \_ non \_ corretto**</span><span class="sxs-lookup"><span data-stu-id="6b123-107"><span id="WPD_COLOR_CORRECTED_STATUS_NOT_CORRECTED"></span><span id="wpd_color_corrected_status_not_corrected"></span>**WPD\_COLOR\_CORRECTED\_STATUS\_NOT\_CORRECTED**</span></span>
</dt> <dd>

<span data-ttu-id="6b123-108">Colore non corretto per l'immagine.</span><span class="sxs-lookup"><span data-stu-id="6b123-108">The image has not been color corrected.</span></span>

</dd> <dt>

<span data-ttu-id="6b123-109"><span id="WPD_COLOR_CORRECTED_STATUS_CORRECTED"></span><span id="wpd_color_corrected_status_corrected"></span>**\_ \_ \_ correzione stato correzione colore \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="6b123-109"><span id="WPD_COLOR_CORRECTED_STATUS_CORRECTED"></span><span id="wpd_color_corrected_status_corrected"></span>**WPD\_COLOR\_CORRECTED\_STATUS\_CORRECTED**</span></span>
</dt> <dd>

<span data-ttu-id="6b123-110">Il colore dell'immagine è stato corretto.</span><span class="sxs-lookup"><span data-stu-id="6b123-110">The image has been color corrected.</span></span>

</dd> <dt>

<span data-ttu-id="6b123-111"><span id="WPD_COLOR_CORRECTED_STATUS_SHOULD_NOT_BE_CORRECTED"></span><span id="wpd_color_corrected_status_should_not_be_corrected"></span>**\_ \_ lo stato corretto del colore WPD \_ \_ \_ non deve \_ essere \_ corretto**</span><span class="sxs-lookup"><span data-stu-id="6b123-111"><span id="WPD_COLOR_CORRECTED_STATUS_SHOULD_NOT_BE_CORRECTED"></span><span id="wpd_color_corrected_status_should_not_be_corrected"></span>**WPD\_COLOR\_CORRECTED\_STATUS\_SHOULD\_NOT\_BE\_CORRECTED**</span></span>
</dt> <dd>

<span data-ttu-id="6b123-112">L'immagine non è stata e non deve essere con correzione del colore.</span><span class="sxs-lookup"><span data-stu-id="6b123-112">The image has not been, and should not be, color corrected.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6b123-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="6b123-113">Remarks</span></span>

<span data-ttu-id="6b123-114">Indica lo stato corretto del colore di un'immagine.</span><span class="sxs-lookup"><span data-stu-id="6b123-114">Indicates the color corrected status of an image.</span></span> <span data-ttu-id="6b123-115">Questa enumerazione viene utilizzata dalla proprietà [ \_ \_ \_ \_ dello stato WPD image correct color](image-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="6b123-115">This enumeration is used by the [WPD\_IMAGE\_COLOR\_CORRECTED\_STATUS](image-properties.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b123-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6b123-116">Requirements</span></span>



| <span data-ttu-id="6b123-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="6b123-117">Requirement</span></span> | <span data-ttu-id="6b123-118">Valore</span><span class="sxs-lookup"><span data-stu-id="6b123-118">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b123-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6b123-119">Header</span></span><br/> | <dl> <span data-ttu-id="6b123-120"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="6b123-120"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b123-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6b123-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b123-122">**Strutture e tipi di enumerazione**</span><span class="sxs-lookup"><span data-stu-id="6b123-122">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




