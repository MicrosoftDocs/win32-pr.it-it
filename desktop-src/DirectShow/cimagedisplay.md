---
description: La classe CImageDisplay è una classe helper per i renderer video GDI per gestire il formato di visualizzazione.
ms.assetid: c9221e5c-30c6-489a-89d7-132203314dc8
title: Classe CImageDisplay (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a5a7cbb28c53d8ff357d4e5174d24f92ba2d0cad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332275"
---
# <a name="cimagedisplay-class"></a><span data-ttu-id="e9f39-103">Classe CImageDisplay</span><span class="sxs-lookup"><span data-stu-id="e9f39-103">CImageDisplay class</span></span>

![cimagedisplayclasshierarchy](images/wutil06.png)

<span data-ttu-id="e9f39-105">La `CImageDisplay` classe è una classe helper per i renderer video GDI per gestire il formato di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="e9f39-105">The `CImageDisplay` class is a helper class for GDI video renderers to manage the display format.</span></span> <span data-ttu-id="e9f39-106">L'oggetto archivia una struttura [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) che descrive la modalità di visualizzazione corrente, inizializzata nel metodo del costruttore dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="e9f39-106">The object stores a [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) structure that describes the current display mode, which is initialized in the object's constructor method.</span></span> <span data-ttu-id="e9f39-107">Il metodo **CheckMediaType** dell'oggetto verifica se è possibile eseguire il rendering efficiente di un tipo di supporto proposto utilizzando GDI.</span><span class="sxs-lookup"><span data-stu-id="e9f39-107">The object's **CheckMediaType** method checks whether a proposed media type can be rendered efficiently using GDI.</span></span>



| <span data-ttu-id="e9f39-108">Variabili membro protette</span><span class="sxs-lookup"><span data-stu-id="e9f39-108">Protected Member Variables</span></span>                                       | <span data-ttu-id="e9f39-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e9f39-109">Description</span></span>                                                                            |
|------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [<span data-ttu-id="e9f39-110">**\_visualizzazione m**</span><span class="sxs-lookup"><span data-stu-id="e9f39-110">**m\_Display**</span></span>](cimagedisplay-m-display.md)                    | <span data-ttu-id="e9f39-111">Struttura **VIDEOINFO** che descrive il formato di visualizzazione corrente.</span><span class="sxs-lookup"><span data-stu-id="e9f39-111">**VIDEOINFO** structure that describes the current display format.</span></span>                     |
| <span data-ttu-id="e9f39-112">Metodi protetti</span><span class="sxs-lookup"><span data-stu-id="e9f39-112">Protected Methods</span></span>                                                | <span data-ttu-id="e9f39-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e9f39-113">Description</span></span>                                                                            |
| [<span data-ttu-id="e9f39-114">**CheckBitFields**</span><span class="sxs-lookup"><span data-stu-id="e9f39-114">**CheckBitFields**</span></span>](cimagedisplay-checkbitfields.md)           | <span data-ttu-id="e9f39-115">Convalida le maschere dei colori in una struttura **VIDEOINFO** .</span><span class="sxs-lookup"><span data-stu-id="e9f39-115">Validates the color masks in a **VIDEOINFO** structure.</span></span>                                |
| [<span data-ttu-id="e9f39-116">**CountPrefixBits**</span><span class="sxs-lookup"><span data-stu-id="e9f39-116">**CountPrefixBits**</span></span>](cimagedisplay-countprefixbits.md)         | <span data-ttu-id="e9f39-117">Calcola il numero di bit zero all'inizio di un campo di bit specificato.</span><span class="sxs-lookup"><span data-stu-id="e9f39-117">Calculates the number of zero bits at the start of a specified bit field.</span></span>              |
| [<span data-ttu-id="e9f39-118">**CountSetBits**</span><span class="sxs-lookup"><span data-stu-id="e9f39-118">**CountSetBits**</span></span>](cimagedisplay-countsetbits.md)               | <span data-ttu-id="e9f39-119">Restituisce il numero di bit impostato su 1 in un campo di bit specificato.</span><span class="sxs-lookup"><span data-stu-id="e9f39-119">Returns the number of bits set to 1 in a specified bit field.</span></span>                          |
| <span data-ttu-id="e9f39-120">Metodi pubblici</span><span class="sxs-lookup"><span data-stu-id="e9f39-120">Public Methods</span></span>                                                   | <span data-ttu-id="e9f39-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e9f39-121">Description</span></span>                                                                            |
| [<span data-ttu-id="e9f39-122">**CheckHeaderValidity**</span><span class="sxs-lookup"><span data-stu-id="e9f39-122">**CheckHeaderValidity**</span></span>](cimagedisplay-checkheadervalidity.md) | <span data-ttu-id="e9f39-123">Convalida una struttura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) .</span><span class="sxs-lookup"><span data-stu-id="e9f39-123">Validates a [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure.</span></span>                    |
| [<span data-ttu-id="e9f39-124">**CheckMediaType**</span><span class="sxs-lookup"><span data-stu-id="e9f39-124">**CheckMediaType**</span></span>](cimagedisplay-checkmediatype.md)           | <span data-ttu-id="e9f39-125">Determina se un tipo di supporto proposto è compatibile con il formato di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="e9f39-125">Determines whether a proposed media type is compatible with the display format.</span></span>        |
| [<span data-ttu-id="e9f39-126">**CheckPaletteHeader**</span><span class="sxs-lookup"><span data-stu-id="e9f39-126">**CheckPaletteHeader**</span></span>](cimagedisplay-checkpaletteheader.md)   | <span data-ttu-id="e9f39-127">Convalida le voci della tavolozza in una struttura **VIDEOINFO** .</span><span class="sxs-lookup"><span data-stu-id="e9f39-127">Validates the palette entries in a **VIDEOINFO** structure.</span></span>                            |
| [<span data-ttu-id="e9f39-128">**CheckVideoType**</span><span class="sxs-lookup"><span data-stu-id="e9f39-128">**CheckVideoType**</span></span>](cimagedisplay-checkvideotype.md)           | <span data-ttu-id="e9f39-129">Verifica se un formato **VIDEOINFO** specificato è compatibile con il formato di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="e9f39-129">Checks whether a specified **VIDEOINFO** format is compatible with the display format.</span></span> |
| [<span data-ttu-id="e9f39-130">**CImageDisplay**</span><span class="sxs-lookup"><span data-stu-id="e9f39-130">**CImageDisplay**</span></span>](cimagedisplay-cimagedisplay.md)             | <span data-ttu-id="e9f39-131">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="e9f39-131">Constructor method.</span></span>                                                                    |
| [<span data-ttu-id="e9f39-132">**Getmascheramenti**</span><span class="sxs-lookup"><span data-stu-id="e9f39-132">**GetBitMasks**</span></span>](cimagedisplay-getbitmasks.md)                 | <span data-ttu-id="e9f39-133">Recupera le maschere dei colori per un formato **VIDEOINFO** specificato.</span><span class="sxs-lookup"><span data-stu-id="e9f39-133">Retrieves the color masks for a specified **VIDEOINFO** format.</span></span>                        |
| [<span data-ttu-id="e9f39-134">**GetColourMask**</span><span class="sxs-lookup"><span data-stu-id="e9f39-134">**GetColourMask**</span></span>](cimagedisplay-getcolourmask.md)             | <span data-ttu-id="e9f39-135">Recupera le maschere dei colori per il formato di visualizzazione corrente.</span><span class="sxs-lookup"><span data-stu-id="e9f39-135">Retrieves the color masks for the current display format.</span></span>                              |
| [<span data-ttu-id="e9f39-136">**GetDisplayDepth**</span><span class="sxs-lookup"><span data-stu-id="e9f39-136">**GetDisplayDepth**</span></span>](cimagedisplay-getdisplaydepth.md)         | <span data-ttu-id="e9f39-137">Recupera la profondità di bit della modalità di visualizzazione corrente.</span><span class="sxs-lookup"><span data-stu-id="e9f39-137">Retrieves the bit depth of the current display mode.</span></span>                                   |
| [<span data-ttu-id="e9f39-138">**GetDisplayFormat**</span><span class="sxs-lookup"><span data-stu-id="e9f39-138">**GetDisplayFormat**</span></span>](cimagedisplay-getdisplayformat.md)       | <span data-ttu-id="e9f39-139">Recupera un formato video che descrive la modalità di visualizzazione corrente.</span><span class="sxs-lookup"><span data-stu-id="e9f39-139">Retrieves a video format that describes the current display mode.</span></span>                      |
| [<span data-ttu-id="e9f39-140">**IsPalettised**</span><span class="sxs-lookup"><span data-stu-id="e9f39-140">**IsPalettised**</span></span>](cimagedisplay-ispalettised.md)               | <span data-ttu-id="e9f39-141">Determina se il formato di visualizzazione corrente è pallettizzati.</span><span class="sxs-lookup"><span data-stu-id="e9f39-141">Retermines whether the current display format is palettized.</span></span>                           |
| [<span data-ttu-id="e9f39-142">**RefreshDisplayType**</span><span class="sxs-lookup"><span data-stu-id="e9f39-142">**RefreshDisplayType**</span></span>](cimagedisplay-refreshdisplaytype.md)   | <span data-ttu-id="e9f39-143">Aggiorna il formato video dell'oggetto in modo che corrisponda alla visualizzazione specificata</span><span class="sxs-lookup"><span data-stu-id="e9f39-143">Updates the object's video format to match the specified display</span></span>                       |



 

## <a name="requirements"></a><span data-ttu-id="e9f39-144">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e9f39-144">Requirements</span></span>



| <span data-ttu-id="e9f39-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9f39-145">Requirement</span></span> | <span data-ttu-id="e9f39-146">Valore</span><span class="sxs-lookup"><span data-stu-id="e9f39-146">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9f39-147">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e9f39-147">Header</span></span><br/>  | <dl> <span data-ttu-id="e9f39-148"><dt>WinUtil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e9f39-148"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e9f39-149">Libreria</span><span class="sxs-lookup"><span data-stu-id="e9f39-149">Library</span></span><br/> | <dl> <span data-ttu-id="e9f39-150"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="e9f39-150"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




