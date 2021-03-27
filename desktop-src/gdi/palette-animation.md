---
description: L'animazione della tavolozza è una tecnica per simulare il movimento modificando rapidamente i colori delle voci selezionate in una tavolozza dei colori.
ms.assetid: fc5b8061-fd4f-4751-883d-877fa32cdfcc
title: Animazione tavolozza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9761e99033e7a01fa875fce7c41e5a35cf40ab6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103754338"
---
# <a name="palette-animation"></a><span data-ttu-id="a642e-103">Animazione tavolozza</span><span class="sxs-lookup"><span data-stu-id="a642e-103">Palette Animation</span></span>

<span data-ttu-id="a642e-104">L'animazione della tavolozza è una tecnica per simulare il movimento modificando rapidamente i colori delle voci selezionate in una tavolozza dei colori.</span><span class="sxs-lookup"><span data-stu-id="a642e-104">Palette animation is a technique to simulate motion by rapidly changing the colors of selected entries in a color palette.</span></span> <span data-ttu-id="a642e-105">Un'applicazione può eseguire l'animazione della tavolozza creando una tavolozza logica che contiene voci "riservate" e quindi utilizzando la funzione [**AnimatePalette**](/windows/desktop/api/Wingdi/nf-wingdi-animatepalette) per modificare i colori in tali voci riservate.</span><span class="sxs-lookup"><span data-stu-id="a642e-105">An application can carry out palette animation by creating a logical palette that contains "reserved" entries and then using the [**AnimatePalette**](/windows/desktop/api/Wingdi/nf-wingdi-animatepalette) function to change colors in those reserved entries.</span></span>

<span data-ttu-id="a642e-106">Un'applicazione crea una voce riservata in una tavolozza logica impostando il membro **peFlags** della struttura [**PaletteEntry**](/previous-versions//dd162769(v=vs.85)) sul \_ flag riservato PC.</span><span class="sxs-lookup"><span data-stu-id="a642e-106">An application creates a reserved entry in a logical palette by setting the **peFlags** member of the [**PALETTEENTRY**](/previous-versions//dd162769(v=vs.85)) structure to the PC\_RESERVED flag.</span></span> <span data-ttu-id="a642e-107">Una volta selezionata e realizzata questa tavolozza logica, l'applicazione può chiamare la funzione [**AnimatePalette**](/windows/desktop/api/Wingdi/nf-wingdi-animatepalette) per modificare una o più voci riservate.</span><span class="sxs-lookup"><span data-stu-id="a642e-107">Once this logical palette is selected and realized, the application can call the [**AnimatePalette**](/windows/desktop/api/Wingdi/nf-wingdi-animatepalette) function to change one or more reserved entries.</span></span> <span data-ttu-id="a642e-108">Se la tavolozza specificata è associata alla finestra attiva, il sistema aggiorna immediatamente i colori sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="a642e-108">If the given palette is associated with the active window, the system updates the colors on the screen immediately.</span></span>

 

 
