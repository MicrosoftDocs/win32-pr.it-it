---
description: Questa proprietà viene utilizzata per segnalare la versione della proprietà rate Change impostata che il decodificatore deve utilizzare.
ms.assetid: 49d1bfda-749b-4614-9a75-1f76fa8b320d
title: Proprietà AM_RATE_UseRateVersion (dvdmedia. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ab609d2d38dc28257d13994e6cd464094b714be
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330322"
---
# <a name="am_rate_userateversion-property"></a><span data-ttu-id="684a8-103">\_Proprietà rate \_ UseRateVersion</span><span class="sxs-lookup"><span data-stu-id="684a8-103">AM\_RATE\_UseRateVersion Property</span></span>

<span data-ttu-id="684a8-104">Questa proprietà viene utilizzata per segnalare la versione della proprietà rate Change impostata che il decodificatore deve utilizzare.</span><span class="sxs-lookup"><span data-stu-id="684a8-104">This property is used to signal which version of the Rate Change property set the decoder should use.</span></span> <span data-ttu-id="684a8-105">Il valore è un tipo di **parola** .</span><span class="sxs-lookup"><span data-stu-id="684a8-105">The value is a **WORD** type.</span></span> <span data-ttu-id="684a8-106">Il byte di ordine superiore contiene il numero di versione secondario e il byte di ordine inferiore contiene il byte di ordine inferiore.</span><span class="sxs-lookup"><span data-stu-id="684a8-106">The high-order byte contains the minor version number, and the low-order byte contains the low-order byte.</span></span> <span data-ttu-id="684a8-107">Quindi, la versione 1,1 viene segnalata con il valore 0x0101.</span><span class="sxs-lookup"><span data-stu-id="684a8-107">Thus, version 1.1 is signaled with the value 0x0101.</span></span>

<span data-ttu-id="684a8-108">Se il decodificatore non supporta la versione specificata, deve avere esito negativo la chiamata a [**IKsPropertySet:: set**](ikspropertyset-set.md) E restituire e \_ nointerface.</span><span class="sxs-lookup"><span data-stu-id="684a8-108">If the decoder does not support the specified version, it should fail the call to [**IKsPropertySet::Set**](ikspropertyset-set.md) and return E\_NOINTERFACE.</span></span> <span data-ttu-id="684a8-109">Se il filtro di origine non imposta la versione, il decodificatore deve avere come valore predefinito la versione 1,0.</span><span class="sxs-lookup"><span data-stu-id="684a8-109">If the source filter does not set the version, the decoder should default to version 1.0.</span></span>



|                   |                               |
|-------------------|-------------------------------|
| <span data-ttu-id="684a8-110">GUID set di proprietà</span><span class="sxs-lookup"><span data-stu-id="684a8-110">Property Set GUID</span></span> | <span data-ttu-id="684a8-111">\_TSRateChange KSPROPSETID \_</span><span class="sxs-lookup"><span data-stu-id="684a8-111">AM\_KSPROPSETID\_TSRateChange</span></span> |
| <span data-ttu-id="684a8-112">ID proprietà</span><span class="sxs-lookup"><span data-stu-id="684a8-112">Property ID</span></span>       | <span data-ttu-id="684a8-113">\_Frequenza \_ UseRateVersion</span><span class="sxs-lookup"><span data-stu-id="684a8-113">AM\_RATE\_UseRateVersion</span></span>      |
| <span data-ttu-id="684a8-114">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="684a8-114">Data Type</span></span>         | <span data-ttu-id="684a8-115">**WORD**</span><span class="sxs-lookup"><span data-stu-id="684a8-115">**WORD**</span></span>                      |



 

## <a name="requirements"></a><span data-ttu-id="684a8-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="684a8-116">Requirements</span></span>



| <span data-ttu-id="684a8-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="684a8-117">Requirement</span></span> | <span data-ttu-id="684a8-118">Valore</span><span class="sxs-lookup"><span data-stu-id="684a8-118">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="684a8-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="684a8-119">Header</span></span><br/> | <dl> <span data-ttu-id="684a8-120"><dt>Dvdmedia. h</dt></span><span class="sxs-lookup"><span data-stu-id="684a8-120"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="684a8-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="684a8-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="684a8-122">**Set di proprietà di modifica della frequenza**</span><span class="sxs-lookup"><span data-stu-id="684a8-122">**Rate Change Property Set**</span></span>](rate-change-property-set.md)
</dt> </dl>

 

 




