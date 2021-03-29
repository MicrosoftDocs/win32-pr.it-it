---
description: Windows supporta cinque modalità grafiche che consentono a un'applicazione di specificare la modalità di combinazione dei colori, il modo in cui viene visualizzato l'output, la modalità di ridimensionamento dell'output e così via. Queste modalità, archiviate in un controller di dominio, sono descritte nella tabella seguente.
ms.assetid: 061af47e-fd49-4eb4-9b1b-03eb9c841622
title: Modalità grafica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 823c7e25024eafb3b111b96b97907bc9b772006a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528344"
---
# <a name="graphic-modes"></a><span data-ttu-id="7a10c-104">Modalità grafica</span><span class="sxs-lookup"><span data-stu-id="7a10c-104">Graphic Modes</span></span>

<span data-ttu-id="7a10c-105">Windows supporta cinque modalità grafiche che consentono a un'applicazione di specificare la modalità di combinazione dei colori, il modo in cui viene visualizzato l'output, la modalità di ridimensionamento dell'output e così via.</span><span class="sxs-lookup"><span data-stu-id="7a10c-105">Windows supports five graphic modes that allow an application to specify how colors are mixed, where output appears, how the output is scaled, and so on.</span></span> <span data-ttu-id="7a10c-106">Queste modalità, archiviate in un controller di dominio, sono descritte nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="7a10c-106">These modes, which are stored in a DC, are described in the following table.</span></span>



| <span data-ttu-id="7a10c-107">Modalità grafica</span><span class="sxs-lookup"><span data-stu-id="7a10c-107">Graphics mode</span></span> | <span data-ttu-id="7a10c-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7a10c-108">Description</span></span>                                                                                                                |
|---------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a10c-109">Sfondo</span><span class="sxs-lookup"><span data-stu-id="7a10c-109">Background</span></span>    | <span data-ttu-id="7a10c-110">Definisce la modalità di combinazione dei colori di sfondo con la finestra o i colori dello schermo esistenti per le operazioni bitmap e di testo.</span><span class="sxs-lookup"><span data-stu-id="7a10c-110">Defines how background colors are mixed with existing window or screen colors for bitmap and text operations.</span></span>              |
| <span data-ttu-id="7a10c-111">Disegno</span><span class="sxs-lookup"><span data-stu-id="7a10c-111">Drawing</span></span>       | <span data-ttu-id="7a10c-112">Definisce il modo in cui i colori di primo piano vengono combinati con i colori della finestra o dello schermo esistenti per operazioni di penna, pennello, bitmap e testo.</span><span class="sxs-lookup"><span data-stu-id="7a10c-112">Defines how foreground colors are mixed with existing window or screen colors for pen, brush, bitmap, and text operations.</span></span> |
| <span data-ttu-id="7a10c-113">Mapping</span><span class="sxs-lookup"><span data-stu-id="7a10c-113">Mapping</span></span>       | <span data-ttu-id="7a10c-114">Definisce il modo in cui viene eseguito il mapping dell'output della grafica da uno spazio logico o globale alla finestra, alla schermata o alla stampante.</span><span class="sxs-lookup"><span data-stu-id="7a10c-114">Defines how graphics output is mapped from logical (or world) space onto the window, screen, or printer paper.</span></span>             |
| <span data-ttu-id="7a10c-115">Riempimento poligono</span><span class="sxs-lookup"><span data-stu-id="7a10c-115">Polygon-fill</span></span>  | <span data-ttu-id="7a10c-116">Definisce la modalità di utilizzo del modello di pennello per riempire l'area interna delle aree complesse.</span><span class="sxs-lookup"><span data-stu-id="7a10c-116">Defines how the brush pattern is used to fill the interior of complex regions.</span></span>                                             |
| <span data-ttu-id="7a10c-117">L'estensione</span><span class="sxs-lookup"><span data-stu-id="7a10c-117">Stretching</span></span>    | <span data-ttu-id="7a10c-118">Definisce il modo in cui i colori bitmap vengono combinati con i colori della finestra o dello schermo esistenti quando la bitmap viene compressa (o ridotta).</span><span class="sxs-lookup"><span data-stu-id="7a10c-118">Defines how bitmap colors are mixed with existing window or screen colors when the bitmap is compressed (or scaled down).</span></span>  |



 

<span data-ttu-id="7a10c-119">Come avviene con gli oggetti grafici, il sistema Inizializza un controller di dominio con le modalità grafiche predefinite.</span><span class="sxs-lookup"><span data-stu-id="7a10c-119">As it does with graphic objects, the system initializes a DC with default graphic modes.</span></span> <span data-ttu-id="7a10c-120">Un'applicazione può recuperare ed esaminare queste modalità predefinite chiamando le funzioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="7a10c-120">An application can retrieve and examine these default modes by calling the following functions.</span></span>



