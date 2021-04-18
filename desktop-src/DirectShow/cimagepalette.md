---
description: La classe CImagePalette gestisce le tavolozze per i renderer video. Può essere usato per creare una tavolozza logica da un formato video. Questa classe è destinata all'uso con le classi CBaseWindow e CDrawImage, quindi è in qualche modo specializzata.
ms.assetid: dcbe5049-0e8c-4221-825a-0fd8e6efd2a5
title: Classe CImagePalette
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImagePalette
api_type:
- COM
api_location: ''
ms.openlocfilehash: 696c51e4918815e18accbadd66c764493dc0b98e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303786"
---
# <a name="cimagepalette-class"></a><span data-ttu-id="e52ca-105">Classe CImagePalette</span><span class="sxs-lookup"><span data-stu-id="e52ca-105">CImagePalette class</span></span>

<span data-ttu-id="e52ca-106">La `CImagePalette` classe gestisce le tavolozze per i renderer video.</span><span class="sxs-lookup"><span data-stu-id="e52ca-106">The `CImagePalette` class manages palettes for video renderers.</span></span> <span data-ttu-id="e52ca-107">Può essere usato per creare una tavolozza logica da un formato video.</span><span class="sxs-lookup"><span data-stu-id="e52ca-107">It can be used to create a logical palette from a video format.</span></span> <span data-ttu-id="e52ca-108">Questa classe è destinata all'uso con le classi [**CBaseWindow**](cbasewindow.md) e [**CDrawImage**](cdrawimage.md) , quindi è in qualche modo specializzata.</span><span class="sxs-lookup"><span data-stu-id="e52ca-108">This class is intended to be used with the [**CBaseWindow**](cbasewindow.md) and [**CDrawImage**](cdrawimage.md) classes, so it is somewhat specialized.</span></span>



| <span data-ttu-id="e52ca-109">Variabili membro protette</span><span class="sxs-lookup"><span data-stu-id="e52ca-109">Protected Member Variables</span></span>                                       | <span data-ttu-id="e52ca-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e52ca-110">Description</span></span>                                                                                    |
|------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e52ca-111">**\_hPalette m**</span><span class="sxs-lookup"><span data-stu-id="e52ca-111">**m\_hPalette**</span></span>](cimagepalette-m-hpalette.md)                  | <span data-ttu-id="e52ca-112">Handle per la tavolozza logica gestita da questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="e52ca-112">Handle to the logical palette that this object manages.</span></span>                                        |
| [<span data-ttu-id="e52ca-113">**\_pBaseWindow m**</span><span class="sxs-lookup"><span data-stu-id="e52ca-113">**m\_pBaseWindow**</span></span>](cimagepalette-m-pbasewindow.md)            | <span data-ttu-id="e52ca-114">Puntatore all'oggetto **CBaseWindow** che gestisce la finestra.</span><span class="sxs-lookup"><span data-stu-id="e52ca-114">Pointer to the **CBaseWindow** object that manages the window.</span></span>                                 |
| [<span data-ttu-id="e52ca-115">**\_pDrawImage m**</span><span class="sxs-lookup"><span data-stu-id="e52ca-115">**m\_pDrawImage**</span></span>](cimagepalette-m-pdrawimage.md)              | <span data-ttu-id="e52ca-116">Puntatore all'oggetto **CDrawImage** che disegna l'immagine del video.</span><span class="sxs-lookup"><span data-stu-id="e52ca-116">Pointer to the **CDrawImage** object that draws the video image.</span></span>                               |
| [<span data-ttu-id="e52ca-117">**\_pFilter m**</span><span class="sxs-lookup"><span data-stu-id="e52ca-117">**m\_pFilter**</span></span>](cimagepalette-m-pfilter.md)                    | <span data-ttu-id="e52ca-118">Puntatore al filtro proprietario.</span><span class="sxs-lookup"><span data-stu-id="e52ca-118">Pointer to the owning filter.</span></span>                                                                  |
| <span data-ttu-id="e52ca-119">Metodi pubblici</span><span class="sxs-lookup"><span data-stu-id="e52ca-119">Public Methods</span></span>                                                   | <span data-ttu-id="e52ca-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e52ca-120">Description</span></span>                                                                                    |
| [<span data-ttu-id="e52ca-121">**CImagePalette**</span><span class="sxs-lookup"><span data-stu-id="e52ca-121">**CImagePalette**</span></span>](cimagepalette-cimagepalette.md)             | <span data-ttu-id="e52ca-122">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="e52ca-122">Constructor method.</span></span>                                                                            |
| [<span data-ttu-id="e52ca-123">**CopyPalette**</span><span class="sxs-lookup"><span data-stu-id="e52ca-123">**CopyPalette**</span></span>](cimagepalette-copypalette.md)                 | <span data-ttu-id="e52ca-124">Copia la tavolozza da qualsiasi struttura **VIDEOINFO** a qualsiasi struttura **VIDEOINFO** di pallettizzati.</span><span class="sxs-lookup"><span data-stu-id="e52ca-124">Copies the palette from any **VIDEOINFO** structure to any palettized **VIDEOINFO** structure.</span></span> |
| [<span data-ttu-id="e52ca-125">**MakeIdentityPalette**</span><span class="sxs-lookup"><span data-stu-id="e52ca-125">**MakeIdentityPalette**</span></span>](cimagepalette-makeidentitypalette.md) | <span data-ttu-id="e52ca-126">Tenta di creare una tavolozza che esegue il mapping direttamente alla tavolozza selezionata nel dispositivo di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="e52ca-126">Attempts to make a palette that maps directly to the palette selected in the display device.</span></span>   |
| [<span data-ttu-id="e52ca-127">**MakePalette**</span><span class="sxs-lookup"><span data-stu-id="e52ca-127">**MakePalette**</span></span>](cimagepalette-makepalette.md)                 | <span data-ttu-id="e52ca-128">Crea una tavolozza logica dalla tabella dei colori in un formato video.</span><span class="sxs-lookup"><span data-stu-id="e52ca-128">Creates a logical palette from the color table in a video format.</span></span>                              |
| [<span data-ttu-id="e52ca-129">**PreparePalette**</span><span class="sxs-lookup"><span data-stu-id="e52ca-129">**PreparePalette**</span></span>](cimagepalette-preparepalette.md)           | <span data-ttu-id="e52ca-130">Imposta una tavolozza in base a un tipo di supporto dal filtro proprietario.</span><span class="sxs-lookup"><span data-stu-id="e52ca-130">Sets up a palette, based on a media type from the owning filter.</span></span>                               |
| [<span data-ttu-id="e52ca-131">**RemovePalette**</span><span class="sxs-lookup"><span data-stu-id="e52ca-131">**RemovePalette**</span></span>](cimagepalette-removepalette.md)             | <span data-ttu-id="e52ca-132">Elimina la tavolozza logica esistente.</span><span class="sxs-lookup"><span data-stu-id="e52ca-132">Deletes the existing logical palette.</span></span>                                                          |



 

 

 



