---
description: Flag che indica se il pin tenta i propri tipi di supporti preferiti prima di quelli del PIN di ricezione.
ms.assetid: 50462ee4-4a61-472f-9a7e-9cdb39be4dea
title: 'Membro CBasePin:: m_bTryMyTypesFirst (Amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bTryMyTypesFirst
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 72f98021b6ba97d32974f26ac4e76ca31fa54e5c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331536"
---
# <a name="cbasepinm_btrymytypesfirst-member"></a><span data-ttu-id="39f37-103">Membro bTryMyTypesFirst di CBasePin:: m \_</span><span class="sxs-lookup"><span data-stu-id="39f37-103">CBasePin::m\_bTryMyTypesFirst member</span></span>

<span data-ttu-id="39f37-104">Flag che indica se il pin tenta i propri tipi di supporti preferiti prima di quelli del PIN di ricezione.</span><span class="sxs-lookup"><span data-stu-id="39f37-104">Flag that indicates whether the pin tries its own preferred media types before those of the receiving pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="39f37-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="39f37-105">Syntax</span></span>


```C++
bool m_bTryMyTypesFirst;
```



## <a name="remarks"></a><span data-ttu-id="39f37-106">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="39f37-106">Remarks</span></span>

<span data-ttu-id="39f37-107">Il valore predefinito di questo flag è **false**.</span><span class="sxs-lookup"><span data-stu-id="39f37-107">This flag defaults to **FALSE**.</span></span> <span data-ttu-id="39f37-108">Se il flag è **true**, il metodo [**CBasePin:: AgreeMediaType**](cbasepin-agreemediatype.md) inverte l'ordine in cui tenta i tipi di supporto.</span><span class="sxs-lookup"><span data-stu-id="39f37-108">If the flag is **TRUE**, the [**CBasePin::AgreeMediaType**](cbasepin-agreemediatype.md) method reverses the order in which it tries media types.</span></span>

## <a name="requirements"></a><span data-ttu-id="39f37-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="39f37-109">Requirements</span></span>



| <span data-ttu-id="39f37-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="39f37-110">Requirement</span></span> | <span data-ttu-id="39f37-111">Valore</span><span class="sxs-lookup"><span data-stu-id="39f37-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39f37-112">Intestazione</span><span class="sxs-lookup"><span data-stu-id="39f37-112">Header</span></span><br/>  | <dl> <span data-ttu-id="39f37-113"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="39f37-113"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="39f37-114">Libreria</span><span class="sxs-lookup"><span data-stu-id="39f37-114">Library</span></span><br/> | <dl> <span data-ttu-id="39f37-115"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="39f37-115"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39f37-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="39f37-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39f37-117">**Classe CBasePin**</span><span class="sxs-lookup"><span data-stu-id="39f37-117">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




