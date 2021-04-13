---
description: Un'applicazione crea un'area chiamando una funzione associata a una forma specifica. Nella tabella seguente vengono illustrate le funzioni associate a ognuna delle forme standard.
ms.assetid: e94ae371-8365-4e42-ac8c-04c3928fcffb
title: Creazione e selezione dell'area
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d27a7887e41a04a62015fa3fc9d82f5beeb01d6a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978351"
---
# <a name="region-creation-and-selection"></a><span data-ttu-id="1c263-104">Creazione e selezione dell'area</span><span class="sxs-lookup"><span data-stu-id="1c263-104">Region Creation and Selection</span></span>

<span data-ttu-id="1c263-105">Un'applicazione crea un'area chiamando una funzione associata a una forma specifica.</span><span class="sxs-lookup"><span data-stu-id="1c263-105">An application creates a region by calling a function associated with a specific shape.</span></span> <span data-ttu-id="1c263-106">Nella tabella seguente vengono illustrate le funzioni associate a ognuna delle forme standard.</span><span class="sxs-lookup"><span data-stu-id="1c263-106">The following table shows the function(s) associated with each of the standard shapes.</span></span>



| <span data-ttu-id="1c263-107">Con forme</span><span class="sxs-lookup"><span data-stu-id="1c263-107">Shape</span></span>                                   | <span data-ttu-id="1c263-108">Funzione</span><span class="sxs-lookup"><span data-stu-id="1c263-108">Function</span></span>                                                                                                                         |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c263-109">Area rettangolare</span><span class="sxs-lookup"><span data-stu-id="1c263-109">Rectangular region</span></span>                      | <span data-ttu-id="1c263-110">[**CreateRectRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createrectrgn), [**CreateRectRgnIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createrectrgnindirect), [**SetRectRgn**](/windows/desktop/api/Wingdi/nf-wingdi-setrectrgn)</span><span class="sxs-lookup"><span data-stu-id="1c263-110">[**CreateRectRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createrectrgn), [**CreateRectRgnIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createrectrgnindirect), [**SetRectRgn**](/windows/desktop/api/Wingdi/nf-wingdi-setrectrgn)</span></span> |
| <span data-ttu-id="1c263-111">Area rettangolare con angoli arrotondati</span><span class="sxs-lookup"><span data-stu-id="1c263-111">Rectangular region with rounded corners</span></span> | [<span data-ttu-id="1c263-112">**CreateRoundRectRgn**</span><span class="sxs-lookup"><span data-stu-id="1c263-112">**CreateRoundRectRgn**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-createroundrectrgn)                                                                                 |
| <span data-ttu-id="1c263-113">Area ellittica</span><span class="sxs-lookup"><span data-stu-id="1c263-113">Elliptical region</span></span>                       | <span data-ttu-id="1c263-114">[**CreateEllipticRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createellipticrgn), [ **CreateEllipticRgnIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createellipticrgnindirect)</span><span class="sxs-lookup"><span data-stu-id="1c263-114">[**CreateEllipticRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createellipticrgn), [**CreateEllipticRgnIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createellipticrgnindirect)</span></span>                   |
| <span data-ttu-id="1c263-115">Area poligonale</span><span class="sxs-lookup"><span data-stu-id="1c263-115">Polygonal region</span></span>                        | <span data-ttu-id="1c263-116">[**CreatePolygonRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createpolygonrgn), [ **CreatePolyPolygonRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createpolypolygonrgn)</span><span class="sxs-lookup"><span data-stu-id="1c263-116">[**CreatePolygonRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createpolygonrgn), [**CreatePolyPolygonRgn**](/windows/desktop/api/Wingdi/nf-wingdi-createpolypolygonrgn)</span></span>                               |



 

<span data-ttu-id="1c263-117">Ogni funzione di creazione dell'area restituisce un handle che identifica la nuova area.</span><span class="sxs-lookup"><span data-stu-id="1c263-117">Each region creation function returns a handle that identifies the new region.</span></span> <span data-ttu-id="1c263-118">Un'applicazione può usare questo handle per selezionare l'area in un contesto di dispositivo chiamando la funzione [**SelezionaOggetto**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) e specificando questo handle come secondo argomento.</span><span class="sxs-lookup"><span data-stu-id="1c263-118">An application can use this handle to select the region into a device context by calling the [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) function and supplying this handle as the second argument.</span></span> <span data-ttu-id="1c263-119">Dopo aver selezionato un'area in un contesto di dispositivo, l'applicazione può eseguire varie operazioni su di essa.</span><span class="sxs-lookup"><span data-stu-id="1c263-119">After a region is selected into a device context, the application can perform various operations on it.</span></span>

 

 



