---
title: DPI e Device-Independent pixel
ms.assetid: d282de02-62f4-4a12-a77c-f602f6db0216
description: 'Altre informazioni su: DPI e Device-Independent pixel'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e6f04e1a056611fcdfe8b59ff65b38ecec99eaf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885305"
---
# <a name="dpi-and-device-independent-pixels"></a><span data-ttu-id="24460-103">DPI e Device-Independent pixel</span><span class="sxs-lookup"><span data-stu-id="24460-103">DPI and Device-Independent Pixels</span></span>

<span data-ttu-id="24460-104">Per programmare in modo efficace con la grafica di Windows, è necessario comprendere due concetti correlati:</span><span class="sxs-lookup"><span data-stu-id="24460-104">To program effectively with Windows graphics, you must understand two related concepts:</span></span>

-   <span data-ttu-id="24460-105">Punti per pollice (DPI)</span><span class="sxs-lookup"><span data-stu-id="24460-105">Dots per inch (DPI)</span></span>
-   <span data-ttu-id="24460-106">Pixel (DIP) indipendenti dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="24460-106">Device-independent pixel (DIPs).</span></span>

<span data-ttu-id="24460-107">Iniziamo con DPI.</span><span class="sxs-lookup"><span data-stu-id="24460-107">Let's start with DPI.</span></span> <span data-ttu-id="24460-108">Questa operazione richiederà una breve deviazione nella tipografia.</span><span class="sxs-lookup"><span data-stu-id="24460-108">This will require a short detour into typography.</span></span> <span data-ttu-id="24460-109">In tipografia la dimensione del tipo viene misurata in unità denominate *punti*.</span><span class="sxs-lookup"><span data-stu-id="24460-109">In typography, the size of type is measured in units called *points*.</span></span> <span data-ttu-id="24460-110">Un punto è uguale a 1/72 di pollice.</span><span class="sxs-lookup"><span data-stu-id="24460-110">One point equals 1/72 of an inch.</span></span>

<dl> <span data-ttu-id="24460-111">1 PT = 1/72 pollice</span><span class="sxs-lookup"><span data-stu-id="24460-111">1 pt = 1/72 inch</span></span>  
</dl>

> [!Note]  
> <span data-ttu-id="24460-112">Si tratta della definizione di pubblicazione del desktop del punto.</span><span class="sxs-lookup"><span data-stu-id="24460-112">This is the desktop publishing definition of point.</span></span> <span data-ttu-id="24460-113">In passato, la misura esatta di un punto è cambiata.</span><span class="sxs-lookup"><span data-stu-id="24460-113">Historically, the exact measure of a point has varied.</span></span>

 

<span data-ttu-id="24460-114">Ad esempio, un tipo di carattere a 12 punti è progettato per adattarsi all'interno di una riga di testo di 1/6 "(12/72).</span><span class="sxs-lookup"><span data-stu-id="24460-114">For example, a 12-point font is designed to fit within a 1/6" (12/72) line of text.</span></span> <span data-ttu-id="24460-115">Ovviamente, questo non significa che ogni carattere del tipo di carattere è esattamente 1/6 "Tall".</span><span class="sxs-lookup"><span data-stu-id="24460-115">Obviously, this does not mean that every character in the font is exactly 1/6" tall.</span></span> <span data-ttu-id="24460-116">Infatti, alcuni caratteri potrebbero essere più alti di 1/6 ".</span><span class="sxs-lookup"><span data-stu-id="24460-116">In fact, some characters might be taller than 1/6".</span></span> <span data-ttu-id="24460-117">In molti tipi di carattere, ad esempio, il carattere Å è più alto dell'altezza nominale del tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="24460-117">For example, in many fonts the character Å is taller than the nominal height of the font.</span></span> <span data-ttu-id="24460-118">Per la visualizzazione corretta, il tipo di carattere necessita di spazio aggiuntivo tra il testo.</span><span class="sxs-lookup"><span data-stu-id="24460-118">To display correctly, the font needs some additional space between the text.</span></span> <span data-ttu-id="24460-119">Questo spazio è denominato " *Leading*".</span><span class="sxs-lookup"><span data-stu-id="24460-119">This space is called the *leading*.</span></span>

<span data-ttu-id="24460-120">Nella figura seguente viene illustrato un tipo di carattere a 72 punti.</span><span class="sxs-lookup"><span data-stu-id="24460-120">The following illustration shows a 72-point font.</span></span> <span data-ttu-id="24460-121">Le linee continue mostrano un "rettangolo di delimitazione" di altezza intorno al testo.</span><span class="sxs-lookup"><span data-stu-id="24460-121">The solid lines show a 1" tall bounding box around the text.</span></span> <span data-ttu-id="24460-122">La linea tratteggiata è detta *baseline*.</span><span class="sxs-lookup"><span data-stu-id="24460-122">The dashed line is called the *baseline*.</span></span> <span data-ttu-id="24460-123">La maggior parte dei caratteri di un tipo di carattere nella linea di base.</span><span class="sxs-lookup"><span data-stu-id="24460-123">Most of the characters in a font rest on the baseline.</span></span> <span data-ttu-id="24460-124">L'altezza del tipo di carattere include la parte sopra la linea di base (l' *ascesa*) e la parte sotto la linea di base (la *discesa*).</span><span class="sxs-lookup"><span data-stu-id="24460-124">The height of the font includes the portion above the baseline (the *ascent*) and the portion below the baseline (the *descent*).</span></span> <span data-ttu-id="24460-125">Nel tipo di carattere riportato di seguito, l'ascesa è pari a 56 punti e la discesa è 16 punti.</span><span class="sxs-lookup"><span data-stu-id="24460-125">In the font shown here, the ascent is 56 points and the descent is 16 points.</span></span>

