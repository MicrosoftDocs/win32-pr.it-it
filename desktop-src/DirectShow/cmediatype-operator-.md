---
description: "Il metodo CMediaType. CMediaType:: operator = (mtype. h) consente di eseguire l'overload dell'operatore di assegnazione per copiare un tipo di supporto."
ms.assetid: 28115548-97a5-426d-97cd-c5e759d8e39e
title: 'CMediaType. CMediaType:: operator = Method (mtype. h)-parametro cmtype'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.CMediaType::operator=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 56eb16c99d867e3cad3be9018c279e3e69f4f122
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/19/2021
ms.locfileid: "106323858"
---
# <a name="cmediatypecmediatypeoperator-method-mtypeh---cmtype-parameter"></a><span data-ttu-id="e9a4d-103">CMediaType. CMediaType:: operator = Method (mtype. h)-parametro cmtype</span><span class="sxs-lookup"><span data-stu-id="e9a4d-103">CMediaType.CMediaType::operator= method (Mtype.h) - cmtype parameter</span></span>

<span data-ttu-id="e9a4d-104">Questo operatore consente di eseguire l'overload dell'operatore di assegnazione per copiare un tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="e9a4d-104">This operator overloads the assignment operator to copy a media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9a4d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e9a4d-105">Syntax</span></span>


```C++
CMediaType& CMediaType::operator=(
  [ref] const CMediaType &cmtype
);
```



## <a name="parameters"></a><span data-ttu-id="e9a4d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e9a4d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9a4d-107">*cmtype* \[ Ref\]</span><span class="sxs-lookup"><span data-stu-id="e9a4d-107">*cmtype* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="e9a4d-108">Riferimento a un oggetto **CMediaType** .</span><span class="sxs-lookup"><span data-stu-id="e9a4d-108">Reference to a **CMediaType** object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9a4d-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e9a4d-109">Return value</span></span>

<span data-ttu-id="e9a4d-110">Restituisce un riferimento all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="e9a4d-110">Returns a reference to the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9a4d-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e9a4d-111">Requirements</span></span>

| <span data-ttu-id="e9a4d-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9a4d-112">Requirement</span></span>                   | <span data-ttu-id="e9a4d-113">Valore</span><span class="sxs-lookup"><span data-stu-id="e9a4d-113">Value</span></span>                                                                                                                                                                                           |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9a4d-114">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e9a4d-114">Header</span></span>  | <span data-ttu-id="e9a4d-115">Mtype. h (include Streams. h)</span><span class="sxs-lookup"><span data-stu-id="e9a4d-115">Mtype.h (include Streams.h)</span></span>                                                                                     |
| <span data-ttu-id="e9a4d-116">Libreria</span><span class="sxs-lookup"><span data-stu-id="e9a4d-116">Library</span></span> | <span data-ttu-id="e9a4d-117">Strmbase. lib (compilazioni finali); Strmbasd. lib (build di debug)</span><span class="sxs-lookup"><span data-stu-id="e9a4d-117">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="e9a4d-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e9a4d-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9a4d-119">**Classe CMediaType**</span><span class="sxs-lookup"><span data-stu-id="e9a4d-119">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




