---
description: Le funzioni seguenti vengono utilizzate con i pennelli.
ms.assetid: 617eb778-876c-4bbb-90da-c5f13359becb
title: Funzioni pennello (Windows GDI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2170ff5c4b743e19da669bd76b340ca95ac2ef9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528393"
---
# <a name="brush-functions-windows-gdi"></a><span data-ttu-id="e9cdd-103">Funzioni pennello (Windows GDI)</span><span class="sxs-lookup"><span data-stu-id="e9cdd-103">Brush Functions (Windows GDI)</span></span>

<span data-ttu-id="e9cdd-104">Le funzioni seguenti vengono utilizzate con i pennelli.</span><span class="sxs-lookup"><span data-stu-id="e9cdd-104">The following functions are used with brushes.</span></span>



| <span data-ttu-id="e9cdd-105">Funzione</span><span class="sxs-lookup"><span data-stu-id="e9cdd-105">Function</span></span>                                                   | <span data-ttu-id="e9cdd-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e9cdd-106">Description</span></span>                                                |
|------------------------------------------------------------|------------------------------------------------------------|
| [<span data-ttu-id="e9cdd-107">**CreateBrushIndirect**</span><span class="sxs-lookup"><span data-stu-id="e9cdd-107">**CreateBrushIndirect**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-createbrushindirect)         | <span data-ttu-id="e9cdd-108">Crea un pennello con lo stile, il colore e il modello specificati.</span><span class="sxs-lookup"><span data-stu-id="e9cdd-108">Creates a brush with a specified style, color, and pattern</span></span> |
| [<span data-ttu-id="e9cdd-109">**CreateDIBPatternBrushPt**</span><span class="sxs-lookup"><span data-stu-id="e9cdd-109">**CreateDIBPatternBrushPt**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-createdibpatternbrushpt) | <span data-ttu-id="e9cdd-110">Crea un pennello con il modello da una DIB</span><span class="sxs-lookup"><span data-stu-id="e9cdd-110">Creates a brush with the pattern from a DIB</span></span>                |
| [<span data-ttu-id="e9cdd-111">**CreateHatchBrush**</span><span class="sxs-lookup"><span data-stu-id="e9cdd-111">**CreateHatchBrush**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-createhatchbrush)               | <span data-ttu-id="e9cdd-112">Crea un pennello con un motivo di tratteggio e un colore</span><span class="sxs-lookup"><span data-stu-id="e9cdd-112">Creates a brush with a hatch pattern and color</span></span>             |
| [<span data-ttu-id="e9cdd-113">**CreatePatternBrush**</span><span class="sxs-lookup"><span data-stu-id="e9cdd-113">**CreatePatternBrush**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-createpatternbrush)           | <span data-ttu-id="e9cdd-114">Crea un pennello con un modello bitmap</span><span class="sxs-lookup"><span data-stu-id="e9cdd-114">Creates a brush with a bitmap pattern</span></span>                      |
| [<span data-ttu-id="e9cdd-115">**CreateSolidBrush**</span><span class="sxs-lookup"><span data-stu-id="e9cdd-115">**CreateSolidBrush**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-createsolidbrush)               | <span data-ttu-id="e9cdd-116">Crea un pennello con un colore a tinta unita</span><span class="sxs-lookup"><span data-stu-id="e9cdd-116">Creates a brush with a solid color</span></span>                         |
| [<span data-ttu-id="e9cdd-117">**GetBrushOrgEx**</span><span class="sxs-lookup"><span data-stu-id="e9cdd-117">**GetBrushOrgEx**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getbrushorgex)                     | <span data-ttu-id="e9cdd-118">Ottiene l'origine del pennello per un contesto di dispositivo</span><span class="sxs-lookup"><span data-stu-id="e9cdd-118">Gets the brush origin for a device context</span></span>                 |
| [<span data-ttu-id="e9cdd-119">**GetSysColorBrush**</span><span class="sxs-lookup"><span data-stu-id="e9cdd-119">**GetSysColorBrush**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getsyscolorbrush)               | <span data-ttu-id="e9cdd-120">Ottiene un handle per un pennello che corrisponde a un indice colori</span><span class="sxs-lookup"><span data-stu-id="e9cdd-120">Gets a handle to a brush that corresponds to a color index</span></span> |
| [<span data-ttu-id="e9cdd-121">**PatBlt**</span><span class="sxs-lookup"><span data-stu-id="e9cdd-121">**PatBlt**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-patblt)                                   | <span data-ttu-id="e9cdd-122">Disegna un rettangolo</span><span class="sxs-lookup"><span data-stu-id="e9cdd-122">Paints a rectangle</span></span>                                         |
| [<span data-ttu-id="e9cdd-123">**SetBrushOrgEx**</span><span class="sxs-lookup"><span data-stu-id="e9cdd-123">**SetBrushOrgEx**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-setbrushorgex)                     | <span data-ttu-id="e9cdd-124">Imposta l'origine del pennello per un contesto di dispositivo</span><span class="sxs-lookup"><span data-stu-id="e9cdd-124">Sets the brush origin for a device context</span></span>                 |
| [<span data-ttu-id="e9cdd-125">**SetDCBrushColor**</span><span class="sxs-lookup"><span data-stu-id="e9cdd-125">**SetDCBrushColor**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-setdcbrushcolor)                 | <span data-ttu-id="e9cdd-126">Imposta il colore corrente del pennello del contesto di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e9cdd-126">Sets the current device context brush color.</span></span>               |



 

## <a name="obsolete-functions"></a><span data-ttu-id="e9cdd-127">Funzioni obsolete</span><span class="sxs-lookup"><span data-stu-id="e9cdd-127">Obsolete Functions</span></span>

<span data-ttu-id="e9cdd-128">Le funzioni seguenti vengono fornite solo per la compatibilità con le versioni di Windows a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="e9cdd-128">The following functions are provided only for compatibility with 16-bit versions of Windows.</span></span>

[<span data-ttu-id="e9cdd-129">**CreateDIBPatternBrush**</span><span class="sxs-lookup"><span data-stu-id="e9cdd-129">**CreateDIBPatternBrush**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-createdibpatternbrush)

 

 



