---
description: Metodo del costruttore.
ms.assetid: dafe0d5c-b4c8-4efb-8c47-a8c5db6e8aed
title: Costruttore CUnknown. CUnknown (ComBase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CUnknown.CUnknown
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b500e7f12a2242b6c05367bc061f50680d2d608b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326165"
---
# <a name="cunknowncunknown-constructor"></a><span data-ttu-id="939b1-103">Costruttore CUnknown. CUnknown</span><span class="sxs-lookup"><span data-stu-id="939b1-103">CUnknown.CUnknown constructor</span></span>

<span data-ttu-id="939b1-104">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="939b1-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="939b1-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="939b1-105">Syntax</span></span>


```C++
CUnknown(
   const TCHAR     *pName,
         LPUNKNOWN pUnk
);
```



## <a name="parameters"></a><span data-ttu-id="939b1-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="939b1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="939b1-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="939b1-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="939b1-108">Stringa contenente il nome dell'oggetto. usato nel costruttore [**CBaseObject**](cbaseobject.md) per il debug.</span><span class="sxs-lookup"><span data-stu-id="939b1-108">String containing the name of the object; used in the [**CBaseObject**](cbaseobject.md) constructor for debugging.</span></span>

</dd> <dt>

<span data-ttu-id="939b1-109">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="939b1-109">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="939b1-110">Puntatore al proprietario di questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="939b1-110">Pointer to the owner of this object.</span></span> <span data-ttu-id="939b1-111">Se l'oggetto è aggregato, passare un puntatore all'interfaccia IUnknown dell'oggetto di aggregazione.</span><span class="sxs-lookup"><span data-stu-id="939b1-111">If the object is aggregated, pass a pointer to the aggregating object's IUnknown interface.</span></span> <span data-ttu-id="939b1-112">In caso contrario, impostare questo parametro su **null**.</span><span class="sxs-lookup"><span data-stu-id="939b1-112">Otherwise, set this parameter to **NULL**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="939b1-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="939b1-113">Remarks</span></span>

<span data-ttu-id="939b1-114">L'oggetto viene inizializzato con un conteggio dei riferimenti pari a zero.</span><span class="sxs-lookup"><span data-stu-id="939b1-114">The object is initialized with a reference count of zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="939b1-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="939b1-115">Requirements</span></span>



| <span data-ttu-id="939b1-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="939b1-116">Requirement</span></span> | <span data-ttu-id="939b1-117">Valore</span><span class="sxs-lookup"><span data-stu-id="939b1-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="939b1-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="939b1-118">Header</span></span><br/>  | <dl> <span data-ttu-id="939b1-119"><dt>ComBase. h (Includi Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="939b1-119"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="939b1-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="939b1-120">Library</span></span><br/> | <dl> <span data-ttu-id="939b1-121"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="939b1-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




