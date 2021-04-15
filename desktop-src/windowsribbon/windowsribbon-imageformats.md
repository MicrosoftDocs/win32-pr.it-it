---
title: Specifica delle risorse dell'immagine della barra multifunzione
description: Il Framework della barra multifunzione di Windows è progettato per supportare le risorse di immagine in modo esteso nell'interfaccia utente (UI) della barra multifunzione. Tutte le risorse immagine sono dichiarate in markup della barra multifunzione o eseguite da un'applicazione host della barra multifunzione.
ms.assetid: 37b57992-8da8-4e6b-869d-72a136f6ad77
keywords:
- Barra multifunzione di Windows, risorse immagine
- Barra multifunzione, risorse immagine
- Barra multifunzione di Windows, trasparenza
- Barra multifunzione, trasparenza
- Barra multifunzione di Windows, profondità colore
- Barra multifunzione, profondità colore
- Barra multifunzione di Windows, contrasto
- Barra multifunzione, contrasto
- risorse immagine nella barra multifunzione di Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13e7666126e5b8f7fbe8b610678a8a1d71589373
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473923"
---
# <a name="specifying-ribbon-image-resources"></a><span data-ttu-id="49b25-113">Specifica delle risorse dell'immagine della barra multifunzione</span><span class="sxs-lookup"><span data-stu-id="49b25-113">Specifying Ribbon Image Resources</span></span>

<span data-ttu-id="49b25-114">Il Framework della barra multifunzione di Windows è progettato per supportare le risorse di immagine in modo esteso nell'interfaccia utente (UI) della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="49b25-114">As a rich command presentation system, the Windows Ribbon framework is designed to support image resources extensively throughout the Ribbon user interface (UI).</span></span> <span data-ttu-id="49b25-115">Tutte le risorse immagine sono dichiarate in [markup della barra multifunzione](windowsribbon-schema.md) o eseguite da un'applicazione host della barra multifunzione.</span><span class="sxs-lookup"><span data-stu-id="49b25-115">All image resources are declared in [Ribbon markup](windowsribbon-schema.md) or queried from a Ribbon host application.</span></span>

<span data-ttu-id="49b25-116">Per Windows 8 e versioni successive, il Framework della barra multifunzione supporta i formati grafici seguenti: file di bitmap (BMP) a 32 bit ARGB (BMP) e file Portable Network Graphics (PNG) con trasparenza.</span><span class="sxs-lookup"><span data-stu-id="49b25-116">For Windows 8 and later, the Ribbon framework supports the following graphics formats: 32-bit ARGB bitmap (BMP) files and Portable Network Graphics (PNG) files with transparency.</span></span>

<span data-ttu-id="49b25-117">Per Windows 7 e versioni precedenti, le risorse di immagine devono essere conformi al formato di grafica BMP standard usato in Windows.</span><span class="sxs-lookup"><span data-stu-id="49b25-117">For Windows 7 and earlier, image resources must conform to the standard BMP graphics format used in Windows.</span></span>

> [!Note]  
> <span data-ttu-id="49b25-118">È possibile che si verifichi un errore di compilazione se al Framework viene fornito un formato di immagine non supportato.</span><span class="sxs-lookup"><span data-stu-id="49b25-118">A compilation error may occur if an unsupported image format is supplied to the framework.</span></span>

 

## <a name="image-sizes"></a><span data-ttu-id="49b25-119">Dimensioni delle immagini</span><span class="sxs-lookup"><span data-stu-id="49b25-119">Image Sizes</span></span>

<span data-ttu-id="49b25-120">Per garantire una maggiore flessibilità per i layout di controllo della barra multifunzione durante il ridimensionamento di una finestra dell'applicazione, il Framework della barra multifunzione accetta ed esegue il rendering delle immagini in una delle due dimensioni: grande o piccola.</span><span class="sxs-lookup"><span data-stu-id="49b25-120">To provide greater flexibility for Ribbon control layouts when resizing an application window, the Ribbon framework accepts and renders images in one of two sizes: large or small.</span></span>

