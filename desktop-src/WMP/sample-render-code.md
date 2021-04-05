---
title: Esempio di codice di rendering
description: Esempio di codice di rendering
ms.assetid: 14978cf4-47fa-4b2e-ba51-799be873dc8a
keywords:
- Visualizzazioni, codice di esempio
- Visualizzazioni personalizzate, codice di esempio
- Visualizzazioni, funzione render
- Visualizzazioni personalizzate, funzione render
- Funzione render, codice di esempio
- esempi, funzione Render per le visualizzazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a1ee5d00bc1aed5bd8bd91880e43e2ac2d1f6bc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044956"
---
# <a name="sample-render-code"></a><span data-ttu-id="dcfad-109">Esempio di codice di rendering</span><span class="sxs-lookup"><span data-stu-id="dcfad-109">Sample Render Code</span></span>

<span data-ttu-id="dcfad-110">Di seguito è riportato un codice di esempio che usa la funzione **Render** per disegnare una riga sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="dcfad-110">Here is some sample code that uses the **Render** function to draw a line across the screen.</span></span> <span data-ttu-id="dcfad-111">L'altezza della linea è definita dal valore della forma d'onda.</span><span class="sxs-lookup"><span data-stu-id="dcfad-111">The height of the line is defined by the waveform value.</span></span>


```C++
STDMETHODIMP CStock::Render(TimedLevel *pLevels, HDC hdc, RECT *prc)
{
    // Create new brushes and pens.
    HBRUSH hNewBrush = ::CreateSolidBrush( 0 );
    // Create a new solid pen the color of the foreground.
    HPEN hNewPen = ::CreatePen( PS_SOLID, 0, m_clrForeground );


    // Add the pen to the device context.
    HPEN hOldPen= static_cast<HPEN>(::SelectObject( hdc, hNewPen ));

    // Fill the background with the black brush.
    ::FillRect( hdc, prc, hNewBrush );

    // Get the y value from the waveform.
    int y = pLevels->waveform[0][0];

    // Draw the line from left to right.
    ::MoveToEx( hdc, prc->left, y, NULL);  
    ::LineTo(hdc, prc->right, y); 

    // Delete your brush.
    if (hNewBrush)
    {
        ::DeleteObject( hNewBrush );
    }
    // Delete your pen.
    if (hNewPen)
    {
        ::SelectObject( hdc, hOldPen );
        ::DeleteObject( hNewPen );
    }

    // You're done for this round.
    return S_OK;
}

```



<span data-ttu-id="dcfad-112">La funzione **Render** è la posizione in cui viene eseguita l'attività principale del codice.</span><span class="sxs-lookup"><span data-stu-id="dcfad-112">The **Render** function is where the main work of your code takes place.</span></span> <span data-ttu-id="dcfad-113">Ogni volta che Windows Media Player acquisisce un'istantanea dell'audio, chiamerà questa funzione e il codice verrà eseguito.</span><span class="sxs-lookup"><span data-stu-id="dcfad-113">Every time Windows Media Player takes a snapshot of the audio, it will call this function and your code will run.</span></span>

<span data-ttu-id="dcfad-114">Questo codice esegue le attività seguenti.</span><span class="sxs-lookup"><span data-stu-id="dcfad-114">This code performs the following tasks.</span></span> <span data-ttu-id="dcfad-115">Per informazioni dettagliate sulle funzioni specifiche, vedere Microsoft Windows Platform SDK per Windows a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="dcfad-115">Refer to the Microsoft Windows Platform SDK for 32-bit Windows for more details about specific functions.</span></span>

## <a name="creating-objects"></a><span data-ttu-id="dcfad-116">Creazione di oggetti</span><span class="sxs-lookup"><span data-stu-id="dcfad-116">Creating Objects</span></span>

<span data-ttu-id="dcfad-117">In genere si useranno le funzioni di disegno disponibili con l'interfaccia di visualizzazione grafica (GDI) di Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="dcfad-117">Usually you will be using the drawing functions that come with the Microsoft Windows Graphical Display Interface (GDI).</span></span> <span data-ttu-id="dcfad-118">È necessario creare le penne per creare linee e pennelli per riempire le aree.</span><span class="sxs-lookup"><span data-stu-id="dcfad-118">You need to create pens to draw lines and brushes to fill areas.</span></span>

<span data-ttu-id="dcfad-119">Viene creato un pennello nero a tinta unita per riempire lo sfondo.</span><span class="sxs-lookup"><span data-stu-id="dcfad-119">A solid black brush is created to fill in the background.</span></span>

<span data-ttu-id="dcfad-120">Viene creata una penna a tinta unita per creare una linea.</span><span class="sxs-lookup"><span data-stu-id="dcfad-120">A solid pen is created to draw a line.</span></span> <span data-ttu-id="dcfad-121">Il colore sarà il colore di primo piano definito dall'interfaccia che visualizzerà la visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="dcfad-121">The color will be the foreground color as defined by the skin that is going to display the visualization.</span></span>

