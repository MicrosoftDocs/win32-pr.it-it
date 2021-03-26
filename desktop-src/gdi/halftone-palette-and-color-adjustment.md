---
description: Le tavolozze di mezzitoni sono progettate per essere usate ogni volta che la modalità di adattamento di un contesto di dispositivo è impostata su mezzitoni.
ms.assetid: ee171379-2ab3-4c38-8e86-ff80fa63a357
title: Tavolozza mezzitoni e regolazione colore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b3e6708aff92387b792424f07e9b82a1f6125ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528339"
---
# <a name="halftone-palette-and-color-adjustment"></a><span data-ttu-id="d8d63-103">Tavolozza mezzitoni e regolazione colore</span><span class="sxs-lookup"><span data-stu-id="d8d63-103">Halftone Palette and Color Adjustment</span></span>

<span data-ttu-id="d8d63-104">Le tavolozze di mezzitoni sono progettate per essere usate ogni volta che la modalità di adattamento di un contesto di dispositivo è impostata su mezzitoni.</span><span class="sxs-lookup"><span data-stu-id="d8d63-104">Halftone palettes are intended to be used whenever the stretching mode of a device context is set to HALFTONE.</span></span> <span data-ttu-id="d8d63-105">Un'applicazione crea una tavolozza di mezzitoni usando la funzione [**CreateHalftonePalette**](/windows/desktop/api/Wingdi/nf-wingdi-createhalftonepalette) .</span><span class="sxs-lookup"><span data-stu-id="d8d63-105">An application creates a halftone palette by using the [**CreateHalftonePalette**](/windows/desktop/api/Wingdi/nf-wingdi-createhalftonepalette) function.</span></span> <span data-ttu-id="d8d63-106">L'applicazione deve selezionare e realizzare questa tavolozza nel contesto di dispositivo prima di chiamare la funzione [**StretchBlt**](/windows/desktop/api/Wingdi/nf-wingdi-stretchblt) o [**StretchDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits) .</span><span class="sxs-lookup"><span data-stu-id="d8d63-106">The application must select and realize this palette into the device context before calling the [**StretchBlt**](/windows/desktop/api/Wingdi/nf-wingdi-stretchblt) or [**StretchDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits) function.</span></span>

<span data-ttu-id="d8d63-107">Il sistema regola automaticamente il colore di input delle bitmap di origine ogni volta che le applicazioni chiamano le funzioni [**StretchBlt**](/windows/desktop/api/Wingdi/nf-wingdi-stretchblt) e [**StretchDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits) e la modalità di adattamento di un contesto di dispositivo è impostata su mezzitoni.</span><span class="sxs-lookup"><span data-stu-id="d8d63-107">The system automatically adjusts the input color of source bitmaps whenever applications call the [**StretchBlt**](/windows/desktop/api/Wingdi/nf-wingdi-stretchblt) and [**StretchDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits) functions and the stretching mode of a device context is set to HALFTONE.</span></span> <span data-ttu-id="d8d63-108">Queste regolazioni dei colori influiscono su determinati attributi dell'immagine, ad esempio contrasto e luminosità.</span><span class="sxs-lookup"><span data-stu-id="d8d63-108">These color adjustments affect certain attributes of the image, such as contrast and brightness.</span></span> <span data-ttu-id="d8d63-109">Un'applicazione può impostare i valori di regolazione del colore tramite la funzione [**SetColorAdjustment**](/windows/desktop/api/Wingdi/nf-wingdi-setcoloradjustment) .</span><span class="sxs-lookup"><span data-stu-id="d8d63-109">An application can set the color adjustment values by using the [**SetColorAdjustment**](/windows/desktop/api/Wingdi/nf-wingdi-setcoloradjustment) function.</span></span> <span data-ttu-id="d8d63-110">L'applicazione può recuperare i valori di regolazione del colore per il contesto di dispositivo specificato tramite la funzione [**GetColorAdjustment**](/windows/desktop/api/Wingdi/nf-wingdi-getcoloradjustment) .</span><span class="sxs-lookup"><span data-stu-id="d8d63-110">The application can retrieve the color adjustment values for the specified device context by using the [**GetColorAdjustment**](/windows/desktop/api/Wingdi/nf-wingdi-getcoloradjustment) function.</span></span>

 

 



