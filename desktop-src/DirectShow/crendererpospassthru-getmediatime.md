---
description: Il metodo GetMediaTime recupera i timestamp nell'esempio corrente.
ms.assetid: 13710373-04fd-4c1d-ba97-78be5cf27e7d
title: Metodo CRendererPosPassThru. GetMediaTime (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererPosPassThru.GetMediaTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 628c0f0c65dad4e00dd259edbeee97fd8f6f13ac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330205"
---
# <a name="crendererpospassthrugetmediatime-method"></a><span data-ttu-id="3e307-103">CRendererPosPassThru. GetMediaTime, metodo</span><span class="sxs-lookup"><span data-stu-id="3e307-103">CRendererPosPassThru.GetMediaTime method</span></span>

<span data-ttu-id="3e307-104">Il `GetMediaTime` metodo recupera i timestamp nell'esempio corrente.</span><span class="sxs-lookup"><span data-stu-id="3e307-104">The `GetMediaTime` method retrieves the time stamps on the current sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e307-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3e307-105">Syntax</span></span>


```C++
HRESULT GetMediaTime(
   LONGLONG *pStartTime,
   LONGLONG *pEndTime
);
```



## <a name="parameters"></a><span data-ttu-id="3e307-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3e307-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e307-107">*pStartTime*</span><span class="sxs-lookup"><span data-stu-id="3e307-107">*pStartTime*</span></span> 
</dt> <dd>

<span data-ttu-id="3e307-108">Puntatore a una variabile che riceve l'ora di inizio, in unità del formato dell'ora corrente.</span><span class="sxs-lookup"><span data-stu-id="3e307-108">Pointer to a variable that receives the start time, in units of the current time format.</span></span>

</dd> <dt>

<span data-ttu-id="3e307-109">*pEndTime*</span><span class="sxs-lookup"><span data-stu-id="3e307-109">*pEndTime*</span></span> 
</dt> <dd>

<span data-ttu-id="3e307-110">Puntatore a una variabile che riceve l'ora di fine, in unità del formato dell'ora corrente.</span><span class="sxs-lookup"><span data-stu-id="3e307-110">Pointer to a variable that receives the end time, in units of the current time format.</span></span> <span data-ttu-id="3e307-111">Può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="3e307-111">Can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e307-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3e307-112">Return value</span></span>

<span data-ttu-id="3e307-113">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3e307-113">Returns an **HRESULT** value.</span></span> <span data-ttu-id="3e307-114">I valori possibili includono quelli elencati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="3e307-114">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="3e307-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="3e307-115">Return code</span></span>                                                                                  | <span data-ttu-id="3e307-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3e307-116">Description</span></span>                                            |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <span data-ttu-id="3e307-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="3e307-117"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="3e307-118">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="3e307-118">Success.</span></span><br/>                                    |
| <dl> <span data-ttu-id="3e307-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="3e307-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="3e307-120">La conversione in questo formato non è supportata.</span><span class="sxs-lookup"><span data-stu-id="3e307-120">Conversion to this format is not supported.</span></span><br/> |
| <dl> <span data-ttu-id="3e307-121"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="3e307-121"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="3e307-122">Argomento puntatore **null** .</span><span class="sxs-lookup"><span data-stu-id="3e307-122">**NULL** pointer argument.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="3e307-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="3e307-123">Remarks</span></span>

<span data-ttu-id="3e307-124">Questo metodo esegue l'override del metodo [**CPosPassThru:: GetMediaTime**](cpospassthru-getmediatime.md) .</span><span class="sxs-lookup"><span data-stu-id="3e307-124">This method overrides the [**CPosPassThru::GetMediaTime**](cpospassthru-getmediatime.md) method.</span></span> <span data-ttu-id="3e307-125">I valori dell'indicatore di data e ora vengono convertiti nel formato di ora corrente chiamando il metodo [**CPosPassThru:: ConvertTimeFormat**](cpospassthru-converttimeformat.md) .</span><span class="sxs-lookup"><span data-stu-id="3e307-125">The time-stamp values are converted to the current time format by calling the [**CPosPassThru::ConvertTimeFormat**](cpospassthru-converttimeformat.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e307-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3e307-126">Requirements</span></span>



| <span data-ttu-id="3e307-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e307-127">Requirement</span></span> | <span data-ttu-id="3e307-128">Valore</span><span class="sxs-lookup"><span data-stu-id="3e307-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e307-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3e307-129">Header</span></span><br/>  | <dl> <span data-ttu-id="3e307-130"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3e307-130"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="3e307-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="3e307-131">Library</span></span><br/> | <dl> <span data-ttu-id="3e307-132"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="3e307-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