<span data-ttu-id="49b25-121">Nelle immagini seguenti viene illustrata un'applicazione Ribbon che supporta più dimensioni della barra multifunzione tramite layout di controllo flessibili e la sostituzione di immagini di grandi dimensioni con piccole immagini, ove disponibili.</span><span class="sxs-lookup"><span data-stu-id="49b25-121">The following images illustrate a Ribbon application that supports multiple Ribbon sizes through flexible control layouts and the replacement of large images with small images where available.</span></span>

<span data-ttu-id="49b25-122">Lo screenshot seguente mostra la barra multifunzione con immagini di grandi dimensioni per i controlli dello zoom.</span><span class="sxs-lookup"><span data-stu-id="49b25-122">The following screen shot shows the Ribbon with large images for the Zoom controls.</span></span>

![screenshot che mostra una barra multifunzione che usa immagini di grandi dimensioni per i controlli dello zoom.](images/overviews/imageresources-largeimage.png)

<span data-ttu-id="49b25-124">Lo screenshot seguente mostra la stessa barra multifunzione ridimensionata con immagini piccole per i controlli zoom</span><span class="sxs-lookup"><span data-stu-id="49b25-124">The following screen shot shows the same Ribbon resized with small images for the Zoom controls</span></span>

![screenshot che mostra una barra multifunzione che usa immagini piccole per i controlli dello zoom.](images/overviews/imageresources-smallimage.png)

<span data-ttu-id="49b25-126">Lo screenshot seguente mostra la barra multifunzione nello stato nascosto.</span><span class="sxs-lookup"><span data-stu-id="49b25-126">The following screen shot shows the ribbon in hidden state.</span></span> <span data-ttu-id="49b25-127">La barra multifunzione è nascosta quando tutti i layout di controllo potenziali sono esauriti e non è possibile eseguire il rendering della barra multifunzione con un'area di lavoro applicazione utilizzabile.</span><span class="sxs-lookup"><span data-stu-id="49b25-127">The ribbon is hidden when all potential control layouts have been exhausted and the ribbon cannot be rendered with a usable application workspace.</span></span>

![screenshot che mostra una barra multifunzione compressa.](images/overviews/imageresources-noimage.png)

<span data-ttu-id="49b25-129">Per qualsiasi immagine, le dimensioni esatte del pixel dipendono dalla risoluzione dello schermo o da punti per pollice (dpi) del monitoraggio usato.</span><span class="sxs-lookup"><span data-stu-id="49b25-129">For any image, the exact pixel size is dependent on the display resolution, or dots per inch (dpi), of the monitor being used.</span></span> <span data-ttu-id="49b25-130">A 96 dpi, le immagini di grandi dimensioni sono 32x32 pixel e le immagini piccole hanno dimensioni di 16x16 pixel.</span><span class="sxs-lookup"><span data-stu-id="49b25-130">At 96 dpi, large images are 32x32 pixels in size and small images are 16x16 pixels in size.</span></span> <span data-ttu-id="49b25-131">Le dimensioni dell'immagine aumentano in modo lineare rispetto a dpi, come illustrato nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="49b25-131">The image sizes increase in a linear fashion relative to dpi as illustrated in the following table.</span></span>



| <span data-ttu-id="49b25-132">DPI</span><span class="sxs-lookup"><span data-stu-id="49b25-132">DPI</span></span>     | <span data-ttu-id="49b25-133">Immagine piccola</span><span class="sxs-lookup"><span data-stu-id="49b25-133">Small Image</span></span>  | <span data-ttu-id="49b25-134">Immagine grande</span><span class="sxs-lookup"><span data-stu-id="49b25-134">Large Image</span></span>  |
|---------|--------------|--------------|
| <span data-ttu-id="49b25-135">96 dpi</span><span class="sxs-lookup"><span data-stu-id="49b25-135">96 dpi</span></span>  | <span data-ttu-id="49b25-136">pixel 16x16</span><span class="sxs-lookup"><span data-stu-id="49b25-136">16x16 pixels</span></span> | <span data-ttu-id="49b25-137">pixel 32x32</span><span class="sxs-lookup"><span data-stu-id="49b25-137">32x32 pixels</span></span> |
| <span data-ttu-id="49b25-138">120 dpi</span><span class="sxs-lookup"><span data-stu-id="49b25-138">120 dpi</span></span> | <span data-ttu-id="49b25-139">pixel 20x20</span><span class="sxs-lookup"><span data-stu-id="49b25-139">20x20 pixels</span></span> | <span data-ttu-id="49b25-140">40x40 pixel</span><span class="sxs-lookup"><span data-stu-id="49b25-140">40x40 pixels</span></span> |
| <span data-ttu-id="49b25-141">144 dpi</span><span class="sxs-lookup"><span data-stu-id="49b25-141">144 dpi</span></span> | <span data-ttu-id="49b25-142">pixel 24x24</span><span class="sxs-lookup"><span data-stu-id="49b25-142">24x24 pixels</span></span> | <span data-ttu-id="49b25-143">pixel 48x48</span><span class="sxs-lookup"><span data-stu-id="49b25-143">48x48 pixels</span></span> |
| <span data-ttu-id="49b25-144">192 DPI</span><span class="sxs-lookup"><span data-stu-id="49b25-144">192 dpi</span></span> | <span data-ttu-id="49b25-145">pixel 32x32</span><span class="sxs-lookup"><span data-stu-id="49b25-145">32x32 pixels</span></span> | <span data-ttu-id="49b25-146">pixel 64x64</span><span class="sxs-lookup"><span data-stu-id="49b25-146">64x64 pixels</span></span> |



 

