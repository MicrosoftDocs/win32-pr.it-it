---
description: È possibile creare l'inizio o la fine di una riga in una delle diverse forme denominate Caps di riga. Windows GDI+ supporta diversi limiti di riga, ad esempio round, Square, Diamond e Arrowhead.
ms.assetid: c9d90114-3913-486c-a808-b08dd473d9a1
title: Disegno di una linea con estremità di riga
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50ee4dd12a3068fe5200e0f1ae786765170ccba7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104987674"
---
# <a name="drawing-a-line-with-line-caps"></a><span data-ttu-id="e26be-104">Disegno di una linea con estremità di riga</span><span class="sxs-lookup"><span data-stu-id="e26be-104">Drawing a Line with Line Caps</span></span>

<span data-ttu-id="e26be-105">È possibile creare l'inizio o la fine di una riga in una delle diverse forme denominate Caps di riga.</span><span class="sxs-lookup"><span data-stu-id="e26be-105">You can draw the start or end of a line in one of several shapes called line caps.</span></span> <span data-ttu-id="e26be-106">Windows GDI+ supporta diversi limiti di riga, ad esempio round, Square, Diamond e Arrowhead.</span><span class="sxs-lookup"><span data-stu-id="e26be-106">Windows GDI+ supports several line caps, such as round, square, diamond, and arrowhead.</span></span>

<span data-ttu-id="e26be-107">È possibile specificare i limiti di riga per l'inizio di una riga (Cap iniziale), la fine di una riga (estremità finale) o i trattini di una linea tratteggiata (limite del trattino).</span><span class="sxs-lookup"><span data-stu-id="e26be-107">You can specify line caps for the start of a line (start cap), the end of a line (end cap), or the dashes of a dashed line (dash cap).</span></span>

<span data-ttu-id="e26be-108">Nell'esempio seguente viene disegnata una linea con una freccia a un'estremità e un arrotondamento all'altra estremità:</span><span class="sxs-lookup"><span data-stu-id="e26be-108">The following example draws a line with an arrowhead at one end and a round cap at the other end:</span></span>


```
Pen pen(Color(255, 0, 0, 255), 8);
stat = pen.SetStartCap(LineCapArrowAnchor);
stat = pen.SetEndCap(LineCapRoundAnchor);
stat = graphics.DrawLine(&pen, 20, 175, 300, 175);
```



<span data-ttu-id="e26be-109">Nella figura seguente viene illustrata la riga risultante.</span><span class="sxs-lookup"><span data-stu-id="e26be-109">The following illustration shows the resulting line.</span></span>

![illustrazione che mostra una linea orizzontale con una freccia a sinistra e un cerchio all'estremità destra](images/pens4.png)

<span data-ttu-id="e26be-111">**LineCapArrowAnchor** e **LineCapRoundAnchor** sono elementi dell'enumerazione [**estremità**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-linecap) .</span><span class="sxs-lookup"><span data-stu-id="e26be-111">**LineCapArrowAnchor** and **LineCapRoundAnchor** are elements of the [**LineCap**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-linecap) enumeration.</span></span>

 

 