![illustrazione che mostra un tipo di carattere a 72 punti.](images/graphics11.png)

<span data-ttu-id="24460-127">Per quanto riguarda la visualizzazione di un computer, tuttavia, la misurazione delle dimensioni del testo è problematica, perché i pixel non hanno tutte le stesse dimensioni.</span><span class="sxs-lookup"><span data-stu-id="24460-127">When it comes to a computer display, however, measuring text size is problematic, because pixels are not all the same size.</span></span> <span data-ttu-id="24460-128">Le dimensioni di un pixel dipendono da due fattori: la risoluzione dello schermo e le dimensioni fisiche del monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="24460-128">The size of a pixel depends on two factors: the display resolution, and the physical size of the monitor.</span></span> <span data-ttu-id="24460-129">Pertanto, i pollici fisici non sono una misura utile, perché non esiste una relazione fissa tra i pollici e i pixel fisici.</span><span class="sxs-lookup"><span data-stu-id="24460-129">Therefore, physical inches are not a useful measure, because there is no fixed relation between physical inches and pixels.</span></span> <span data-ttu-id="24460-130">I tipi di carattere vengono invece misurati in unità *logiche* .</span><span class="sxs-lookup"><span data-stu-id="24460-130">Instead, fonts are measured in *logical* units.</span></span> <span data-ttu-id="24460-131">Un tipo di carattere a 72 punti viene definito come un pollice logico di altezza.</span><span class="sxs-lookup"><span data-stu-id="24460-131">A 72-point font is defined to be one logical inch tall.</span></span> <span data-ttu-id="24460-132">I pollici logici vengono quindi convertiti in pixel.</span><span class="sxs-lookup"><span data-stu-id="24460-132">Logical inches are then converted to pixels.</span></span> <span data-ttu-id="24460-133">Per molti anni, Windows usava la seguente conversione: un pollice logico equivale a 96 pixel.</span><span class="sxs-lookup"><span data-stu-id="24460-133">For many years, Windows used the following conversion: One logical inch equals 96 pixels.</span></span> <span data-ttu-id="24460-134">Utilizzando questo fattore di scala, viene eseguito il rendering di un tipo di carattere a 72 punti come 96 pixel di altezza.</span><span class="sxs-lookup"><span data-stu-id="24460-134">Using this scaling factor, a 72-point font is rendered as 96 pixels tall.</span></span> <span data-ttu-id="24460-135">Un tipo di carattere A 12 punti è di 16 pixel di altezza.</span><span class="sxs-lookup"><span data-stu-id="24460-135">A 12-point font is 16 pixels tall.</span></span>

<dl> <span data-ttu-id="24460-136">12 punti = 12/72 pollice logico = 1/6 pollice logico = 96/6 pixel = 16 pixel</span><span class="sxs-lookup"><span data-stu-id="24460-136">12 points = 12/72 logical inch = 1/6 logical inch = 96/6 pixels = 16 pixels</span></span>  
</dl>

<span data-ttu-id="24460-137">Questo fattore di scala viene descritto come 96 punti per pollice (DPI).</span><span class="sxs-lookup"><span data-stu-id="24460-137">This scaling factor is described as 96 dots per inch (DPI).</span></span> <span data-ttu-id="24460-138">I punti dei termini derivano dalla stampa, in cui i punti di input fisici vengono inseriti su carta.</span><span class="sxs-lookup"><span data-stu-id="24460-138">The term dots derives from printing, where physical dots of ink are put onto paper.</span></span> <span data-ttu-id="24460-139">Per gli schermi dei computer, sarebbe più accurato indicare 96 pixel per ogni pollice logico, ma il termine DPI si è bloccato.</span><span class="sxs-lookup"><span data-stu-id="24460-139">For computer displays, it would be more accurate to say 96 pixels per logical inch, but the term DPI has stuck.</span></span>

