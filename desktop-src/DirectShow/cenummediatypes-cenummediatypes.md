---
description: 'Costruttore CEnumMediaTypes.CEnumMediaTypes : metodo costruttore.'
ms.assetid: fae2e05c-3f7b-4511-9b9d-5a37ea03f851
title: Costruttore CEnumMediaTypes.CEnumMediaTypes (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumMediaTypes.CEnumMediaTypes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2d243ed25cc48c5d30d467f97e2ec20e1f0f2b58
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095679"
---
# <a name="cenummediatypescenummediatypes-constructor"></a><span data-ttu-id="e7005-103">Costruttore CEnumMediaTypes.CEnumMediaTypes</span><span class="sxs-lookup"><span data-stu-id="e7005-103">CEnumMediaTypes.CEnumMediaTypes constructor</span></span>

<span data-ttu-id="e7005-104">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="e7005-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7005-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e7005-105">Syntax</span></span>


```C++
CEnumMediaTypes(
   CBasePin        *pPin,
   CEnumMediaTypes *pEnumMediaTypes
);
```



## <a name="parameters"></a><span data-ttu-id="e7005-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e7005-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7005-107">*pPin*</span><span class="sxs-lookup"><span data-stu-id="e7005-107">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="e7005-108">Puntatore al pin su cui deve essere eseguita l'enumerazione.</span><span class="sxs-lookup"><span data-stu-id="e7005-108">Pointer to the pin on which the enumeration is to be performed.</span></span>

</dd> <dt>

<span data-ttu-id="e7005-109">*pEnumMediaTypes*</span><span class="sxs-lookup"><span data-stu-id="e7005-109">*pEnumMediaTypes*</span></span> 
</dt> <dd>

<span data-ttu-id="e7005-110">Puntatore [**all'interfaccia IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) di un enumeratore da clonare oppure **NULL.**</span><span class="sxs-lookup"><span data-stu-id="e7005-110">Pointer to the [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) interface of an enumerator to clone, or **NULL**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e7005-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="e7005-111">Remarks</span></span>

<span data-ttu-id="e7005-112">Se *pEnumMediaTypes è* **NULL,** questo metodo inizializza l'enumeratore all'inizio della sequenza di enumerazione.</span><span class="sxs-lookup"><span data-stu-id="e7005-112">If *pEnumMediaTypes* is **NULL**, this method initializes the enumerator to the beginning of the enumeration sequence.</span></span> <span data-ttu-id="e7005-113">In caso contrario, duplica lo stato interno dell'enumeratore specificato *da pEnumMediaTypes.*</span><span class="sxs-lookup"><span data-stu-id="e7005-113">Otherwise, it duplicates the internal state of the enumerator specified by *pEnumMediaTypes*.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7005-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e7005-114">Requirements</span></span>



| <span data-ttu-id="e7005-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7005-115">Requirement</span></span> | <span data-ttu-id="e7005-116">Valore</span><span class="sxs-lookup"><span data-stu-id="e7005-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7005-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e7005-117">Header</span></span><br/>  | <dl> <span data-ttu-id="e7005-118"><dt>Amfilter.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="e7005-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="e7005-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="e7005-119">Library</span></span><br/> | <dl> <span data-ttu-id="e7005-120"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="e7005-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7005-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e7005-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7005-122">**Classe CEnumMediaTypes**</span><span class="sxs-lookup"><span data-stu-id="e7005-122">**CEnumMediaTypes Class**</span></span>](cenummediatypes.md)
</dt> </dl>

 

 




