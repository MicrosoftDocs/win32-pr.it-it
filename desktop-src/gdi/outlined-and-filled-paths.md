---
description: Un'applicazione può tracciare il contorno di un percorso chiamando la funzione StrokePath, può riempire l'area interna di un percorso chiamando la funzione FillPath ed è in grado di delineare e riempire il percorso chiamando la funzione StrokeAndFillPath.
ms.assetid: e3e82676-3095-43f0-9fb4-959f925e66c2
title: Percorsi delineati e riempiti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 735ee9ee5d7e69922241c5647b883e1800b525e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967058"
---
# <a name="outlined-and-filled-paths"></a><span data-ttu-id="d8761-103">Percorsi delineati e riempiti</span><span class="sxs-lookup"><span data-stu-id="d8761-103">Outlined and Filled Paths</span></span>

<span data-ttu-id="d8761-104">Un'applicazione può tracciare il contorno di un percorso chiamando la funzione [**strokePath**](/windows/desktop/api/Wingdi/nf-wingdi-strokepath) , può riempire l'area interna di un percorso chiamando la funzione [**FillPath**](/windows/desktop/api/Wingdi/nf-wingdi-fillpath) ed è in grado di delineare e riempire il percorso chiamando la funzione [**StrokeAndFillPath**](/windows/desktop/api/Wingdi/nf-wingdi-strokeandfillpath) .</span><span class="sxs-lookup"><span data-stu-id="d8761-104">An application can draw the outline of a path by calling the [**StrokePath**](/windows/desktop/api/Wingdi/nf-wingdi-strokepath) function, it can fill the interior of a path by calling the [**FillPath**](/windows/desktop/api/Wingdi/nf-wingdi-fillpath) function, and it can both outline and fill the path by calling the [**StrokeAndFillPath**](/windows/desktop/api/Wingdi/nf-wingdi-strokeandfillpath) function.</span></span>

<span data-ttu-id="d8761-105">Ogni volta che un'applicazione compila un percorso, il sistema utilizza la modalità di riempimento corrente del controller di dominio.</span><span class="sxs-lookup"><span data-stu-id="d8761-105">Whenever an application fills a path, the system uses the DC's current fill mode.</span></span> <span data-ttu-id="d8761-106">Un'applicazione può recuperare questa modalità chiamando la funzione [**GetPolyFillMode**](/windows/desktop/api/Wingdi/nf-wingdi-getpolyfillmode) e può impostare una nuova modalità di riempimento chiamando la funzione [**SetPolyFillMode**](/windows/desktop/api/Wingdi/nf-wingdi-setpolyfillmode) .</span><span class="sxs-lookup"><span data-stu-id="d8761-106">An application can retrieve this mode by calling the [**GetPolyFillMode**](/windows/desktop/api/Wingdi/nf-wingdi-getpolyfillmode) function, and it can set a new fill mode by calling the [**SetPolyFillMode**](/windows/desktop/api/Wingdi/nf-wingdi-setpolyfillmode) function.</span></span> <span data-ttu-id="d8761-107">Per una descrizione delle due modalità di riempimento, vedere [aree](regions.md).</span><span class="sxs-lookup"><span data-stu-id="d8761-107">For a description of the two fill modes, see [Regions](regions.md).</span></span>

<span data-ttu-id="d8761-108">Nella figura seguente viene illustrata la sezione incrociata di un oggetto creato da un'applicazione di progettazione assistita da computer (CAD) utilizzando percorsi che sono stati entrambi delineati e riempiti.</span><span class="sxs-lookup"><span data-stu-id="d8761-108">The following illustration shows the cross-section of an object created by a computer-aided design (CAD) application using paths that were both outlined and filled.</span></span>

![illustrazione che mostra la visualizzazione tra sezioni di un oggetto, con varie parti indicate da modelli di riempimento diversi](images/cspth-01.png)

 

 



