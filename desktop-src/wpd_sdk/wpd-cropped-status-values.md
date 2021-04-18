---
description: Il \_ \_ tipo di enumerazione dei valori di stato ritagliati WPD \_ descrive lo stato di ritaglio di un'immagine.
ms.assetid: 7ee87fb7-1d17-4e89-aee7-e7abacbd790d
title: Enumerazione WPD_CROPPED_STATUS_VALUES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_CROPPED_STATUS_VALUES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 3f324fd90e58e486a12bffebde9f844d96c3ed83
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324214"
---
# <a name="wpd_cropped_status_values-enumeration"></a><span data-ttu-id="332c6-103">\_ \_ Enumerazione dei valori di stato ritagliati WPD \_</span><span class="sxs-lookup"><span data-stu-id="332c6-103">WPD\_CROPPED\_STATUS\_VALUES enumeration</span></span>

<span data-ttu-id="332c6-104">Il tipo di enumerazione dei **\_ \_ \_ valori di stato ritagliati WPD** descrive lo stato di ritaglio di un'immagine.</span><span class="sxs-lookup"><span data-stu-id="332c6-104">The **WPD\_CROPPED\_STATUS\_VALUES** enumeration type describes the cropping status of an image.</span></span>

## <a name="syntax"></a><span data-ttu-id="332c6-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="332c6-105">Syntax</span></span>


```C++
typedef enum WPD_CROPPED_STATUS_VALUES { 
  WPD_CROPPED_STATUS_NOT_CROPPED            = 0,
  WPD_CROPPED_STATUS_CROPPED                = 1,
  WPD_CROPPED_STATUS_SHOULD_NOT_BE_CROPPED  = 2
} ;
```



## <a name="constants"></a><span data-ttu-id="332c6-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="332c6-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="332c6-107"><span id="WPD_CROPPED_STATUS_NOT_CROPPED"></span><span id="wpd_cropped_status_not_cropped"></span>**\_stato ritagliato WPD \_ \_ non \_ ritagliato**</span><span class="sxs-lookup"><span data-stu-id="332c6-107"><span id="WPD_CROPPED_STATUS_NOT_CROPPED"></span><span id="wpd_cropped_status_not_cropped"></span>**WPD\_CROPPED\_STATUS\_NOT\_CROPPED**</span></span>
</dt> <dd>

<span data-ttu-id="332c6-108">L'immagine non è stata ritagliata.</span><span class="sxs-lookup"><span data-stu-id="332c6-108">The image has not been cropped.</span></span>

</dd> <dt>

<span data-ttu-id="332c6-109"><span id="WPD_CROPPED_STATUS_CROPPED"></span><span id="wpd_cropped_status_cropped"></span>**stato ritagliato WPD \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="332c6-109"><span id="WPD_CROPPED_STATUS_CROPPED"></span><span id="wpd_cropped_status_cropped"></span>**WPD\_CROPPED\_STATUS\_CROPPED**</span></span>
</dt> <dd>

<span data-ttu-id="332c6-110">L'immagine è stata ritagliata.</span><span class="sxs-lookup"><span data-stu-id="332c6-110">The image has been cropped.</span></span>

</dd> <dt>

<span data-ttu-id="332c6-111"><span id="WPD_CROPPED_STATUS_SHOULD_NOT_BE_CROPPED"></span><span id="wpd_cropped_status_should_not_be_cropped"></span>**\_lo stato ritagliato WPD \_ \_ \_ non deve \_ essere \_ ritagliato**</span><span class="sxs-lookup"><span data-stu-id="332c6-111"><span id="WPD_CROPPED_STATUS_SHOULD_NOT_BE_CROPPED"></span><span id="wpd_cropped_status_should_not_be_cropped"></span>**WPD\_CROPPED\_STATUS\_SHOULD\_NOT\_BE\_CROPPED**</span></span>
</dt> <dd>

<span data-ttu-id="332c6-112">L'immagine non è stata e non deve essere ritagliata.</span><span class="sxs-lookup"><span data-stu-id="332c6-112">The image has not been, and should not be, cropped.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="332c6-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="332c6-113">Remarks</span></span>

<span data-ttu-id="332c6-114">Indica lo stato ritagliato di un'immagine.</span><span class="sxs-lookup"><span data-stu-id="332c6-114">Indicates the cropped status of an image.</span></span> <span data-ttu-id="332c6-115">Questa enumerazione viene utilizzata dalla proprietà [di \_ \_ \_ stato ritagliata immagine WPD](image-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="332c6-115">This enumeration is used by the [WPD\_IMAGE\_CROPPED\_STATUS](image-properties.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="332c6-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="332c6-116">Requirements</span></span>



| <span data-ttu-id="332c6-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="332c6-117">Requirement</span></span> | <span data-ttu-id="332c6-118">Valore</span><span class="sxs-lookup"><span data-stu-id="332c6-118">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="332c6-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="332c6-119">Header</span></span><br/> | <dl> <span data-ttu-id="332c6-120"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="332c6-120"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="332c6-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="332c6-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="332c6-122">**Strutture e tipi di enumerazione**</span><span class="sxs-lookup"><span data-stu-id="332c6-122">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




