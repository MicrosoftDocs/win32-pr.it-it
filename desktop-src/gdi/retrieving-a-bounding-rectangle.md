---
description: Un'applicazione recupera le dimensioni del rettangolo di delimitazione di un'area chiamando la funzione GetRgnBox.
ms.assetid: 3851d0f4-33ec-44db-9cb8-c2afb03ffc25
title: Recupero di un rettangolo di delimitazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b214a3f2e8d4fcd81e7f03ecf6dddc72442e209b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103754306"
---
# <a name="retrieving-a-bounding-rectangle"></a><span data-ttu-id="dfc0e-103">Recupero di un rettangolo di delimitazione</span><span class="sxs-lookup"><span data-stu-id="dfc0e-103">Retrieving a Bounding Rectangle</span></span>

<span data-ttu-id="dfc0e-104">Un'applicazione recupera le dimensioni del rettangolo di delimitazione di un'area chiamando la funzione [**GetRgnBox**](/windows/desktop/api/Wingdi/nf-wingdi-getrgnbox) .</span><span class="sxs-lookup"><span data-stu-id="dfc0e-104">An application retrieves the dimensions of a region's bounding rectangle by calling the [**GetRgnBox**](/windows/desktop/api/Wingdi/nf-wingdi-getrgnbox) function.</span></span> <span data-ttu-id="dfc0e-105">Se l'area è rettangolare, **GetRgnBox** restituisce le dimensioni dell'area.</span><span class="sxs-lookup"><span data-stu-id="dfc0e-105">If the region is rectangular, **GetRgnBox** returns the dimensions of the region.</span></span> <span data-ttu-id="dfc0e-106">Se l'area è ellittica, la funzione restituisce le dimensioni del rettangolo più piccolo che può essere tracciato intorno all'ellisse.</span><span class="sxs-lookup"><span data-stu-id="dfc0e-106">If the region is elliptical, the function returns the dimensions of the smallest rectangle that can be drawn around the ellipse.</span></span> <span data-ttu-id="dfc0e-107">I lati lunghi del rettangolo hanno la stessa lunghezza dell'asse principale dell'ellisse e i lati corti del rettangolo hanno la stessa lunghezza dell'asse secondario dell'ellisse.</span><span class="sxs-lookup"><span data-stu-id="dfc0e-107">The long sides of the rectangle are the same length as the ellipse's major axis, and the short sides of the rectangle are the same length as the ellipse's minor axis.</span></span> <span data-ttu-id="dfc0e-108">Se l'area è poligonale, **GetRgnBox** restituisce le dimensioni del rettangolo più piccolo che può essere tracciato intorno all'intero poligono.</span><span class="sxs-lookup"><span data-stu-id="dfc0e-108">If the region is polygonal, **GetRgnBox** returns the dimensions of the smallest rectangle that can be drawn around the entire polygon.</span></span>

 

 



