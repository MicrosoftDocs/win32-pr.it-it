---
description: "Il metodo NonDelegatingAddRef incrementa il conteggio dei riferimenti nell'oggetto. Questo metodo implementa il metodo INonDelegatingUnknown:: NonDelegatingAddRef."
ms.assetid: abb6ee51-8fb8-4307-b127-b3667260e35a
title: Metodo CUnknown. NonDelegatingAddRef (ComBase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CUnknown.NonDelegatingAddRef
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2f97260c03f0931e94e8ce6de8b7816789b2fe66
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331448"
---
# <a name="cunknownnondelegatingaddref-method"></a><span data-ttu-id="a3aaa-104">CUnknown. NonDelegatingAddRef, metodo</span><span class="sxs-lookup"><span data-stu-id="a3aaa-104">CUnknown.NonDelegatingAddRef method</span></span>

<span data-ttu-id="a3aaa-105">Il `NonDelegatingAddRef` metodo incrementa il conteggio dei riferimenti nell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="a3aaa-105">The `NonDelegatingAddRef` method increments the reference count on the object.</span></span> <span data-ttu-id="a3aaa-106">Questo metodo implementa il metodo **INonDelegatingUnknown:: NonDelegatingAddRef** .</span><span class="sxs-lookup"><span data-stu-id="a3aaa-106">This method implements the **INonDelegatingUnknown::NonDelegatingAddRef** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3aaa-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a3aaa-107">Syntax</span></span>


```C++
ULONG NonDelegatingAddRef();
```



## <a name="parameters"></a><span data-ttu-id="a3aaa-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="a3aaa-108">Parameters</span></span>

<span data-ttu-id="a3aaa-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="a3aaa-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a3aaa-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a3aaa-110">Return value</span></span>

<span data-ttu-id="a3aaa-111">Restituisce il conteggio dei riferimenti.</span><span class="sxs-lookup"><span data-stu-id="a3aaa-111">Returns the reference count.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3aaa-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a3aaa-112">Requirements</span></span>



| <span data-ttu-id="a3aaa-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="a3aaa-113">Requirement</span></span> | <span data-ttu-id="a3aaa-114">Valore</span><span class="sxs-lookup"><span data-stu-id="a3aaa-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3aaa-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a3aaa-115">Header</span></span><br/>  | <dl> <span data-ttu-id="a3aaa-116"><dt>ComBase. h (Includi Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a3aaa-116"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a3aaa-117">Libreria</span><span class="sxs-lookup"><span data-stu-id="a3aaa-117">Library</span></span><br/> | <dl> <span data-ttu-id="a3aaa-118"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="a3aaa-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