<span data-ttu-id="24460-140">Poiché le dimensioni effettive dei pixel variano, il testo leggibile su un monitor potrebbe essere troppo piccolo su un altro monitor.</span><span class="sxs-lookup"><span data-stu-id="24460-140">Because actual pixel sizes vary, text that is readable on one monitor might be too small on another monitor.</span></span> <span data-ttu-id="24460-141">Inoltre, le persone hanno preferenze diverse: alcune persone preferiscono un testo più grande.</span><span class="sxs-lookup"><span data-stu-id="24460-141">Also, people have different preferences—some people prefer larger text.</span></span> <span data-ttu-id="24460-142">Per questo motivo, Windows consente all'utente di modificare l'impostazione DPI.</span><span class="sxs-lookup"><span data-stu-id="24460-142">For this reason, Windows enables the user to change the DPI setting.</span></span> <span data-ttu-id="24460-143">Se, ad esempio, l'utente imposta la visualizzazione su 144 DPI, un tipo di carattere a 72 è 144 pixel di altezza.</span><span class="sxs-lookup"><span data-stu-id="24460-143">For example, if the user sets the display to 144 DPI, a 72-point font is 144 pixels tall.</span></span> <span data-ttu-id="24460-144">Le impostazioni DPI standard sono 100% (96 DPI), 125% (120 DPI) e 150% (144 DPI).</span><span class="sxs-lookup"><span data-stu-id="24460-144">The standard DPI settings are 100% (96 DPI), 125% (120 DPI), and 150% (144 DPI).</span></span> <span data-ttu-id="24460-145">L'utente può anche applicare un'impostazione personalizzata.</span><span class="sxs-lookup"><span data-stu-id="24460-145">The user can also apply a custom setting.</span></span> <span data-ttu-id="24460-146">A partire da Windows 7, DPI è un'impostazione per utente.</span><span class="sxs-lookup"><span data-stu-id="24460-146">Starting in Windows 7, DPI is a per-user setting.</span></span>

## <a name="dwm-scaling"></a><span data-ttu-id="24460-147">Ridimensionamento di DWM</span><span class="sxs-lookup"><span data-stu-id="24460-147">DWM Scaling</span></span>

<span data-ttu-id="24460-148">Se un programma non tiene conto di DPI, i difetti seguenti potrebbero essere evidenti con impostazioni DPI elevate:</span><span class="sxs-lookup"><span data-stu-id="24460-148">If a program does not account for DPI, the following defects might be apparent at high-DPI settings:</span></span>

-   <span data-ttu-id="24460-149">Elementi dell'interfaccia utente ritagliati.</span><span class="sxs-lookup"><span data-stu-id="24460-149">Clipped UI elements.</span></span>
-   <span data-ttu-id="24460-150">Layout non corretto.</span><span class="sxs-lookup"><span data-stu-id="24460-150">Incorrect layout.</span></span>
-   <span data-ttu-id="24460-151">Bitmap e icone pixel.</span><span class="sxs-lookup"><span data-stu-id="24460-151">Pixelated bitmaps and icons.</span></span>
-   <span data-ttu-id="24460-152">Coordinate del mouse non corrette, che possono influire sull'hit test, il trascinamento della selezione e così via.</span><span class="sxs-lookup"><span data-stu-id="24460-152">Incorrect mouse coordinates, which can affect hit testing, drag and drop, and so forth.</span></span>

<span data-ttu-id="24460-153">Per assicurarsi che i programmi meno recenti funzionino con impostazioni DPI elevate, DWM implementa un utile fallback.</span><span class="sxs-lookup"><span data-stu-id="24460-153">To ensure that older programs work at high-DPI settings, the DWM implements a useful fallback.</span></span> <span data-ttu-id="24460-154">Se un programma non è contrassegnato come DPI compatibile, DWM ridimensiona l'intera interfaccia utente in modo che corrisponda all'impostazione DPI.</span><span class="sxs-lookup"><span data-stu-id="24460-154">If a program is not marked as being DPI aware, the DWM will scale the entire UI to match the DPI setting.</span></span> <span data-ttu-id="24460-155">Ad esempio, a 144 DPI, l'interfaccia utente viene ridimensionata del 150%, inclusi testo, elementi grafici, controlli e dimensioni della finestra.</span><span class="sxs-lookup"><span data-stu-id="24460-155">For example, at 144 DPI, the UI is scaled by 150%, including text, graphics, controls, and window sizes.</span></span> <span data-ttu-id="24460-156">Se il programma crea una finestra 500 × 500, la finestra viene effettivamente visualizzata come 750 × 750 pixel e il contenuto della finestra viene ridimensionato di conseguenza.</span><span class="sxs-lookup"><span data-stu-id="24460-156">If the program creates a 500 × 500 window, the window actually appears as 750 × 750 pixels, and the contents of the window are scaled accordingly.</span></span>

<span data-ttu-id="24460-157">Questo comportamento indica che i programmi meno recenti "semplicemente funzionano" con impostazioni DPI elevate.</span><span class="sxs-lookup"><span data-stu-id="24460-157">This behavior means that older programs "just work" at high-DPI settings.</span></span> <span data-ttu-id="24460-158">Tuttavia, il ridimensionamento determina anche un aspetto sfocato, perché il ridimensionamento viene applicato dopo che la finestra è stata disegnata.</span><span class="sxs-lookup"><span data-stu-id="24460-158">However, scaling also results in a somewhat blurry appearance, because the scaling is applied after the window is drawn.</span></span>

