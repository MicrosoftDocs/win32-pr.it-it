---
description: 'Costruttore CEnumPins.CEnumPins : metodo costruttore.'
ms.assetid: f696e433-b051-4de0-80e5-f9cd31fd0f23
title: Costruttore CEnumPins.CEnumPins (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumPins.CEnumPins
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: caa27dfe0190df15be1e41b7128c06249f1ae2b8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099229"
---
# <a name="cenumpinscenumpins-constructor"></a><span data-ttu-id="56b31-103">Costruttore CEnumPins.CEnumPins</span><span class="sxs-lookup"><span data-stu-id="56b31-103">CEnumPins.CEnumPins constructor</span></span>

<span data-ttu-id="56b31-104">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="56b31-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="56b31-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="56b31-105">Syntax</span></span>


```C++
CEnumPins(
   CBaseFilter *pFilter,
   CEnumPins   *pEnumPins
);
```



## <a name="parameters"></a><span data-ttu-id="56b31-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="56b31-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56b31-107">*pFilter*</span><span class="sxs-lookup"><span data-stu-id="56b31-107">*pFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="56b31-108">Puntatore al filtro in base al quale enumerare i pin.</span><span class="sxs-lookup"><span data-stu-id="56b31-108">Pointer to the filter on which to enumerate the pins.</span></span>

</dd> <dt>

<span data-ttu-id="56b31-109">*pEnumPins*</span><span class="sxs-lookup"><span data-stu-id="56b31-109">*pEnumPins*</span></span> 
</dt> <dd>

<span data-ttu-id="56b31-110">Puntatore [**all'interfaccia IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) di un enumeratore da clonare oppure **NULL.**</span><span class="sxs-lookup"><span data-stu-id="56b31-110">Pointer to the [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) interface of an enumerator to clone, or **NULL**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="56b31-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="56b31-111">Remarks</span></span>

<span data-ttu-id="56b31-112">Se *pEnumPins* è **NULL,** questo metodo inizializza l'enumeratore all'inizio della sequenza di enumerazione.</span><span class="sxs-lookup"><span data-stu-id="56b31-112">If *pEnumPins* is **NULL**, this method initializes the enumerator to the beginning of the enumeration sequence.</span></span> <span data-ttu-id="56b31-113">In caso contrario, duplica lo stato interno dell'enumeratore specificato da *pEnumPins*.</span><span class="sxs-lookup"><span data-stu-id="56b31-113">Otherwise, it duplicates the internal state of the enumerator specified by *pEnumPins*.</span></span>

## <a name="requirements"></a><span data-ttu-id="56b31-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="56b31-114">Requirements</span></span>



| <span data-ttu-id="56b31-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="56b31-115">Requirement</span></span> | <span data-ttu-id="56b31-116">Valore</span><span class="sxs-lookup"><span data-stu-id="56b31-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="56b31-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="56b31-117">Header</span></span><br/>  | <dl> <span data-ttu-id="56b31-118"><dt>Amfilter.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="56b31-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="56b31-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="56b31-119">Library</span></span><br/> | <dl> <span data-ttu-id="56b31-120"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="56b31-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56b31-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="56b31-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56b31-122">**Classe CEnumPins**</span><span class="sxs-lookup"><span data-stu-id="56b31-122">**CEnumPins Class**</span></span>](cenumpins.md)
</dt> </dl>

 

 