| <span data-ttu-id="7a10c-121">Modalità grafica</span><span class="sxs-lookup"><span data-stu-id="7a10c-121">Graphics mode</span></span> | <span data-ttu-id="7a10c-122">Funzione</span><span class="sxs-lookup"><span data-stu-id="7a10c-122">Function</span></span>                                       |
|---------------|------------------------------------------------|
| <span data-ttu-id="7a10c-123">Sfondo</span><span class="sxs-lookup"><span data-stu-id="7a10c-123">Background</span></span>    | [<span data-ttu-id="7a10c-124">**GetBkMode**</span><span class="sxs-lookup"><span data-stu-id="7a10c-124">**GetBkMode**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getbkmode)                 |
| <span data-ttu-id="7a10c-125">Disegno</span><span class="sxs-lookup"><span data-stu-id="7a10c-125">Drawing</span></span>       | [<span data-ttu-id="7a10c-126">**GetROP2**</span><span class="sxs-lookup"><span data-stu-id="7a10c-126">**GetROP2**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getrop2)                     |
| <span data-ttu-id="7a10c-127">Mapping</span><span class="sxs-lookup"><span data-stu-id="7a10c-127">Mapping</span></span>       | [<span data-ttu-id="7a10c-128">**GetMapMode**</span><span class="sxs-lookup"><span data-stu-id="7a10c-128">**GetMapMode**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getmapmode)               |
| <span data-ttu-id="7a10c-129">Riempimento poligono</span><span class="sxs-lookup"><span data-stu-id="7a10c-129">Polygon-fill</span></span>  | [<span data-ttu-id="7a10c-130">**GetPolyFillMode**</span><span class="sxs-lookup"><span data-stu-id="7a10c-130">**GetPolyFillMode**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getpolyfillmode)     |
| <span data-ttu-id="7a10c-131">L'estensione</span><span class="sxs-lookup"><span data-stu-id="7a10c-131">Stretching</span></span>    | [<span data-ttu-id="7a10c-132">**GetStretchBltMode**</span><span class="sxs-lookup"><span data-stu-id="7a10c-132">**GetStretchBltMode**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getstretchbltmode) |



 

<span data-ttu-id="7a10c-133">Un'applicazione può modificare le modalità predefinite chiamando una delle funzioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="7a10c-133">An application can change the default modes by calling one of the following functions.</span></span>



| <span data-ttu-id="7a10c-134">Modalità grafica</span><span class="sxs-lookup"><span data-stu-id="7a10c-134">Graphics mode</span></span> | <span data-ttu-id="7a10c-135">Funzione</span><span class="sxs-lookup"><span data-stu-id="7a10c-135">Function</span></span>                                       |
|---------------|------------------------------------------------|
| <span data-ttu-id="7a10c-136">Sfondo</span><span class="sxs-lookup"><span data-stu-id="7a10c-136">Background</span></span>    | [<span data-ttu-id="7a10c-137">**SetBkMode**</span><span class="sxs-lookup"><span data-stu-id="7a10c-137">**SetBkMode**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-setbkmode)                 |
| <span data-ttu-id="7a10c-138">Disegno</span><span class="sxs-lookup"><span data-stu-id="7a10c-138">Drawing</span></span>       | [<span data-ttu-id="7a10c-139">**SetROP2**</span><span class="sxs-lookup"><span data-stu-id="7a10c-139">**SetROP2**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-setrop2)                     |
| <span data-ttu-id="7a10c-140">Mapping</span><span class="sxs-lookup"><span data-stu-id="7a10c-140">Mapping</span></span>       | [<span data-ttu-id="7a10c-141">**SetMapMode**</span><span class="sxs-lookup"><span data-stu-id="7a10c-141">**SetMapMode**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-setmapmode)               |
| <span data-ttu-id="7a10c-142">Riempimento poligono</span><span class="sxs-lookup"><span data-stu-id="7a10c-142">Polygon-fill</span></span>  | [<span data-ttu-id="7a10c-143">**SetPolyFillMode**</span><span class="sxs-lookup"><span data-stu-id="7a10c-143">**SetPolyFillMode**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-setpolyfillmode)     |
| <span data-ttu-id="7a10c-144">L'estensione</span><span class="sxs-lookup"><span data-stu-id="7a10c-144">Stretching</span></span>    | [<span data-ttu-id="7a10c-145">**SetStretchBltMode**</span><span class="sxs-lookup"><span data-stu-id="7a10c-145">**SetStretchBltMode**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-setstretchbltmode) |



 

 

 



