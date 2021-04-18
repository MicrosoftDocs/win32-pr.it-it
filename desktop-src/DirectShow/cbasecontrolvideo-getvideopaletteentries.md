---
description: Il metodo GetVideoPaletteEntries recupera un intervallo di voci della tavolozza per il video.
ms.assetid: 7ac12e28-daa7-4d6c-9983-401971e6704d
title: Metodo CBaseControlVideo. GetVideoPaletteEntries (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetVideoPaletteEntries
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6fa354922e57436c0d9e3e18924dcf31afe1629e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332083"
---
# <a name="cbasecontrolvideogetvideopaletteentries-method"></a><span data-ttu-id="fd979-103">CBaseControlVideo. GetVideoPaletteEntries, metodo</span><span class="sxs-lookup"><span data-stu-id="fd979-103">CBaseControlVideo.GetVideoPaletteEntries method</span></span>

<span data-ttu-id="fd979-104">Il `GetVideoPaletteEntries` metodo recupera un intervallo di voci della tavolozza per il video.</span><span class="sxs-lookup"><span data-stu-id="fd979-104">The `GetVideoPaletteEntries` method retrieves a range of palette entries for the video.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd979-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fd979-105">Syntax</span></span>


```C++
HRESULT GetVideoPaletteEntries(
   long StartIndex,
   long Entries,
   long *pRetrieved,
   long *pPalette
);
```



## <a name="parameters"></a><span data-ttu-id="fd979-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="fd979-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd979-107">*StartIndex*</span><span class="sxs-lookup"><span data-stu-id="fd979-107">*StartIndex*</span></span> 
</dt> <dd>

<span data-ttu-id="fd979-108">Voce della tavolozza iniziale in base zero.</span><span class="sxs-lookup"><span data-stu-id="fd979-108">Zero-based start palette entry.</span></span>

</dd> <dt>

<span data-ttu-id="fd979-109">*Voci*</span><span class="sxs-lookup"><span data-stu-id="fd979-109">*Entries*</span></span> 
</dt> <dd>

<span data-ttu-id="fd979-110">Numero di voci richieste.</span><span class="sxs-lookup"><span data-stu-id="fd979-110">Number of entries required.</span></span>

</dd> <dt>

<span data-ttu-id="fd979-111">*pRetrieved*</span><span class="sxs-lookup"><span data-stu-id="fd979-111">*pRetrieved*</span></span> 
</dt> <dd>

<span data-ttu-id="fd979-112">Puntatore al numero di colori ottenuti.</span><span class="sxs-lookup"><span data-stu-id="fd979-112">Pointer to the number of colors obtained.</span></span>

</dd> <dt>

<span data-ttu-id="fd979-113">*pPalette*</span><span class="sxs-lookup"><span data-stu-id="fd979-113">*pPalette*</span></span> 
</dt> <dd>

<span data-ttu-id="fd979-114">Puntatore al buffer di output per i colori.</span><span class="sxs-lookup"><span data-stu-id="fd979-114">Pointer to output buffer for colors.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd979-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fd979-115">Return value</span></span>

<span data-ttu-id="fd979-116">Restituisce NOERROR se ha esito positivo, VFW \_ E \_ Nessuna \_ tavolozza \_ disponibile se gli esempi video non hanno tavolozza colori, e \_ OutOfMemory se la memoria disponibile non è sufficiente, e \_ INVALIDARG se *startIndex* non è valido oppure S \_ false se non sono presenti colori nella tavolozza.</span><span class="sxs-lookup"><span data-stu-id="fd979-116">Returns NOERROR if successful, VFW\_E\_NO\_PALETTE\_AVAILABLE if the video samples has no color palette, E\_OUTOFMEMORY if there is not enough memory available, E\_INVALIDARG if *StartIndex* is invalid, or S\_FALSE if there are no colors in the palette.</span></span>

## <a name="remarks"></a><span data-ttu-id="fd979-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="fd979-117">Remarks</span></span>

<span data-ttu-id="fd979-118">Questa funzione membro restituisce la tavolozza corrente del video come matrice allocata dall'utente.</span><span class="sxs-lookup"><span data-stu-id="fd979-118">This member function returns the current palette of the video as an array allocated by the user.</span></span> <span data-ttu-id="fd979-119">Per rimanere coerenti, usare i membri della struttura Win32 **PaletteEntry** per restituire i colori, anziché i membri nella struttura **RGBQUAD** (anche se il parametro è **Long**).</span><span class="sxs-lookup"><span data-stu-id="fd979-119">To remain consistent, use the members in the Win32 **PALETTEENTRY** structure to return the colors, rather than the members in the **RGBQUAD** structure (although the parameter is a **LONG**).</span></span> <span data-ttu-id="fd979-120">La memoria viene allocata dal chiamante, quindi è sufficiente copiarla a turno.</span><span class="sxs-lookup"><span data-stu-id="fd979-120">The memory is allocated by the caller, so simply copy each in turn.</span></span> <span data-ttu-id="fd979-121">Determinare se il numero di voci richieste e l'offset della posizione iniziale sono entrambi validi.</span><span class="sxs-lookup"><span data-stu-id="fd979-121">Determine that the number of entries requested and the start position offset are both valid.</span></span> <span data-ttu-id="fd979-122">Se il numero di voci restituisce zero, restituire un \_ codice S false.</span><span class="sxs-lookup"><span data-stu-id="fd979-122">If the number of entries evaluates to zero, return an S\_FALSE code.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd979-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fd979-123">Requirements</span></span>



| <span data-ttu-id="fd979-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="fd979-124">Requirement</span></span> | <span data-ttu-id="fd979-125">Valore</span><span class="sxs-lookup"><span data-stu-id="fd979-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd979-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fd979-126">Header</span></span><br/>  | <dl> <span data-ttu-id="fd979-127"><dt>Ctlutil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fd979-127"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="fd979-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="fd979-128">Library</span></span><br/> | <dl> <span data-ttu-id="fd979-129"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="fd979-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd979-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fd979-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd979-131">**Classe CBaseControlVideo**</span><span class="sxs-lookup"><span data-stu-id="fd979-131">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




