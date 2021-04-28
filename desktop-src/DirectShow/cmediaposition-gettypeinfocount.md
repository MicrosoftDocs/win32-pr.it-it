---
description: "Metodo CMediaPosition.GetTypeInfoCount: il metodo GetTypeInfoCount recupera il numero di interfacce di informazioni sul tipo fornite dall'oggetto."
ms.assetid: c98368f2-ae0c-4301-be30-7332b19f53ee
title: Metodo CMediaPosition.GetTypeInfoCount (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaPosition.GetTypeInfoCount
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8cfc54f414a6722f7f69a0330fad2d1a0cfab425
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095479"
---
# <a name="cmediapositiongettypeinfocount-method"></a><span data-ttu-id="366f1-103">Metodo CMediaPosition.GetTypeInfoCount</span><span class="sxs-lookup"><span data-stu-id="366f1-103">CMediaPosition.GetTypeInfoCount method</span></span>

<span data-ttu-id="366f1-104">Il `GetTypeInfoCount` metodo recupera il numero di interfacce di informazioni sul tipo fornite dall'oggetto.</span><span class="sxs-lookup"><span data-stu-id="366f1-104">The `GetTypeInfoCount` method retrieves the number of type information interfaces the object provides.</span></span>

## <a name="syntax"></a><span data-ttu-id="366f1-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="366f1-105">Syntax</span></span>


```C++
HRESULT GetTypeInfoCount(
   UINT *pctinfo
);
```



## <a name="parameters"></a><span data-ttu-id="366f1-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="366f1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="366f1-107">*pctinfo*</span><span class="sxs-lookup"><span data-stu-id="366f1-107">*pctinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="366f1-108">Puntatore a una variabile che riceve il numero di interfacce di informazioni sul tipo fornite dall'oggetto .</span><span class="sxs-lookup"><span data-stu-id="366f1-108">Pointer to a variable that receives the number of type-information interfaces provided by the object.</span></span> <span data-ttu-id="366f1-109">Quando il metodo viene restituito, il valore è 1.</span><span class="sxs-lookup"><span data-stu-id="366f1-109">When the method returns, the value is 1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="366f1-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="366f1-110">Return value</span></span>

<span data-ttu-id="366f1-111">Restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="366f1-111">Returns one of the following values.</span></span>



| <span data-ttu-id="366f1-112">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="366f1-112">Return code</span></span>                                                                               | <span data-ttu-id="366f1-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="366f1-113">Description</span></span>                           |
|-------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="366f1-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="366f1-114"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="366f1-115">Operazione completata.</span><span class="sxs-lookup"><span data-stu-id="366f1-115">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="366f1-116"><dt>**PUNTATORE E \_**</dt></span><span class="sxs-lookup"><span data-stu-id="366f1-116"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="366f1-117">Argomento del puntatore **NULL.**</span><span class="sxs-lookup"><span data-stu-id="366f1-117">**NULL** pointer argument.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="366f1-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="366f1-118">Requirements</span></span>



| <span data-ttu-id="366f1-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="366f1-119">Requirement</span></span> | <span data-ttu-id="366f1-120">Valore</span><span class="sxs-lookup"><span data-stu-id="366f1-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="366f1-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="366f1-121">Header</span></span><br/>  | <dl> <span data-ttu-id="366f1-122"><dt>Ctlutil.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="366f1-122"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="366f1-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="366f1-123">Library</span></span><br/> | <dl> <span data-ttu-id="366f1-124"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="366f1-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="366f1-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="366f1-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="366f1-126">**Classe CMediaPosition**</span><span class="sxs-lookup"><span data-stu-id="366f1-126">**CMediaPosition Class**</span></span>](cmediaposition.md)
</dt> </dl>

 

 




