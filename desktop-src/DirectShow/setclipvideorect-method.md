---
description: Il metodo SetClipVideoRect esegue lo zoom della visualizzazione video sul sottorettangolo specificato.
ms.assetid: 3940a382-8d53-4ff9-b024-38de1aa00f54
title: Metodo SetClipVideoRect
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ff7f4b003ef20b82f1e783ebf074e8bbd5cc793
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746295"
---
# <a name="setclipvideorect-method"></a><span data-ttu-id="9cbb0-103">Metodo SetClipVideoRect</span><span class="sxs-lookup"><span data-stu-id="9cbb0-103">SetClipVideoRect Method</span></span>

> [!Note]  
> <span data-ttu-id="9cbb0-104">Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="9cbb0-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="9cbb0-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="9cbb0-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="9cbb0-106">Il `SetClipVideoRect` metodo esegue lo zoom della visualizzazione video sul sottorettangolo specificato.</span><span class="sxs-lookup"><span data-stu-id="9cbb0-106">The `SetClipVideoRect` method zooms the video display to the specified subrectangle.</span></span>

``` syntax
MSWebDVD.SetClipVideoRect(oRect)
```

## <a name="parameters"></a><span data-ttu-id="9cbb0-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="9cbb0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9cbb0-108"><span id="oRect"></span><span id="orect"></span><span id="ORECT"></span>*oRect*</span><span class="sxs-lookup"><span data-stu-id="9cbb0-108"><span id="oRect"></span><span id="orect"></span><span id="ORECT"></span>*oRect*</span></span>
</dt> <dd>

<span data-ttu-id="9cbb0-109">Specifica un oggetto [DVDRect](dvdrect-object.md) che contiene il rettangolo di ridimensionamento.</span><span class="sxs-lookup"><span data-stu-id="9cbb0-109">Specifies a [DVDRect](dvdrect-object.md) object, which contains the clipping rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9cbb0-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9cbb0-110">Return Value</span></span>

<span data-ttu-id="9cbb0-111">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="9cbb0-111">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9cbb0-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="9cbb0-112">Remarks</span></span>

<span data-ttu-id="9cbb0-113">Quando si imposta un nuovo rettangolo di ridimensionamento, l'oggetto ingrandisce l'area per adattarla alle dimensioni di visualizzazione complessive dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9cbb0-113">When you set a new clipping rectangle, the object enlarges that area to fit within the application's overall display dimensions.</span></span> <span data-ttu-id="9cbb0-114">Questo consente di creare l'effetto zoom avanti su un'area specifica dello schermo.</span><span class="sxs-lookup"><span data-stu-id="9cbb0-114">This creates the effect zooming in on a particular area of the screen.</span></span> <span data-ttu-id="9cbb0-115">Per specificare il rettangolo, creare un nuovo oggetto [DVDRect](dvdrect-object.md) e compilare le relative proprietà.</span><span class="sxs-lookup"><span data-stu-id="9cbb0-115">To specify the rectangle, create a new [DVDRect](dvdrect-object.md) object and fill in its properties.</span></span>

<span data-ttu-id="9cbb0-116">Il rettangolo più comune per la visualizzazione video è 720 x 540.</span><span class="sxs-lookup"><span data-stu-id="9cbb0-116">The most common rectangle for video display is 720 x 540.</span></span>

## <a name="see-also"></a><span data-ttu-id="9cbb0-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9cbb0-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9cbb0-118">**GetClipVideoRect**</span><span class="sxs-lookup"><span data-stu-id="9cbb0-118">**GetClipVideoRect**</span></span>](getclipvideorect-method.md)
</dt> </dl>

 

 