## <a name="adding-the-object-to-the-dc"></a><span data-ttu-id="dcfad-122">Aggiunta dell'oggetto al controller di dominio</span><span class="sxs-lookup"><span data-stu-id="dcfad-122">Adding the Object to the DC</span></span>

<span data-ttu-id="dcfad-123">È necessario aggiungere la penna al contesto di dispositivo (DC).</span><span class="sxs-lookup"><span data-stu-id="dcfad-123">You need to add the pen to the device context (DC).</span></span> <span data-ttu-id="dcfad-124">Il controller di dominio è la porzione di memoria in cui sono archiviati tutti i dati e gli oggetti del disegno.</span><span class="sxs-lookup"><span data-stu-id="dcfad-124">The DC is the portion of memory that all drawing data and objects are stored in.</span></span> <span data-ttu-id="dcfad-125">In sostanza, il controller di dominio è gestione traffico di Windows che tiene traccia di tutti gli elementi grafici.</span><span class="sxs-lookup"><span data-stu-id="dcfad-125">Essentially the DC is the window traffic manager that keeps track of everything graphical.</span></span>

<span data-ttu-id="dcfad-126">È necessario *eseguire il cast* dell'oggetto Pen creato e archiviarlo come penna precedente.</span><span class="sxs-lookup"><span data-stu-id="dcfad-126">You need to *cast* the pen object you created and store it as an old pen.</span></span> <span data-ttu-id="dcfad-127">Usare questa tecnica di codifica per tutte le nuove penne.</span><span class="sxs-lookup"><span data-stu-id="dcfad-127">Use this coding technique for all new pens.</span></span> <span data-ttu-id="dcfad-128">Questa tecnica è necessaria per la programmazione a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="dcfad-128">This technique is required for 32-bit programming.</span></span>

## <a name="filling-in-the-background"></a><span data-ttu-id="dcfad-129">Riempimento in background</span><span class="sxs-lookup"><span data-stu-id="dcfad-129">Filling in the Background</span></span>

<span data-ttu-id="dcfad-130">A questo punto è possibile creare.</span><span class="sxs-lookup"><span data-stu-id="dcfad-130">You now are ready to draw.</span></span> <span data-ttu-id="dcfad-131">La funzione **fillRect** riempirà il rettangolo della finestra, come definito dai parametri della funzione **Render** .</span><span class="sxs-lookup"><span data-stu-id="dcfad-131">The **FillRect** function will fill the rectangle of the window, as defined by the parameters of the **Render** function.</span></span> <span data-ttu-id="dcfad-132">Il rettangolo è riempito con un pennello nero.</span><span class="sxs-lookup"><span data-stu-id="dcfad-132">The rectangle is filled with a black brush.</span></span>

## <a name="getting-audio-data"></a><span data-ttu-id="dcfad-133">Recupero di dati audio</span><span class="sxs-lookup"><span data-stu-id="dcfad-133">Getting Audio Data</span></span>

<span data-ttu-id="dcfad-134">Il codice ottiene quindi alcuni dati audio da Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="dcfad-134">Next the code gets some audio data from Windows Media Player.</span></span> <span data-ttu-id="dcfad-135">Usando la matrice di forme d'onda, è possibile ottenere il valore corrente della potenza audio nel momento in cui è stato effettuato lo snapshot.</span><span class="sxs-lookup"><span data-stu-id="dcfad-135">By using the waveform array, you can get the current value of the audio power at the moment the snapshot was taken.</span></span> <span data-ttu-id="dcfad-136">In questo caso, si stanno prendendo i dati audio del canale sinistro.</span><span class="sxs-lookup"><span data-stu-id="dcfad-136">In this case, you are taking the audio data of the left channel.</span></span> <span data-ttu-id="dcfad-137">Il primo valore nella matrice è il primo 1024th dello snapshot di alimentazione audio.</span><span class="sxs-lookup"><span data-stu-id="dcfad-137">The first value in the array is the first 1024th of the audio power snapshot.</span></span>

<span data-ttu-id="dcfad-138">Queste informazioni verranno usate per visualizzare una riga la cui altezza corrisponderà allo snapshot di Power audio.</span><span class="sxs-lookup"><span data-stu-id="dcfad-138">This information will be used to display a line whose height will match the audio power snapshot.</span></span>

## <a name="draw-the-line"></a><span data-ttu-id="dcfad-139">Creare la linea</span><span class="sxs-lookup"><span data-stu-id="dcfad-139">Draw the Line</span></span>

<span data-ttu-id="dcfad-140">La linea viene disegnata da sinistra a destra usando le funzioni GDI **MoveToEx** e **LineTo** .</span><span class="sxs-lookup"><span data-stu-id="dcfad-140">The line is drawn from left to right using the **MoveToEx** and **LineTo** GDI functions.</span></span>

