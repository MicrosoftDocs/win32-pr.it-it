---
description: Per eseguire operazioni bitmap, un numero di funzioni usa il pennello attualmente selezionato in un contesto di dispositivo.
ms.assetid: 98fb2fd5-9cf4-4016-9e30-ec724e77cebc
title: Bitmap come pennelli
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c693e3c144dec2d26eccca1f1b628252dea187c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226709"
---
# <a name="bitmaps-as-brushes"></a><span data-ttu-id="0326b-103">Bitmap come pennelli</span><span class="sxs-lookup"><span data-stu-id="0326b-103">Bitmaps as Brushes</span></span>

<span data-ttu-id="0326b-104">Per eseguire operazioni bitmap, un numero di funzioni usa il pennello attualmente selezionato in un contesto di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0326b-104">A number of functions use the brush currently selected into a device context to perform bitmap operations.</span></span> <span data-ttu-id="0326b-105">Ad esempio, la funzione [**PatBlt**](/windows/desktop/api/Wingdi/nf-wingdi-patblt) replica il pennello in un'area rettangolare all'interno di una finestra e la funzione [**FLOODFILL**](/windows/desktop/api/Wingdi/nf-wingdi-floodfill) replica il pennello all'interno di un'area in una finestra delimitata dal colore specificato (a differenza di **PatBlt**, **FLOODFILL** riempie forme non rettangolari).</span><span class="sxs-lookup"><span data-stu-id="0326b-105">For example, the [**PatBlt**](/windows/desktop/api/Wingdi/nf-wingdi-patblt) function replicates the brush in a rectangular region within a window, and the [**FloodFill**](/windows/desktop/api/Wingdi/nf-wingdi-floodfill) function replicates the brush inside an area in a window bounded by the specified color (unlike **PatBlt**, **FloodFill** does fill nonrectangular shapes).</span></span>

<span data-ttu-id="0326b-106">La funzione [**FLOODFILL**](/windows/desktop/api/Wingdi/nf-wingdi-floodfill) replica il pennello all'interno di un'area delimitata da un colore specificato.</span><span class="sxs-lookup"><span data-stu-id="0326b-106">The [**FloodFill**](/windows/desktop/api/Wingdi/nf-wingdi-floodfill) function replicates the brush within a region bounded by a specified color.</span></span> <span data-ttu-id="0326b-107">Tuttavia, a differenza della funzione [**PatBlt**](/windows/desktop/api/Wingdi/nf-wingdi-patblt) , **FLOODFILL** non combina i dati relativi al colore per il pennello con i dati relativi al colore per i pixel sullo schermo; imposta semplicemente il colore di tutti i pixel all'interno dell'area racchiusa sullo schermo sul colore del pennello attualmente selezionato nel contesto di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0326b-107">However, unlike the [**PatBlt**](/windows/desktop/api/Wingdi/nf-wingdi-patblt) function, **FloodFill** does not combine the color data for the brush with the color data for the pixels on the display; it simply sets the color of all pixels within the enclosed region on the display to the color of the brush that is currently selected into the device context.</span></span>

 

 



