---
description: La funzione StringFromResource carica una stringa da un file di risorse con l'identificatore di risorsa specificato.
ms.assetid: 26b40905-db16-46d1-8621-9aa8cb8e7232
title: Funzione StringFromResource (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StringFromResource
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a9bb13944f281d528ff95a7856ebc8a0a2374c6e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331917"
---
# <a name="stringfromresource-function"></a><span data-ttu-id="f90f9-103">StringFromResource (funzione)</span><span class="sxs-lookup"><span data-stu-id="f90f9-103">StringFromResource function</span></span>

<span data-ttu-id="f90f9-104">La `StringFromResource` funzione carica una stringa da un file di risorse con l'identificatore di risorsa specificato.</span><span class="sxs-lookup"><span data-stu-id="f90f9-104">The `StringFromResource` function loads a string from a resource file with the given resource identifier.</span></span>

## <a name="syntax"></a><span data-ttu-id="f90f9-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f90f9-105">Syntax</span></span>


```C++
TCHAR* WINAPI StringFromResource(
   TCHAR *pBuffer,
   int   iResourceID
);
```



## <a name="parameters"></a><span data-ttu-id="f90f9-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f90f9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f90f9-107">*pBuffer*</span><span class="sxs-lookup"><span data-stu-id="f90f9-107">*pBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="f90f9-108">Puntatore alla stringa corrispondente a *iResourceID*.</span><span class="sxs-lookup"><span data-stu-id="f90f9-108">Pointer to the string corresponding to *iResourceID*.</span></span>

</dd> <dt>

<span data-ttu-id="f90f9-109">*iResourceID*</span><span class="sxs-lookup"><span data-stu-id="f90f9-109">*iResourceID*</span></span> 
</dt> <dd>

<span data-ttu-id="f90f9-110">Identificatore di risorsa della stringa da recuperare.</span><span class="sxs-lookup"><span data-stu-id="f90f9-110">Resource identifier of the string to retrieve.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f90f9-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f90f9-111">Return value</span></span>

<span data-ttu-id="f90f9-112">Restituisce la stessa stringa di *pbuffer*.</span><span class="sxs-lookup"><span data-stu-id="f90f9-112">Returns the same string as *pBuffer*.</span></span> <span data-ttu-id="f90f9-113">Se la funzione ha esito negativo, restituisce una stringa null.</span><span class="sxs-lookup"><span data-stu-id="f90f9-113">If the function is not successful, returns a null string.</span></span>

## <a name="remarks"></a><span data-ttu-id="f90f9-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="f90f9-114">Remarks</span></span>

<span data-ttu-id="f90f9-115">Il buffer *pbuffer* deve essere almeno di \_ lunghezza massima di Str \_ byte.</span><span class="sxs-lookup"><span data-stu-id="f90f9-115">The *pBuffer* buffer must be at least STR\_MAX\_LENGTH bytes.</span></span>

## <a name="requirements"></a><span data-ttu-id="f90f9-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f90f9-116">Requirements</span></span>



| <span data-ttu-id="f90f9-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="f90f9-117">Requirement</span></span> | <span data-ttu-id="f90f9-118">Valore</span><span class="sxs-lookup"><span data-stu-id="f90f9-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f90f9-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f90f9-119">Header</span></span><br/>  | <dl> <span data-ttu-id="f90f9-120"><dt>Wxutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f90f9-120"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="f90f9-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="f90f9-121">Library</span></span><br/> | <dl> <span data-ttu-id="f90f9-122"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="f90f9-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f90f9-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f90f9-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f90f9-124">Funzioni di supporto della pagina delle proprietà</span><span class="sxs-lookup"><span data-stu-id="f90f9-124">Property Page Helper Functions</span></span>](property-page-helper-functions.md)
</dt> </dl>

 

 