<span data-ttu-id="49b25-147">Il Framework della barra multifunzione ridimensiona le risorse dell'immagine in modo obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="49b25-147">The Ribbon framework scales image resources as required.</span></span> <span data-ttu-id="49b25-148">Tuttavia, poiché il ridimensionamento può produrre artefatti indesiderati e un calo delle immagini, è consigliabile che l'applicazione fornisca un piccolo set di risorse immagine che si estendono su diverse impostazioni dpi utilizzate comunemente.</span><span class="sxs-lookup"><span data-stu-id="49b25-148">However, because resizing may yield undesirable artifacts and image degradation, it is highly recommended that the application provide a small set of image resources that span various commonly used dpi settings.</span></span> <span data-ttu-id="49b25-149">Se non viene trovata una corrispondenza esatta, l'immagine più vicina verrà ridimensionata verso l'alto o verso il basso.</span><span class="sxs-lookup"><span data-stu-id="49b25-149">If an exact match is not found, the nearest image will be scaled up or down.</span></span>

<span data-ttu-id="49b25-150">Per semplificare questa operazione, le risorse di immagine possono essere dichiarate nel markup della barra multifunzione usando un set di elementi [**immagine**](windowsribbon-element-image.md) per ogni elemento [**Command**](windowsribbon-element-command.md) .</span><span class="sxs-lookup"><span data-stu-id="49b25-150">To facilitate this, image resources can be declared in Ribbon markup by using a set of [**Image**](windowsribbon-element-image.md) elements for each [**Command**](windowsribbon-element-command.md) element.</span></span> <span data-ttu-id="49b25-151">In fase di esecuzione, il Framework seleziona l'immagine da visualizzare in base all'attributo *MinDPI* di ogni elemento **Image** .</span><span class="sxs-lookup"><span data-stu-id="49b25-151">At run time, the framework selects the image to display based on the *MinDPI* attribute of each **Image** element.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="49b25-152">Quando una raccolta di risorse immagine progettate per supportare specifiche impostazioni DPI dello schermo viene fornita al framework della barra multifunzione tramite un set di elementi [**immagine**](windowsribbon-element-image.md) , il Framework usa l' **immagine** con un valore dell'attributo *MinDPI* che corrisponde all'impostazione DPI dello schermo corrente.</span><span class="sxs-lookup"><span data-stu-id="49b25-152">When a collection of image resources that are designed to support specific screen dpi settings is supplied to the Ribbon framework through a set of [**Image**](windowsribbon-element-image.md) elements, the framework uses the **Image** with a *MinDPI* attribute value that matches the current screen dpi setting.</span></span>
>
> <span data-ttu-id="49b25-153">Se nessun elemento [**Image**](windowsribbon-element-image.md) è dichiarato con un valore *MinDPI* che corrisponde all'impostazione DPI dello schermo corrente, il Framework seleziona l' **immagine** con il valore *MinDPI* più vicino inferiore rispetto all'impostazione DPI dello schermo corrente e ridimensiona la risorsa dell'immagine verso l'alto.</span><span class="sxs-lookup"><span data-stu-id="49b25-153">If no [**Image**](windowsribbon-element-image.md) element is declared with a *MinDPI* value that matches the current screen dpi setting, the framework picks the **Image** that has the nearest *MinDPI* value less than the current screen dpi setting and scales the image resource up.</span></span> <span data-ttu-id="49b25-154">In caso contrario, se non viene dichiarato alcun elemento **Image** con un valore dell'attributo *MinDPI* inferiore a quello della schermata corrente, il Framework sceglie il valore *MinDPI* più vicino maggiore dell'impostazione corrente DPI dello schermo e ridimensiona la risorsa immagine verso il basso.</span><span class="sxs-lookup"><span data-stu-id="49b25-154">Otherwise, if no **Image** element is declared with a *MinDPI* attribute value less than the current screen dpi setting, the framework picks the nearest *MinDPI* value greater than the current screen dpi setting and scales the image resource down.</span></span>

 

