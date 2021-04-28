---
description: "Metodo CBaseDispatch.GetTypeInfoCount: il metodo GetTypeInfoCount recupera il numero di interfacce di informazioni sul tipo fornite dall'oggetto."
ms.assetid: e09e6f6c-6ac8-4ce1-8ce1-ee5374d54183
title: Metodo CBaseDispatch.GetTypeInfoCount (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseDispatch.GetTypeInfoCount
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 81e68c94420b3d7715845f8d6bd14e26b770b44f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099889"
---
# <a name="cbasedispatchgettypeinfocount-method"></a><span data-ttu-id="8ae27-103">Metodo CBaseDispatch.GetTypeInfoCount</span><span class="sxs-lookup"><span data-stu-id="8ae27-103">CBaseDispatch.GetTypeInfoCount method</span></span>

<span data-ttu-id="8ae27-104">Il `GetTypeInfoCount` metodo recupera il numero di interfacce di informazioni sul tipo fornite dall'oggetto.</span><span class="sxs-lookup"><span data-stu-id="8ae27-104">The `GetTypeInfoCount` method retrieves the number of type information interfaces the object provides.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ae27-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8ae27-105">Syntax</span></span>


```C++
HRESULT GetTypeInfoCount(
   UINT *pctinfo
);
```



## <a name="parameters"></a><span data-ttu-id="8ae27-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8ae27-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ae27-107">*pctinfo*</span><span class="sxs-lookup"><span data-stu-id="8ae27-107">*pctinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="8ae27-108">Puntatore a una variabile che riceve il numero di interfacce di informazioni sul tipo fornite dall'oggetto .</span><span class="sxs-lookup"><span data-stu-id="8ae27-108">Pointer to a variable that receives the number of type-information interfaces provided by the object.</span></span> <span data-ttu-id="8ae27-109">Quando il metodo viene restituito, il valore è 1.</span><span class="sxs-lookup"><span data-stu-id="8ae27-109">When the method returns, the value is 1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ae27-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8ae27-110">Return value</span></span>

<span data-ttu-id="8ae27-111">Restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="8ae27-111">Returns one of the following values.</span></span>



| <span data-ttu-id="8ae27-112">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="8ae27-112">Return code</span></span>                                                                               | <span data-ttu-id="8ae27-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8ae27-113">Description</span></span>                           |
|-------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="8ae27-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8ae27-114"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="8ae27-115">Operazione completata.</span><span class="sxs-lookup"><span data-stu-id="8ae27-115">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="8ae27-116"><dt>**PUNTATORE \_ E**</dt></span><span class="sxs-lookup"><span data-stu-id="8ae27-116"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="8ae27-117">Argomento del puntatore **NULL.**</span><span class="sxs-lookup"><span data-stu-id="8ae27-117">**NULL** pointer argument.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="8ae27-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8ae27-118">Requirements</span></span>



| <span data-ttu-id="8ae27-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="8ae27-119">Requirement</span></span> | <span data-ttu-id="8ae27-120">Valore</span><span class="sxs-lookup"><span data-stu-id="8ae27-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ae27-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8ae27-121">Header</span></span><br/>  | <dl> <span data-ttu-id="8ae27-122"><dt>Ctlutil.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="8ae27-122"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="8ae27-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="8ae27-123">Library</span></span><br/> | <dl> <span data-ttu-id="8ae27-124"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="8ae27-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ae27-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8ae27-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ae27-126">**Classe CBaseDispatch**</span><span class="sxs-lookup"><span data-stu-id="8ae27-126">**CBaseDispatch Class**</span></span>](cbasedispatch.md)
</dt> </dl>

 

 