## <a name="dpi-aware-applications"></a><span data-ttu-id="24460-159">Applicazioni DPI-Aware</span><span class="sxs-lookup"><span data-stu-id="24460-159">DPI-Aware Applications</span></span>

<span data-ttu-id="24460-160">Per evitare il ridimensionamento di DWM, un programma può contrassegnarsi come compatibile con DPI.</span><span class="sxs-lookup"><span data-stu-id="24460-160">To avoid DWM scaling, a program can mark itself as DPI-aware.</span></span> <span data-ttu-id="24460-161">In questo modo si indica a DWM di non eseguire alcun ridimensionamento DPI automatico.</span><span class="sxs-lookup"><span data-stu-id="24460-161">This tells the DWM not to perform any automatic DPI scaling.</span></span> <span data-ttu-id="24460-162">Tutte le nuove applicazioni devono essere progettate in modo da essere compatibili con DPI, perché la consapevolezza DPI migliora l'aspetto dell'interfaccia utente con impostazioni DPI più elevate.</span><span class="sxs-lookup"><span data-stu-id="24460-162">All new applications should be designed to be DPI-aware, because DPI awareness improves the appearance of the UI at higher DPI settings.</span></span>

<span data-ttu-id="24460-163">Un programma dichiara autonomamente il riconoscimento DPI tramite il manifesto dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="24460-163">A program declares itself DPI-aware through its application manifest.</span></span> <span data-ttu-id="24460-164">Un *manifesto* è semplicemente un file XML che descrive una dll o un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="24460-164">A *manifest* is a simply an XML file that describes a DLL or application.</span></span> <span data-ttu-id="24460-165">Il manifesto è in genere incorporato nel file eseguibile, sebbene possa essere fornito come file separato.</span><span class="sxs-lookup"><span data-stu-id="24460-165">The manifest is typically embedded in the executable file, although it can be provided as a separate file.</span></span> <span data-ttu-id="24460-166">Un manifesto contiene informazioni quali le dipendenze DLL, il livello di privilegio richiesto e la versione di Windows per cui è stato progettato il programma.</span><span class="sxs-lookup"><span data-stu-id="24460-166">A manifest contains information such as DLL dependencies, the requested privilege level, and what version of Windows the program was designed for.</span></span>

<span data-ttu-id="24460-167">Per dichiarare che il programma è compatibile con DPI, includere nel manifesto le informazioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="24460-167">To declare that your program is DPI-aware, include the following information in the manifest.</span></span>

``` syntax
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3" >
  <asmv3:application>
    <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2005/WindowsSettings">
      <dpiAware>true</dpiAware>
    </asmv3:windowsSettings>
  </asmv3:application>
</assembly>
```

<span data-ttu-id="24460-168">L'elenco riportato di seguito è solo un manifesto parziale, ma il linker di Visual Studio genera automaticamente il resto del manifesto.</span><span class="sxs-lookup"><span data-stu-id="24460-168">The listing shown here is only a partial manifest, but the Visual Studio linker generates the rest of the manifest for you automatically.</span></span> <span data-ttu-id="24460-169">Per includere un manifesto parziale nel progetto, seguire questa procedura in Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="24460-169">To include a partial manifest in your project, perform the following steps in Visual Studio.</span></span>

1.  <span data-ttu-id="24460-170">Scegliere **Proprietà** dal menu **progetto** .</span><span class="sxs-lookup"><span data-stu-id="24460-170">On the **Project** menu, click **Property**.</span></span>
2.  <span data-ttu-id="24460-171">Nel riquadro sinistro espandere Proprietà di **configurazione**, espandere **strumento Manifesto**, quindi fare clic su **input e output**.</span><span class="sxs-lookup"><span data-stu-id="24460-171">In the left pane, expand **Configuration Properties**, expand **Manifest Tool**, and then click **Input and Output**.</span></span>
3.  <span data-ttu-id="24460-172">Nella casella di testo **file manifesto aggiuntivi** Digitare il nome del file manifesto, quindi fare clic su **OK**.</span><span class="sxs-lookup"><span data-stu-id="24460-172">In the **Additional Manifest Files** text box, type the name of the manifest file, and then click **OK**.</span></span>

<span data-ttu-id="24460-173">Contrassegnando il programma come compatibile con DPI, si indica a DWM di non ridimensionare la finestra dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="24460-173">By marking your program as DPI-aware, you are telling the DWM not to scale your application window.</span></span> <span data-ttu-id="24460-174">A questo punto, se si crea una finestra 500 × 500, la finestra occuperà 500 × 500 pixel, indipendentemente dall'impostazione DPI dell'utente.</span><span class="sxs-lookup"><span data-stu-id="24460-174">Now if you create a 500 × 500 window, the window will occupy 500 × 500 pixels, regardless of the user's DPI setting.</span></span>

