---
description: Le penne, i pennelli, le bitmap, le tavolozze, le aree e i percorsi associati a un controller di dominio sono detti oggetti grafici. Gli attributi seguenti sono associati a ognuno di questi oggetti.
ms.assetid: 95c82efa-257e-4718-9853-7ef10cdfd76c
title: Oggetti grafici
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b80aadcb0988e7bd64910d04ecfbf6ec608845d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104993984"
---
# <a name="graphic-objects"></a><span data-ttu-id="b640e-104">Oggetti grafici</span><span class="sxs-lookup"><span data-stu-id="b640e-104">Graphic Objects</span></span>

<span data-ttu-id="b640e-105">Le penne, i pennelli, le bitmap, le tavolozze, le aree e i percorsi associati a un controller di dominio sono detti oggetti grafici.</span><span class="sxs-lookup"><span data-stu-id="b640e-105">The pen, brush, bitmap, palette, region, and path associated with a DC are referred to as its graphic objects.</span></span> <span data-ttu-id="b640e-106">Gli attributi seguenti sono associati a ognuno di questi oggetti.</span><span class="sxs-lookup"><span data-stu-id="b640e-106">The following attributes are associated with each of these objects.</span></span>



| <span data-ttu-id="b640e-107">Oggetto grafico</span><span class="sxs-lookup"><span data-stu-id="b640e-107">Graphic object</span></span> | <span data-ttu-id="b640e-108">Attributi associati</span><span class="sxs-lookup"><span data-stu-id="b640e-108">Associated attributes</span></span>                                                               |
|----------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b640e-109">Bitmap</span><span class="sxs-lookup"><span data-stu-id="b640e-109">Bitmap</span></span>         | <span data-ttu-id="b640e-110">Dimensioni, in byte; dimensioni, in pixel; formato colore; schema di compressione; E così via.</span><span class="sxs-lookup"><span data-stu-id="b640e-110">Size, in bytes; dimensions, in pixels; color-format; compression scheme; and so on.</span></span> |
| <span data-ttu-id="b640e-111">Brush</span><span class="sxs-lookup"><span data-stu-id="b640e-111">Brush</span></span>          | <span data-ttu-id="b640e-112">Stile, colore, motivo e origine.</span><span class="sxs-lookup"><span data-stu-id="b640e-112">Style, color, pattern, and origin.</span></span>                                                  |
| <span data-ttu-id="b640e-113">Tavolozza</span><span class="sxs-lookup"><span data-stu-id="b640e-113">Palette</span></span>        | <span data-ttu-id="b640e-114">Colori e dimensioni (o numero di colori).</span><span class="sxs-lookup"><span data-stu-id="b640e-114">Colors and size (or number of colors).</span></span>                                              |
| <span data-ttu-id="b640e-115">Carattere</span><span class="sxs-lookup"><span data-stu-id="b640e-115">Font</span></span>           | <span data-ttu-id="b640e-116">Nome tipografico, larghezza, altezza, peso, set di caratteri e così via.</span><span class="sxs-lookup"><span data-stu-id="b640e-116">Typeface name, width, height, weight, character set, and so on.</span></span>                     |
| <span data-ttu-id="b640e-117">Percorso</span><span class="sxs-lookup"><span data-stu-id="b640e-117">Path</span></span>           | <span data-ttu-id="b640e-118">Forma.</span><span class="sxs-lookup"><span data-stu-id="b640e-118">Shape.</span></span>                                                                              |
| <span data-ttu-id="b640e-119">Penna</span><span class="sxs-lookup"><span data-stu-id="b640e-119">Pen</span></span>            | <span data-ttu-id="b640e-120">Stile, larghezza e colore.</span><span class="sxs-lookup"><span data-stu-id="b640e-120">Style, width, and color.</span></span>                                                            |
| <span data-ttu-id="b640e-121">Region</span><span class="sxs-lookup"><span data-stu-id="b640e-121">Region</span></span>         | <span data-ttu-id="b640e-122">Posizione e dimensioni.</span><span class="sxs-lookup"><span data-stu-id="b640e-122">Location and dimensions.</span></span>                                                            |



 

<span data-ttu-id="b640e-123">Quando un'applicazione crea un controller di dominio, il sistema archivia automaticamente un set di oggetti predefiniti (non esiste alcuna bitmap o percorso predefinito).</span><span class="sxs-lookup"><span data-stu-id="b640e-123">When an application creates a DC, the system automatically stores a set of default objects in it (there is no default bitmap or path).</span></span> <span data-ttu-id="b640e-124">Un'applicazione può esaminare gli attributi degli oggetti predefiniti chiamando le funzioni [**GetCurrentObject**](/windows/desktop/api/Wingdi/nf-wingdi-getcurrentobject) e [**GetObject**](/windows/desktop/api/Wingdi/nf-wingdi-getobject) .</span><span class="sxs-lookup"><span data-stu-id="b640e-124">An application can examine the attributes of the default objects by calling the [**GetCurrentObject**](/windows/desktop/api/Wingdi/nf-wingdi-getcurrentobject) and [**GetObject**](/windows/desktop/api/Wingdi/nf-wingdi-getobject) functions.</span></span> <span data-ttu-id="b640e-125">L'applicazione può modificare queste impostazioni predefinite creando un nuovo oggetto e selezionandolo nel controller di dominio.</span><span class="sxs-lookup"><span data-stu-id="b640e-125">The application can change these defaults by creating a new object and selecting it into the DC.</span></span> <span data-ttu-id="b640e-126">Un oggetto viene selezionato in un controller di dominio chiamando la funzione [**SelezionaOggetto**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) .</span><span class="sxs-lookup"><span data-stu-id="b640e-126">An object is selected into a DC by calling the [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) function.</span></span>

<span data-ttu-id="b640e-127">Un'applicazione può impostare il colore corrente del pennello su un valore di colore specificato con [**SetDCBrushColor**](/windows/desktop/api/Wingdi/nf-wingdi-setdcbrushcolor).</span><span class="sxs-lookup"><span data-stu-id="b640e-127">An application can set the current brush color to a specified color value with [**SetDCBrushColor**](/windows/desktop/api/Wingdi/nf-wingdi-setdcbrushcolor).</span></span>

<span data-ttu-id="b640e-128">La funzione [**GetDCBrushColor**](/windows/desktop/api/WinGdi/nf-wingdi-getdcbrushcolor) restituisce il colore del pennello del controller di dominio.</span><span class="sxs-lookup"><span data-stu-id="b640e-128">The [**GetDCBrushColor**](/windows/desktop/api/WinGdi/nf-wingdi-getdcbrushcolor) function returns the DC brush color.</span></span> <span data-ttu-id="b640e-129">La funzione [**SetDCPenColor**](/windows/desktop/api/Wingdi/nf-wingdi-setdcpencolor) imposta il colore della penna su un valore di colore specificato.</span><span class="sxs-lookup"><span data-stu-id="b640e-129">The [**SetDCPenColor**](/windows/desktop/api/Wingdi/nf-wingdi-setdcpencolor) function sets the pen color to a specified color value.</span></span> <span data-ttu-id="b640e-130">La funzione [**GetDCPenColor**](/windows/desktop/api/WinGdi/nf-wingdi-getdcpencolor) restituisce il colore della penna del controller di dominio.</span><span class="sxs-lookup"><span data-stu-id="b640e-130">The [**GetDCPenColor**](/windows/desktop/api/WinGdi/nf-wingdi-getdcpencolor) function returns the DC pen color.</span></span>

 

 



