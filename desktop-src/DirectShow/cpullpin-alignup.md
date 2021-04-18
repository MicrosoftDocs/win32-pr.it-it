---
description: Il metodo AlignUp Arrotonda un valore fino a un limite di allineamento specificato. Nota rimossa in Windows 7. .
ms.assetid: fa2a6567-3eb1-4aa9-b966-2e88b15c67b1
title: Metodo CPullPin. AlignUp (Pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.AlignUp
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a4f33ae2b7434d90d909315edda4d49e07d8adab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328491"
---
# <a name="cpullpinalignup-method"></a><span data-ttu-id="ce1b0-104">CPullPin. AlignUp, metodo</span><span class="sxs-lookup"><span data-stu-id="ce1b0-104">CPullPin.AlignUp method</span></span>

<span data-ttu-id="ce1b0-105">Il metodo **AlignUp** Arrotonda un valore fino a un limite di allineamento specificato.</span><span class="sxs-lookup"><span data-stu-id="ce1b0-105">The **AlignUp** method rounds a value up to a specified alignment boundary.</span></span>

> [!Note]  
> <span data-ttu-id="ce1b0-106">Rimosso in Windows 7.</span><span class="sxs-lookup"><span data-stu-id="ce1b0-106">Removed in Windows 7.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="ce1b0-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ce1b0-107">Syntax</span></span>


```C++
LONGLONG AlignUp(
   LONGLONG ll,
   LONG     lAlign
);
```



## <a name="parameters"></a><span data-ttu-id="ce1b0-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="ce1b0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce1b0-109">*ll*</span><span class="sxs-lookup"><span data-stu-id="ce1b0-109">*ll*</span></span> 
</dt> <dd>

<span data-ttu-id="ce1b0-110">Specifica il numero da allineare.</span><span class="sxs-lookup"><span data-stu-id="ce1b0-110">Specifies the number to align.</span></span>

</dd> <dt>

<span data-ttu-id="ce1b0-111">*lAlign*</span><span class="sxs-lookup"><span data-stu-id="ce1b0-111">*lAlign*</span></span> 
</dt> <dd>

<span data-ttu-id="ce1b0-112">Specifica il limite di allineamento.</span><span class="sxs-lookup"><span data-stu-id="ce1b0-112">Specifies the alignment boundary.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce1b0-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ce1b0-113">Return value</span></span>

<span data-ttu-id="ce1b0-114">Restituisce il risultato allineato.</span><span class="sxs-lookup"><span data-stu-id="ce1b0-114">Returns the aligned result.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce1b0-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="ce1b0-115">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="ce1b0-116">Questo metodo può causare un overflow numerico se *ll* + (*lAlign* -1) si verifica in overflow.</span><span class="sxs-lookup"><span data-stu-id="ce1b0-116">This method can cause numeric overflow if *ll* + (*lAlign* - 1) overflows.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ce1b0-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ce1b0-117">Requirements</span></span>



| <span data-ttu-id="ce1b0-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce1b0-118">Requirement</span></span> | <span data-ttu-id="ce1b0-119">Valore</span><span class="sxs-lookup"><span data-stu-id="ce1b0-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce1b0-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ce1b0-120">Header</span></span><br/>  | <dl> <span data-ttu-id="ce1b0-121"><dt>Pullpin. h</dt></span><span class="sxs-lookup"><span data-stu-id="ce1b0-121"><dt>Pullpin.h</dt></span></span> </dl>                                                                                                       |
| <span data-ttu-id="ce1b0-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="ce1b0-122">Library</span></span><br/> | <dl> <span data-ttu-id="ce1b0-123"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="ce1b0-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce1b0-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ce1b0-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce1b0-125">**Classe CPullPin**</span><span class="sxs-lookup"><span data-stu-id="ce1b0-125">**CPullPin Class**</span></span>](cpullpin.md)
</dt> </dl>

 

 




