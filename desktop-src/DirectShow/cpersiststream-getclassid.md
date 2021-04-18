---
description: Recupera l'identificatore di classe per questo filtro.
ms.assetid: f0559437-5d0d-4522-a3dc-947e3494b576
title: Metodo CPersistStream. GetClassID (pStream. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.GetClassID
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7603541eae4f431327a91777488a740afb7f628b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328933"
---
# <a name="cpersiststreamgetclassid-method"></a><span data-ttu-id="e367f-103">CPersistStream. GetClassID, metodo</span><span class="sxs-lookup"><span data-stu-id="e367f-103">CPersistStream.GetClassID method</span></span>

<span data-ttu-id="e367f-104">Recupera l'identificatore di classe per questo filtro.</span><span class="sxs-lookup"><span data-stu-id="e367f-104">Retrieves the class identifier for this filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="e367f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e367f-105">Syntax</span></span>


```C++
HRESULT GetClassID(
   CLSID *pClsID
);
```



## <a name="parameters"></a><span data-ttu-id="e367f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e367f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e367f-107">*pClsID*</span><span class="sxs-lookup"><span data-stu-id="e367f-107">*pClsID*</span></span> 
</dt> <dd>

<span data-ttu-id="e367f-108">Puntatore a una struttura CLSID.</span><span class="sxs-lookup"><span data-stu-id="e367f-108">Pointer to a CLSID structure.</span></span> <span data-ttu-id="e367f-109">Copiare l'ID della classe qui.</span><span class="sxs-lookup"><span data-stu-id="e367f-109">Copy your class ID to here.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e367f-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e367f-110">Return value</span></span>

<span data-ttu-id="e367f-111">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e367f-111">Returns an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="e367f-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e367f-112">Requirements</span></span>



| <span data-ttu-id="e367f-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="e367f-113">Requirement</span></span> | <span data-ttu-id="e367f-114">Valore</span><span class="sxs-lookup"><span data-stu-id="e367f-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e367f-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e367f-115">Header</span></span><br/>  | <dl> <span data-ttu-id="e367f-116"><dt>PStream. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e367f-116"><dt>Pstream.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e367f-117">Libreria</span><span class="sxs-lookup"><span data-stu-id="e367f-117">Library</span></span><br/> | <dl> <span data-ttu-id="e367f-118"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="e367f-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e367f-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e367f-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e367f-120">**Classe CPersistStream**</span><span class="sxs-lookup"><span data-stu-id="e367f-120">**CPersistStream Class**</span></span>](cpersiststream.md)
</dt> </dl>

 

 




