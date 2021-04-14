---
title: CARETS
description: In questa sezione vengono illustrati i passaggi che lampeggiano a linee, blocchi o bitmap nell'area client di una finestra.
ms.assetid: vs|winui|~\winui\windowsuserinterface\resources\carets.htm
keywords:
- risorse, punto di inserimento
- occupazioni, informazioni
- righe lampeggianti
- blocchi lampeggianti
- bitmap intermittenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50cb99dfc324aa039924fa26683ab0a7674706ea
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/04/2021
ms.locfileid: "104401812"
---
# <a name="carets"></a><span data-ttu-id="3119b-108">CARETS</span><span class="sxs-lookup"><span data-stu-id="3119b-108">Carets</span></span>

<span data-ttu-id="3119b-109">Un *accento circonflesso* è una linea, un blocco o una bitmap lampeggiante nell'area client di una finestra.</span><span class="sxs-lookup"><span data-stu-id="3119b-109">A *caret* is a blinking line, block, or bitmap in the client area of a window.</span></span> <span data-ttu-id="3119b-110">Il cursore indica in genere la posizione in cui verrà inserito il testo o la grafica.</span><span class="sxs-lookup"><span data-stu-id="3119b-110">The caret typically indicates the place at which text or graphics will be inserted.</span></span>

<span data-ttu-id="3119b-111">Nella figura seguente vengono illustrate alcune variazioni comuni nell'aspetto del cursore.</span><span class="sxs-lookup"><span data-stu-id="3119b-111">The following illustration shows some common variations in the appearance of the caret.</span></span>

![Mostra 5 diversi modi in cui può essere visualizzato un punto di inserimento.](images/cscrt-01.png)

<span data-ttu-id="3119b-113">Le applicazioni possono creare un accento circonflesso, modificare il tempo di lampeggio e visualizzare, nascondere o spostare il punto di inserimento.</span><span class="sxs-lookup"><span data-stu-id="3119b-113">Applications can create a caret, change its blink time, and display, hide, or relocate the caret.</span></span>

### <a name="in-this-section"></a><span data-ttu-id="3119b-114">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="3119b-114">In This Section</span></span>



| <span data-ttu-id="3119b-115">Nome</span><span class="sxs-lookup"><span data-stu-id="3119b-115">Name</span></span>                                   | <span data-ttu-id="3119b-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3119b-116">Description</span></span>                                                               |
|----------------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="3119b-117">Informazioni sui Carrier</span><span class="sxs-lookup"><span data-stu-id="3119b-117">About Carets</span></span>](about-carets.md)       | <span data-ttu-id="3119b-118">Vengono illustrati i punto di inserimento.</span><span class="sxs-lookup"><span data-stu-id="3119b-118">Discusses carets.</span></span><br/>                                              |
| [<span data-ttu-id="3119b-119">Uso del punto di inserimento</span><span class="sxs-lookup"><span data-stu-id="3119b-119">Using Carets</span></span>](using-carets.md)       | <span data-ttu-id="3119b-120">Esempi di codice che illustrano come eseguire attività correlate ai carrier.</span><span class="sxs-lookup"><span data-stu-id="3119b-120">Code samples that show how to perform tasks related to carets.</span></span><br/> |
| [<span data-ttu-id="3119b-121">Riferimento al punto di inserimento</span><span class="sxs-lookup"><span data-stu-id="3119b-121">Caret Reference</span></span>](caret-reference.md) | <span data-ttu-id="3119b-122">Contiene il riferimento all'API.</span><span class="sxs-lookup"><span data-stu-id="3119b-122">Contains the API reference.</span></span><br/>                                    |



 

### <a name="caret-functions"></a><span data-ttu-id="3119b-123">Funzioni del cursore</span><span class="sxs-lookup"><span data-stu-id="3119b-123">Caret Functions</span></span>



