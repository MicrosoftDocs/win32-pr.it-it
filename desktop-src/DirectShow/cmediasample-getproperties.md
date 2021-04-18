---
description: "Il metodo GetProperties recupera le proprietà dell'esempio. Questo metodo implementa il metodo IMediaSample2:: GetProperties."
ms.assetid: c2a6d611-9c17-41fb-bb6d-f5b17f1c9966
title: Metodo CMediaSample. GetProperties (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.GetProperties
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 06ee1022f298e2f5167d348777b33fc2f1703eef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324963"
---
# <a name="cmediasamplegetproperties-method"></a><span data-ttu-id="2451b-104">Metodo CMediaSample. GetProperties</span><span class="sxs-lookup"><span data-stu-id="2451b-104">CMediaSample.GetProperties method</span></span>

<span data-ttu-id="2451b-105">Il `GetProperties` metodo recupera le proprietà dell'esempio.</span><span class="sxs-lookup"><span data-stu-id="2451b-105">The `GetProperties` method retrieves the properties of the sample.</span></span> <span data-ttu-id="2451b-106">Questo metodo implementa il metodo [**IMediaSample2:: GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-getproperties) .</span><span class="sxs-lookup"><span data-stu-id="2451b-106">This method implements the [**IMediaSample2::GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-getproperties) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="2451b-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2451b-107">Syntax</span></span>


```C++
HRESULT GetProperties(
   DWORD cbProperties,
   BYTE  *pbProperties
);
```



## <a name="parameters"></a><span data-ttu-id="2451b-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="2451b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2451b-109">*cbProperties*</span><span class="sxs-lookup"><span data-stu-id="2451b-109">*cbProperties*</span></span> 
</dt> <dd>

<span data-ttu-id="2451b-110">Lunghezza dei dati della proprietà da recuperare, in byte.</span><span class="sxs-lookup"><span data-stu-id="2451b-110">Length of property data to retrieve, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="2451b-111">*pbProperties*</span><span class="sxs-lookup"><span data-stu-id="2451b-111">*pbProperties*</span></span> 
</dt> <dd>

<span data-ttu-id="2451b-112">Puntatore a un buffer di dimensioni *cbProperties*.</span><span class="sxs-lookup"><span data-stu-id="2451b-112">Pointer to a buffer of size *cbProperties*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2451b-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2451b-113">Return value</span></span>

<span data-ttu-id="2451b-114">Restituisce uno dei valori **HRESULT** indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="2451b-114">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="2451b-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="2451b-115">Return code</span></span>                                                                               | <span data-ttu-id="2451b-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2451b-116">Description</span></span>                           |
|-------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="2451b-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="2451b-117"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="2451b-118">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="2451b-118">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="2451b-119"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="2451b-119"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="2451b-120">Argomento puntatore **null** .</span><span class="sxs-lookup"><span data-stu-id="2451b-120">**NULL** pointer argument.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="2451b-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2451b-121">Requirements</span></span>



| <span data-ttu-id="2451b-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="2451b-122">Requirement</span></span> | <span data-ttu-id="2451b-123">Valore</span><span class="sxs-lookup"><span data-stu-id="2451b-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2451b-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2451b-124">Header</span></span><br/>  | <dl> <span data-ttu-id="2451b-125"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2451b-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="2451b-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="2451b-126">Library</span></span><br/> | <dl> <span data-ttu-id="2451b-127"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="2451b-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2451b-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2451b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2451b-129">**Classe CMediaSample**</span><span class="sxs-lookup"><span data-stu-id="2451b-129">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