<span data-ttu-id="49b25-155">Nell'esempio seguente viene illustrato come dichiarare un set di immagini per adattare le varie dimensioni della barra multifunzione e le impostazioni di sistema.</span><span class="sxs-lookup"><span data-stu-id="49b25-155">The following example illustrates how to declare a set of images to accommodate various Ribbon sizes and system settings.</span></span>


```C++
<Command.LargeImages>
  <Image Source="res/CutLargeImage32.bmp" Id="116" Symbol="ID_CUT_LARGEIMAGE1" MinDPI="96" />
  <Image Source="res/CutLargeImage40.bmp" Id="117" Symbol="ID_CUT_LARGEIMAGE2" MinDPI="120" />
  <Image Source="res/CutLargeImage48.bmp" Id="118" Symbol="ID_CUT_LARGEIMAGE3" MinDPI="144" />
  <Image Source="res/CutLargeImage64.bmp" Id="119" Symbol="ID_CUT_LARGEIMAGE4" MinDPI="192" />
</Command.LargeImages>
<Command.SmallImages>
  <Image Source="res/CutSmallImage16.bmp" Id="122" Symbol="ID_CUT_SMALLIMAGE1" MinDPI="96" />
  <Image Source="res/CutSmallImage20.bmp" Id="123" Symbol="ID_CUT_SMALLIMAGE2" MinDPI="120" />
  <Image Source="res/CutSmallImage24.bmp" Id="124" Symbol="ID_CUT_SMALLIMAGE3" MinDPI="144" />
  <Image Source="res/CutSmallImage32.bmp" Id="125" Symbol="ID_CUT_SMALLIMAGE4" MinDPI="192" />
</Command.SmallImages>
<Command.LargeHighContrastImages>
  <Image Source="res/CutLargeImage32HC.bmp" Id="130" Symbol="ID_CUT_LARGEIMAGE1HC" MinDPI="96" />
  <Image Source="res/CutLargeImage40HC.bmp" Id="131" Symbol="ID_CUT_LARGEIMAGE2HC" MinDPI="120" />
  <Image Source="res/CutLargeImage48HC.bmp" Id="132" Symbol="ID_CUT_LARGEIMAGE3HC" MinDPI="144" />
  <Image Source="res/CutLargeImage64HC.bmp" Id="133" Symbol="ID_CUT_LARGEIMAGE4HC" MinDPI="192" />
</Command.LargeHighContrastImages>
<Command.SmallHighContrastImages>
  <Image Source="res/CutSmallImage16HC.bmp" Id="135" Symbol="ID_CUT_SMALLIMAGE1HC" MinDPI="96" />
  <Image Source="res/CutSmallImage20HC.bmp" Id="136" Symbol="ID_CUT_SMALLIMAGE2HC" MinDPI="120" />
  <Image Source="res/CutSmallImage24HC.bmp" Id="137" Symbol="ID_CUT_SMALLIMAGE3HC" MinDPI="144" />
  <Image Source="res/CutSmallImage32HC.bmp" Id="138" Symbol="ID_CUT_SMALLIMAGE4HC" MinDPI="192" />
</Command.SmallHighContrastImages>
```



