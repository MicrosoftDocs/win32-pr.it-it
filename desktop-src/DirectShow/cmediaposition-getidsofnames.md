---
description: Il metodo GetIDsOfNames esegue il mapping di un set di nomi a un set di DISPID corrispondente.
ms.assetid: 4d3780ff-905f-4166-86d4-32395090b5cb
title: Metodo CMediaPosition. GetIDsOfNames (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaPosition.GetIDsOfNames
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dc2c7eee4304bb32ac1af2759bc2f094aca1d592
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332332"
---
# <a name="cmediapositiongetidsofnames-method"></a><span data-ttu-id="81dba-103">CMediaPosition. GetIDsOfNames, metodo</span><span class="sxs-lookup"><span data-stu-id="81dba-103">CMediaPosition.GetIDsOfNames method</span></span>

<span data-ttu-id="81dba-104">Il `GetIDsOfNames` metodo esegue il mapping di un set di nomi a un set di DISPID corrispondente.</span><span class="sxs-lookup"><span data-stu-id="81dba-104">The `GetIDsOfNames` method maps a set of names to a corresponding set of DISPIDs.</span></span>

## <a name="syntax"></a><span data-ttu-id="81dba-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="81dba-105">Syntax</span></span>


```C++
HRESULT GetIDsOfNames(
   REFIID  riid,
   OLECHAR **rgszNames,
   UINT    cNames,
   LCID    lcid,
   DISPID  *rgdispid
);
```



## <a name="parameters"></a><span data-ttu-id="81dba-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="81dba-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81dba-107">*riid*</span><span class="sxs-lookup"><span data-stu-id="81dba-107">*riid*</span></span> 
</dt> <dd>

<span data-ttu-id="81dba-108">Riservato.</span><span class="sxs-lookup"><span data-stu-id="81dba-108">Reserved.</span></span> <span data-ttu-id="81dba-109">Usare IID \_ null.</span><span class="sxs-lookup"><span data-stu-id="81dba-109">Use IID\_NULL.</span></span>

</dd> <dt>

<span data-ttu-id="81dba-110">*rgszNames*</span><span class="sxs-lookup"><span data-stu-id="81dba-110">*rgszNames*</span></span> 
</dt> <dd>

<span data-ttu-id="81dba-111">Indirizzo di una matrice di stringhe di caratteri wide che contengono i nomi di cui eseguire il mapping.</span><span class="sxs-lookup"><span data-stu-id="81dba-111">Address of an array of wide-character strings that contain the names to be mapped.</span></span>

</dd> <dt>

<span data-ttu-id="81dba-112">*CNAME*</span><span class="sxs-lookup"><span data-stu-id="81dba-112">*cNames*</span></span> 
</dt> <dd>

<span data-ttu-id="81dba-113">Dimensione della matrice specificata dal parametro *rgszNames* .</span><span class="sxs-lookup"><span data-stu-id="81dba-113">Size of the array given by the *rgszNames* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="81dba-114">*lcid*</span><span class="sxs-lookup"><span data-stu-id="81dba-114">*lcid*</span></span> 
</dt> <dd>

<span data-ttu-id="81dba-115">Contesto delle impostazioni locali in cui interpretare i nomi.</span><span class="sxs-lookup"><span data-stu-id="81dba-115">Locale context in which to interpret the names.</span></span> <span data-ttu-id="81dba-116">Può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="81dba-116">Can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="81dba-117">*rgdispid*</span><span class="sxs-lookup"><span data-stu-id="81dba-117">*rgdispid*</span></span> 
</dt> <dd>

<span data-ttu-id="81dba-118">Puntatore a una matrice che riceve i DISPID.</span><span class="sxs-lookup"><span data-stu-id="81dba-118">Pointer to an array that receives the DISPIDs.</span></span> <span data-ttu-id="81dba-119">Ogni elemento di riceve un identificatore che corrisponde a uno dei nomi passati nel parametro *rgszNames* .</span><span class="sxs-lookup"><span data-stu-id="81dba-119">Each element of receives an identifier that corresponds to one of the names passed in the *rgszNames* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81dba-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="81dba-120">Return value</span></span>

<span data-ttu-id="81dba-121">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="81dba-121">Returns an **HRESULT** value.</span></span> <span data-ttu-id="81dba-122">Di seguito sono indicati alcuni valori possibili.</span><span class="sxs-lookup"><span data-stu-id="81dba-122">Possible values include the following.</span></span>



| <span data-ttu-id="81dba-123">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="81dba-123">Return code</span></span>                                                                                         | <span data-ttu-id="81dba-124">Descrizione</span><span class="sxs-lookup"><span data-stu-id="81dba-124">Description</span></span>                                         |
|-----------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <span data-ttu-id="81dba-125"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="81dba-125"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="81dba-126">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="81dba-126">Success.</span></span><br/>                                 |
| <dl> <span data-ttu-id="81dba-127"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="81dba-127"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>       | <span data-ttu-id="81dba-128">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="81dba-128">Insufficient memory.</span></span><br/>                     |
| <dl> <span data-ttu-id="81dba-129"><dt>**DISP \_ E \_ unknowname**</dt></span><span class="sxs-lookup"><span data-stu-id="81dba-129"><dt>**DISP\_E\_UNKNOWNNAME**</dt></span></span> </dl> | <span data-ttu-id="81dba-130">Uno o più nomi non sono noti.</span><span class="sxs-lookup"><span data-stu-id="81dba-130">One or more of the names were not known.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="81dba-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="81dba-131">Requirements</span></span>



| <span data-ttu-id="81dba-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="81dba-132">Requirement</span></span> | <span data-ttu-id="81dba-133">Valore</span><span class="sxs-lookup"><span data-stu-id="81dba-133">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81dba-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="81dba-134">Header</span></span><br/>  | <dl> <span data-ttu-id="81dba-135"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="81dba-135"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="81dba-136">Libreria</span><span class="sxs-lookup"><span data-stu-id="81dba-136">Library</span></span><br/> | <dl> <span data-ttu-id="81dba-137"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="81dba-137"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81dba-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="81dba-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81dba-139">**Classe CMediaPosition**</span><span class="sxs-lookup"><span data-stu-id="81dba-139">**CMediaPosition Class**</span></span>](cmediaposition.md)
</dt> </dl>

 

 




