---
title: Sintassi intervallo
description: Rappresenta un valore di intervallo di tempo.
ms.assetid: e41b71da-cd05-4a4a-8b97-9210dbe314de
ms.tgt_platform: multiple
keywords:
- Schema di AD di sintassi intervallo
topic_type:
- apiref
api_name:
- Interval
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59b92961deecde7faa879dbbda6bfd24560ad705
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "104400954"
---
# <a name="interval-syntax"></a><span data-ttu-id="237a6-104">Sintassi intervallo</span><span class="sxs-lookup"><span data-stu-id="237a6-104">Interval syntax</span></span>

<span data-ttu-id="237a6-105">Rappresenta un valore di intervallo di tempo.</span><span class="sxs-lookup"><span data-stu-id="237a6-105">Represents a time interval value.</span></span> <span data-ttu-id="237a6-106">Le unità di tempo effettive dipendono dall'attributo che usa questa sintassi.</span><span class="sxs-lookup"><span data-stu-id="237a6-106">The actual time units depend on which attribute is using this syntax.</span></span> <span data-ttu-id="237a6-107">Questa sintassi è identica alla sintassi [**LargeInteger**](s-largeinteger.md) , ad eccezione del fatto che i valori High e low sono interi senza segno.</span><span class="sxs-lookup"><span data-stu-id="237a6-107">This syntax is identical to the [**LargeInteger**](s-largeinteger.md) syntax, except the high and low values are unsigned integers.</span></span>



| <span data-ttu-id="237a6-108">Voce</span><span class="sxs-lookup"><span data-stu-id="237a6-108">Entry</span></span> | <span data-ttu-id="237a6-109">Valore</span><span class="sxs-lookup"><span data-stu-id="237a6-109">Value</span></span> |
|--------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="237a6-110">Nome</span><span class="sxs-lookup"><span data-stu-id="237a6-110">Name</span></span>         | <span data-ttu-id="237a6-111">Interval</span><span class="sxs-lookup"><span data-stu-id="237a6-111">Interval</span></span>                                                                           |
| <span data-ttu-id="237a6-112">ID sintassi</span><span class="sxs-lookup"><span data-stu-id="237a6-112">Syntax ID</span></span>    | <span data-ttu-id="237a6-113">2.5.5.16</span><span class="sxs-lookup"><span data-stu-id="237a6-113">2.5.5.16</span></span>                                                                           |
| <span data-ttu-id="237a6-114">ID OM</span><span class="sxs-lookup"><span data-stu-id="237a6-114">OM ID</span></span>        | <span data-ttu-id="237a6-115">65</span><span class="sxs-lookup"><span data-stu-id="237a6-115">65</span></span>                                                                                 |
| <span data-ttu-id="237a6-116">Tipo MAPI</span><span class="sxs-lookup"><span data-stu-id="237a6-116">MAPI Type</span></span>    | \-                                                                                 |
| <span data-ttu-id="237a6-117">Tipo di annunci</span><span class="sxs-lookup"><span data-stu-id="237a6-117">ADS Type</span></span>     | <span data-ttu-id="237a6-118">ADSTYPE \_ \_ Integer grande</span><span class="sxs-lookup"><span data-stu-id="237a6-118">ADSTYPE\_LARGE\_INTEGER</span></span>                                                            |
| <span data-ttu-id="237a6-119">Tipo Variant</span><span class="sxs-lookup"><span data-stu-id="237a6-119">Variant Type</span></span> | <span data-ttu-id="237a6-120">\_invio VT</span><span class="sxs-lookup"><span data-stu-id="237a6-120">VT\_DISPATCH</span></span>                                                                       |
| <span data-ttu-id="237a6-121">Tipo SDS</span><span class="sxs-lookup"><span data-stu-id="237a6-121">SDS Type</span></span>     | <span data-ttu-id="237a6-122">Oggetto COM di cui è possibile eseguire il cast a un [**IADsLargeInteger**](/windows/desktop/api/iads/nn-iads-iadslargeinteger).</span><span class="sxs-lookup"><span data-stu-id="237a6-122">A COM object that can be cast to an [**IADsLargeInteger**](/windows/desktop/api/iads/nn-iads-iadslargeinteger).</span></span> |



## <a name="see-also"></a><span data-ttu-id="237a6-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="237a6-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="237a6-124">**IADsLargeInteger**</span><span class="sxs-lookup"><span data-stu-id="237a6-124">**IADsLargeInteger**</span></span>](/windows/desktop/api/iads/nn-iads-iadslargeinteger)
</dt> <dt>

[<span data-ttu-id="237a6-125">**LargeInteger**</span><span class="sxs-lookup"><span data-stu-id="237a6-125">**LargeInteger**</span></span>](s-largeinteger.md)
</dt> </dl>

 

 
