---
description: Indica se l'oggetto è stato modificato dopo l'ultimo salvataggio nel flusso corrente.
ms.assetid: 69840be6-062e-4505-8381-ea04e822c660
title: Metodo CPersistStream. IsDirty (pStream. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.IsDirty
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4f3bc57998b63ece5ca32543fc00d1d3b5b4389b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328928"
---
# <a name="cpersiststreamisdirty-method"></a><span data-ttu-id="9f3b3-103">Metodo CPersistStream. IsDirty</span><span class="sxs-lookup"><span data-stu-id="9f3b3-103">CPersistStream.IsDirty method</span></span>

<span data-ttu-id="9f3b3-104">Indica se l'oggetto è stato modificato dopo l'ultimo salvataggio nel flusso corrente.</span><span class="sxs-lookup"><span data-stu-id="9f3b3-104">Indicates whether the object has changed since it was last saved to its current stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f3b3-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9f3b3-105">Syntax</span></span>


```C++
HRESULT IsDirty();
```



## <a name="parameters"></a><span data-ttu-id="9f3b3-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="9f3b3-106">Parameters</span></span>

<span data-ttu-id="9f3b3-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="9f3b3-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9f3b3-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9f3b3-108">Return value</span></span>

<span data-ttu-id="9f3b3-109">Restituisce \_ OK se il filtro deve essere salvato e \_ false se non è necessario salvarlo.</span><span class="sxs-lookup"><span data-stu-id="9f3b3-109">Returns S\_OK if the filter needs saving and S\_FALSE if it does not need saving.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f3b3-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="9f3b3-110">Remarks</span></span>

<span data-ttu-id="9f3b3-111">Questa funzione membro implementa il metodo **IPersistStream:: IsDirty** .</span><span class="sxs-lookup"><span data-stu-id="9f3b3-111">This member function implements the **IPersistStream::IsDirty** method.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f3b3-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9f3b3-112">Requirements</span></span>



| <span data-ttu-id="9f3b3-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="9f3b3-113">Requirement</span></span> | <span data-ttu-id="9f3b3-114">Valore</span><span class="sxs-lookup"><span data-stu-id="9f3b3-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f3b3-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9f3b3-115">Header</span></span><br/>  | <dl> <span data-ttu-id="9f3b3-116"><dt>PStream. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9f3b3-116"><dt>Pstream.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="9f3b3-117">Libreria</span><span class="sxs-lookup"><span data-stu-id="9f3b3-117">Library</span></span><br/> | <dl> <span data-ttu-id="9f3b3-118"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="9f3b3-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f3b3-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9f3b3-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f3b3-120">**Classe CPersistStream**</span><span class="sxs-lookup"><span data-stu-id="9f3b3-120">**CPersistStream Class**</span></span>](cpersiststream.md)
</dt> </dl>

 

 




