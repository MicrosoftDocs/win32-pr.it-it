---
description: Il metodo CheckMediaType determina se un tipo di supporto proposto è compatibile con il formato di visualizzazione.
ms.assetid: 567663cf-c79f-4549-9fa9-b16da957d2b1
title: Metodo CImageDisplay. CheckMediaType (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a8ebcdbe6bbfe6538a2ea166be0816f31954c7d2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325323"
---
# <a name="cimagedisplaycheckmediatype-method"></a><span data-ttu-id="8d523-103">CImageDisplay. CheckMediaType, metodo</span><span class="sxs-lookup"><span data-stu-id="8d523-103">CImageDisplay.CheckMediaType method</span></span>

<span data-ttu-id="8d523-104">Il `CheckMediaType` metodo determina se un tipo di supporto proposto è compatibile con il formato di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="8d523-104">The `CheckMediaType` method determines whether a proposed media type is compatible with the display format.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d523-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8d523-105">Syntax</span></span>


```C++
HRESULT CheckMediaType(
   const CMediaType *pmtIn
);
```



## <a name="parameters"></a><span data-ttu-id="8d523-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8d523-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d523-107">*pmtIn*</span><span class="sxs-lookup"><span data-stu-id="8d523-107">*pmtIn*</span></span> 
</dt> <dd>

<span data-ttu-id="8d523-108">Puntatore a un oggetto [**CMediaType**](cmediatype.md) che contiene il tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="8d523-108">Pointer to a [**CMediaType**](cmediatype.md) object that contains the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d523-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8d523-109">Return value</span></span>

<span data-ttu-id="8d523-110">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8d523-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="8d523-111">Di seguito sono indicati alcuni valori possibili.</span><span class="sxs-lookup"><span data-stu-id="8d523-111">Possible values include the following.</span></span>



| <span data-ttu-id="8d523-112">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="8d523-112">Return code</span></span>                                                                                  | <span data-ttu-id="8d523-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8d523-113">Description</span></span>                              |
|----------------------------------------------------------------------------------------------|------------------------------------------|
| <dl> <span data-ttu-id="8d523-114"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="8d523-114"><dt>**E\_FAIL**</dt></span></span> </dl>       | <span data-ttu-id="8d523-115">Tipo di supporto non valido.</span><span class="sxs-lookup"><span data-stu-id="8d523-115">Invalid media type.</span></span><br/>           |
| <dl> <span data-ttu-id="8d523-116"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="8d523-116"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="8d523-117">Tipo di supporto non valido.</span><span class="sxs-lookup"><span data-stu-id="8d523-117">Invalid media type.</span></span><br/>           |
| <dl> <span data-ttu-id="8d523-118"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8d523-118"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="8d523-119">Il tipo di supporto è compatibile.</span><span class="sxs-lookup"><span data-stu-id="8d523-119">The media type is compatible.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="8d523-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8d523-120">Requirements</span></span>



| <span data-ttu-id="8d523-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="8d523-121">Requirement</span></span> | <span data-ttu-id="8d523-122">Valore</span><span class="sxs-lookup"><span data-stu-id="8d523-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d523-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8d523-123">Header</span></span><br/>  | <dl> <span data-ttu-id="8d523-124"><dt>WinUtil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8d523-124"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="8d523-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="8d523-125">Library</span></span><br/> | <dl> <span data-ttu-id="8d523-126"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="8d523-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d523-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8d523-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d523-128">**Classe CImageDisplay**</span><span class="sxs-lookup"><span data-stu-id="8d523-128">**CImageDisplay Class**</span></span>](cimagedisplay.md)
</dt> </dl>

 

 




