---
description: 'Costruttore CDispParams.CDispParams : metodo costruttore.'
ms.assetid: da67a5e4-b4a1-4a38-93fe-0965695e93f5
title: Costruttore CDispParams.CDispParams (Ctlutil.h)
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
ms.openlocfilehash: 42f55a57a0f9e06d3001c2638d457fe0b82a914d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095789"
---
# <a name="cdispparamscdispparams-constructor"></a><span data-ttu-id="61fc9-103">Costruttore CDispParams.CDispParams</span><span class="sxs-lookup"><span data-stu-id="61fc9-103">CDispParams.CDispParams constructor</span></span>

<span data-ttu-id="61fc9-104">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="61fc9-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="61fc9-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="61fc9-105">Syntax</span></span>


```C++
CDispParams(
   UINT    nArgs,
   VARIANT *pArgs
);
```



## <a name="parameters"></a><span data-ttu-id="61fc9-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="61fc9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61fc9-107">*nArgs*</span><span class="sxs-lookup"><span data-stu-id="61fc9-107">*nArgs*</span></span> 
</dt> <dd>

<span data-ttu-id="61fc9-108">Numero di argomenti passati al metodo o alla proprietà.</span><span class="sxs-lookup"><span data-stu-id="61fc9-108">Number of arguments passed to the method or property.</span></span>

</dd> <dt>

<span data-ttu-id="61fc9-109">*pArgs*</span><span class="sxs-lookup"><span data-stu-id="61fc9-109">*pArgs*</span></span> 
</dt> <dd>

<span data-ttu-id="61fc9-110">Puntatore all'elenco di argomenti.</span><span class="sxs-lookup"><span data-stu-id="61fc9-110">Pointer to the list of arguments.</span></span> <span data-ttu-id="61fc9-111">Nell'elenco ogni argomento viene archiviato con il relativo tipo variant.</span><span class="sxs-lookup"><span data-stu-id="61fc9-111">In the list, each argument is stored with its variant type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="61fc9-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="61fc9-112">Requirements</span></span>



| <span data-ttu-id="61fc9-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="61fc9-113">Requirement</span></span> | <span data-ttu-id="61fc9-114">Valore</span><span class="sxs-lookup"><span data-stu-id="61fc9-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61fc9-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="61fc9-115">Header</span></span><br/>  | <dl> <span data-ttu-id="61fc9-116"><dt>Ctlutil.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="61fc9-116"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="61fc9-117">Libreria</span><span class="sxs-lookup"><span data-stu-id="61fc9-117">Library</span></span><br/> | <dl> <span data-ttu-id="61fc9-118"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="61fc9-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61fc9-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="61fc9-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61fc9-120">**Classe CDispParams**</span><span class="sxs-lookup"><span data-stu-id="61fc9-120">**CDispParams Class**</span></span>](cdispparams.md)
</dt> </dl>

 

 




