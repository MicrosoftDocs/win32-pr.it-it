---
description: Verifica se un puntatore è allineato a un limite specificato. In caso contrario, la macro richiama la macro ASSERT. Ignorato nelle compilazioni al dettaglio.
ms.assetid: 4d9ec3a9-7107-45a3-a7aa-28d6e38fa92a
title: Macro DbgAssertAligned (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgAssertAligned
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: 22b357f7f28e9df04ce36636e3972dbadc3036a6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332706"
---
# <a name="dbgassertaligned-macro"></a><span data-ttu-id="017ab-105">DbgAssertAligned (macro)</span><span class="sxs-lookup"><span data-stu-id="017ab-105">DbgAssertAligned macro</span></span>

<span data-ttu-id="017ab-106">Verifica se un puntatore è allineato a un limite specificato.</span><span class="sxs-lookup"><span data-stu-id="017ab-106">Tests whether a pointer is aligned to a specified boundary.</span></span> <span data-ttu-id="017ab-107">In caso contrario, la macro richiama la macro [**Assert**](assert.md) .</span><span class="sxs-lookup"><span data-stu-id="017ab-107">If not, this macro invokes the [**ASSERT**](assert.md) macro.</span></span> <span data-ttu-id="017ab-108">Ignorato nelle compilazioni al dettaglio.</span><span class="sxs-lookup"><span data-stu-id="017ab-108">Ignored in retail builds.</span></span>

## <a name="syntax"></a><span data-ttu-id="017ab-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="017ab-109">Syntax</span></span>


```C++
void DbgAssertAligned(
    ptr,
    alignment
);
```



## <a name="parameters"></a><span data-ttu-id="017ab-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="017ab-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="017ab-111">*ptr*</span><span class="sxs-lookup"><span data-stu-id="017ab-111">*ptr*</span></span> 
</dt> <dd>

<span data-ttu-id="017ab-112">Variabile puntatore.</span><span class="sxs-lookup"><span data-stu-id="017ab-112">Pointer variable.</span></span>

</dd> <dt>

<span data-ttu-id="017ab-113">*allineamento*</span><span class="sxs-lookup"><span data-stu-id="017ab-113">*alignment*</span></span> 
</dt> <dd>

<span data-ttu-id="017ab-114">Allineamento obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="017ab-114">Required alignment.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="017ab-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="017ab-115">Return value</span></span>

<span data-ttu-id="017ab-116">Questa macro non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="017ab-116">This macro does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="017ab-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="017ab-117">Requirements</span></span>



| <span data-ttu-id="017ab-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="017ab-118">Requirement</span></span> | <span data-ttu-id="017ab-119">Valore</span><span class="sxs-lookup"><span data-stu-id="017ab-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="017ab-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="017ab-120">Header</span></span><br/> | <dl> <span data-ttu-id="017ab-121"><dt>Wxdebug. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="017ab-121"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="017ab-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="017ab-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="017ab-123">Macro di asserzione e punti di interruzione</span><span class="sxs-lookup"><span data-stu-id="017ab-123">Assert and Breakpoint Macros</span></span>](assert-and-breakpoint-macros.md)
</dt> </dl>

 

 




