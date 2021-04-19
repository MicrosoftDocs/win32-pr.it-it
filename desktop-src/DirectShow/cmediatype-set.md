---
description: Il metodo CMediaType. set (mtype. h) imposta il tipo di supporto da un altro tipo di supporto. Il metodo usa il parametro ' cmtype '.
ms.assetid: 71c19d0f-93b6-41db-8659-c64411b83e7c
title: Metodo CMediaType. set (mtype. h)-cmtype [Ref] parametro
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.Set
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f9bf14132660045afbd171173a38d3ea320ba1aa
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/19/2021
ms.locfileid: "106323815"
---
# <a name="cmediatypeset-method-mtypeh---cmtype-ref-parameter"></a><span data-ttu-id="8c975-104">Metodo CMediaType. set (mtype. h)-cmtype [Ref] parametro</span><span class="sxs-lookup"><span data-stu-id="8c975-104">CMediaType.Set method (Mtype.h) - cmtype [ref] parameter</span></span>

<span data-ttu-id="8c975-105">Il `Set` metodo imposta il tipo di supporto da un altro tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="8c975-105">The `Set` method sets the media type from another media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c975-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8c975-106">Syntax</span></span>


```C++
HRESULT Set(
  [ref] const CMediaType &cmtype
);
```



## <a name="parameters"></a><span data-ttu-id="8c975-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="8c975-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c975-108">*cmtype* \[ Ref\]</span><span class="sxs-lookup"><span data-stu-id="8c975-108">*cmtype* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="8c975-109">Riferimento a un oggetto [**CMediaType**](cmediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="8c975-109">Reference to a [**CMediaType**](cmediatype.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c975-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8c975-110">Return value</span></span>

<span data-ttu-id="8c975-111">Restituisce S \_ OK o e \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="8c975-111">Returns S\_OK or E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c975-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="8c975-112">Remarks</span></span>

<span data-ttu-id="8c975-113">Questo metodo copia l'intero tipo di supporto da *cmtype*.</span><span class="sxs-lookup"><span data-stu-id="8c975-113">This method copies the entire media type from *cmtype*.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c975-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8c975-114">Requirements</span></span>

| <span data-ttu-id="8c975-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c975-115">Requirement</span></span>                   | <span data-ttu-id="8c975-116">Valore</span><span class="sxs-lookup"><span data-stu-id="8c975-116">Value</span></span>                                                                                                                                                                                           |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c975-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8c975-117">Header</span></span>  | <span data-ttu-id="8c975-118">Mtype. h (include Streams. h)</span><span class="sxs-lookup"><span data-stu-id="8c975-118">Mtype.h (include Streams.h)</span></span>                                                                                     |
| <span data-ttu-id="8c975-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="8c975-119">Library</span></span> | <span data-ttu-id="8c975-120">Strmbase. lib (compilazioni finali); Strmbasd. lib (build di debug)</span><span class="sxs-lookup"><span data-stu-id="8c975-120">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="8c975-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8c975-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c975-122">**Classe CMediaType**</span><span class="sxs-lookup"><span data-stu-id="8c975-122">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




