---
description: Il \_ \_ \_ tipo di enumerazione delle impostazioni di bilanciamento del bianco WPD descrive il modo in cui un dispositivo video o immagine pondera i canali di colore per ottenere un giusto equilibrio bianco.
ms.assetid: 7bc173dd-4fdd-4b03-994e-f0711c910618
title: Enumerazione WPD_WHITE_BALANCE_SETTINGS (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_WHITE_BALANCE_SETTINGS
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 06e607acc06ed00cc9fe91670650caee44c30430
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327258"
---
# <a name="wpd_white_balance_settings-enumeration"></a><span data-ttu-id="b3006-103">\_ \_ Enumerazione impostazioni bilanciamento bianco WPD \_</span><span class="sxs-lookup"><span data-stu-id="b3006-103">WPD\_WHITE\_BALANCE\_SETTINGS enumeration</span></span>

<span data-ttu-id="b3006-104">Il tipo di enumerazione **\_ \_ \_ delle impostazioni di bilanciamento del bianco WPD** descrive il modo in cui un dispositivo video o immagine pondera i canali di colore per ottenere un giusto equilibrio bianco.</span><span class="sxs-lookup"><span data-stu-id="b3006-104">The **WPD\_WHITE\_BALANCE\_SETTINGS** enumeration type describes how a video or image device weights color channels to achieve a proper white balance.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3006-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b3006-105">Syntax</span></span>


```C++
typedef enum WPD_WHITE_BALANCE_SETTINGS { 
  WPD_WHITE_BALANCE_UNDEFINED           = 0,
  WPD_WHITE_BALANCE_MANUAL              = 1,
  WPD_WHITE_BALANCE_AUTOMATIC           = 2,
  WPD_WHITE_BALANCE_ONE_PUSH_AUTOMATIC  = 3,
  WPD_WHITE_BALANCE_DAYLIGHT            = 4,
  WPD_WHITE_BALANCE_TUNGSTEN            = 5,
  WPD_WHITE_BALANCE_FLASH               = 6
} ;
```



## <a name="constants"></a><span data-ttu-id="b3006-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="b3006-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="b3006-107"><span id="WPD_WHITE_BALANCE_UNDEFINED"></span><span id="wpd_white_balance_undefined"></span>**\_bilanciamento bianco WPD non \_ \_ definito**</span><span class="sxs-lookup"><span data-stu-id="b3006-107"><span id="WPD_WHITE_BALANCE_UNDEFINED"></span><span id="wpd_white_balance_undefined"></span>**WPD\_WHITE\_BALANCE\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="b3006-108">Questo valore non è stato definito.</span><span class="sxs-lookup"><span data-stu-id="b3006-108">This value has not been defined.</span></span>

</dd> <dt>

<span data-ttu-id="b3006-109"><span id="WPD_WHITE_BALANCE_MANUAL"></span><span id="wpd_white_balance_manual"></span>**\_Manuale di \_ bilanciamento del bianco WPD \_**</span><span class="sxs-lookup"><span data-stu-id="b3006-109"><span id="WPD_WHITE_BALANCE_MANUAL"></span><span id="wpd_white_balance_manual"></span>**WPD\_WHITE\_BALANCE\_MANUAL**</span></span>
</dt> <dd>

<span data-ttu-id="b3006-110">Il bilanciamento bianco viene impostato in modo esplicito tramite la proprietà [WPD \_ still \_ Image \_ RGB \_ Gain](still-image-properties.md) e non verrà modificato da solo.</span><span class="sxs-lookup"><span data-stu-id="b3006-110">The white balance is set explicitly by using the [WPD\_STILL\_IMAGE\_RGB\_GAIN](still-image-properties.md) property and will not change by itself.</span></span>

</dd> <dt>

<span data-ttu-id="b3006-111"><span id="WPD_WHITE_BALANCE_AUTOMATIC"></span><span id="wpd_white_balance_automatic"></span>**\_bilanciamento del bianco WPD \_ \_ automatico**</span><span class="sxs-lookup"><span data-stu-id="b3006-111"><span id="WPD_WHITE_BALANCE_AUTOMATIC"></span><span id="wpd_white_balance_automatic"></span>**WPD\_WHITE\_BALANCE\_AUTOMATIC**</span></span>
</dt> <dd>

<span data-ttu-id="b3006-112">Il dispositivo imposterà il saldo bianco.</span><span class="sxs-lookup"><span data-stu-id="b3006-112">The device will set the white balance.</span></span>

</dd> <dt>

<span data-ttu-id="b3006-113"><span id="WPD_WHITE_BALANCE_ONE_PUSH_AUTOMATIC"></span><span id="wpd_white_balance_one_push_automatic"></span>**\_bilanciamento del bianco WPD \_ \_ One \_ push \_ automatico**</span><span class="sxs-lookup"><span data-stu-id="b3006-113"><span id="WPD_WHITE_BALANCE_ONE_PUSH_AUTOMATIC"></span><span id="wpd_white_balance_one_push_automatic"></span>**WPD\_WHITE\_BALANCE\_ONE\_PUSH\_AUTOMATIC**</span></span>
</dt> <dd>

<span data-ttu-id="b3006-114">Il dispositivo imposterà il saldo bianco, ma solo quando l'utente preme il pulsante di acquisizione del dispositivo puntando al dispositivo in un campo bianco.</span><span class="sxs-lookup"><span data-stu-id="b3006-114">The device will set the white balance, but only when the user pushes the device's capture button while aiming the device at a white field.</span></span>

</dd> <dt>

<span data-ttu-id="b3006-115"><span id="WPD_WHITE_BALANCE_DAYLIGHT"></span><span id="wpd_white_balance_daylight"></span>**WPD \_ di \_ bilanciamento del bianco \_**</span><span class="sxs-lookup"><span data-stu-id="b3006-115"><span id="WPD_WHITE_BALANCE_DAYLIGHT"></span><span id="wpd_white_balance_daylight"></span>**WPD\_WHITE\_BALANCE\_DAYLIGHT**</span></span>
</dt> <dd>

<span data-ttu-id="b3006-116">Il dispositivo utilizzerà i numeri di bilancia bianca appropriati per l'uso nella maggior parte delle impostazioni dell'ora legale.</span><span class="sxs-lookup"><span data-stu-id="b3006-116">The device will use white balance numbers appropriate for use in most daylight settings.</span></span>

</dd> <dt>

<span data-ttu-id="b3006-117"><span id="WPD_WHITE_BALANCE_TUNGSTEN"></span><span id="wpd_white_balance_tungsten"></span>**WPD \_ bilanciamento del bianco di \_ \_ tungsteno**</span><span class="sxs-lookup"><span data-stu-id="b3006-117"><span id="WPD_WHITE_BALANCE_TUNGSTEN"></span><span id="wpd_white_balance_tungsten"></span>**WPD\_WHITE\_BALANCE\_TUNGSTEN**</span></span>
</dt> <dd>

<span data-ttu-id="b3006-118">Il dispositivo utilizzerà i numeri di bilancia bianca appropriati per l'uso nella maggior parte delle impostazioni di illuminazione incandescenza interna.</span><span class="sxs-lookup"><span data-stu-id="b3006-118">The device will use white balance numbers appropriate for use in most indoor, incandescent lighting settings.</span></span>

</dd> <dt>

<span data-ttu-id="b3006-119"><span id="WPD_WHITE_BALANCE_FLASH"></span><span id="wpd_white_balance_flash"></span>**\_ \_ Flash Bilanciamento bianco \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="b3006-119"><span id="WPD_WHITE_BALANCE_FLASH"></span><span id="wpd_white_balance_flash"></span>**WPD\_WHITE\_BALANCE\_FLASH**</span></span>
</dt> <dd>

<span data-ttu-id="b3006-120">Il dispositivo utilizzerà i numeri di bilancia bianca appropriati per l'uso con Flash.</span><span class="sxs-lookup"><span data-stu-id="b3006-120">The device will use white balance numbers appropriate for use with a flash.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b3006-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="b3006-121">Remarks</span></span>

<span data-ttu-id="b3006-122">Questa enumerazione viene utilizzata dalla proprietà [di \_ \_ bilanciamento del \_ bianco \_ WPD Still Image](still-image-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="b3006-122">This enumeration is used by the [WPD\_STILL\_IMAGE\_WHITE\_BALANCE](still-image-properties.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3006-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b3006-123">Requirements</span></span>



| <span data-ttu-id="b3006-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3006-124">Requirement</span></span> | <span data-ttu-id="b3006-125">Valore</span><span class="sxs-lookup"><span data-stu-id="b3006-125">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3006-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b3006-126">Header</span></span><br/> | <dl> <span data-ttu-id="b3006-127"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="b3006-127"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3006-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b3006-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3006-129">**Strutture e tipi di enumerazione**</span><span class="sxs-lookup"><span data-stu-id="b3006-129">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




