---
description: È possibile utilizzare un pennello sfumatura per riempire una forma con un colore a modifica graduale.
ms.assetid: e37b4c3a-b753-483a-990f-da3bcc70acf5
title: Riempimento di forme con un pennello sfumatura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6784d0bfd59fd37f217e8d7a1cdd230348807d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994253"
---
# <a name="filling-shapes-with-a-gradient-brush"></a><span data-ttu-id="1de59-103">Riempimento di forme con un pennello sfumatura</span><span class="sxs-lookup"><span data-stu-id="1de59-103">Filling Shapes with a Gradient Brush</span></span>

<span data-ttu-id="1de59-104">È possibile utilizzare un pennello sfumatura per riempire una forma con un colore a modifica graduale.</span><span class="sxs-lookup"><span data-stu-id="1de59-104">You can use a gradient brush to fill a shape with a gradually changing color.</span></span> <span data-ttu-id="1de59-105">È ad esempio possibile utilizzare una sfumatura orizzontale per riempire una forma con un colore che cambia gradualmente man mano che si passa dal bordo sinistro della forma al bordo destro.</span><span class="sxs-lookup"><span data-stu-id="1de59-105">For example, you can use a horizontal gradient to fill a shape with color that changes gradually as you move from the left edge of the shape to the right edge.</span></span> <span data-ttu-id="1de59-106">Immaginate un rettangolo con un bordo sinistro nero (rappresentato da componenti rosso, verde e blu 0, 0, 0) e un bordo destro rosso (rappresentato da 255, 0, 0).</span><span class="sxs-lookup"><span data-stu-id="1de59-106">Imagine a rectangle with a left edge that is black (represented by red, green, and blue components 0, 0, 0) and a right edge that is red (represented by 255, 0, 0).</span></span> <span data-ttu-id="1de59-107">Se il rettangolo è 256 pixel di larghezza, il componente rosso di un determinato pixel sarà maggiore di uno rispetto al componente rosso del pixel alla sua sinistra.</span><span class="sxs-lookup"><span data-stu-id="1de59-107">If the rectangle is 256 pixels wide, the red component of a given pixel will be one greater than the red component of the pixel to its left.</span></span> <span data-ttu-id="1de59-108">Il pixel più a sinistra in una riga ha componenti di colore (0, 0, 0), il secondo pixel ha (1, 0, 0), il terzo pixel ha (2, 0, 0) e così via, fino a quando non si arriva al pixel più a destra, che include componenti colore (255, 0, 0).</span><span class="sxs-lookup"><span data-stu-id="1de59-108">The leftmost pixel in a row has color components (0, 0, 0), the second pixel has (1, 0, 0), the third pixel has (2, 0, 0), and so on, until you get to the rightmost pixel, which has color components (255, 0, 0).</span></span> <span data-ttu-id="1de59-109">Questi valori di colore interpolati costituiscono la sfumatura di colore.</span><span class="sxs-lookup"><span data-stu-id="1de59-109">These interpolated color values make up the color gradient.</span></span>

<span data-ttu-id="1de59-110">Una sfumatura lineare cambia colore mentre si sposta orizzontalmente, verticalmente o in parallelo in una linea inclinata specificata.</span><span class="sxs-lookup"><span data-stu-id="1de59-110">A linear gradient changes color as you move horizontally, vertically, or parallel to a specified slanted line.</span></span> <span data-ttu-id="1de59-111">Una sfumatura di tracciato cambia colore mentre si sposta sull'interno e sul limite di un tracciato.</span><span class="sxs-lookup"><span data-stu-id="1de59-111">A path gradient changes color as you move about the interior and boundary of a path.</span></span> <span data-ttu-id="1de59-112">È possibile personalizzare le sfumature del tracciato per ottenere una vasta gamma di effetti.</span><span class="sxs-lookup"><span data-stu-id="1de59-112">You can customize path gradients to achieve a wide variety of effects.</span></span>

<span data-ttu-id="1de59-113">GDI+ fornisce le classi [**LinearGradientBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush) e [**PathGradientBrush**](/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush) , entrambe ereditate dalla classe [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) .</span><span class="sxs-lookup"><span data-stu-id="1de59-113">GDI+ provides the [**LinearGradientBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush) and [**PathGradientBrush**](/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush) classes, both of which inherit from the [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) class.</span></span>

<span data-ttu-id="1de59-114">Negli argomenti seguenti vengono illustrate le sfumature lineari e di percorso in modo più dettagliato:</span><span class="sxs-lookup"><span data-stu-id="1de59-114">The following topics cover linear and path gradients in more detail:</span></span>

-   [<span data-ttu-id="1de59-115">Creazione di una sfumatura lineare</span><span class="sxs-lookup"><span data-stu-id="1de59-115">Creating a Linear Gradient</span></span>](-gdiplus-creating-a-linear-gradient-use.md)
-   [<span data-ttu-id="1de59-116">Creazione di una sfumatura del percorso</span><span class="sxs-lookup"><span data-stu-id="1de59-116">Creating a Path Gradient</span></span>](-gdiplus-creating-a-path-gradient-use.md)
-   [<span data-ttu-id="1de59-117">Applicazione della correzione gamma a una sfumatura</span><span class="sxs-lookup"><span data-stu-id="1de59-117">Applying Gamma Correction to a Gradient</span></span>](-gdiplus-applying-gamma-correction-to-a-gradient-use.md)

 

 