<span data-ttu-id="49b25-156">Se le immagini dichiarate nel markup vengono invalidate in fase di esecuzione per qualsiasi motivo, viene eseguita una query sulle nuove immagini nell'applicazione host.</span><span class="sxs-lookup"><span data-stu-id="49b25-156">If images declared in markup are invalidated at run time for any reason, the host application is queried for new images.</span></span> <span data-ttu-id="49b25-157">Quando queste immagini vengono generate e caricate a livello di codice, l'applicazione deve tentare di restituire immagini ridimensionate in base alle dimensioni predefinite delle icone di sistema determinate dalla [ \_ metrica di sistema CXICON SM](/windows/win32/api/winuser/nf-winuser-getsystemmetrics).</span><span class="sxs-lookup"><span data-stu-id="49b25-157">When these images are generated and loaded programmatically, the application should attempt to return images that are sized according to the default system icon sizes determined by the [SM\_CXICON system metric](/windows/win32/api/winuser/nf-winuser-getsystemmetrics).</span></span>

> [!Note]  
> <span data-ttu-id="49b25-158">Le immagini di grandi dimensioni hanno una dimensione di SM \_ CXICON per SM \_ CXICON e le immagini piccole hanno una dimensione di SM \_ CXICON/2 per SM \_ CXICON/2.</span><span class="sxs-lookup"><span data-stu-id="49b25-158">Large images have a size of SM\_CXICON by SM\_CXICON and small images have a size of SM\_CXICON/2 by SM\_CXICON/2.</span></span>

 

## <a name="color-depth-transparency-and-contrast"></a><span data-ttu-id="49b25-159">Profondità di colore, trasparenza e contrasto</span><span class="sxs-lookup"><span data-stu-id="49b25-159">Color Depth, Transparency, and Contrast</span></span>

<span data-ttu-id="49b25-160">Si prevede che le immagini regolari siano in formato pixel ARGB a 32 bit per pixel (BPP) e ridimensionate in base alle dimensioni dell'icona di sistema predefinite.</span><span class="sxs-lookup"><span data-stu-id="49b25-160">Regular images are expected to be in 32 bits per pixel (BPP) ARGB pixel format and scaled to the default system icon size.</span></span> <span data-ttu-id="49b25-161">Questo formato supporta la trasparenza e l'anti-aliasing (con 8 bit per canale).</span><span class="sxs-lookup"><span data-stu-id="49b25-161">This format supports both transparency and antialiasing (using 8 bits per channel).</span></span>

> [!WARNING]
> <span data-ttu-id="49b25-162">Molti strumenti di modifica delle immagini non mantengono il canale alfa a 8 bit di ordine più alto durante il caricamento o il salvataggio di immagini di 32 BPP.</span><span class="sxs-lookup"><span data-stu-id="49b25-162">Many image editing tools do not preserve the highest order 8-bit alpha channel when loading or saving 32 BPP images.</span></span>

 

<span data-ttu-id="49b25-163">Per visualizzare correttamente un'immagine in modalità a contrasto elevato, è necessario che sia in formato pixel a 4 BPP.</span><span class="sxs-lookup"><span data-stu-id="49b25-163">For an image to display correctly in high-contrast mode, it must be in a 4 BPP palletized pixel format.</span></span> <span data-ttu-id="49b25-164">Quando viene eseguito il rendering dell'immagine, il Framework della barra multifunzione esegue il mapping dei colori specifici in base al contesto a contrasto elevato dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="49b25-164">When the image is rendered, the Ribbon framework remaps specific colors based on the high-contrast context of the image.</span></span>

<span data-ttu-id="49b25-165">La tabella seguente elenca il comportamento di rendering dei colori a contrasto elevato del Framework.</span><span class="sxs-lookup"><span data-stu-id="49b25-165">The following table lists the high-contrast color rendering behavior of the framework.</span></span>



<span data-ttu-id="49b25-166">Colore dei pixel</span><span class="sxs-lookup"><span data-stu-id="49b25-166">Pixel color</span></span>

<span data-ttu-id="49b25-167">Valore RGB</span><span class="sxs-lookup"><span data-stu-id="49b25-167">RGB value</span></span>

<span data-ttu-id="49b25-168">Comportamento</span><span class="sxs-lookup"><span data-stu-id="49b25-168">Behavior</span></span>

