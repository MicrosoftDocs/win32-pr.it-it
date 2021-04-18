---
description: "Decrementa il conteggio dei riferimenti nell'oggetto. Questo metodo implementa il metodo INonDelegatingUnknown:: NonDelegatingRelease."
ms.assetid: 58610f7d-5524-450f-a0f8-b299944abc78
title: Metodo CUnknown. NonDelegatingRelease (ComBase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CUnknown.NonDelegatingRelease
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ec709d4b636eea6a145f9a24a868ad5c495e4477
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331445"
---
# <a name="cunknownnondelegatingrelease-method"></a><span data-ttu-id="dded2-104">CUnknown. NonDelegatingRelease, metodo</span><span class="sxs-lookup"><span data-stu-id="dded2-104">CUnknown.NonDelegatingRelease method</span></span>

<span data-ttu-id="dded2-105">Decrementa il conteggio dei riferimenti nell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="dded2-105">Decrements the reference count on the object.</span></span> <span data-ttu-id="dded2-106">Questo metodo implementa il metodo **INonDelegatingUnknown:: NonDelegatingRelease** .</span><span class="sxs-lookup"><span data-stu-id="dded2-106">This method implements the **INonDelegatingUnknown::NonDelegatingRelease** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="dded2-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dded2-107">Syntax</span></span>


```C++
ULONG NonDelegatingRelease();
```



## <a name="parameters"></a><span data-ttu-id="dded2-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="dded2-108">Parameters</span></span>

<span data-ttu-id="dded2-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="dded2-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="dded2-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="dded2-110">Return value</span></span>

<span data-ttu-id="dded2-111">Restituisce il conteggio dei riferimenti.</span><span class="sxs-lookup"><span data-stu-id="dded2-111">Returns the reference count.</span></span>

## <a name="remarks"></a><span data-ttu-id="dded2-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="dded2-112">Remarks</span></span>

<span data-ttu-id="dded2-113">Quando il conteggio dei riferimenti raggiunge zero, l'oggetto viene eliminato automaticamente.</span><span class="sxs-lookup"><span data-stu-id="dded2-113">When the reference count reaches zero, the object deletes itself.</span></span>

## <a name="requirements"></a><span data-ttu-id="dded2-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dded2-114">Requirements</span></span>



| <span data-ttu-id="dded2-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="dded2-115">Requirement</span></span> | <span data-ttu-id="dded2-116">Valore</span><span class="sxs-lookup"><span data-stu-id="dded2-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dded2-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="dded2-117">Header</span></span><br/>  | <dl> <span data-ttu-id="dded2-118"><dt>ComBase. h (Includi Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dded2-118"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="dded2-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="dded2-119">Library</span></span><br/> | <dl> <span data-ttu-id="dded2-120"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="dded2-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