## <a name="gdi-and-dpi"></a><span data-ttu-id="24460-175">GDI e DPI</span><span class="sxs-lookup"><span data-stu-id="24460-175">GDI and DPI</span></span>

<span data-ttu-id="24460-176">Il disegno GDI viene misurato in pixel.</span><span class="sxs-lookup"><span data-stu-id="24460-176">GDI drawing is measured in pixels.</span></span> <span data-ttu-id="24460-177">Ciò significa che se il programma è contrassegnato come compatibile con DPI e si chiede a GDI di creare un rettangolo 200 × 100, il rettangolo risultante sarà 200 pixel di larghezza e 100 pixel di altezza sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="24460-177">That means if your program is marked as DPI-aware, and you ask GDI to draw a 200 × 100 rectangle, the resulting rectangle will be 200 pixels wide and 100 pixels tall on the screen.</span></span> <span data-ttu-id="24460-178">Tuttavia, le dimensioni dei tipi di carattere GDI vengono ridimensionate all'impostazione DPI corrente.</span><span class="sxs-lookup"><span data-stu-id="24460-178">However, GDI font sizes are scaled to the current DPI setting.</span></span> <span data-ttu-id="24460-179">In altre parole, se si crea un tipo di carattere a 72 punti, la dimensione del tipo di carattere sarà 96 pixel a 96 DPI, ma 144 pixel a 144 DPI.</span><span class="sxs-lookup"><span data-stu-id="24460-179">In other words, if you create a 72-point font, the size of the font will be 96 pixels at 96 DPI, but 144 pixels at 144 DPI.</span></span> <span data-ttu-id="24460-180">Di seguito è riportato un tipo di carattere a 72 punti sottoposto a rendering a 144 DPI con GDI.</span><span class="sxs-lookup"><span data-stu-id="24460-180">Here is a 72 point font rendered at 144 DPI using GDI.</span></span>

![diagramma che mostra il ridimensionamento del tipo di carattere dpi in GDI.](images/graphics12.png)

<span data-ttu-id="24460-182">Se l'applicazione è compatibile con DPI e si usa GDI per il disegno, ridimensionare tutte le coordinate del disegno in modo che corrispondano al valore DPI.</span><span class="sxs-lookup"><span data-stu-id="24460-182">If your application is DPI-aware and you use GDI for drawing, scale all of your drawing coordinates to match the DPI.</span></span>

## <a name="direct2d-and-dpi"></a><span data-ttu-id="24460-183">Direct2D e DPI</span><span class="sxs-lookup"><span data-stu-id="24460-183">Direct2D and DPI</span></span>

<span data-ttu-id="24460-184">Direct2D esegue automaticamente il ridimensionamento in base all'impostazione DPI.</span><span class="sxs-lookup"><span data-stu-id="24460-184">Direct2D automatically performs scaling to match the DPI setting.</span></span> <span data-ttu-id="24460-185">In Direct2D le coordinate sono misurate in unità denominate DIP ( *device independent pixel* ).</span><span class="sxs-lookup"><span data-stu-id="24460-185">In Direct2D, coordinates are measured in units called *device-independent pixels* (DIPs).</span></span> <span data-ttu-id="24460-186">Un DIP viene definito come 1/1/96 di un pollice *logico* .</span><span class="sxs-lookup"><span data-stu-id="24460-186">A DIP is defined as 1/96th of a *logical* inch.</span></span> <span data-ttu-id="24460-187">In Direct2D tutte le operazioni di disegno vengono specificate in DIP e quindi ridimensionate all'impostazione DPI corrente.</span><span class="sxs-lookup"><span data-stu-id="24460-187">In Direct2D, all drawing operations are specified in DIPs and then scaled to the current DPI setting.</span></span>



| <span data-ttu-id="24460-188">Impostazione DPI</span><span class="sxs-lookup"><span data-stu-id="24460-188">DPI setting</span></span> | <span data-ttu-id="24460-189">Dimensioni DIP</span><span class="sxs-lookup"><span data-stu-id="24460-189">DIP size</span></span>    |
|-------------|-------------|
| <span data-ttu-id="24460-190">96</span><span class="sxs-lookup"><span data-stu-id="24460-190">96</span></span>          | <span data-ttu-id="24460-191">1 pixel</span><span class="sxs-lookup"><span data-stu-id="24460-191">1 pixel</span></span>     |
| <span data-ttu-id="24460-192">120</span><span class="sxs-lookup"><span data-stu-id="24460-192">120</span></span>         | <span data-ttu-id="24460-193">1,25 pixel</span><span class="sxs-lookup"><span data-stu-id="24460-193">1.25 pixels</span></span> |
| <span data-ttu-id="24460-194">144</span><span class="sxs-lookup"><span data-stu-id="24460-194">144</span></span>         | <span data-ttu-id="24460-195">1,5 pixel</span><span class="sxs-lookup"><span data-stu-id="24460-195">1.5 pixels</span></span>  |



 