<span data-ttu-id="49b25-169">Sfondo bianco</span><span class="sxs-lookup"><span data-stu-id="49b25-169">White background</span></span>

<span data-ttu-id="49b25-170">Sfondo scuro</span><span class="sxs-lookup"><span data-stu-id="49b25-170">Dark Background</span></span>

<span data-ttu-id="49b25-171">MAGENTA</span><span class="sxs-lookup"><span data-stu-id="49b25-171">MAGENTA</span></span>

<span data-ttu-id="49b25-172">800080</span><span class="sxs-lookup"><span data-stu-id="49b25-172">800080</span></span>

<span data-ttu-id="49b25-173">Modalità trasparente</span><span class="sxs-lookup"><span data-stu-id="49b25-173">Transparent</span></span>

<span data-ttu-id="49b25-174">Modalità trasparente</span><span class="sxs-lookup"><span data-stu-id="49b25-174">Transparent</span></span>

<span data-ttu-id="49b25-175">NERO</span><span class="sxs-lookup"><span data-stu-id="49b25-175">BLACK</span></span>

<span data-ttu-id="49b25-176">000000</span><span class="sxs-lookup"><span data-stu-id="49b25-176">000000</span></span>

<span data-ttu-id="49b25-177">\_WINDOWTEXT colore</span><span class="sxs-lookup"><span data-stu-id="49b25-177">COLOR\_WINDOWTEXT</span></span>

<span data-ttu-id="49b25-178">BIANCO</span><span class="sxs-lookup"><span data-stu-id="49b25-178">WHITE</span></span>

<span data-ttu-id="49b25-179">BIANCO</span><span class="sxs-lookup"><span data-stu-id="49b25-179">WHITE</span></span>

<span data-ttu-id="49b25-180">FFFFFF</span><span class="sxs-lookup"><span data-stu-id="49b25-180">FFFFFF</span></span>

<span data-ttu-id="49b25-181">\_finestra colori</span><span class="sxs-lookup"><span data-stu-id="49b25-181">COLOR\_WINDOW</span></span>

<span data-ttu-id="49b25-182">NERO</span><span class="sxs-lookup"><span data-stu-id="49b25-182">BLACK</span></span>

<span data-ttu-id="49b25-183">GRIGIO SCURO</span><span class="sxs-lookup"><span data-stu-id="49b25-183">DARK GRAY</span></span>

<span data-ttu-id="49b25-184">808080</span><span class="sxs-lookup"><span data-stu-id="49b25-184">808080</span></span>

<span data-ttu-id="49b25-185">\_3DSHADOW colore</span><span class="sxs-lookup"><span data-stu-id="49b25-185">COLOR\_3DSHADOW</span></span>

<span data-ttu-id="49b25-186">\_3DSHADOW colore</span><span class="sxs-lookup"><span data-stu-id="49b25-186">COLOR\_3DSHADOW</span></span>

<span data-ttu-id="49b25-187">GRIGIO</span><span class="sxs-lookup"><span data-stu-id="49b25-187">GRAY</span></span>

<span data-ttu-id="49b25-188">C0C0C0</span><span class="sxs-lookup"><span data-stu-id="49b25-188">C0C0C0</span></span>

<span data-ttu-id="49b25-189">\_3DFACE colore</span><span class="sxs-lookup"><span data-stu-id="49b25-189">COLOR\_3DFACE</span></span>

<span data-ttu-id="49b25-190">\_3DFACE colore</span><span class="sxs-lookup"><span data-stu-id="49b25-190">COLOR\_3DFACE</span></span>

<span data-ttu-id="49b25-191">GRIGIO CHIARO</span><span class="sxs-lookup"><span data-stu-id="49b25-191">LIGHT GRAY</span></span>

<span data-ttu-id="49b25-192">ATTIGLIO</span><span class="sxs-lookup"><span data-stu-id="49b25-192">DFDFDF</span></span>

<span data-ttu-id="49b25-193">\_3DLIGHT colore</span><span class="sxs-lookup"><span data-stu-id="49b25-193">COLOR\_3DLIGHT</span></span>

<span data-ttu-id="49b25-194">\_3DLIGHT colore</span><span class="sxs-lookup"><span data-stu-id="49b25-194">COLOR\_3DLIGHT</span></span>

