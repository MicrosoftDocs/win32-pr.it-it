---
description: Il metodo SetSubtype specifica il sottotipo.
ms.assetid: cf52e0dc-d75b-408e-a63c-481d55151d4a
title: Metodo CMediaType. SetSubtype (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.SetSubtype
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6474777b1b2e91ce0b676fdc7dbd572d7c622f0b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327204"
---
# <a name="cmediatypesetsubtype-method"></a><span data-ttu-id="9b9da-103">CMediaType. SetSubtype, metodo</span><span class="sxs-lookup"><span data-stu-id="9b9da-103">CMediaType.SetSubtype method</span></span>

<span data-ttu-id="9b9da-104">Il `SetSubtype` metodo specifica il sottotipo.</span><span class="sxs-lookup"><span data-stu-id="9b9da-104">The `SetSubtype` method specifies the subtype.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b9da-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9b9da-105">Syntax</span></span>


```C++
void SetSubtype(
   const GUID *psubtype
);
```



## <a name="parameters"></a><span data-ttu-id="9b9da-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="9b9da-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b9da-107">*psubtype*</span><span class="sxs-lookup"><span data-stu-id="9b9da-107">*psubtype*</span></span> 
</dt> <dd>

<span data-ttu-id="9b9da-108">Puntatore a un **GUID** che specifica il sottotipo.</span><span class="sxs-lookup"><span data-stu-id="9b9da-108">Pointer to a **GUID** that specifies the subtype.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9b9da-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9b9da-109">Return value</span></span>

<span data-ttu-id="9b9da-110">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="9b9da-110">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b9da-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9b9da-111">Requirements</span></span>



| <span data-ttu-id="9b9da-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="9b9da-112">Requirement</span></span> | <span data-ttu-id="9b9da-113">Valore</span><span class="sxs-lookup"><span data-stu-id="9b9da-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b9da-114">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9b9da-114">Header</span></span><br/>  | <dl> <span data-ttu-id="9b9da-115"><dt>Mtype. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9b9da-115"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="9b9da-116">Libreria</span><span class="sxs-lookup"><span data-stu-id="9b9da-116">Library</span></span><br/> | <dl> <span data-ttu-id="9b9da-117"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="9b9da-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b9da-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9b9da-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b9da-119">**Classe CMediaType**</span><span class="sxs-lookup"><span data-stu-id="9b9da-119">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




