---
description: Il metodo set imposta il tipo di supporto da un altro tipo di supporto.
ms.assetid: b3cf65c2-48db-4ee0-9a74-c1652f017eed
title: Metodo CMediaType. set (mtype. h)
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
ms.openlocfilehash: afe99c3f5ee10e6aacd3dadf69af320b110688af
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325515"
---
# <a name="cmediatypeset-method-mtypeh"></a><span data-ttu-id="726c6-103">Metodo CMediaType. set (mtype. h)</span><span class="sxs-lookup"><span data-stu-id="726c6-103">CMediaType.Set method (Mtype.h)</span></span>

<span data-ttu-id="726c6-104">Il `Set` metodo imposta il tipo di supporto da un altro tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="726c6-104">The `Set` method sets the media type from another media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="726c6-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="726c6-105">Syntax</span></span>


```C++
HRESULT Set(
  [ref] const AM_MEDIA_TYPE &mtype
);
```



## <a name="parameters"></a><span data-ttu-id="726c6-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="726c6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="726c6-107">*mtype* \[ Ref\]</span><span class="sxs-lookup"><span data-stu-id="726c6-107">*mtype* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="726c6-108">Riferimento a una struttura del [**\_ \_ tipo di supporto am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .</span><span class="sxs-lookup"><span data-stu-id="726c6-108">Reference to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="726c6-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="726c6-109">Return value</span></span>

<span data-ttu-id="726c6-110">Restituisce S \_ OK o e \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="726c6-110">Returns S\_OK or E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="726c6-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="726c6-111">Remarks</span></span>

<span data-ttu-id="726c6-112">Questo metodo copia l'intero tipo di supporto da *mtype*.</span><span class="sxs-lookup"><span data-stu-id="726c6-112">This method copies the entire media type from *mtype*.</span></span>

## <a name="requirements"></a><span data-ttu-id="726c6-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="726c6-113">Requirements</span></span>



| <span data-ttu-id="726c6-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="726c6-114">Requirement</span></span> | <span data-ttu-id="726c6-115">Valore</span><span class="sxs-lookup"><span data-stu-id="726c6-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="726c6-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="726c6-116">Header</span></span><br/>  | <dl> <span data-ttu-id="726c6-117"><dt>Mtype. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="726c6-117"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="726c6-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="726c6-118">Library</span></span><br/> | <dl> <span data-ttu-id="726c6-119"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="726c6-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="726c6-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="726c6-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="726c6-121">**Classe CMediaType**</span><span class="sxs-lookup"><span data-stu-id="726c6-121">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




