---
title: Metodi IPaper
description: Fornisce oggetti della cocarta controllati principalmente dall'interfaccia IPaper nativa.
ms.assetid: 3b77a6b3-8ec3-4a91-82cd-1f08d10fbf73
keywords:
- IPaper
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f84153c9fcec021d9084807d73d46198e3a56482
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221972"
---
# <a name="ipaper-methods"></a><span data-ttu-id="2726d-104">Metodi IPaper</span><span class="sxs-lookup"><span data-stu-id="2726d-104">IPaper Methods</span></span>

<span data-ttu-id="2726d-105">**StoServe** fornisce oggetti della cocarta controllati principalmente dall'interfaccia **iPaper** nativa.</span><span class="sxs-lookup"><span data-stu-id="2726d-105">**StoServe** provides COPaper objects that are controlled primarily by their native **IPaper** interface.</span></span>

<span data-ttu-id="2726d-106">La tabella seguente elenca i metodi **iPaper** da iPaper. H nella directory di pari livello \\ Inc.</span><span class="sxs-lookup"><span data-stu-id="2726d-106">The following table lists **IPaper** methods from IPAPER.H in the sibling \\INC directory.</span></span>



| <span data-ttu-id="2726d-107">Metodo</span><span class="sxs-lookup"><span data-stu-id="2726d-107">Method</span></span>    | <span data-ttu-id="2726d-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2726d-108">Description</span></span>                                                         |
|-----------|---------------------------------------------------------------------|
| <span data-ttu-id="2726d-109">InitPaper</span><span class="sxs-lookup"><span data-stu-id="2726d-109">InitPaper</span></span> | <span data-ttu-id="2726d-110">Inizializza l'oggetto paper e crea una matrice di dati Ink.</span><span class="sxs-lookup"><span data-stu-id="2726d-110">Initializes paper object and create ink data array.</span></span>                 |
| <span data-ttu-id="2726d-111">Lock</span><span class="sxs-lookup"><span data-stu-id="2726d-111">Lock</span></span>      | <span data-ttu-id="2726d-112">Fornisce il controllo client del documento e blocca altri client.</span><span class="sxs-lookup"><span data-stu-id="2726d-112">Gives client control of the paper and locks out other clients.</span></span>      |
| <span data-ttu-id="2726d-113">Sblocca</span><span class="sxs-lookup"><span data-stu-id="2726d-113">Unlock</span></span>    | <span data-ttu-id="2726d-114">Cede il controllo client del documento.</span><span class="sxs-lookup"><span data-stu-id="2726d-114">Relinquishes client control of the paper.</span></span>                           |
| <span data-ttu-id="2726d-115">Caricamento</span><span class="sxs-lookup"><span data-stu-id="2726d-115">Load</span></span>      | <span data-ttu-id="2726d-116">Carica il contenuto della carta dal file composto del client e invia notifiche ai sink.</span><span class="sxs-lookup"><span data-stu-id="2726d-116">Loads paper content from client's compound file and notifies sinks.</span></span> |
| <span data-ttu-id="2726d-117">Salva</span><span class="sxs-lookup"><span data-stu-id="2726d-117">Save</span></span>      | <span data-ttu-id="2726d-118">Salva il contenuto della carta nel file composto del client.</span><span class="sxs-lookup"><span data-stu-id="2726d-118">Saves paper content to client's compound file.</span></span>                      |
| <span data-ttu-id="2726d-119">InkStart</span><span class="sxs-lookup"><span data-stu-id="2726d-119">InkStart</span></span>  | <span data-ttu-id="2726d-120">Avvia il disegno dell'input penna sulla superficie della carta.</span><span class="sxs-lookup"><span data-stu-id="2726d-120">Starts color ink drawing to the paper surface.</span></span>                      |
| <span data-ttu-id="2726d-121">InkDraw</span><span class="sxs-lookup"><span data-stu-id="2726d-121">InkDraw</span></span>   | <span data-ttu-id="2726d-122">Inserisce i punti dati dell'input penna sull'area della carta elettronica.</span><span class="sxs-lookup"><span data-stu-id="2726d-122">Puts ink data points on the electronic paper surface.</span></span>               |
| <span data-ttu-id="2726d-123">InkStop</span><span class="sxs-lookup"><span data-stu-id="2726d-123">InkStop</span></span>   | <span data-ttu-id="2726d-124">Arresta il disegno dell'input penna sull'area della carta.</span><span class="sxs-lookup"><span data-stu-id="2726d-124">Stops ink drawing to the paper surface.</span></span>                             |
| <span data-ttu-id="2726d-125">Cancellazione</span><span class="sxs-lookup"><span data-stu-id="2726d-125">Erase</span></span>     | <span data-ttu-id="2726d-126">Cancellare il contenuto della carta corrente e notificare i sink.</span><span class="sxs-lookup"><span data-stu-id="2726d-126">Erase the current paper content and notifies sinks.</span></span>                 |
| <span data-ttu-id="2726d-127">Ridimensionamento</span><span class="sxs-lookup"><span data-stu-id="2726d-127">Resize</span></span>    | <span data-ttu-id="2726d-128">Ridimensiona le dimensioni del rettangolo della carta di disegno e invia notifiche ai sink.</span><span class="sxs-lookup"><span data-stu-id="2726d-128">Resizes the drawing paper rectangle size and notifies sinks.</span></span>        |
| <span data-ttu-id="2726d-129">Nuovo disegno</span><span class="sxs-lookup"><span data-stu-id="2726d-129">Redraw</span></span>    | <span data-ttu-id="2726d-130">Ritrae il contenuto dell'oggetto carta e notifica i sink.</span><span class="sxs-lookup"><span data-stu-id="2726d-130">Redraws contents of paper object and notifies sinks.</span></span>                |



 

