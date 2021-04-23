---
description: Questa proprietà viene usata per segnalare quale versione del set di proprietà Rate Change deve essere usata dal decodificatore.
ms.assetid: 49d1bfda-749b-4614-9a75-1f76fa8b320d
title: AM_RATE_UseRateVersion proprietà (Dvdmedia.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4dd33ef96c50ecc3da0711f08f0c7ffbf0a20825
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910219"
---
# <a name="am_rate_userateversion-property"></a><span data-ttu-id="b7259-103">Proprietà \_ Am RATE \_ UseRateVersion</span><span class="sxs-lookup"><span data-stu-id="b7259-103">AM\_RATE\_UseRateVersion Property</span></span>

<span data-ttu-id="b7259-104">Questa proprietà viene usata per segnalare quale versione del set di proprietà Rate Change deve essere usata dal decodificatore.</span><span class="sxs-lookup"><span data-stu-id="b7259-104">This property is used to signal which version of the Rate Change property set the decoder should use.</span></span> <span data-ttu-id="b7259-105">Il valore è di **tipo WORD.**</span><span class="sxs-lookup"><span data-stu-id="b7259-105">The value is a **WORD** type.</span></span> <span data-ttu-id="b7259-106">Il byte più significativo contiene il numero di versione secondaria e il byte meno significativo contiene il byte meno significativo.</span><span class="sxs-lookup"><span data-stu-id="b7259-106">The high-order byte contains the minor version number, and the low-order byte contains the low-order byte.</span></span> <span data-ttu-id="b7259-107">La versione 1.1 viene quindi segnalata con il valore 0x0101.</span><span class="sxs-lookup"><span data-stu-id="b7259-107">Thus, version 1.1 is signaled with the value 0x0101.</span></span>

<span data-ttu-id="b7259-108">Se il decodificatore non supporta la versione specificata, dovrebbe non riuscire la chiamata a [**IKsPropertySet::Set**](ikspropertyset-set.md) e restituire E \_ NOINTERFACE.</span><span class="sxs-lookup"><span data-stu-id="b7259-108">If the decoder does not support the specified version, it should fail the call to [**IKsPropertySet::Set**](ikspropertyset-set.md) and return E\_NOINTERFACE.</span></span> <span data-ttu-id="b7259-109">Se il filtro di origine non imposta la versione, per impostazione predefinita il decodificatore deve essere la versione 1.0.</span><span class="sxs-lookup"><span data-stu-id="b7259-109">If the source filter does not set the version, the decoder should default to version 1.0.</span></span>



| <span data-ttu-id="b7259-110">Label</span><span class="sxs-lookup"><span data-stu-id="b7259-110">Label</span></span> | <span data-ttu-id="b7259-111">Valore</span><span class="sxs-lookup"><span data-stu-id="b7259-111">Value</span></span> |
|-------------------|-------------------------------|
| <span data-ttu-id="b7259-112">GUID set di proprietà</span><span class="sxs-lookup"><span data-stu-id="b7259-112">Property Set GUID</span></span> | <span data-ttu-id="b7259-113">AM \_ KSPROPSETID \_ TSRateChange</span><span class="sxs-lookup"><span data-stu-id="b7259-113">AM\_KSPROPSETID\_TSRateChange</span></span> |
| <span data-ttu-id="b7259-114">ID proprietà</span><span class="sxs-lookup"><span data-stu-id="b7259-114">Property ID</span></span>       | <span data-ttu-id="b7259-115">AM \_ RATE \_ UseRateVersion</span><span class="sxs-lookup"><span data-stu-id="b7259-115">AM\_RATE\_UseRateVersion</span></span>      |
| <span data-ttu-id="b7259-116">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="b7259-116">Data Type</span></span>         | <span data-ttu-id="b7259-117">**WORD**</span><span class="sxs-lookup"><span data-stu-id="b7259-117">**WORD**</span></span>                      |



 

## <a name="requirements"></a><span data-ttu-id="b7259-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b7259-118">Requirements</span></span>



| <span data-ttu-id="b7259-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="b7259-119">Requirement</span></span> | <span data-ttu-id="b7259-120">Valore</span><span class="sxs-lookup"><span data-stu-id="b7259-120">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b7259-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b7259-121">Header</span></span><br/> | <dl> <span data-ttu-id="b7259-122"><dt>Dvdmedia.h</dt></span><span class="sxs-lookup"><span data-stu-id="b7259-122"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7259-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b7259-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7259-124">**Rate Change Property Set**</span><span class="sxs-lookup"><span data-stu-id="b7259-124">**Rate Change Property Set**</span></span>](rate-change-property-set.md)
</dt> </dl>

 

 




