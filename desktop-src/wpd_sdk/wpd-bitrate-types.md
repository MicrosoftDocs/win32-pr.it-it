---
description: Il \_ tipo di enumerazione WPD bitrate \_ types descrive un tipo di compressione di file audio.
ms.assetid: 9905b189-00c5-469b-ae48-10c79b9ac903
title: Enumerazione WPD_BITRATE_TYPES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_BITRATE_TYPES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 2597af21c5655c3c12c0ca29f097d0eba2bb8d54
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331686"
---
# <a name="wpd_bitrate_types-enumeration"></a><span data-ttu-id="9069b-103">\_Enumerazione tipi a bitrate WPD \_</span><span class="sxs-lookup"><span data-stu-id="9069b-103">WPD\_BITRATE\_TYPES enumeration</span></span>

<span data-ttu-id="9069b-104">Il tipo di enumerazione **WPD \_ bitrate \_ types** descrive il tipo di compressione di un file audio.</span><span class="sxs-lookup"><span data-stu-id="9069b-104">The **WPD\_BITRATE\_TYPES** enumeration type describes an audio file's compression type.</span></span>

## <a name="syntax"></a><span data-ttu-id="9069b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9069b-105">Syntax</span></span>


```C++
typedef enum WPD_BITRATE_TYPES { 
  WPD_BITRATE_TYPE_UNUSED    = 0,
  WPD_BITRATE_TYPE_DISCRETE  = 1,
  WPD_BITRATE_TYPE_VARIABLE  = 2,
  WPD_BITRATE_TYPE_FREE      = 3
} ;
```



## <a name="constants"></a><span data-ttu-id="9069b-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="9069b-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="9069b-107"><span id="WPD_BITRATE_TYPE_UNUSED"></span><span id="wpd_bitrate_type_unused"></span>**\_tipo di bitrate WPD \_ \_ inutilizzato**</span><span class="sxs-lookup"><span data-stu-id="9069b-107"><span id="WPD_BITRATE_TYPE_UNUSED"></span><span id="wpd_bitrate_type_unused"></span>**WPD\_BITRATE\_TYPE\_UNUSED**</span></span>
</dt> <dd>

<span data-ttu-id="9069b-108">Questo valore non è stato specificato.</span><span class="sxs-lookup"><span data-stu-id="9069b-108">This value has not been specified.</span></span>

</dd> <dt>

<span data-ttu-id="9069b-109"><span id="WPD_BITRATE_TYPE_DISCRETE"></span><span id="wpd_bitrate_type_discrete"></span>**\_tipo di bitrate WPD \_ \_ discreto**</span><span class="sxs-lookup"><span data-stu-id="9069b-109"><span id="WPD_BITRATE_TYPE_DISCRETE"></span><span id="wpd_bitrate_type_discrete"></span>**WPD\_BITRATE\_TYPE\_DISCRETE**</span></span>
</dt> <dd>

<span data-ttu-id="9069b-110">Compressione della velocità in bit costante.</span><span class="sxs-lookup"><span data-stu-id="9069b-110">Constant bit rate compression.</span></span>

</dd> <dt>

<span data-ttu-id="9069b-111"><span id="WPD_BITRATE_TYPE_VARIABLE"></span><span id="wpd_bitrate_type_variable"></span>**\_variabile di \_ tipo BITRAte WPD \_**</span><span class="sxs-lookup"><span data-stu-id="9069b-111"><span id="WPD_BITRATE_TYPE_VARIABLE"></span><span id="wpd_bitrate_type_variable"></span>**WPD\_BITRATE\_TYPE\_VARIABLE**</span></span>
</dt> <dd>

<span data-ttu-id="9069b-112">Compressione della velocità in bit variabile.</span><span class="sxs-lookup"><span data-stu-id="9069b-112">Variable bit rate compression.</span></span>

</dd> <dt>

<span data-ttu-id="9069b-113"><span id="WPD_BITRATE_TYPE_FREE"></span><span id="wpd_bitrate_type_free"></span>**\_ \_ tipo gratuito a BITRAte WPD \_**</span><span class="sxs-lookup"><span data-stu-id="9069b-113"><span id="WPD_BITRATE_TYPE_FREE"></span><span id="wpd_bitrate_type_free"></span>**WPD\_BITRATE\_TYPE\_FREE**</span></span>
</dt> <dd>

<span data-ttu-id="9069b-114">Velocità in bit in formato libero.</span><span class="sxs-lookup"><span data-stu-id="9069b-114">Free format bit rate.</span></span> <span data-ttu-id="9069b-115">Si tratta di una velocità in bit costante inferiore alla velocità in bit massima consentita.</span><span class="sxs-lookup"><span data-stu-id="9069b-115">This is a constant bit rate that is lower than the maximum allowed bit rate.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9069b-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9069b-116">Requirements</span></span>



| <span data-ttu-id="9069b-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="9069b-117">Requirement</span></span> | <span data-ttu-id="9069b-118">Valore</span><span class="sxs-lookup"><span data-stu-id="9069b-118">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="9069b-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9069b-119">Header</span></span><br/> | <dl> <span data-ttu-id="9069b-120"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="9069b-120"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9069b-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9069b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9069b-122">**Strutture e tipi di enumerazione**</span><span class="sxs-lookup"><span data-stu-id="9069b-122">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