<span data-ttu-id="2726d-131">I metodi di interesse per questo esempio di codice sui file composti sono [**Load**](ipaper--load.md), [**Save**](ipaper--save.md)e reload [**.**](ipaper--redraw.md)</span><span class="sxs-lookup"><span data-stu-id="2726d-131">Methods of interest for this code sample on compound files are [**Load**](ipaper--load.md), [**Save**](ipaper--save.md), and [**Redraw**](ipaper--redraw.md).</span></span>

<span data-ttu-id="2726d-132">[**InkStart**](inkstart-method.md), [**InkDraw**](inkdraw-method.md)e [**InkStop**](cguipaper-methods.md) sono metodi usati dai client per eseguire il comando di un foglio di lavoro per registrare le sequenze di disegno input penna.</span><span class="sxs-lookup"><span data-stu-id="2726d-132">[**InkStart**](inkstart-method.md), [**InkDraw**](inkdraw-method.md), and [**InkStop**](cguipaper-methods.md) are methods used by clients to command COPaper to record ink drawing sequences.</span></span> <span data-ttu-id="2726d-133">Il client risponde in genere a un \_ messaggio WM LBUTTONDOWN come inizio di una sequenza di disegno dell'input penna chiamando **InkStart** su un documento.</span><span class="sxs-lookup"><span data-stu-id="2726d-133">The client will typically respond to a WM\_LBUTTONDOWN message as the start of an ink drawing sequence by calling **InkStart** on COPaper.</span></span> <span data-ttu-id="2726d-134">Quando l'utente sposta il mouse o la penna da creare tenendo premuto il pulsante sinistro, il client risponderà ai messaggi di WM MOUSEMOVE ripetuti \_ con le chiamate corrispondenti a **InkDraw**.</span><span class="sxs-lookup"><span data-stu-id="2726d-134">As the user moves the mouse or pen to draw while holding down the left button, the client will respond to repeated WM\_MOUSEMOVE messages with corresponding calls to **InkDraw**.</span></span> <span data-ttu-id="2726d-135">Quando l'utente rilascia il pulsante sinistro del mouse, il client risponderà a un \_ messaggio WM LBUTTONUP con una chiamata a **InkStop**, che contrassegna la fine della sequenza di disegno dell'input penna.</span><span class="sxs-lookup"><span data-stu-id="2726d-135">When the user releases the left mouse button, the client will respond to a WM\_LBUTTONUP message with a call to **InkStop**, which marks the end of the ink drawing sequence.</span></span>

<span data-ttu-id="2726d-136">[**InkStart**](inkstart-method.md) indica al documento la posizione iniziale per la sequenza di disegno nelle coordinate della finestra client.</span><span class="sxs-lookup"><span data-stu-id="2726d-136">[**InkStart**](inkstart-method.md) tells COPaper the start position for the drawing sequence in client window coordinates.</span></span> <span data-ttu-id="2726d-137">Passa anche il colore e la larghezza dell'inchiostro attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="2726d-137">It also passes the currently selected ink color and width.</span></span> <span data-ttu-id="2726d-138">Il client gestisce queste selezioni; Il formato del documento viene semplicemente registrato quando viene effettuata la chiamata **InkStart** .</span><span class="sxs-lookup"><span data-stu-id="2726d-138">The client maintains these selections; COPaper merely records them when the **InkStart** call is made.</span></span> <span data-ttu-id="2726d-139">[**InkDraw**](inkdraw-method.md) viene chiamato ripetutamente per indicare al documento la successione delle coordinate della finestra che rappresentano il movimento del disegno del mouse o della penna.</span><span class="sxs-lookup"><span data-stu-id="2726d-139">[**InkDraw**](inkdraw-method.md) is called repeatedly to tell COPaper the succession of window coordinates that represent the drawing motion of the mouse or pen.</span></span> <span data-ttu-id="2726d-140">[**InkStop**](cguipaper-methods.md) indica a Copaper di contrassegnare la fine di una sequenza di disegno.</span><span class="sxs-lookup"><span data-stu-id="2726d-140">[**InkStop**](cguipaper-methods.md) instructs COPaper to mark the end of a drawing sequence.</span></span>

 

 




