---
title: Oggetto PropertySheet
description: Oggetto PropertySheet
ms.assetid: 9d15d198-a4fe-4c05-a7be-0807a179cd9c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90ae4ded2625440ba34170df605b60287f105800
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104116792"
---
# <a name="the-propertysheet-object"></a><span data-ttu-id="46470-103">Oggetto PropertySheet</span><span class="sxs-lookup"><span data-stu-id="46470-103">The PropertySheet Object</span></span>

<span data-ttu-id="46470-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="46470-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="46470-105">L'oggetto [**PropertySheet**](https://www.bing.com/search?q=**PropertySheet**) fornisce diverse proprietà che è possibile usare se si vuole modificare il carattere relativo alla finestra delle proprietà di Microsoft Agent, nota anche come finestra Opzioni carattere avanzate.</span><span class="sxs-lookup"><span data-stu-id="46470-105">The [**PropertySheet**](https://www.bing.com/search?q=**PropertySheet**) object provides several properties you can use if you want to manipulate the character relative to the Microsoft Agent property sheet (also known as the Advanced Character Options window).</span></span>

-   [<span data-ttu-id="46470-106">**Altezza**</span><span class="sxs-lookup"><span data-stu-id="46470-106">**Height**</span></span>](height-property-pso.md)
-   [<span data-ttu-id="46470-107">**Sinistra**</span><span class="sxs-lookup"><span data-stu-id="46470-107">**Left**</span></span>](left-property-pso.md)
-   [<span data-ttu-id="46470-108">**Page**</span><span class="sxs-lookup"><span data-stu-id="46470-108">**Page**</span></span>](page-property.md)
-   [<span data-ttu-id="46470-109">**In alto**</span><span class="sxs-lookup"><span data-stu-id="46470-109">**Top**</span></span>](top-property-pso.md)
-   [<span data-ttu-id="46470-110">**Visible**</span><span class="sxs-lookup"><span data-stu-id="46470-110">**Visible**</span></span>](visible-property.md)
-   [<span data-ttu-id="46470-111">**Larghezza**</span><span class="sxs-lookup"><span data-stu-id="46470-111">**Width**</span></span>](width-property-pso.md)

<span data-ttu-id="46470-112">Se si esegue una query sulle proprietà [**Height**](height-property-pso.md), [**Left**](left-property-pso.md), [**Top**](top-property-pso.md)e [**Width**](width-property-pso.md) prima che la finestra delle proprietà venga mai visualizzata, i relativi valori vengono restituiti come zero (0).</span><span class="sxs-lookup"><span data-stu-id="46470-112">If you query [**Height**](height-property-pso.md), [**Left**](left-property-pso.md), [**Top**](top-property-pso.md), and [**Width**](width-property-pso.md) properties before the property sheet has ever been shown, their values return as zero (0).</span></span> <span data-ttu-id="46470-113">Una volta visualizzate, queste proprietà restituiscono l'ultima posizione e le dimensioni della finestra (rispetto alla risoluzione dello schermo corrente).</span><span class="sxs-lookup"><span data-stu-id="46470-113">Once shown, these properties return the last position and size of the window (relative to your current screen resolution).</span></span>

 

 




