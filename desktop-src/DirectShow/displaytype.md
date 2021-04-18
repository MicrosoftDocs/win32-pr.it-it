---
description: La funzione DisplayType invia informazioni su un tipo di supporto al percorso di output di debug. Ignorato nelle compilazioni al dettaglio.
ms.assetid: 63a88508-dff8-4869-97e5-0f75f4a9dca0
title: Funzione DisplayType (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DisplayType
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4f3d83bbe7a24463fc4cfaed4ace3adec9d6fcf7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328478"
---
# <a name="displaytype-function"></a><span data-ttu-id="1dd14-104">DisplayType (funzione)</span><span class="sxs-lookup"><span data-stu-id="1dd14-104">DisplayType function</span></span>

<span data-ttu-id="1dd14-105">La `DisplayType` funzione Invia informazioni su un tipo di supporto al percorso di output di debug.</span><span class="sxs-lookup"><span data-stu-id="1dd14-105">The `DisplayType` function sends information about a media type to the debug output location.</span></span> <span data-ttu-id="1dd14-106">Ignorato nelle compilazioni al dettaglio.</span><span class="sxs-lookup"><span data-stu-id="1dd14-106">Ignored in retail builds.</span></span>

## <a name="syntax"></a><span data-ttu-id="1dd14-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1dd14-107">Syntax</span></span>


```C++
void DisplayType(
         LPTSTR        label,
   const AM_MEDIA_TYPE *pmtIn
);
```



## <a name="parameters"></a><span data-ttu-id="1dd14-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="1dd14-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1dd14-109">*label*</span><span class="sxs-lookup"><span data-stu-id="1dd14-109">*label*</span></span> 
</dt> <dd>

<span data-ttu-id="1dd14-110">Stringa contenente un messaggio da visualizzare con le informazioni sul tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="1dd14-110">String that contains a message to display with the media type information.</span></span>

</dd> <dt>

<span data-ttu-id="1dd14-111">*pmtIn*</span><span class="sxs-lookup"><span data-stu-id="1dd14-111">*pmtIn*</span></span> 
</dt> <dd>

<span data-ttu-id="1dd14-112">ointer alla struttura [**del \_ \_ tipo di supporto am**](/windows/win32/api/strmif/ns-strmif-am_media_type) che contiene il tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="1dd14-112">ointer to the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure that contains the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1dd14-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1dd14-113">Return value</span></span>

<span data-ttu-id="1dd14-114">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="1dd14-114">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1dd14-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="1dd14-115">Remarks</span></span>

<span data-ttu-id="1dd14-116">Questa funzione genera diversi messaggi di traccia del LOG \_ .</span><span class="sxs-lookup"><span data-stu-id="1dd14-116">This function generates several LOG\_TRACE messages.</span></span> <span data-ttu-id="1dd14-117">Al livello di registrazione 2 o superiore, la funzione Visualizza il tipo principale, il sottotipo e il tipo di formato e i dati del blocco di formato.</span><span class="sxs-lookup"><span data-stu-id="1dd14-117">At logging level 2 or higher, the function displays the major type, subtype, and format type, and data from the format block.</span></span> <span data-ttu-id="1dd14-118">Al livello di registrazione 5 o superiore, la funzione Visualizza informazioni aggiuntive, ad esempio i rettangoli di origine e di destinazione per i tipi di video.</span><span class="sxs-lookup"><span data-stu-id="1dd14-118">At logging level 5 or higher, the function displays additional information, such as the source and target rectangles for video types.</span></span>

## <a name="requirements"></a><span data-ttu-id="1dd14-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1dd14-119">Requirements</span></span>



| <span data-ttu-id="1dd14-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="1dd14-120">Requirement</span></span> | <span data-ttu-id="1dd14-121">Valore</span><span class="sxs-lookup"><span data-stu-id="1dd14-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1dd14-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1dd14-122">Header</span></span><br/>  | <dl> <span data-ttu-id="1dd14-123"><dt>Wxdebug. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1dd14-123"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1dd14-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="1dd14-124">Library</span></span><br/> | <dl> <span data-ttu-id="1dd14-125"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="1dd14-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1dd14-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1dd14-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1dd14-127">Funzioni di output di debug</span><span class="sxs-lookup"><span data-stu-id="1dd14-127">Debug Output Functions</span></span>](debug-output-functions.md)
</dt> </dl>

 

 




