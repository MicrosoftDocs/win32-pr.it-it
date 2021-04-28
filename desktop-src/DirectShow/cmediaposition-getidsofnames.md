---
description: 'Metodo CMediaPosition.GetIDsOfNames: il metodo GetIDsOfNames esegue il mapping di un set di nomi a un set corrispondente di DISPID.'
ms.assetid: 4d3780ff-905f-4166-86d4-32395090b5cb
title: Metodo CMediaPosition.GetIDsOfNames (Ctlutil.h)
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
ms.openlocfilehash: 26a348e58fa84aa4134ce9f2ea756874b9ce2724
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095529"
---
# <a name="cmediapositiongetidsofnames-method"></a><span data-ttu-id="87aed-103">Metodo CMediaPosition.GetIDsOfNames</span><span class="sxs-lookup"><span data-stu-id="87aed-103">CMediaPosition.GetIDsOfNames method</span></span>

<span data-ttu-id="87aed-104">Il `GetIDsOfNames` metodo esegue il mapping di un set di nomi a un set corrispondente di DISPID.</span><span class="sxs-lookup"><span data-stu-id="87aed-104">The `GetIDsOfNames` method maps a set of names to a corresponding set of DISPIDs.</span></span>

## <a name="syntax"></a><span data-ttu-id="87aed-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="87aed-105">Syntax</span></span>


```C++
HRESULT GetIDsOfNames(
   REFIID  riid,
   OLECHAR **rgszNames,
   UINT    cNames,
   LCID    lcid,
   DISPID  *rgdispid
);
```



## <a name="parameters"></a><span data-ttu-id="87aed-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="87aed-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87aed-107">*Riid*</span><span class="sxs-lookup"><span data-stu-id="87aed-107">*riid*</span></span> 
</dt> <dd>

<span data-ttu-id="87aed-108">Riservato.</span><span class="sxs-lookup"><span data-stu-id="87aed-108">Reserved.</span></span> <span data-ttu-id="87aed-109">Usare IID \_ NULL.</span><span class="sxs-lookup"><span data-stu-id="87aed-109">Use IID\_NULL.</span></span>

</dd> <dt>

<span data-ttu-id="87aed-110">*rgszNames*</span><span class="sxs-lookup"><span data-stu-id="87aed-110">*rgszNames*</span></span> 
</dt> <dd>

<span data-ttu-id="87aed-111">Indirizzo di una matrice di stringhe di caratteri wide che contengono i nomi di cui eseguire il mapping.</span><span class="sxs-lookup"><span data-stu-id="87aed-111">Address of an array of wide-character strings that contain the names to be mapped.</span></span>

</dd> <dt>

<span data-ttu-id="87aed-112">*cNames*</span><span class="sxs-lookup"><span data-stu-id="87aed-112">*cNames*</span></span> 
</dt> <dd>

<span data-ttu-id="87aed-113">Dimensione della matrice specificata dal *parametro rgszNames.*</span><span class="sxs-lookup"><span data-stu-id="87aed-113">Size of the array given by the *rgszNames* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="87aed-114">*lcid*</span><span class="sxs-lookup"><span data-stu-id="87aed-114">*lcid*</span></span> 
</dt> <dd>

<span data-ttu-id="87aed-115">Contesto delle impostazioni locali in cui interpretare i nomi.</span><span class="sxs-lookup"><span data-stu-id="87aed-115">Locale context in which to interpret the names.</span></span> <span data-ttu-id="87aed-116">Può essere **NULL.**</span><span class="sxs-lookup"><span data-stu-id="87aed-116">Can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="87aed-117">*rgdispid*</span><span class="sxs-lookup"><span data-stu-id="87aed-117">*rgdispid*</span></span> 
</dt> <dd>

<span data-ttu-id="87aed-118">Puntatore a una matrice che riceve i DISPID.</span><span class="sxs-lookup"><span data-stu-id="87aed-118">Pointer to an array that receives the DISPIDs.</span></span> <span data-ttu-id="87aed-119">Ogni elemento di riceve un identificatore che corrisponde a uno dei nomi passati nel *parametro rgszNames.*</span><span class="sxs-lookup"><span data-stu-id="87aed-119">Each element of receives an identifier that corresponds to one of the names passed in the *rgszNames* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87aed-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="87aed-120">Return value</span></span>

<span data-ttu-id="87aed-121">Restituisce un **valore HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="87aed-121">Returns an **HRESULT** value.</span></span> <span data-ttu-id="87aed-122">Di seguito sono indicati alcuni valori possibili.</span><span class="sxs-lookup"><span data-stu-id="87aed-122">Possible values include the following.</span></span>



| <span data-ttu-id="87aed-123">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="87aed-123">Return code</span></span>                                                                                         | <span data-ttu-id="87aed-124">Descrizione</span><span class="sxs-lookup"><span data-stu-id="87aed-124">Description</span></span>                                         |
|-----------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <span data-ttu-id="87aed-125"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="87aed-125"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="87aed-126">Operazione completata.</span><span class="sxs-lookup"><span data-stu-id="87aed-126">Success.</span></span><br/>                                 |
| <dl> <span data-ttu-id="87aed-127"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="87aed-127"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>       | <span data-ttu-id="87aed-128">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="87aed-128">Insufficient memory.</span></span><br/>                     |
| <dl> <span data-ttu-id="87aed-129"><dt>**DISP \_ E \_ UNKNOWNNAME**</dt></span><span class="sxs-lookup"><span data-stu-id="87aed-129"><dt>**DISP\_E\_UNKNOWNNAME**</dt></span></span> </dl> | <span data-ttu-id="87aed-130">Uno o più nomi non erano noti.</span><span class="sxs-lookup"><span data-stu-id="87aed-130">One or more of the names were not known.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="87aed-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="87aed-131">Requirements</span></span>



| <span data-ttu-id="87aed-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="87aed-132">Requirement</span></span> | <span data-ttu-id="87aed-133">Valore</span><span class="sxs-lookup"><span data-stu-id="87aed-133">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87aed-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="87aed-134">Header</span></span><br/>  | <dl> <span data-ttu-id="87aed-135"><dt>Ctlutil.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="87aed-135"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="87aed-136">Libreria</span><span class="sxs-lookup"><span data-stu-id="87aed-136">Library</span></span><br/> | <dl> <span data-ttu-id="87aed-137"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="87aed-137"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87aed-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="87aed-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87aed-139">**Classe CMediaPosition**</span><span class="sxs-lookup"><span data-stu-id="87aed-139">**CMediaPosition Class**</span></span>](cmediaposition.md)
</dt> </dl>

 

 




