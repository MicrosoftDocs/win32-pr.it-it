---
title: Uso di controlli ToolTip
description: Questa sezione contiene esempi che illustrano come creare tipi diversi di descrizioni comandi.
ms.assetid: 4486b406-a069-4250-b7ab-671d895b79f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86fd4a0cef452be3f9700f8466959043ac8d30b7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710024"
---
# <a name="using-tooltip-controls"></a><span data-ttu-id="9bd3d-103">Uso di controlli ToolTip</span><span class="sxs-lookup"><span data-stu-id="9bd3d-103">Using Tooltip Controls</span></span>

<span data-ttu-id="9bd3d-104">Questa sezione contiene esempi che illustrano come creare tipi diversi di descrizioni comandi.</span><span class="sxs-lookup"><span data-stu-id="9bd3d-104">This section contains examples that demonstrate how to create different types of tooltips.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="9bd3d-105">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="9bd3d-105">In this section</span></span>



| <span data-ttu-id="9bd3d-106">Argomento</span><span class="sxs-lookup"><span data-stu-id="9bd3d-106">Topic</span></span>                                                                                                    | <span data-ttu-id="9bd3d-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9bd3d-107">Description</span></span>                                                                                                                                                                                                                                                                      |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9bd3d-108">Come creare una descrizione comando per un controllo</span><span class="sxs-lookup"><span data-stu-id="9bd3d-108">How to Create a Tooltip for a Control</span></span>](create-a-tooltip-for-a-control.md)<br/>                   | <span data-ttu-id="9bd3d-109">La funzione di esempio seguente crea una descrizione comando e la associa al controllo il cui ID di risorsa viene passato.</span><span class="sxs-lookup"><span data-stu-id="9bd3d-109">The following example function creates a tooltip and associates it with the control whose resource ID is passed in.</span></span> <br/>                                                                                                                                                  |
| [<span data-ttu-id="9bd3d-110">Come creare una descrizione comando per un'area rettangolare</span><span class="sxs-lookup"><span data-stu-id="9bd3d-110">How to Create a Tooltip for a Rectangular Area</span></span>](create-a-tooltip-for-a-rectangular-area.md)<br/> | <span data-ttu-id="9bd3d-111">Nell'esempio seguente viene illustrato come creare un controllo ToolTip standard per l'intera area client di una finestra.</span><span class="sxs-lookup"><span data-stu-id="9bd3d-111">The following example demonstrates how to create a standard tooltip control for a window's entire client area.</span></span> <br/>                                                                                                                                                       |
| [<span data-ttu-id="9bd3d-112">Come implementare le descrizioni comandi di rilevamento</span><span class="sxs-lookup"><span data-stu-id="9bd3d-112">How to Implement Tracking Tooltips</span></span>](implement-tracking-tooltips.md)<br/>                         | <span data-ttu-id="9bd3d-113">Le descrizioni comandi di rilevamento rimangono visibili fino a quando non vengono chiuse in modo esplicito dall'applicazione e possono modificare la posizione sullo schermo in modo dinamico.</span><span class="sxs-lookup"><span data-stu-id="9bd3d-113">Tracking tooltips remain visible until they are explicitly closed by the application, and can change position on the screen dynamically.</span></span> <span data-ttu-id="9bd3d-114">Sono supportati dalla [versione 4,70](common-control-versions.md) e successive dei controlli comuni.</span><span class="sxs-lookup"><span data-stu-id="9bd3d-114">They are supported by [version 4.70](common-control-versions.md) and later of the common controls.</span></span> <br/>                         |
| [<span data-ttu-id="9bd3d-115">Come implementare descrizioni comandi su più righe</span><span class="sxs-lookup"><span data-stu-id="9bd3d-115">How to Implement Multiline Tooltips</span></span>](implement-multiline-tooltips.md)<br/>                       | <span data-ttu-id="9bd3d-116">Le descrizioni comando su più righe consentono di visualizzare il testo su più di una riga.</span><span class="sxs-lookup"><span data-stu-id="9bd3d-116">Multiline tooltips allow text to be displayed on more than one line.</span></span> <br/>                                                                                                                                                                                                 |
| [<span data-ttu-id="9bd3d-117">Come implementare le descrizioni comandi del fumetto</span><span class="sxs-lookup"><span data-stu-id="9bd3d-117">How to Implement Balloon Tooltips</span></span>](implement-balloon-tooltips.md)<br/>                           | <span data-ttu-id="9bd3d-118">Le descrizioni comandi a fumetti sono simili alle descrizioni comandi standard, ma vengono visualizzate in un "fumetto" di tipo Cartoon con un gambo che punta allo strumento.</span><span class="sxs-lookup"><span data-stu-id="9bd3d-118">Balloon tooltips are similar to standard tooltips, but are displayed in a cartoon-style "balloon" with a stem pointing to the tool.</span></span> <span data-ttu-id="9bd3d-119">Le descrizioni comando a fumetti possono essere a riga singola o a più righe.</span><span class="sxs-lookup"><span data-stu-id="9bd3d-119">Balloon tooltips can be either single-line or multiline.</span></span> <span data-ttu-id="9bd3d-120">Vengono creati e gestiti in modo molto simile alle descrizioni comandi standard.</span><span class="sxs-lookup"><span data-stu-id="9bd3d-120">They are created and handled in much the same way as standard tooltips.</span></span> <br/> |
| [<span data-ttu-id="9bd3d-121">Come implementare le descrizioni comandi per le icone della barra di stato</span><span class="sxs-lookup"><span data-stu-id="9bd3d-121">How to Implement Tooltips for Status Bar Icons</span></span>](implement-tooltips-for-status-bar-icons.md)<br/> | <span data-ttu-id="9bd3d-122">Un modo non intrusivo per visualizzare un messaggio esplicativo per un'icona della barra di stato consiste nell'implementare una descrizione comando.</span><span class="sxs-lookup"><span data-stu-id="9bd3d-122">A nonintrusive way to display an explanatory message for a status bar icon is to implement a tooltip.</span></span> <span data-ttu-id="9bd3d-123">La descrizione comando scompare quando si fa clic, ma è anche possibile specificare un valore di timeout.</span><span class="sxs-lookup"><span data-stu-id="9bd3d-123">The tooltip disappears when clicked, but you can also specify a time-out value.</span></span> <br/>                                                                                |
| [<span data-ttu-id="9bd3d-124">Come implementare In-Place descrizioni comandi</span><span class="sxs-lookup"><span data-stu-id="9bd3d-124">How to Implement In-Place Tooltips</span></span>](implement-in-place-tooltips.md)<br/>                         | <span data-ttu-id="9bd3d-125">Le descrizioni comando sul posto vengono usate per visualizzare le stringhe di testo per gli oggetti che sono stati ritagliati.</span><span class="sxs-lookup"><span data-stu-id="9bd3d-125">In-place tooltips are used to display text strings for objects that have been clipped.</span></span> <span data-ttu-id="9bd3d-126">Per un'illustrazione, vedere [informazioni sui controlli ToolTip](tooltip-controls.md).</span><span class="sxs-lookup"><span data-stu-id="9bd3d-126">For an illustration, see [About Tooltip Controls](tooltip-controls.md).</span></span> <br/>                                                                                                      |



 

 

 