<span data-ttu-id="49b25-195">BLU SCURO</span><span class="sxs-lookup"><span data-stu-id="49b25-195">DARK BLUE</span></span>

<span data-ttu-id="49b25-196">000080</span><span class="sxs-lookup"><span data-stu-id="49b25-196">000080</span></span>

<span data-ttu-id="49b25-197">n/d</span><span class="sxs-lookup"><span data-stu-id="49b25-197">n/a</span></span>

<span data-ttu-id="49b25-198">BIANCO</span><span class="sxs-lookup"><span data-stu-id="49b25-198">WHITE</span></span>



 

<span data-ttu-id="49b25-199">Per ulteriori informazioni sui formati di immagine supportati dal framework della barra multifunzione, vedere gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="49b25-199">For more information on the image formats supported by the Ribbon framework, see the following:</span></span>

-   <span data-ttu-id="49b25-200">[Struttura BITMAPINFOHEADER](/previous-versions//dd183376(v=vs.85)) : descrive il formato pixel ARGB di 32 BPP.</span><span class="sxs-lookup"><span data-stu-id="49b25-200">[BITMAPINFOHEADER structure](/previous-versions//dd183376(v=vs.85)) - describes the 32 BPP ARGB pixel format.</span></span>
-   <span data-ttu-id="49b25-201">[Funzione CreateDIBSection](/windows/win32/api/wingdi/nf-wingdi-createdibsection) : descrive come creare un'immagine in formato pixel ARGB a 32 BPP.</span><span class="sxs-lookup"><span data-stu-id="49b25-201">[CreateDIBSection function](/windows/win32/api/wingdi/nf-wingdi-createdibsection) - describes how to create a 32 BPP ARGB pixel format image.</span></span>
-   <span data-ttu-id="49b25-202">[Funzione LoadImage](/windows/win32/api/winuser/nf-winuser-loadimagea) : descrive come caricare un'immagine in formato pixel ARGB a 32 BPP.</span><span class="sxs-lookup"><span data-stu-id="49b25-202">[LoadImage function](/windows/win32/api/winuser/nf-winuser-loadimagea) - describes how to load a 32 BPP ARGB pixel format image.</span></span>

## <a name="accessibility"></a><span data-ttu-id="49b25-203">Accessibilità</span><span class="sxs-lookup"><span data-stu-id="49b25-203">Accessibility</span></span>

<span data-ttu-id="49b25-204">Basandosi sulle risorse immagine per fornire informazioni, trasmettere funzionalità di controllo ed esporre lo stato dell'applicazione, è possibile aumentare la necessità di requisiti di accessibilità durante la progettazione e lo sviluppo di applicazioni.</span><span class="sxs-lookup"><span data-stu-id="49b25-204">Relying on image resources to provide information, convey control functionality, and expose application state, increases the need for accessibility requirements during application design and development.</span></span>

<span data-ttu-id="49b25-205">Per il supporto di base a contrasto elevato, la barra multifunzione consente di visualizzare un set separato di file di immagine quando è attivo un tema a contrasto elevato.</span><span class="sxs-lookup"><span data-stu-id="49b25-205">For basic high contrast support, the Ribbon allows for a separate set of image files to be displayed when a high-contrast theme is active.</span></span> <span data-ttu-id="49b25-206">Queste immagini possono essere di 32 BPP o 4 BPP, con colori mappati a una tavolozza speciale in cui i colori scuro e chiaro vengono invertiti a seconda dei colori di primo piano e di sfondo del tema attivo a contrasto elevato.</span><span class="sxs-lookup"><span data-stu-id="49b25-206">These images can be 32 BPP or 4 BPP, with colors mapped to a special palette where dark and light colors are inverted depending on the foreground and background colors of the active high-contrast theme.</span></span>

<span data-ttu-id="49b25-207">Nell'esempio seguente viene illustrato come vengono dichiarate le risorse immagine a contrasto elevato nel markup della barra multifunzione:</span><span class="sxs-lookup"><span data-stu-id="49b25-207">The following example demonstrates how high-contrast image resources are declared in Ribbon markup:</span></span>


```C++
<Command Name="cmdNew" Id="0xE100" Symbol="ID_CMD_NEW" LabelTitle="New document" Keytip="N" >
      <Command.TooltipTitle>New (Ctrl+N)</Command.TooltipTitle>
      <Command.TooltipDescription>Create a new document.</Command.TooltipDescription>
      <Command.LargeImages>
        <Image Source="cmdNew-32px.bmp" MinDPI="96" />
        <Image Source="cmdNew-40px.bmp" MinDPI="120" />
        <Image Source="cmdNew-48px.bmp" MinDPI="144" />
        <Image Source="cmdNew-64px.bmp" MinDPI="192" />
      </Command.LargeImages>
      <Command.LargeHighContrastImages>
        <Image Source="cmdNew-32px-HC.bmp" MinDPI="96" />
        <Image Source="cmdNew-40px-HC.bmp" MinDPI="120" />
        <Image Source="cmdNew-48px-HC.bmp" MinDPI="144" />
        <Image Source="cmdNew-64px-HC.bmp" MinDPI="192" />
      </Command.LargeHighContrastImages>
      <Command.SmallImages>
        <Image Source="cmdNew-16px.bmp" MinDPI="96" />
        <Image Source="cmdNew-20px.bmp" MinDPI="120" />
        <Image Source="cmdNew-24px.bmp" MinDPI="144" />
        <Image Source="cmdNew-32px.bmp" MinDPI="192" />
      </Command.SmallImages>
      <Command.SmallHighContrastImages>
        <Image Source="cmdNew-16px-HC.bmp" MinDPI="96" />
        <Image Source="cmdNew-20px-HC.bmp" MinDPI="120" />
        <Image Source="cmdNew-24px-HC.bmp" MinDPI="144" />
        <Image Source="cmdNew-32px-HC.bmp" MinDPI="192" />
      </Command.SmallHighContrastImages>
    </Command>
```



## <a name="related-topics"></a><span data-ttu-id="49b25-208">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="49b25-208">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="49b25-209">**Comando. SmallImages**</span><span class="sxs-lookup"><span data-stu-id="49b25-209">**Command.SmallImages**</span></span>](windowsribbon-element-command-smallimages.md)
</dt> <dt>

[<span data-ttu-id="49b25-210">Interfaccia utente \_ pkey \_ smallImage</span><span class="sxs-lookup"><span data-stu-id="49b25-210">UI\_PKEY\_SmallImage</span></span>](windowsribbon-reference-properties-uipkey-smallimage.md)
</dt> <dt>

[<span data-ttu-id="49b25-211">**Comando. LargeImages**</span><span class="sxs-lookup"><span data-stu-id="49b25-211">**Command.LargeImages**</span></span>](windowsribbon-element-command-largeimages.md)
</dt> <dt>

[<span data-ttu-id="49b25-212">Interfaccia utente \_ pkey \_ largeImage</span><span class="sxs-lookup"><span data-stu-id="49b25-212">UI\_PKEY\_LargeImage</span></span>](windowsribbon-reference-properties-uipkey-largeimage.md)
</dt> <dt>

[<span data-ttu-id="49b25-213">**Comando. SmallHighContrastImages**</span><span class="sxs-lookup"><span data-stu-id="49b25-213">**Command.SmallHighContrastImages**</span></span>](windowsribbon-element-command-smallhighcontrastimages.md)
</dt> <dt>

[<span data-ttu-id="49b25-214">Interfaccia utente \_ pkey \_ SmallHighContrastImage</span><span class="sxs-lookup"><span data-stu-id="49b25-214">UI\_PKEY\_SmallHighContrastImage</span></span>](windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md)
</dt> <dt>

[<span data-ttu-id="49b25-215">**Comando. LargeHighContrastImages**</span><span class="sxs-lookup"><span data-stu-id="49b25-215">**Command.LargeHighContrastImages**</span></span>](windowsribbon-element-command-largehighcontrastimages.md)
</dt> <dt>

[<span data-ttu-id="49b25-216">Interfaccia utente \_ pkey \_ LargeHighContrastImage</span><span class="sxs-lookup"><span data-stu-id="49b25-216">UI\_PKEY\_LargeHighContrastImage</span></span>](windowsribbon-reference-properties-uipkey-largehighcontrastimage.md)
</dt> </dl>

 

 