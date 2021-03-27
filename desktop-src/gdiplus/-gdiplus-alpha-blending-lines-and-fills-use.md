---
description: In Windows GDI+, un colore è un valore a 32 bit con 8 bit ciascuno per Alpha, rosso, verde e blu.
ms.assetid: f8c22d1a-b96b-4d16-928e-20adbae4c4a7
title: Linee e riempimenti con fusione alfa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd13fe306dbf31c2a60a0bd38bf71b9e96edb201
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880929"
---
# <a name="alpha-blending-lines-and-fills"></a><span data-ttu-id="63281-103">Linee e riempimenti con fusione alfa</span><span class="sxs-lookup"><span data-stu-id="63281-103">Alpha Blending Lines and Fills</span></span>

<span data-ttu-id="63281-104">In Windows GDI+, un colore è un valore a 32 bit con 8 bit ciascuno per Alpha, rosso, verde e blu.</span><span class="sxs-lookup"><span data-stu-id="63281-104">In Windows GDI+, a color is a 32-bit value with 8 bits each for alpha, red, green, and blue.</span></span> <span data-ttu-id="63281-105">Il valore alfa indica la trasparenza del colore, ovvero la misura in cui il colore viene mescolato con il colore di sfondo.</span><span class="sxs-lookup"><span data-stu-id="63281-105">The alpha value indicates the transparency of the color — the extent to which the color is blended with the background color.</span></span> <span data-ttu-id="63281-106">I valori alfa variano da 0 a 255, dove 0 rappresenta un colore completamente trasparente e 255 rappresenta un colore completamente opaco.</span><span class="sxs-lookup"><span data-stu-id="63281-106">Alpha values range from 0 through 255, where 0 represents a fully transparent color, and 255 represents a fully opaque color.</span></span>

<span data-ttu-id="63281-107">La fusione alfa è una combinazione pixel per pixel dei dati di origine e di colore di sfondo.</span><span class="sxs-lookup"><span data-stu-id="63281-107">Alpha blending is a pixel-by-pixel blending of source and background color data.</span></span> <span data-ttu-id="63281-108">Ognuno dei tre componenti (rosso, verde, blu) di un determinato colore di origine viene mescolato con il componente corrispondente del colore di sfondo in base alla formula seguente:</span><span class="sxs-lookup"><span data-stu-id="63281-108">Each of the three components (red, green, blue) of a given source color is blended with the corresponding component of the background color according to the following formula:</span></span>

<span data-ttu-id="63281-109">displayColor = sourceColor × Alpha/255 + backgroundColor × (255 – Alpha)/255</span><span class="sxs-lookup"><span data-stu-id="63281-109">displayColor = sourceColor × alpha / 255 + backgroundColor × (255 – alpha) / 255</span></span>

<span data-ttu-id="63281-110">Si supponga, ad esempio, che il componente rosso del colore di origine sia 150 e che il componente rosso del colore di sfondo sia 100.</span><span class="sxs-lookup"><span data-stu-id="63281-110">For example, suppose the red component of the source color is 150 and the red component of the background color is 100.</span></span> <span data-ttu-id="63281-111">Se il valore alfa è 200, il componente rosso del colore risultante viene calcolato come segue:</span><span class="sxs-lookup"><span data-stu-id="63281-111">If the alpha value is 200, the red component of the resultant color is calculated as follows:</span></span>

<span data-ttu-id="63281-112">150 × 200 / 255 + 100 × (255 – 200) / 255 = 139</span><span class="sxs-lookup"><span data-stu-id="63281-112">150 × 200 / 255 + 100 × (255 – 200) / 255 = 139</span></span>

<span data-ttu-id="63281-113">Gli argomenti seguenti riguardano la fusione alfa in modo più dettagliato:</span><span class="sxs-lookup"><span data-stu-id="63281-113">The following topics cover alpha blending in more detail:</span></span>

-   [<span data-ttu-id="63281-114">Disegno di linee opache e semitrasparenti</span><span class="sxs-lookup"><span data-stu-id="63281-114">Drawing Opaque and Semitransparent Lines</span></span>](-gdiplus-drawing-opaque-and-semitransparent-lines-use.md)
-   [<span data-ttu-id="63281-115">Disegno con pennelli opachi e semitrasparenti</span><span class="sxs-lookup"><span data-stu-id="63281-115">Drawing with Opaque and Semitransparent Brushes</span></span>](-gdiplus-drawing-with-opaque-and-semitransparent-brushes-use.md)
-   [<span data-ttu-id="63281-116">Uso della modalità di composizione per controllare la fusione alfa</span><span class="sxs-lookup"><span data-stu-id="63281-116">Using Compositing Mode to Control Alpha Blending</span></span>](-gdiplus-using-compositing-mode-to-control-alpha-blending-use.md)
-   [<span data-ttu-id="63281-117">Uso di una matrice di colori per impostare valori alfa nelle immagini</span><span class="sxs-lookup"><span data-stu-id="63281-117">Using a Color Matrix to Set Alpha Values in Images</span></span>](-gdiplus-using-a-color-matrix-to-set-alpha-values-in-images-use.md)
-   [<span data-ttu-id="63281-118">Impostazione dei valori alfa dei singoli pixel</span><span class="sxs-lookup"><span data-stu-id="63281-118">Setting the Alpha Values of Individual Pixels</span></span>](-gdiplus-setting-the-alpha-values-of-individual-pixels-use.md)

 

 



