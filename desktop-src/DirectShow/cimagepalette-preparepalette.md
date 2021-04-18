---
description: Il metodo PreparePalette configura una tavolozza in base a un tipo di supporto dal filtro proprietario.
ms.assetid: cb012391-39ab-4ad1-aeb7-ec25010ac64a
title: Metodo CImagePalette. PreparePalette (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImagePalette.PreparePalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a9b09804b2ee6ad9fbda394a7fb8f9f188b46453
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325063"
---
# <a name="cimagepalettepreparepalette-method"></a><span data-ttu-id="a0054-103">CImagePalette. PreparePalette, metodo</span><span class="sxs-lookup"><span data-stu-id="a0054-103">CImagePalette.PreparePalette method</span></span>

<span data-ttu-id="a0054-104">Il `PreparePalette` metodo configura una tavolozza in base a un tipo di supporto dal filtro proprietario.</span><span class="sxs-lookup"><span data-stu-id="a0054-104">The `PreparePalette` method sets up a palette, based on a media type from the owning filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0054-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a0054-105">Syntax</span></span>


```C++
HRESULT PreparePalette(
   const CMediaType *pmtNew,
   const CMediaType *pmtOld,
         LPSTR      szDevice
);
```



## <a name="parameters"></a><span data-ttu-id="a0054-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a0054-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0054-107">*pmtNew*</span><span class="sxs-lookup"><span data-stu-id="a0054-107">*pmtNew*</span></span> 
</dt> <dd>

<span data-ttu-id="a0054-108">Puntatore al nuovo tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="a0054-108">Pointer to the new media type.</span></span> <span data-ttu-id="a0054-109">Il blocco di formato deve essere una struttura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) .</span><span class="sxs-lookup"><span data-stu-id="a0054-109">The format block must be a [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure.</span></span>

</dd> <dt>

<span data-ttu-id="a0054-110">*pmtOld*</span><span class="sxs-lookup"><span data-stu-id="a0054-110">*pmtOld*</span></span> 
</dt> <dd>

<span data-ttu-id="a0054-111">Puntatore al vecchio tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="a0054-111">Pointer to the old media type.</span></span> <span data-ttu-id="a0054-112">Se il tipo di supporto viene impostato per la prima volta, questo parametro può essere un tipo vuoto senza blocco di formato.</span><span class="sxs-lookup"><span data-stu-id="a0054-112">If the media type is being set for the first time, this parameter can be an empty type with no format block.</span></span> <span data-ttu-id="a0054-113">In caso contrario, il blocco di formato deve essere una struttura **VIDEOINFOHEADER** .</span><span class="sxs-lookup"><span data-stu-id="a0054-113">Otherwise, the format block must be a **VIDEOINFOHEADER** structure.</span></span>

</dd> <dt>

<span data-ttu-id="a0054-114">*szDevice*</span><span class="sxs-lookup"><span data-stu-id="a0054-114">*szDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="a0054-115">Puntatore a una stringa che contiene il nome del dispositivo di visualizzazione, come restituito dalla funzione **ENUMDISPLAYDEVICES** GDI.</span><span class="sxs-lookup"><span data-stu-id="a0054-115">Pointer to a string that contains the name of the display device, as returned by the GDI **EnumDisplayDevices** function.</span></span> <span data-ttu-id="a0054-116">Per usare il dispositivo di visualizzazione principale, impostare questo parametro su **null**.</span><span class="sxs-lookup"><span data-stu-id="a0054-116">To use the main display device, set this parameter to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0054-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a0054-117">Return value</span></span>

<span data-ttu-id="a0054-118">Restituisce \_ OK se la tavolozza è stata aggiornata oppure s \_ false se la tavolozza non è stata modificata.</span><span class="sxs-lookup"><span data-stu-id="a0054-118">Returns S\_OK if the palette was updated, or S\_FALSE if the palette did not change.</span></span>

## <a name="remarks"></a><span data-ttu-id="a0054-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="a0054-119">Remarks</span></span>

<span data-ttu-id="a0054-120">Se è necessario aggiornare la tavolozza, questo metodo esegue le azioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="a0054-120">If the palette needs to be updated, this method performs the following actions:</span></span>

-   <span data-ttu-id="a0054-121">Chiama [**CImagePalette:: MakePalette**](cimagepalette-makepalette.md) per creare una nuova tavolozza logica.</span><span class="sxs-lookup"><span data-stu-id="a0054-121">Calls [**CImagePalette::MakePalette**](cimagepalette-makepalette.md) to create a new logical palette.</span></span>
-   <span data-ttu-id="a0054-122">Invia un evento di [**\_ \_ modifica della tavolozza EC**](ec-palette-changed.md) al gestore del grafico dei filtri.</span><span class="sxs-lookup"><span data-stu-id="a0054-122">Sends an [**EC\_PALETTE\_CHANGED**](ec-palette-changed.md) event to the Filter Graph Manager.</span></span>
-   <span data-ttu-id="a0054-123">Chiama [**CBaseWindow:: Setavolozza**](cbasewindow-setpalette.md) sull'oggetto **CBaseWindow** .</span><span class="sxs-lookup"><span data-stu-id="a0054-123">Calls [**CBaseWindow::SetPalette**](cbasewindow-setpalette.md) on the **CBaseWindow** object.</span></span>
-   <span data-ttu-id="a0054-124">Chiama [**CDrawImage:: IncrementPaletteVersion**](cdrawimage-incrementpaletteversion.md) sull'oggetto **CDrawImage** .</span><span class="sxs-lookup"><span data-stu-id="a0054-124">Calls [**CDrawImage::IncrementPaletteVersion**](cdrawimage-incrementpaletteversion.md) on the **CDrawImage** object.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0054-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a0054-125">Requirements</span></span>



| <span data-ttu-id="a0054-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0054-126">Requirement</span></span> | <span data-ttu-id="a0054-127">Valore</span><span class="sxs-lookup"><span data-stu-id="a0054-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0054-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a0054-128">Header</span></span><br/>  | <dl> <span data-ttu-id="a0054-129"><dt>WinUtil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a0054-129"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a0054-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="a0054-130">Library</span></span><br/> | <dl> <span data-ttu-id="a0054-131"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="a0054-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0054-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a0054-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0054-133">**Classe CImagePalette**</span><span class="sxs-lookup"><span data-stu-id="a0054-133">**CImagePalette Class**</span></span>](cimagepalette.md)
</dt> </dl>

 

 