<span data-ttu-id="24460-196">Se, ad esempio, l'impostazione DPI dell'utente è 144 DPI e si chiede a Direct2D di creare un rettangolo 200 × 100, il rettangolo sarà 300 × 150 pixel fisici.</span><span class="sxs-lookup"><span data-stu-id="24460-196">For example, if the user's DPI setting is 144 DPI, and you ask Direct2D to draw a 200 × 100 rectangle, the rectangle will be 300 × 150 physical pixels.</span></span> <span data-ttu-id="24460-197">DirectWrite, inoltre, misura le dimensioni dei caratteri in DIP, anziché in punti.</span><span class="sxs-lookup"><span data-stu-id="24460-197">In addition, DirectWrite measures font sizes in DIPs, rather than points.</span></span> <span data-ttu-id="24460-198">Per creare un tipo di carattere a 12 punti, specificare 16 DIP (12 punti = 1/6 Logical inch = 96/6 DIP).</span><span class="sxs-lookup"><span data-stu-id="24460-198">To create a 12-point font, specify 16 DIPs (12 points = 1/6 logical inch = 96/6 DIPs).</span></span> <span data-ttu-id="24460-199">Quando il testo viene disegnato sullo schermo, Direct2D converte i dip in pixel fisici.</span><span class="sxs-lookup"><span data-stu-id="24460-199">When the text is drawn on the screen, Direct2D converts the DIPs to physical pixels.</span></span> <span data-ttu-id="24460-200">Il vantaggio di questo sistema è che le unità di misura sono coerenti sia per il testo che per il disegno, indipendentemente dall'impostazione DPI corrente.</span><span class="sxs-lookup"><span data-stu-id="24460-200">The benefit of this system is that the units of measurement are consistent for both text and drawing, regardless of the current DPI setting.</span></span>

<span data-ttu-id="24460-201">Una parola di attenzione: le coordinate del mouse e della finestra vengono ancora fornite in pixel fisici, non in DIP.</span><span class="sxs-lookup"><span data-stu-id="24460-201">A word of caution: Mouse and window coordinates are still given in physical pixels, not DIPs.</span></span> <span data-ttu-id="24460-202">Ad esempio, se si elabora il messaggio [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) , la posizione del mouse viene specificata in pixel fisici.</span><span class="sxs-lookup"><span data-stu-id="24460-202">For example, if you process the [**WM\_LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) message, the mouse-down position is given in physical pixels.</span></span> <span data-ttu-id="24460-203">Per creare un punto in quella posizione, è necessario convertire le coordinate dei pixel in DIP.</span><span class="sxs-lookup"><span data-stu-id="24460-203">To draw a point at that position, you must convert the pixel coordinates to DIPs.</span></span>

## <a name="converting-physical-pixels-to-dips"></a><span data-ttu-id="24460-204">Conversione di pixel fisici in DIP</span><span class="sxs-lookup"><span data-stu-id="24460-204">Converting Physical Pixels to DIPs</span></span>

<span data-ttu-id="24460-205">La conversione da pixel fisici a dip usa la formula seguente.</span><span class="sxs-lookup"><span data-stu-id="24460-205">The conversion from physical pixels to DIPs uses the following formula.</span></span>

<dl> <span data-ttu-id="24460-206">DIP = pixel/(DPI/96.0)</span><span class="sxs-lookup"><span data-stu-id="24460-206">DIPs = pixels / (DPI/96.0)</span></span>  
</dl>

<span data-ttu-id="24460-207">Per ottenere l'impostazione DPI, chiamare il metodo [**ID2D1Factory:: GetDesktopDpi**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) .</span><span class="sxs-lookup"><span data-stu-id="24460-207">To get the DPI setting, call the [**ID2D1Factory::GetDesktopDpi**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) method.</span></span> <span data-ttu-id="24460-208">Il valore DPI viene restituito come due valori a virgola mobile, uno per l'asse x e uno per l'asse y.</span><span class="sxs-lookup"><span data-stu-id="24460-208">The DPI is returned as two floating-point values, one for the x-axis and one for the y-axis.</span></span> <span data-ttu-id="24460-209">In teoria, questi valori possono variare.</span><span class="sxs-lookup"><span data-stu-id="24460-209">In theory, these values can differ.</span></span> <span data-ttu-id="24460-210">Calcolare un fattore di scala separato per ogni asse.</span><span class="sxs-lookup"><span data-stu-id="24460-210">Calculate a separate scaling factor for each axis.</span></span>


```C++
float g_DPIScaleX = 1.0f;
float g_DPIScaleY = 1.0f;

void InitializeDPIScale(ID2D1Factory *pFactory)
{
    FLOAT dpiX, dpiY;

    pFactory->GetDesktopDpi(&dpiX, &dpiY);

    g_DPIScaleX = dpiX/96.0f;
    g_DPIScaleY = dpiY/96.0f;
}

template <typename T>
float PixelsToDipsX(T x)
{
    return static_cast<float>(x) / g_DPIScaleX;
}

template <typename T>
float PixelsToDipsY(T y)
{
    return static_cast<float>(y) / g_DPIScaleY;
}
```



