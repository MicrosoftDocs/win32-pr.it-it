---
description: 'Costruttore CUnknown.CUnknown : metodo costruttore.'
ms.assetid: dafe0d5c-b4c8-4efb-8c47-a8c5db6e8aed
title: Costruttore CUnknown.CUnknown (Combase.h)
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
ms.openlocfilehash: 32859871f8ef69ce357fe204f0741356314fbb06
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084609"
---
# <a name="cunknowncunknown-constructor"></a><span data-ttu-id="4d002-103">Costruttore CUnknown.CUnknown</span><span class="sxs-lookup"><span data-stu-id="4d002-103">CUnknown.CUnknown constructor</span></span>

<span data-ttu-id="4d002-104">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="4d002-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d002-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4d002-105">Syntax</span></span>


```C++
CUnknown(
   const TCHAR     *pName,
         LPUNKNOWN pUnk
);
```



## <a name="parameters"></a><span data-ttu-id="4d002-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="4d002-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d002-107">*Pname*</span><span class="sxs-lookup"><span data-stu-id="4d002-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="4d002-108">Stringa contenente il nome dell'oggetto. utilizzato nel costruttore [**CBaseObject per**](cbaseobject.md) il debug.</span><span class="sxs-lookup"><span data-stu-id="4d002-108">String containing the name of the object; used in the [**CBaseObject**](cbaseobject.md) constructor for debugging.</span></span>

</dd> <dt>

<span data-ttu-id="4d002-109">*Punk*</span><span class="sxs-lookup"><span data-stu-id="4d002-109">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="4d002-110">Puntatore al proprietario dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="4d002-110">Pointer to the owner of this object.</span></span> <span data-ttu-id="4d002-111">Se l'oggetto è aggregato, passare un puntatore all'interfaccia IUnknown dell'oggetto di aggregazione.</span><span class="sxs-lookup"><span data-stu-id="4d002-111">If the object is aggregated, pass a pointer to the aggregating object's IUnknown interface.</span></span> <span data-ttu-id="4d002-112">In caso contrario, impostare questo parametro su **NULL.**</span><span class="sxs-lookup"><span data-stu-id="4d002-112">Otherwise, set this parameter to **NULL**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4d002-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="4d002-113">Remarks</span></span>

<span data-ttu-id="4d002-114">L'oggetto viene inizializzato con un conteggio dei riferimenti pari a zero.</span><span class="sxs-lookup"><span data-stu-id="4d002-114">The object is initialized with a reference count of zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="4d002-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4d002-115">Requirements</span></span>



| <span data-ttu-id="4d002-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="4d002-116">Requirement</span></span> | <span data-ttu-id="4d002-117">Valore</span><span class="sxs-lookup"><span data-stu-id="4d002-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d002-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4d002-118">Header</span></span><br/>  | <dl> <span data-ttu-id="4d002-119"><dt>Combase.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="4d002-119"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="4d002-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="4d002-120">Library</span></span><br/> | <dl> <span data-ttu-id="4d002-121"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="4d002-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




