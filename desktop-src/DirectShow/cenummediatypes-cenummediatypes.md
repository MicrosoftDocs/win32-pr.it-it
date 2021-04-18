---
description: Metodo del costruttore.
ms.assetid: fae2e05c-3f7b-4511-9b9d-5a37ea03f851
title: Costruttore CEnumMediaTypes. CEnumMediaTypes (Amfilter. h)
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
ms.openlocfilehash: 3e17357d90c57f1a7d489d07fa56206343f50788
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329855"
---
# <a name="cenummediatypescenummediatypes-constructor"></a><span data-ttu-id="2601f-103">Costruttore CEnumMediaTypes. CEnumMediaTypes</span><span class="sxs-lookup"><span data-stu-id="2601f-103">CEnumMediaTypes.CEnumMediaTypes constructor</span></span>

<span data-ttu-id="2601f-104">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="2601f-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="2601f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2601f-105">Syntax</span></span>


```C++
CEnumMediaTypes(
   CBasePin        *pPin,
   CEnumMediaTypes *pEnumMediaTypes
);
```



## <a name="parameters"></a><span data-ttu-id="2601f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="2601f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2601f-107">*pPin*</span><span class="sxs-lookup"><span data-stu-id="2601f-107">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="2601f-108">Puntatore al pin sul quale deve essere eseguita l'enumerazione.</span><span class="sxs-lookup"><span data-stu-id="2601f-108">Pointer to the pin on which the enumeration is to be performed.</span></span>

</dd> <dt>

<span data-ttu-id="2601f-109">*pEnumMediaTypes*</span><span class="sxs-lookup"><span data-stu-id="2601f-109">*pEnumMediaTypes*</span></span> 
</dt> <dd>

<span data-ttu-id="2601f-110">Puntatore all'interfaccia [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) di un enumeratore da clonare o **null**.</span><span class="sxs-lookup"><span data-stu-id="2601f-110">Pointer to the [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) interface of an enumerator to clone, or **NULL**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2601f-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="2601f-111">Remarks</span></span>

<span data-ttu-id="2601f-112">Se *pEnumMediaTypes* è **null**, questo metodo inizializza l'enumeratore all'inizio della sequenza di enumerazione.</span><span class="sxs-lookup"><span data-stu-id="2601f-112">If *pEnumMediaTypes* is **NULL**, this method initializes the enumerator to the beginning of the enumeration sequence.</span></span> <span data-ttu-id="2601f-113">In caso contrario, duplica lo stato interno dell'enumeratore specificato da *pEnumMediaTypes*.</span><span class="sxs-lookup"><span data-stu-id="2601f-113">Otherwise, it duplicates the internal state of the enumerator specified by *pEnumMediaTypes*.</span></span>

## <a name="requirements"></a><span data-ttu-id="2601f-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2601f-114">Requirements</span></span>



| <span data-ttu-id="2601f-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="2601f-115">Requirement</span></span> | <span data-ttu-id="2601f-116">Valore</span><span class="sxs-lookup"><span data-stu-id="2601f-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2601f-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2601f-117">Header</span></span><br/>  | <dl> <span data-ttu-id="2601f-118"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2601f-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="2601f-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="2601f-119">Library</span></span><br/> | <dl> <span data-ttu-id="2601f-120"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="2601f-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2601f-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2601f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2601f-122">**Classe CEnumMediaTypes**</span><span class="sxs-lookup"><span data-stu-id="2601f-122">**CEnumMediaTypes Class**</span></span>](cenummediatypes.md)
</dt> </dl>

 

 




