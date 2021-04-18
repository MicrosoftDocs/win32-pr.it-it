---
description: Determina se un rettangolo di origine è valido.
ms.assetid: 3fef107b-6f4c-4fab-91d3-6ab72dcc32be
title: Metodo CBaseControlVideo. CheckSourceRect (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.CheckSourceRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fa219687dabcf9124662e3269d157fb0a163a6a1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327583"
---
# <a name="cbasecontrolvideochecksourcerect-method"></a><span data-ttu-id="19e52-103">CBaseControlVideo. CheckSourceRect, metodo</span><span class="sxs-lookup"><span data-stu-id="19e52-103">CBaseControlVideo.CheckSourceRect method</span></span>

<span data-ttu-id="19e52-104">Determina se un rettangolo di origine è valido.</span><span class="sxs-lookup"><span data-stu-id="19e52-104">Determines if a source rectangle is valid.</span></span>

## <a name="syntax"></a><span data-ttu-id="19e52-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="19e52-105">Syntax</span></span>


```C++
virtual HRESULT CheckSourceRect(
   RECT *pSourceRect
);
```



## <a name="parameters"></a><span data-ttu-id="19e52-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="19e52-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19e52-107">*pSourceRect*</span><span class="sxs-lookup"><span data-stu-id="19e52-107">*pSourceRect*</span></span> 
</dt> <dd>

<span data-ttu-id="19e52-108">Puntatore al rettangolo di origine da verificare.</span><span class="sxs-lookup"><span data-stu-id="19e52-108">Pointer to the source rectangle to check.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19e52-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="19e52-109">Return value</span></span>

<span data-ttu-id="19e52-110">Restituisce E \_ INVALIDARG se non è valido; in caso contrario, restituisce NOERROR (S \_ OK).</span><span class="sxs-lookup"><span data-stu-id="19e52-110">Returns E\_INVALIDARG if not valid; otherwise, returns NOERROR (S\_OK).</span></span>

## <a name="remarks"></a><span data-ttu-id="19e52-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="19e52-111">Remarks</span></span>

<span data-ttu-id="19e52-112">Questa funzione membro verifica che il rettangolo di origine richiesto non superi il video di origine disponibile.</span><span class="sxs-lookup"><span data-stu-id="19e52-112">This member function checks that the source rectangle requested does not exceed the available source video.</span></span> <span data-ttu-id="19e52-113">Le coordinate Left e Top non possono essere negative e la larghezza e l'altezza non possono superare il lato destro e inferiore del video.</span><span class="sxs-lookup"><span data-stu-id="19e52-113">The left and top coordinates cannot be negative, and the width and height cannot exceed the right and bottom of the video.</span></span>

## <a name="requirements"></a><span data-ttu-id="19e52-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="19e52-114">Requirements</span></span>



| <span data-ttu-id="19e52-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="19e52-115">Requirement</span></span> | <span data-ttu-id="19e52-116">Valore</span><span class="sxs-lookup"><span data-stu-id="19e52-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19e52-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="19e52-117">Header</span></span><br/>  | <dl> <span data-ttu-id="19e52-118"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="19e52-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="19e52-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="19e52-119">Library</span></span><br/> | <dl> <span data-ttu-id="19e52-120"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="19e52-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19e52-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="19e52-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19e52-122">**Classe CBaseControlVideo**</span><span class="sxs-lookup"><span data-stu-id="19e52-122">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




