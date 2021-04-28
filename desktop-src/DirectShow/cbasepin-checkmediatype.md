---
description: 'Metodo CBasePin.CheckMediaType: il metodo CheckMediaType determina se il pin accetta un tipo di supporto specifico.'
ms.assetid: 6a138679-02b7-4ccc-8881-a0d496f84f93
title: Metodo CBasePin.CheckMediaType (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: afe39f3a7aac155f3cc87fa6d58f402043861d1f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099398"
---
# <a name="cbasepincheckmediatype-method"></a><span data-ttu-id="489d9-103">Metodo CBasePin.CheckMediaType</span><span class="sxs-lookup"><span data-stu-id="489d9-103">CBasePin.CheckMediaType method</span></span>

<span data-ttu-id="489d9-104">Il `CheckMediaType` metodo determina se il pin accetta un tipo di supporto specifico.</span><span class="sxs-lookup"><span data-stu-id="489d9-104">The `CheckMediaType` method determines if the pin accepts a specific media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="489d9-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="489d9-105">Syntax</span></span>


```C++
virtual HRESULT CheckMediaType(
   const CMediaType *pmt
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="489d9-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="489d9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="489d9-107">*Pmt*</span><span class="sxs-lookup"><span data-stu-id="489d9-107">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="489d9-108">Puntatore a un [**oggetto CMediaType**](cmediatype.md) che contiene il tipo di supporto proposto.</span><span class="sxs-lookup"><span data-stu-id="489d9-108">Pointer to a [**CMediaType**](cmediatype.md) object that contains the proposed media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="489d9-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="489d9-109">Return value</span></span>

<span data-ttu-id="489d9-110">Restituisce S \_ OK se il tipo di supporto proposto è accettabile.</span><span class="sxs-lookup"><span data-stu-id="489d9-110">Returns S\_OK if the proposed media type is acceptable.</span></span> <span data-ttu-id="489d9-111">In caso contrario, restituisce S \_ FALSE o un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="489d9-111">Otherwise, returns S\_FALSE or an error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="489d9-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="489d9-112">Remarks</span></span>

<span data-ttu-id="489d9-113">La classe derivata deve eseguire l'override di questo metodo virtuale puro.</span><span class="sxs-lookup"><span data-stu-id="489d9-113">The derived class must override this pure virtual method.</span></span>

## <a name="requirements"></a><span data-ttu-id="489d9-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="489d9-114">Requirements</span></span>



| <span data-ttu-id="489d9-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="489d9-115">Requirement</span></span> | <span data-ttu-id="489d9-116">Valore</span><span class="sxs-lookup"><span data-stu-id="489d9-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="489d9-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="489d9-117">Header</span></span><br/>  | <dl> <span data-ttu-id="489d9-118"><dt>Amfilter.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="489d9-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="489d9-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="489d9-119">Library</span></span><br/> | <dl> <span data-ttu-id="489d9-120"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="489d9-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="489d9-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="489d9-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="489d9-122">**Classe CBasePin**</span><span class="sxs-lookup"><span data-stu-id="489d9-122">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




