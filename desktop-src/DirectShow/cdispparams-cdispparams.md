---
description: Metodo del costruttore.
ms.assetid: da67a5e4-b4a1-4a38-93fe-0965695e93f5
title: Costruttore CDispParams. CDispParams (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDispParams.CDispParams
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f3beeb0a6e3a18c3fac6606385d9206938bbc1cd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329634"
---
# <a name="cdispparamscdispparams-constructor"></a><span data-ttu-id="371c4-103">Costruttore CDispParams. CDispParams</span><span class="sxs-lookup"><span data-stu-id="371c4-103">CDispParams.CDispParams constructor</span></span>

<span data-ttu-id="371c4-104">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="371c4-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="371c4-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="371c4-105">Syntax</span></span>


```C++
CDispParams(
   UINT    nArgs,
   VARIANT *pArgs
);
```



## <a name="parameters"></a><span data-ttu-id="371c4-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="371c4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="371c4-107">*nArgs*</span><span class="sxs-lookup"><span data-stu-id="371c4-107">*nArgs*</span></span> 
</dt> <dd>

<span data-ttu-id="371c4-108">Numero di argomenti passati al metodo o alla proprietà.</span><span class="sxs-lookup"><span data-stu-id="371c4-108">Number of arguments passed to the method or property.</span></span>

</dd> <dt>

<span data-ttu-id="371c4-109">*pArgs*</span><span class="sxs-lookup"><span data-stu-id="371c4-109">*pArgs*</span></span> 
</dt> <dd>

<span data-ttu-id="371c4-110">Puntatore all'elenco di argomenti.</span><span class="sxs-lookup"><span data-stu-id="371c4-110">Pointer to the list of arguments.</span></span> <span data-ttu-id="371c4-111">Nell'elenco ogni argomento viene archiviato con il tipo Variant.</span><span class="sxs-lookup"><span data-stu-id="371c4-111">In the list, each argument is stored with its variant type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="371c4-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="371c4-112">Requirements</span></span>



| <span data-ttu-id="371c4-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="371c4-113">Requirement</span></span> | <span data-ttu-id="371c4-114">Valore</span><span class="sxs-lookup"><span data-stu-id="371c4-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="371c4-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="371c4-115">Header</span></span><br/>  | <dl> <span data-ttu-id="371c4-116"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="371c4-116"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="371c4-117">Libreria</span><span class="sxs-lookup"><span data-stu-id="371c4-117">Library</span></span><br/> | <dl> <span data-ttu-id="371c4-118"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="371c4-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="371c4-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="371c4-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="371c4-120">**Classe CDispParams**</span><span class="sxs-lookup"><span data-stu-id="371c4-120">**CDispParams Class**</span></span>](cdispparams.md)
</dt> </dl>

 

 




