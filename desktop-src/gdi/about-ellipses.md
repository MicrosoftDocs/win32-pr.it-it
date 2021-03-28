---
description: Un'ellisse è una curva chiusa definita da due punti fissi (F1 e F2), in modo che la somma delle distanze (D1 + D2) da qualsiasi punto sulla curva ai due punti fissi sia costante.
ms.assetid: c4aab4cf-9575-4817-b51f-aed4e3c27d2f
title: Informazioni sugli ellissi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77c6b2774da9886e25d3e1dcca7c701b034e7b45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104564752"
---
# <a name="about-ellipses"></a><span data-ttu-id="07486-103">Informazioni sugli ellissi</span><span class="sxs-lookup"><span data-stu-id="07486-103">About Ellipses</span></span>

<span data-ttu-id="07486-104">Un'ellisse è una curva chiusa definita da due punti fissi (F1 e F2), in modo che la somma delle distanze (D1 + D2) da qualsiasi punto sulla curva ai due punti fissi sia costante.</span><span class="sxs-lookup"><span data-stu-id="07486-104">An ellipse is a closed curve defined by two fixed points (f1 and f2 ) such that the sum of the distances (d1 +d2 ) from any point on the curve to the two fixed points is constant.</span></span> <span data-ttu-id="07486-105">La figura seguente mostra un'ellisse disegnata usando la funzione [**ellisse**](/windows/desktop/api/Wingdi/nf-wingdi-ellipse) .</span><span class="sxs-lookup"><span data-stu-id="07486-105">The following illustration shows an ellipse drawn by using the [**Ellipse**](/windows/desktop/api/Wingdi/nf-wingdi-ellipse) function.</span></span>

![illustrazione che mostra un'ellisse, due punti fissi, due distanze e un rettangolo di delimitazione](images/csfsh-01.png)

<span data-ttu-id="07486-107">Quando si chiama [**ellisse**](/windows/desktop/api/Wingdi/nf-wingdi-ellipse), un'applicazione fornisce le coordinate degli angoli superiore sinistro e inferiore destro del rettangolo di delimitazione dell'ellisse.</span><span class="sxs-lookup"><span data-stu-id="07486-107">When calling [**Ellipse**](/windows/desktop/api/Wingdi/nf-wingdi-ellipse), an application supplies the coordinates of the upper-left and lower-right corners of the ellipse's bounding rectangle.</span></span> <span data-ttu-id="07486-108">Un *rettangolo di delimitazione* è il rettangolo più piccolo che circonda completamente l'ellisse.</span><span class="sxs-lookup"><span data-stu-id="07486-108">A *bounding rectangle* is the smallest rectangle completely surrounding the ellipse.</span></span> <span data-ttu-id="07486-109">Quando il sistema disegna l'ellisse, esclude i lati destro e inferiore se non è impostata alcuna trasformazione mondiale.</span><span class="sxs-lookup"><span data-stu-id="07486-109">When the system draws the ellipse, it excludes the right and lower sides if no world transformations are set.</span></span> <span data-ttu-id="07486-110">Pertanto, per qualsiasi rettangolo che misuri x unità di larghezza per unità y elevate, l'ellisse associata misura X1 unità di larghezza per Y1 unità di altezza.</span><span class="sxs-lookup"><span data-stu-id="07486-110">Therefore, for any rectangle measuring x units wide by y units high, the associated ellipse measures x1 units wide by y1 units high.</span></span> <span data-ttu-id="07486-111">Se l'applicazione imposta una trasformazione globale chiamando la funzione [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) o [**ModifyWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-modifyworldtransform) , il sistema include i lati destro e inferiore.</span><span class="sxs-lookup"><span data-stu-id="07486-111">If the application sets a world transformation by calling the [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) or [**ModifyWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-modifyworldtransform) function, the system includes the right and lower sides.</span></span>

 

 



