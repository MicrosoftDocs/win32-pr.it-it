---
title: Costanti WINBIO_BIOMETRIC_SENSOR_SUBTYPE (tipi WinBio \_ . h)
description: Specificare una maschera di maschera per le funzionalità del sensore di onboarding.
ms.assetid: ED2A26BC-AED4-4304-9A17-A9BA126B0AFC
topic_type:
- apiref
api_name:
- WINBIO_SENSOR_SUBTYPE_UNKNOWN
- WINBIO_FP_SENSOR_SUBTYPE_SWIPE
- WINBIO_FP_SENSOR_SUBTYPE_TOUCH
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26229634f3d404921f877bb65d83f7d75634ecbe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400484"
---
# <a name="winbio_biometric_sensor_subtype-constants"></a><span data-ttu-id="f146e-103">\_ \_ Costanti del sottotipo del sensore biometrico WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="f146e-103">WINBIO\_BIOMETRIC\_SENSOR\_SUBTYPE Constants</span></span>

<span data-ttu-id="f146e-104">Le costanti seguenti possono essere utilizzate come maschera di maschera per il parametro *capabilities* della struttura [**\_ \_ dello schema dell'unità WINBIO**](winbio-unit-schema.md) .</span><span class="sxs-lookup"><span data-stu-id="f146e-104">The following constants can be used as a bitmask for the *Capabilities* parameter of the [**WINBIO\_UNIT\_SCHEMA**](winbio-unit-schema.md) structure.</span></span> <span data-ttu-id="f146e-105">Che fanno riferimento alle funzionalità del sensore di onboarding.</span><span class="sxs-lookup"><span data-stu-id="f146e-105">These refer to the onboard sensor capabilities.</span></span>



| <span data-ttu-id="f146e-106">Costante</span><span class="sxs-lookup"><span data-stu-id="f146e-106">Constant</span></span>                                                                                                                                                                                                            | <span data-ttu-id="f146e-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f146e-107">Description</span></span>                                        |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------|
| <span id="WINBIO_SENSOR_SUBTYPE_UNKNOWN"></span><span id="winbio_sensor_subtype_unknown"></span><dl> <span data-ttu-id="f146e-108"><dt>**sottotipo del \_ sensore WINBIO \_ \_ sconosciuto**</dt></span><span class="sxs-lookup"><span data-stu-id="f146e-108"><dt>**WINBIO\_SENSOR\_SUBTYPE\_UNKNOWN**</dt></span></span> </dl>     | <span data-ttu-id="f146e-109">I sottotipi del sensore non sono noti.</span><span class="sxs-lookup"><span data-stu-id="f146e-109">The sensor sub types is not known.</span></span><br/>      |
| <span id="WINBIO_FP_SENSOR_SUBTYPE_SWIPE"></span><span id="winbio_fp_sensor_subtype_swipe"></span><dl> <span data-ttu-id="f146e-110"><dt>**\_scorrimento del \_ sottotipo di sensore FP \_ \_ WINBIO**</dt></span><span class="sxs-lookup"><span data-stu-id="f146e-110"><dt>**WINBIO\_FP\_SENSOR\_SUBTYPE\_SWIPE**</dt></span></span> </dl> | <span data-ttu-id="f146e-111">Il sensore supporta i swipi delle impronte digitali.</span><span class="sxs-lookup"><span data-stu-id="f146e-111">The sensor supports fingerprint swipes.</span></span><br/> |
| <span id="WINBIO_FP_SENSOR_SUBTYPE_TOUCH"></span><span id="winbio_fp_sensor_subtype_touch"></span><dl> <span data-ttu-id="f146e-112"><dt>**\_tocco del \_ sottotipo del sensore FP \_ \_ WINBIO**</dt></span><span class="sxs-lookup"><span data-stu-id="f146e-112"><dt>**WINBIO\_FP\_SENSOR\_SUBTYPE\_TOUCH**</dt></span></span> </dl> | <span data-ttu-id="f146e-113">Il sensore supporta i ritocchi del dito.</span><span class="sxs-lookup"><span data-stu-id="f146e-113">The sensor supports finger touches.</span></span><br/>     |



## <a name="requirements"></a><span data-ttu-id="f146e-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f146e-114">Requirements</span></span>



| <span data-ttu-id="f146e-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="f146e-115">Requirement</span></span> | <span data-ttu-id="f146e-116">Valore</span><span class="sxs-lookup"><span data-stu-id="f146e-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f146e-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f146e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f146e-118">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="f146e-118">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="f146e-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f146e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f146e-120">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="f146e-120">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="f146e-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f146e-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="f146e-122"><dt>\_Tipi WinBio. h (includere WinBio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f146e-122"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f146e-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f146e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f146e-124">Costanti dell'applicazione client</span><span class="sxs-lookup"><span data-stu-id="f146e-124">Client Application Constants</span></span>](client-application-constants.md)
</dt> <dt>

[<span data-ttu-id="f146e-125">**\_schema unità \_ WINBIO**</span><span class="sxs-lookup"><span data-stu-id="f146e-125">**WINBIO\_UNIT\_SCHEMA**</span></span>](winbio-unit-schema.md)
</dt> </dl>

 

 