| <span data-ttu-id="3119b-124">Nome</span><span class="sxs-lookup"><span data-stu-id="3119b-124">Name</span></span>                                           | <span data-ttu-id="3119b-125">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3119b-125">Description</span></span>                                                                                                                                                                                                                                                   |
|------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3119b-126">**CreateCaret**</span><span class="sxs-lookup"><span data-stu-id="3119b-126">**CreateCaret**</span></span>](/windows/desktop/api/Winuser/nf-winuser-createcaret)             | <span data-ttu-id="3119b-127">Crea una nuova forma per il punto di inserimento del sistema e assegna la proprietà del punto di inserimento alla finestra specificata.</span><span class="sxs-lookup"><span data-stu-id="3119b-127">Creates a new shape for the system caret and assigns ownership of the caret to the specified window.</span></span> <span data-ttu-id="3119b-128">La forma del cursore può essere una linea, un blocco o una bitmap.</span><span class="sxs-lookup"><span data-stu-id="3119b-128">The caret shape can be a line, a block, or a bitmap.</span></span> <br/>                                                                                         |
| [<span data-ttu-id="3119b-129">**DestroyCaret**</span><span class="sxs-lookup"><span data-stu-id="3119b-129">**DestroyCaret**</span></span>](/windows/desktop/api/Winuser/nf-winuser-destroycaret)           | <span data-ttu-id="3119b-130">Elimina la forma corrente del cursore, libera il punto di inserimento dalla finestra e rimuove il punto di inserimento dallo schermo.</span><span class="sxs-lookup"><span data-stu-id="3119b-130">Destroys the caret's current shape, frees the caret from the window, and removes the caret from the screen.</span></span> <br/>                                                                                                                                       |
| [<span data-ttu-id="3119b-131">**GetCaretBlinkTime**</span><span class="sxs-lookup"><span data-stu-id="3119b-131">**GetCaretBlinkTime**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getcaretblinktime) | <span data-ttu-id="3119b-132">Recupera il tempo necessario per invertire i pixel del punto di inserimento.</span><span class="sxs-lookup"><span data-stu-id="3119b-132">Retrieves the time required to invert the caret's pixels.</span></span> <span data-ttu-id="3119b-133">L'utente può impostare questo valore.</span><span class="sxs-lookup"><span data-stu-id="3119b-133">The user can set this value.</span></span> <br/>                                                                                                                                                            |
| [<span data-ttu-id="3119b-134">**GetCaretPos**</span><span class="sxs-lookup"><span data-stu-id="3119b-134">**GetCaretPos**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getcaretpos)             | <span data-ttu-id="3119b-135">Copia la posizione del punto di inserimento nella struttura del [**punto**](/previous-versions//dd162805(v=vs.85)) specificata.</span><span class="sxs-lookup"><span data-stu-id="3119b-135">Copies the caret's position to the specified [**POINT**](/previous-versions//dd162805(v=vs.85)) structure.</span></span> <br/>                                                                                                                                                                    |
| [<span data-ttu-id="3119b-136">**HideCaret**</span><span class="sxs-lookup"><span data-stu-id="3119b-136">**HideCaret**</span></span>](/windows/desktop/api/Winuser/nf-winuser-hidecaret)                 | <span data-ttu-id="3119b-137">Rimuove il punto di inserimento dallo schermo.</span><span class="sxs-lookup"><span data-stu-id="3119b-137">Removes the caret from the screen.</span></span> <span data-ttu-id="3119b-138">Nascondendo un cursore, non viene eliminata la forma corrente né viene invalidato il punto di inserimento.</span><span class="sxs-lookup"><span data-stu-id="3119b-138">Hiding a caret does not destroy its current shape or invalidate the insertion point.</span></span> <br/>                                                                                                                           |
| [<span data-ttu-id="3119b-139">**SetCaretBlinkTime**</span><span class="sxs-lookup"><span data-stu-id="3119b-139">**SetCaretBlinkTime**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setcaretblinktime) | <span data-ttu-id="3119b-140">Imposta il tempo di lampeggio del punto di inserimento sul numero di millisecondi specificato.</span><span class="sxs-lookup"><span data-stu-id="3119b-140">Sets the caret blink time to the specified number of milliseconds.</span></span> <span data-ttu-id="3119b-141">Il tempo di lampeggio è il tempo trascorso, in millisecondi, necessario per invertire i pixel del cursore.</span><span class="sxs-lookup"><span data-stu-id="3119b-141">The blink time is the elapsed time, in milliseconds, required to invert the caret's pixels.</span></span> <br/>                                                                                    |
| [<span data-ttu-id="3119b-142">**SetCaretPos**</span><span class="sxs-lookup"><span data-stu-id="3119b-142">**SetCaretPos**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setcaretpos)             | <span data-ttu-id="3119b-143">Sposta il punto di inserimento alle coordinate specificate.</span><span class="sxs-lookup"><span data-stu-id="3119b-143">Moves the caret to the specified coordinates.</span></span> <span data-ttu-id="3119b-144">Se la finestra proprietaria del punto di inserimento è stata creata con lo stile della classe **cs \_ OWNDC** , le coordinate specificate sono soggette alla modalità di mapping del contesto di dispositivo associato a tale finestra.</span><span class="sxs-lookup"><span data-stu-id="3119b-144">If the window that owns the caret was created with the **CS\_OWNDC** class style, then the specified coordinates are subject to the mapping mode of the device context associated with that window.</span></span> <br/> |
| [<span data-ttu-id="3119b-145">**ShowCaret**</span><span class="sxs-lookup"><span data-stu-id="3119b-145">**ShowCaret**</span></span>](/windows/desktop/api/Winuser/nf-winuser-showcaret)                 | <span data-ttu-id="3119b-146">Rende visibile il cursore sullo schermo in corrispondenza della posizione corrente del punto di inserimento.</span><span class="sxs-lookup"><span data-stu-id="3119b-146">Makes the caret visible on the screen at the caret's current position.</span></span> <span data-ttu-id="3119b-147">Quando il punto di inserimento diventa visibile, inizia a lampeggiare automaticamente.</span><span class="sxs-lookup"><span data-stu-id="3119b-147">When the caret becomes visible, it begins flashing automatically.</span></span> <br/>                                                                                                          |



 

 

