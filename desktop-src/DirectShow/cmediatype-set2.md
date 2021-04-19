---
description: Il metodo set imposta il tipo di supporto da un altro tipo di supporto.
ms.assetid: b3cf65c2-48db-4ee0-9a74-c1652f017eed
title: Metodo CMediaType. set (mtype. h)-mtype [Ref] parametro
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
ms.openlocfilehash: e8fd9145ee33dbe4b589b34833836466efa62ada
ms.sourcegitcommit: 4d4a6e9ad5de37e467cd3164276771b71e1f113f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/05/2021
ms.locfileid: "106389086"
---
# <a name="cmediatypeset-method-mtypeh"></a><span data-ttu-id="c8aaf-103">Metodo CMediaType. set (mtype. h)</span><span class="sxs-lookup"><span data-stu-id="c8aaf-103">CMediaType.Set method (Mtype.h)</span></span>

<span data-ttu-id="c8aaf-104">Il `Set` metodo imposta il tipo di supporto da un altro tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="c8aaf-104">The `Set` method sets the media type from another media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8aaf-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c8aaf-105">Syntax</span></span>


```C++
HRESULT Set(
  [ref] const AM_MEDIA_TYPE &mtype
);
```



## <a name="parameters"></a><span data-ttu-id="c8aaf-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c8aaf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8aaf-107">*mtype* \[ Ref\]</span><span class="sxs-lookup"><span data-stu-id="c8aaf-107">*mtype* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="c8aaf-108">Riferimento a una struttura del [**\_ \_ tipo di supporto am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .</span><span class="sxs-lookup"><span data-stu-id="c8aaf-108">Reference to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8aaf-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c8aaf-109">Return value</span></span>

<span data-ttu-id="c8aaf-110">Restituisce S \_ OK o e \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="c8aaf-110">Returns S\_OK or E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="c8aaf-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="c8aaf-111">Remarks</span></span>

<span data-ttu-id="c8aaf-112">Questo metodo copia l'intero tipo di supporto da *mtype*.</span><span class="sxs-lookup"><span data-stu-id="c8aaf-112">This method copies the entire media type from *mtype*.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8aaf-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c8aaf-113">Requirements</span></span>



| <span data-ttu-id="c8aaf-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8aaf-114">Requirement</span></span> | <span data-ttu-id="c8aaf-115">Valore</span><span class="sxs-lookup"><span data-stu-id="c8aaf-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8aaf-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c8aaf-116">Header</span></span><br/>  | <dl> <span data-ttu-id="c8aaf-117"><dt>Mtype. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c8aaf-117"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="c8aaf-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="c8aaf-118">Library</span></span><br/> | <dl> <span data-ttu-id="c8aaf-119"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="c8aaf-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8aaf-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c8aaf-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8aaf-121">**Classe CMediaType**</span><span class="sxs-lookup"><span data-stu-id="c8aaf-121">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




