---
description: "Metodo CRendererPosPassThru.GetMediaTime: il metodo GetMediaTime recupera i timestamp nell'esempio corrente."
ms.assetid: 13710373-04fd-4c1d-ba97-78be5cf27e7d
title: Metodo CRendererPosPassThru.GetMediaTime (Ctlutil.h)
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
ms.openlocfilehash: 588c92faec6b68cfa51392d4df00567c4e881460
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085369"
---
# <a name="crendererpospassthrugetmediatime-method"></a><span data-ttu-id="0d38f-103">Metodo CRendererPosPassThru.GetMediaTime</span><span class="sxs-lookup"><span data-stu-id="0d38f-103">CRendererPosPassThru.GetMediaTime method</span></span>

<span data-ttu-id="0d38f-104">Il `GetMediaTime` metodo recupera i timestamp nell'esempio corrente.</span><span class="sxs-lookup"><span data-stu-id="0d38f-104">The `GetMediaTime` method retrieves the time stamps on the current sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d38f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0d38f-105">Syntax</span></span>


```C++
HRESULT GetMediaTime(
   LONGLONG *pStartTime,
   LONGLONG *pEndTime
);
```



## <a name="parameters"></a><span data-ttu-id="0d38f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="0d38f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d38f-107">*pStartTime*</span><span class="sxs-lookup"><span data-stu-id="0d38f-107">*pStartTime*</span></span> 
</dt> <dd>

<span data-ttu-id="0d38f-108">Puntatore a una variabile che riceve l'ora di inizio, in unità del formato di ora corrente.</span><span class="sxs-lookup"><span data-stu-id="0d38f-108">Pointer to a variable that receives the start time, in units of the current time format.</span></span>

</dd> <dt>

<span data-ttu-id="0d38f-109">*pEndTime*</span><span class="sxs-lookup"><span data-stu-id="0d38f-109">*pEndTime*</span></span> 
</dt> <dd>

<span data-ttu-id="0d38f-110">Puntatore a una variabile che riceve l'ora di fine, in unità del formato di ora corrente.</span><span class="sxs-lookup"><span data-stu-id="0d38f-110">Pointer to a variable that receives the end time, in units of the current time format.</span></span> <span data-ttu-id="0d38f-111">Può essere **NULL.**</span><span class="sxs-lookup"><span data-stu-id="0d38f-111">Can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d38f-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0d38f-112">Return value</span></span>

<span data-ttu-id="0d38f-113">Restituisce un **valore HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="0d38f-113">Returns an **HRESULT** value.</span></span> <span data-ttu-id="0d38f-114">I valori possibili includono quelli elencati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="0d38f-114">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="0d38f-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="0d38f-115">Return code</span></span>                                                                                  | <span data-ttu-id="0d38f-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0d38f-116">Description</span></span>                                            |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <span data-ttu-id="0d38f-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0d38f-117"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="0d38f-118">Operazione completata.</span><span class="sxs-lookup"><span data-stu-id="0d38f-118">Success.</span></span><br/>                                    |
| <dl> <span data-ttu-id="0d38f-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="0d38f-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="0d38f-120">La conversione in questo formato non è supportata.</span><span class="sxs-lookup"><span data-stu-id="0d38f-120">Conversion to this format is not supported.</span></span><br/> |
| <dl> <span data-ttu-id="0d38f-121"><dt>**PUNTATORE \_ E**</dt></span><span class="sxs-lookup"><span data-stu-id="0d38f-121"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="0d38f-122">Argomento del puntatore **NULL.**</span><span class="sxs-lookup"><span data-stu-id="0d38f-122">**NULL** pointer argument.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="0d38f-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="0d38f-123">Remarks</span></span>

<span data-ttu-id="0d38f-124">Questo metodo esegue l'override [**del metodo CPosPassThru::GetMediaTime.**](cpospassthru-getmediatime.md)</span><span class="sxs-lookup"><span data-stu-id="0d38f-124">This method overrides the [**CPosPassThru::GetMediaTime**](cpospassthru-getmediatime.md) method.</span></span> <span data-ttu-id="0d38f-125">I valori del timestamp vengono convertiti nel formato di ora corrente chiamando il [**metodo CPosPassThru::ConvertTimeFormat.**](cpospassthru-converttimeformat.md)</span><span class="sxs-lookup"><span data-stu-id="0d38f-125">The time-stamp values are converted to the current time format by calling the [**CPosPassThru::ConvertTimeFormat**](cpospassthru-converttimeformat.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d38f-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0d38f-126">Requirements</span></span>



| <span data-ttu-id="0d38f-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d38f-127">Requirement</span></span> | <span data-ttu-id="0d38f-128">Valore</span><span class="sxs-lookup"><span data-stu-id="0d38f-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d38f-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0d38f-129">Header</span></span><br/>  | <dl> <span data-ttu-id="0d38f-130"><dt>Ctlutil.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="0d38f-130"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="0d38f-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="0d38f-131">Library</span></span><br/> | <dl> <span data-ttu-id="0d38f-132"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="0d38f-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