<span data-ttu-id="dcfad-141">Spostare prima di tutto la penna al punto di partenza.</span><span class="sxs-lookup"><span data-stu-id="dcfad-141">First you move the pen to the starting point.</span></span> <span data-ttu-id="dcfad-142">In questo caso, x e y vengono utilizzati per definire i valori da sinistra a destra e dall'alto verso il basso che verranno visualizzati dall'utente sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="dcfad-142">In this case, x and y are used to define the left-to-right and top-to-bottom values the user will see on the screen.</span></span> <span data-ttu-id="dcfad-143">X è definito dal rettangolo PRC e in particolare dal valore di PRC->Left.</span><span class="sxs-lookup"><span data-stu-id="dcfad-143">X is defined by the rectangle prc and specifically by the value of prc->left.</span></span> <span data-ttu-id="dcfad-144">Y è definito come valore dei dati della forma d'onda in quel momento.</span><span class="sxs-lookup"><span data-stu-id="dcfad-144">Y is defined as the value of the waveform data at that moment.</span></span>

<span data-ttu-id="dcfad-145">Viene quindi disegnato un oggetto line sull'altro lato della finestra.</span><span class="sxs-lookup"><span data-stu-id="dcfad-145">Then you draw a line to the other side of the window.</span></span> <span data-ttu-id="dcfad-146">Il punto in cui si richiama la linea è di nuovo un valore x, y.</span><span class="sxs-lookup"><span data-stu-id="dcfad-146">The point you draw the line to is again an x, y value.</span></span> <span data-ttu-id="dcfad-147">X è definito dal rettangolo PRC, ma questa volta da PRC->right.</span><span class="sxs-lookup"><span data-stu-id="dcfad-147">X is defined by the rectangle prc, but this time by prc->right.</span></span> <span data-ttu-id="dcfad-148">Y è ancora definito dai dati della forma d'onda ed è uguale al punto da cui è stato avviato, perché si sta disegnando una linea retta da sinistra a destra.</span><span class="sxs-lookup"><span data-stu-id="dcfad-148">Y is still defined by the waveform data and is the same as the point you started from, because you are drawing a straight line from left to right.</span></span>

## <a name="clean-up-everything"></a><span data-ttu-id="dcfad-149">Pulisci tutto</span><span class="sxs-lookup"><span data-stu-id="dcfad-149">Clean up Everything</span></span>

<span data-ttu-id="dcfad-150">È necessario eliminare gli oggetti creati.</span><span class="sxs-lookup"><span data-stu-id="dcfad-150">You must delete the objects you create.</span></span> <span data-ttu-id="dcfad-151">In particolare, è necessario eliminare tutti i pennelli e le penne creati.</span><span class="sxs-lookup"><span data-stu-id="dcfad-151">Specifically you must delete any and all brushes and pens you create.</span></span> <span data-ttu-id="dcfad-152">È consigliabile eliminare penne e pennelli al termine dell'uso.</span><span class="sxs-lookup"><span data-stu-id="dcfad-152">It is good practice to delete pens and brushes when you finish using them.</span></span>

<span data-ttu-id="dcfad-153">Se non vengono eliminati prima di terminare l'implementazione della funzione di **rendering** , la visualizzazione si arresterà in modo anomalo in un minuto o meno.</span><span class="sxs-lookup"><span data-stu-id="dcfad-153">If you do not delete them before finishing your implementation of the **Render** function, your visualization will crash in a minute or less.</span></span> <span data-ttu-id="dcfad-154">È necessario contenere un conteggio delle penne e dei pennelli ed eliminare ogni singolo oggetto.</span><span class="sxs-lookup"><span data-stu-id="dcfad-154">You must keep a count of your pens and brushes and destroy every single one.</span></span> <span data-ttu-id="dcfad-155">Prestare particolare attenzione a non creare penne all'interno di un ciclo di codice.</span><span class="sxs-lookup"><span data-stu-id="dcfad-155">Be especially careful not to create pens inside a code loop.</span></span>

<span data-ttu-id="dcfad-156">Usare la tecnica di codifica fornita nell'esempio per eliminare le penne e i pennelli.</span><span class="sxs-lookup"><span data-stu-id="dcfad-156">Use the coding technique given in the example to destroy your pens and brushes.</span></span>

-   <span data-ttu-id="dcfad-157">**Importante** Elimina le penne e i pennelli.</span><span class="sxs-lookup"><span data-stu-id="dcfad-157">**Important** Destroy your pens and brushes!</span></span>

<span data-ttu-id="dcfad-158">Al termine della pulizia, assicurarsi di restituire S OK, in \_ modo che Windows Media Player sappia che il disegno è terminato.</span><span class="sxs-lookup"><span data-stu-id="dcfad-158">When you have finished cleaning up, be sure to return S\_OK so that Windows Media Player knows you are finished drawing.</span></span> <span data-ttu-id="dcfad-159">Al termine, il disegno verrà trasferito alla finestra, verrà eseguito un altro snapshot, il **rendering** chiederà di nuovo al codice di disegnare e così via.</span><span class="sxs-lookup"><span data-stu-id="dcfad-159">Once you finish, your drawing will be transferred to the window, another snapshot will be taken, **Render** will ask your code to draw again, and so on.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dcfad-160">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="dcfad-160">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dcfad-161">**Implementazione di rendering**</span><span class="sxs-lookup"><span data-stu-id="dcfad-161">**Implementing Render**</span></span>](implementing-render.md)
</dt> </dl>

 

 




