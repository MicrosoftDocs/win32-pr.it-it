---
description: Il metodo ShouldUpdate determina se è necessario creare una nuova tavolozza.
ms.assetid: 50886277-189b-4102-ade9-0366f64fdbcb
title: Metodo CImagePalette. ShouldUpdate (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImagePalette.ShouldUpdate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f8cf27548487ad0338f0c4773c66df8f7d03c2f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325059"
---
# <a name="cimagepaletteshouldupdate-method"></a><span data-ttu-id="5d892-103">CImagePalette. ShouldUpdate, metodo</span><span class="sxs-lookup"><span data-stu-id="5d892-103">CImagePalette.ShouldUpdate method</span></span>

<span data-ttu-id="5d892-104">Il `ShouldUpdate` metodo determina se è necessario creare una nuova tavolozza.</span><span class="sxs-lookup"><span data-stu-id="5d892-104">The `ShouldUpdate` method determines whether it is necessary to create a new palette.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d892-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5d892-105">Syntax</span></span>


```C++
BOOL ShouldUpdate(
   const VIDEOINFOHEADER *pNewInfo,
   const VIDEOINFOHEADER *pOldInfo
);
```



## <a name="parameters"></a><span data-ttu-id="5d892-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="5d892-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d892-107">*pNewInfo*</span><span class="sxs-lookup"><span data-stu-id="5d892-107">*pNewInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="5d892-108">Puntatore a una struttura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) contenente la nuova tabella dei colori.</span><span class="sxs-lookup"><span data-stu-id="5d892-108">Pointer to a [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure containing the new color table.</span></span>

</dd> <dt>

<span data-ttu-id="5d892-109">*pOldInfo*</span><span class="sxs-lookup"><span data-stu-id="5d892-109">*pOldInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="5d892-110">Puntatore a una struttura **VIDEOINFOHEADER** contenente la tabella dei colori obsoleta.</span><span class="sxs-lookup"><span data-stu-id="5d892-110">Pointer to a **VIDEOINFOHEADER** structure containing the old color table.</span></span> <span data-ttu-id="5d892-111">Questo parametro può essere **NULL**.</span><span class="sxs-lookup"><span data-stu-id="5d892-111">This parameter can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d892-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5d892-112">Return value</span></span>

<span data-ttu-id="5d892-113">Restituisce **true** se è necessario aggiornare la tavolozza; in caso contrario, **false** .</span><span class="sxs-lookup"><span data-stu-id="5d892-113">Returns **TRUE** if the palette needs to be updated, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="5d892-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="5d892-114">Remarks</span></span>

-   <span data-ttu-id="5d892-115">Se nessuna delle due strutture **VIDEOINFOHEADER** contiene una tabella dei colori, il metodo restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="5d892-115">If neither **VIDEOINFOHEADER** structure contains a color table, the method returns **FALSE**.</span></span>
-   <span data-ttu-id="5d892-116">Se una sola struttura contiene una tabella dei colori o se *pOldInfo* è **null**, il metodo restituisce **true**.</span><span class="sxs-lookup"><span data-stu-id="5d892-116">If only one structure contains a color table, or if *pOldInfo* is **NULL**, the method returns **TRUE**.</span></span>
-   <span data-ttu-id="5d892-117">Se entrambe le strutture contengono tabelle dei colori e le voci di colore corrispondono, il metodo restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="5d892-117">If both structures contain color tables, and the color entries match, the method returns **FALSE**.</span></span>
-   <span data-ttu-id="5d892-118">Se entrambe le strutture contengono tabelle dei colori, ma le voci di colore non corrispondono, il metodo restituisce **true**.</span><span class="sxs-lookup"><span data-stu-id="5d892-118">If both structures contain color tables, but the color entries do not match, the method returns **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d892-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5d892-119">Requirements</span></span>



| <span data-ttu-id="5d892-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="5d892-120">Requirement</span></span> | <span data-ttu-id="5d892-121">Valore</span><span class="sxs-lookup"><span data-stu-id="5d892-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d892-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5d892-122">Header</span></span><br/>  | <dl> <span data-ttu-id="5d892-123"><dt>WinUtil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5d892-123"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="5d892-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="5d892-124">Library</span></span><br/> | <dl> <span data-ttu-id="5d892-125"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="5d892-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d892-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5d892-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d892-127">**Classe CImagePalette**</span><span class="sxs-lookup"><span data-stu-id="5d892-127">**CImagePalette Class**</span></span>](cimagepalette.md)
</dt> </dl>

 

 




