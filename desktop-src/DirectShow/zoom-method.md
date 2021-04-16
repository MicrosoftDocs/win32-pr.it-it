---
description: Il metodo zoom consente di ingrandire o ridurre la visualizzazione del video, centrata su un determinato set di coordinate dello schermo.
ms.assetid: 050f1264-8fbe-4322-970c-184275d5b219
title: Zoom (metodo)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2625e6c4facf006a0d904e49068853720e20c29e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485637"
---
# <a name="zoom-method"></a><span data-ttu-id="8fb2e-103">Zoom (metodo)</span><span class="sxs-lookup"><span data-stu-id="8fb2e-103">Zoom Method</span></span>

> [!Note]  
> <span data-ttu-id="8fb2e-104">Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="8fb2e-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="8fb2e-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="8fb2e-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="8fb2e-106">Il `Zoom` metodo consente di ingrandire o ridurre la visualizzazione del video, centrata su un determinato set di coordinate dello schermo.</span><span class="sxs-lookup"><span data-stu-id="8fb2e-106">The `Zoom` method zooms the video display in or out, centered on a given set of screen coordinates.</span></span>

``` syntax
MSWebDVD.Zoom(iXPos, iYPos, iZoomRatio)
```

## <a name="parameters"></a><span data-ttu-id="8fb2e-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="8fb2e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8fb2e-108"><span id="iXPos"></span><span id="ixpos"></span><span id="IXPOS"></span>*iXPos*</span><span class="sxs-lookup"><span data-stu-id="8fb2e-108"><span id="iXPos"></span><span id="ixpos"></span><span id="IXPOS"></span>*iXPos*</span></span>
</dt> <dd>

<span data-ttu-id="8fb2e-109">Specifica la coordinata x al centro dell'area di zoom rettangolare come valore integer.</span><span class="sxs-lookup"><span data-stu-id="8fb2e-109">Specifies the x-coordinate at the center of the rectangular zoom area as an Integer.</span></span>

</dd> <dt>

<span data-ttu-id="8fb2e-110"><span id="iYPos"></span><span id="iypos"></span><span id="IYPOS"></span>*iYPos*</span><span class="sxs-lookup"><span data-stu-id="8fb2e-110"><span id="iYPos"></span><span id="iypos"></span><span id="IYPOS"></span>*iYPos*</span></span>
</dt> <dd>

<span data-ttu-id="8fb2e-111">Specifica la coordinata y al centro del rettangolo da ingrandire come Integer.</span><span class="sxs-lookup"><span data-stu-id="8fb2e-111">Specifies the y-coordinate at the center of the rectangle to be zoomed as an Integer.</span></span>

</dd> <dt>

<span data-ttu-id="8fb2e-112"><span id="iZoomRatio"></span><span id="izoomratio"></span><span id="IZOOMRATIO"></span>*iZoomRatio*</span><span class="sxs-lookup"><span data-stu-id="8fb2e-112"><span id="iZoomRatio"></span><span id="izoomratio"></span><span id="IZOOMRATIO"></span>*iZoomRatio*</span></span>
</dt> <dd>

<span data-ttu-id="8fb2e-113">Specifica il fattore di ingrandimento applicato al valore di zoom corrente come intero.</span><span class="sxs-lookup"><span data-stu-id="8fb2e-113">Specifies the magnification factor applied to the current zoom value as an Integer.</span></span> <span data-ttu-id="8fb2e-114">Il valore massimo totale dipende da ciò che la sovrimpressione hardware può supportare. si tratta in genere di un fattore da 32 a 64 volte le dimensioni originali.</span><span class="sxs-lookup"><span data-stu-id="8fb2e-114">The total maximum value depends on what the hardware overlay can support; this is typically a factor of 32 to 64 times the original size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8fb2e-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8fb2e-115">Return Value</span></span>

<span data-ttu-id="8fb2e-116">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="8fb2e-116">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8fb2e-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="8fb2e-117">Remarks</span></span>

<span data-ttu-id="8fb2e-118">Il nuovo rapporto di zoom rimane attivo fino a quando non viene ripristinato alla dimensione originale o nuovamente modificato.</span><span class="sxs-lookup"><span data-stu-id="8fb2e-118">The new zoom ratio stays in effect until it is restored to the original size or changed again.</span></span> <span data-ttu-id="8fb2e-119">In altre parole, due chiamate a questo metodo che specificano un *iZoomRatio* di due comporteranno un rapporto di zoom quattro volte maggiore delle dimensioni del video originale.</span><span class="sxs-lookup"><span data-stu-id="8fb2e-119">In other words, two calls to this method specifying an *iZoomRatio* of two will result in a zoom ratio four times larger than the original video size.</span></span> <span data-ttu-id="8fb2e-120">Se l'utente tenta di ingrandire i dati che l'hardware può supportare, questo metodo avrà esito positivo, ma non eseguirà alcuna operazione.</span><span class="sxs-lookup"><span data-stu-id="8fb2e-120">If the user tries to zoom beyond what the hardware can support, this method will succeed but do nothing.</span></span>

<span data-ttu-id="8fb2e-121">Il metodo [**SetClipVideoRect**](setclipvideorect-method.md) è un altro modo per eseguire lo zoom avanti; l'unica differenza tra i due metodi è il modo in cui viene specificato il rettangolo di zoom.</span><span class="sxs-lookup"><span data-stu-id="8fb2e-121">The [**SetClipVideoRect**](setclipvideorect-method.md) method is another way to zoom in; the only difference between the two methods is the way in which the zoom rectangle is specified.</span></span>

 

 



