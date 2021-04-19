---
description: Informazioni sul metodo del costruttore CMediaType. CMediaType (mtype. h). Questo metodo usa i parametri ' mtype ' è PHR '.
ms.assetid: b7d5264a-2a5f-4111-96bb-1ea2b13405be
title: Costruttore CMediaType. CMediaType (mtype. h)-parametri mtype e PHR
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.CMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 12ef9012e59dfce1f45d21aa720ae13bd660f2d8
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/19/2021
ms.locfileid: "106323830"
---
# <a name="cmediatypecmediatype-constructor-mtypeh---mtype-and-phr-parameters"></a><span data-ttu-id="15c03-104">Costruttore CMediaType. CMediaType (mtype. h)-parametri mtype e PHR</span><span class="sxs-lookup"><span data-stu-id="15c03-104">CMediaType.CMediaType constructor (Mtype.h) - mtype and phr parameters</span></span>

<span data-ttu-id="15c03-105">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="15c03-105">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="15c03-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="15c03-106">Syntax</span></span>


```C++
CMediaType(
  [ref] const AM_MEDIA_TYPE &mtype,
              HRESULT       *phr = NULL
);
```



## <a name="parameters"></a><span data-ttu-id="15c03-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="15c03-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15c03-108">*mtype* \[ Ref\]</span><span class="sxs-lookup"><span data-stu-id="15c03-108">*mtype* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="15c03-109">Riferimento a una struttura del [**\_ \_ tipo di supporto am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .</span><span class="sxs-lookup"><span data-stu-id="15c03-109">Reference to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span> <span data-ttu-id="15c03-110">Il costruttore copia il tipo di supporto nel nuovo oggetto, incluso il blocco di formato, se disponibile.</span><span class="sxs-lookup"><span data-stu-id="15c03-110">The constructor copies the media type to the new object, including the format block, if any.</span></span>

</dd> <dt>

<span data-ttu-id="15c03-111">*PHR*</span><span class="sxs-lookup"><span data-stu-id="15c03-111">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="15c03-112">Puntatore a una variabile che riceve un valore HRESULT.</span><span class="sxs-lookup"><span data-stu-id="15c03-112">Pointer to a variable that receives an HRESULT value.</span></span> <span data-ttu-id="15c03-113">Questo parametro può essere un puntatore **null** .</span><span class="sxs-lookup"><span data-stu-id="15c03-113">This parameter can be a **NULL** pointer.</span></span> <span data-ttu-id="15c03-114">In caso contrario, il chiamante deve impostare il valore su S \_ OK prima di chiamare il costruttore.</span><span class="sxs-lookup"><span data-stu-id="15c03-114">Otherwise, the caller must set the value to S\_OK before calling the constructor.</span></span> <span data-ttu-id="15c03-115">Se il costruttore ha esito negativo, imposta il valore su un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="15c03-115">If the constructor fails, it sets the value to a failure code.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="15c03-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="15c03-116">Remarks</span></span>

<span data-ttu-id="15c03-117">Il costruttore chiama il metodo [**CMediaType:: InitMediaType**](cmediatype-initmediatype.md) per inizializzare il tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="15c03-117">The constructor calls the [**CMediaType::InitMediaType**](cmediatype-initmediatype.md) method to initialize the media type.</span></span>

## <a name="requirements"></a><span data-ttu-id="15c03-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="15c03-118">Requirements</span></span>

| <span data-ttu-id="15c03-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="15c03-119">Requirement</span></span>                   | <span data-ttu-id="15c03-120">Valore</span><span class="sxs-lookup"><span data-stu-id="15c03-120">Value</span></span>                                                                                                                                                                                           |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15c03-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="15c03-121">Header</span></span>  | <span data-ttu-id="15c03-122">Mtype. h (include Streams. h)</span><span class="sxs-lookup"><span data-stu-id="15c03-122">Mtype.h (include Streams.h)</span></span>                                                                                     |
| <span data-ttu-id="15c03-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="15c03-123">Library</span></span> | <span data-ttu-id="15c03-124">Strmbase. lib (compilazioni finali); Strmbasd. lib (build di debug)</span><span class="sxs-lookup"><span data-stu-id="15c03-124">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="15c03-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="15c03-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15c03-126">**Classe CMediaType**</span><span class="sxs-lookup"><span data-stu-id="15c03-126">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




