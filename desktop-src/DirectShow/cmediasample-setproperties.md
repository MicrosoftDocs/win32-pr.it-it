---
description: "Il metodo seproperties imposta le proprietà dell'esempio. Questo metodo implementa il metodo IMediaSample2:: SetValue."
ms.assetid: 639aedf5-0c21-4578-b336-91859e40f3be
title: Metodo CMediaSample. seproperties (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetProperties
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c5e6ef3c3839825586bf47259cf44783d167f503
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324924"
---
# <a name="cmediasamplesetproperties-method"></a><span data-ttu-id="226b7-104">Metodo CMediaSample. seproperties</span><span class="sxs-lookup"><span data-stu-id="226b7-104">CMediaSample.SetProperties method</span></span>

<span data-ttu-id="226b7-105">Il `SetProperties` metodo imposta le proprietà dell'esempio.</span><span class="sxs-lookup"><span data-stu-id="226b7-105">The `SetProperties` method sets the properties of the sample.</span></span> <span data-ttu-id="226b7-106">Questo metodo implementa il metodo [**IMediaSample2::**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-setproperties) SetValue.</span><span class="sxs-lookup"><span data-stu-id="226b7-106">This method implements the [**IMediaSample2::SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-setproperties) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="226b7-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="226b7-107">Syntax</span></span>


```C++
HRESULT SetProperties(
         DWORD cbProperties,
   const BYTE  *pbProperties
);
```



## <a name="parameters"></a><span data-ttu-id="226b7-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="226b7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="226b7-109">*cbProperties*</span><span class="sxs-lookup"><span data-stu-id="226b7-109">*cbProperties*</span></span> 
</dt> <dd>

<span data-ttu-id="226b7-110">Lunghezza dei dati della proprietà da impostare, in byte.</span><span class="sxs-lookup"><span data-stu-id="226b7-110">Length of property data to set, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="226b7-111">*pbProperties*</span><span class="sxs-lookup"><span data-stu-id="226b7-111">*pbProperties*</span></span> 
</dt> <dd>

<span data-ttu-id="226b7-112">Puntatore a un buffer di dimensioni *cbProperties*.</span><span class="sxs-lookup"><span data-stu-id="226b7-112">Pointer to a buffer of size *cbProperties*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="226b7-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="226b7-113">Return value</span></span>

<span data-ttu-id="226b7-114">Restituisce uno dei valori **HRESULT** indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="226b7-114">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="226b7-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="226b7-115">Return code</span></span>                                                                                   | <span data-ttu-id="226b7-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="226b7-116">Description</span></span>                          |
|-----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <span data-ttu-id="226b7-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="226b7-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="226b7-118">Operazione riuscita</span><span class="sxs-lookup"><span data-stu-id="226b7-118">Success</span></span><br/>                   |
| <dl> <span data-ttu-id="226b7-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="226b7-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="226b7-120">Argomento non valido</span><span class="sxs-lookup"><span data-stu-id="226b7-120">Invalid argument</span></span><br/>          |
| <dl> <span data-ttu-id="226b7-121"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="226b7-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="226b7-122">Memoria insufficiente</span><span class="sxs-lookup"><span data-stu-id="226b7-122">Insufficient memory</span></span><br/>       |
| <dl> <span data-ttu-id="226b7-123"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="226b7-123"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="226b7-124">Argomento puntatore **null**</span><span class="sxs-lookup"><span data-stu-id="226b7-124">**NULL** pointer argument</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="226b7-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="226b7-125">Requirements</span></span>



| <span data-ttu-id="226b7-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="226b7-126">Requirement</span></span> | <span data-ttu-id="226b7-127">Valore</span><span class="sxs-lookup"><span data-stu-id="226b7-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="226b7-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="226b7-128">Header</span></span><br/>  | <dl> <span data-ttu-id="226b7-129"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="226b7-129"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="226b7-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="226b7-130">Library</span></span><br/> | <dl> <span data-ttu-id="226b7-131"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="226b7-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="226b7-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="226b7-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="226b7-133">**Classe CMediaSample**</span><span class="sxs-lookup"><span data-stu-id="226b7-133">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