<span data-ttu-id="24460-211">Ecco un metodo alternativo per ottenere l'impostazione DPI se non si usa Direct2D:</span><span class="sxs-lookup"><span data-stu-id="24460-211">Here is an alternate way to get the DPI setting if you are not using Direct2D:</span></span>


```C++
void InitializeDPIScale(HWND hwnd)
{
    HDC hdc = GetDC(hwnd);
    g_DPIScaleX = GetDeviceCaps(hdc, LOGPIXELSX) / 96.0f;
    g_DPIScaleY = GetDeviceCaps(hdc, LOGPIXELSY) / 96.0f;
    ReleaseDC(hwnd, hdc);
}
```
> [!Note]  
> <span data-ttu-id="24460-212">In Windows 10 la versione 1903,  [**ID2D1Factory:: GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) è deprecata e la raccomandazione è [**DisplayInformation:: LogicalDpi**](/uwp/api/windows.graphics.display.displayinformation.logicaldpi?view=winrt-19041) per le app di Windows Store o [**GetDpiForWindow**](/windows/win32/api/winuser/nf-winuser-getdpiforwindow) per le app desktop.</span><span class="sxs-lookup"><span data-stu-id="24460-212">On Windows 10, version 1903,  [**ID2D1Factory::GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) is deprecated and the recommendation is [**DisplayInformation::LogicalDpi**](/uwp/api/windows.graphics.display.displayinformation.logicaldpi?view=winrt-19041) for Windows Store Apps or [**GetDpiForWindow**](/windows/win32/api/winuser/nf-winuser-getdpiforwindow) for desktop apps.</span></span> <span data-ttu-id="24460-213">Se si vuole comunque usarlo, non visualizzare più il messaggio di errore del compilatore scrivendo la riga [**#pragma avviso (Elimina: 4996)**](/cpp/error-messages/compiler-warnings/compiler-warning-level-3-c4996?view=vs-2019) immediatamente prima della chiamata a [**ID2D1Factory:: GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) .</span><span class="sxs-lookup"><span data-stu-id="24460-213">If you still want to use it, suppress the compiler error message by writing the line [**#pragma warning(suppress: 4996)**](/cpp/error-messages/compiler-warnings/compiler-warning-level-3-c4996?view=vs-2019) just before the [**ID2D1Factory::GetDesktopDpi**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi) call.</span></span> <span data-ttu-id="24460-214">Sebbene non sia consigliato, è possibile impostare la consapevolezza DPI predefinita a livello di codice usando [**SetProcessDpiAwarenessContext**](/windows/win32/api/winuser/nf-winuser-setprocessdpiawarenesscontext).</span><span class="sxs-lookup"><span data-stu-id="24460-214">Although it is not recommended, it is possible to set the default DPI awareness programmatically using [**SetProcessDpiAwarenessContext**](/windows/win32/api/winuser/nf-winuser-setprocessdpiawarenesscontext).</span></span> <span data-ttu-id="24460-215">Una volta creata una finestra (HWND) nel processo, la modifica della modalità di riconoscimento DPI non è più supportata.</span><span class="sxs-lookup"><span data-stu-id="24460-215">Once a window (an HWND) has been created in your process, changing the DPI awareness mode is no longer supported.</span></span> <span data-ttu-id="24460-216">Se si imposta la modalità di riconoscimento DPI predefinita del processo a livello di codice, è necessario chiamare l'API corrispondente prima che siano stati creati HWND.</span><span class="sxs-lookup"><span data-stu-id="24460-216">If you are setting the process-default DPI awareness mode programmatically, you must call the corresponding API before any HWNDs have been created.</span></span> <span data-ttu-id="24460-217">Per informazioni, vedere [impostazione della consapevolezza DPI predefinita per un processo](../hidpi/setting-the-default-dpi-awareness-for-a-process.md).</span><span class="sxs-lookup"><span data-stu-id="24460-217">For information see [Setting the default DPI awareness for a process](../hidpi/setting-the-default-dpi-awareness-for-a-process.md).</span></span>

## <a name="resizing-the-render-target"></a><span data-ttu-id="24460-218">Ridimensionamento della destinazione di rendering</span><span class="sxs-lookup"><span data-stu-id="24460-218">Resizing the Render Target</span></span>

<span data-ttu-id="24460-219">Se le dimensioni della finestra cambiano, è necessario ridimensionare la destinazione di rendering in modo che corrisponda.</span><span class="sxs-lookup"><span data-stu-id="24460-219">If the size of the window changes, you must resize the render target to match.</span></span> <span data-ttu-id="24460-220">Nella maggior parte dei casi, sarà necessario aggiornare anche il layout e ridisegnare la finestra.</span><span class="sxs-lookup"><span data-stu-id="24460-220">In most cases, you will also need to update the layout and repaint the window.</span></span> <span data-ttu-id="24460-221">Nel codice seguente vengono illustrati questi passaggi.</span><span class="sxs-lookup"><span data-stu-id="24460-221">The following code shows these steps.</span></span>


```C++
void MainWindow::Resize()
{
    if (pRenderTarget != NULL)
    {
        RECT rc;
        GetClientRect(m_hwnd, &rc);

        D2D1_SIZE_U size = D2D1::SizeU(rc.right, rc.bottom);

        pRenderTarget->Resize(size);
        CalculateLayout();
        InvalidateRect(m_hwnd, NULL, FALSE);
    }
}
```



<span data-ttu-id="24460-222">La funzione [**GetClientRect**](/windows/desktop/api/winuser/nf-winuser-getclientrect) ottiene la nuova dimensione dell'area client, in pixel fisici (non DIP).</span><span class="sxs-lookup"><span data-stu-id="24460-222">The [**GetClientRect**](/windows/desktop/api/winuser/nf-winuser-getclientrect) function gets the new size of the client area, in physical pixels (not DIPs).</span></span> <span data-ttu-id="24460-223">Il metodo [**ID2D1HwndRenderTarget:: Resize**](../direct2d/id2d1hwndrendertarget-resize.md) aggiorna la dimensione della destinazione di rendering, specificata anche in pixel.</span><span class="sxs-lookup"><span data-stu-id="24460-223">The [**ID2D1HwndRenderTarget::Resize**](../direct2d/id2d1hwndrendertarget-resize.md) method updates the size of the render target, also specified in pixels.</span></span> <span data-ttu-id="24460-224">La funzione [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect) forza un ridisegno aggiungendo l'intera area client all'area di aggiornamento della finestra.</span><span class="sxs-lookup"><span data-stu-id="24460-224">The [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect) function forces a repaint by adding the entire client area to the window's update region.</span></span> <span data-ttu-id="24460-225">(Vedere [disegnare la finestra](painting-the-window.md), nel modulo 1).</span><span class="sxs-lookup"><span data-stu-id="24460-225">(See [Painting the Window](painting-the-window.md), in Module 1.)</span></span>

<span data-ttu-id="24460-226">Quando la finestra si espande o si riduce, in genere è necessario ricalcolare la posizione degli oggetti da creare.</span><span class="sxs-lookup"><span data-stu-id="24460-226">As the window grows or shrinks, you will typically need to recalculate the position of the objects that you draw.</span></span> <span data-ttu-id="24460-227">Ad esempio, nel programma Circle è necessario aggiornare il raggio e il punto centrale:</span><span class="sxs-lookup"><span data-stu-id="24460-227">For example, in the circle program, the radius and center point must be updated:</span></span>


```C++
void MainWindow::CalculateLayout()
{
    if (pRenderTarget != NULL)
    {
        D2D1_SIZE_F size = pRenderTarget->GetSize();
        const float x = size.width / 2;
        const float y = size.height / 2;
        const float radius = min(x, y);
        ellipse = D2D1::Ellipse(D2D1::Point2F(x, y), radius, radius);
    }
}
```



<span data-ttu-id="24460-228">Il metodo [**ID2D1RenderTarget:: GetSize**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-getsize) restituisce le dimensioni della destinazione di rendering in DIP (non pixel), che è l'unità appropriata per il calcolo del layout.</span><span class="sxs-lookup"><span data-stu-id="24460-228">The [**ID2D1RenderTarget::GetSize**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-getsize) method returns the size of the render target in DIPs (not pixels), which is the appropriate unit for calculating layout.</span></span> <span data-ttu-id="24460-229">Esiste un metodo strettamente correlato, [**ID2D1RenderTarget:: GetPixelSize**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-getpixelsize), che restituisce le dimensioni in pixel fisici.</span><span class="sxs-lookup"><span data-stu-id="24460-229">There is a closely related method, [**ID2D1RenderTarget::GetPixelSize**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-getpixelsize), that returns the size in physical pixels.</span></span> <span data-ttu-id="24460-230">Per una destinazione di rendering **HWND** , questo valore corrisponde alle dimensioni restituite da [**GetClientRect**](/windows/desktop/api/winuser/nf-winuser-getclientrect).</span><span class="sxs-lookup"><span data-stu-id="24460-230">For an **HWND** render target, this value matches the size returned by [**GetClientRect**](/windows/desktop/api/winuser/nf-winuser-getclientrect).</span></span> <span data-ttu-id="24460-231">Tenere tuttavia presente che il disegno viene eseguito in DIP, non in pixel.</span><span class="sxs-lookup"><span data-stu-id="24460-231">But remember that drawing is performed in DIPs, not pixels.</span></span>

## <a name="next"></a><span data-ttu-id="24460-232">Prossima</span><span class="sxs-lookup"><span data-stu-id="24460-232">Next</span></span>

[<span data-ttu-id="24460-233">Uso del colore in Direct2D</span><span class="sxs-lookup"><span data-stu-id="24460-233">Using Color in Direct2D</span></span>](using-color-in-direct2d.md)

 

 
