---
description: Windows Vista consente di utilizzare in modo più significativo le immagini di anteprima specifiche dei file rispetto alle versioni precedenti di Windows.
title: Gestori di anteprime
ms.topic: article
ms.date: 07/02/2018
ms.assetid: ed9e17bb-aa28-4f8c-8b5a-9b57cab1c438
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: d81accf59401a46dd6b5611e15a67eeec68d5d82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233189"
---
# <a name="thumbnail-handlers"></a><span data-ttu-id="dac9a-103">Gestori di anteprime</span><span class="sxs-lookup"><span data-stu-id="dac9a-103">Thumbnail Handlers</span></span>

<span data-ttu-id="dac9a-104">Windows Vista consente di utilizzare in modo più significativo le immagini di anteprima specifiche dei file rispetto alle versioni precedenti di Windows.</span><span class="sxs-lookup"><span data-stu-id="dac9a-104">Windows Vista makes greater use of file-specific thumbnail images than earlier versions of Windows.</span></span> <span data-ttu-id="dac9a-105">Windows Vista viene usato in tutte le visualizzazioni, nelle finestre di dialogo e per qualsiasi tipo di file che li fornisce.</span><span class="sxs-lookup"><span data-stu-id="dac9a-105">Windows Vista uses them in all views, in dialogs, and for any file type that provides them.</span></span> <span data-ttu-id="dac9a-106">Anche le altre applicazioni possono utilizzare l'anteprima.</span><span class="sxs-lookup"><span data-stu-id="dac9a-106">Other applications can consume your thumbnail as well.</span></span> <span data-ttu-id="dac9a-107">È stata modificata anche la visualizzazione delle anteprime.</span><span class="sxs-lookup"><span data-stu-id="dac9a-107">Thumbnail display has also changed.</span></span> <span data-ttu-id="dac9a-108">A questo punto, è disponibile uno spettro continuo di dimensioni selezionabili dall'utente anziché le dimensioni discrete, ad esempio le icone e le anteprime fornite in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="dac9a-108">Now, a continuous spectrum of user-selectable sizes is available rather than the discrete sizes such as Icons and Thumbnails provided in Windows XP.</span></span>

> [!Note]  
> <span data-ttu-id="dac9a-109">Si potrebbero sentire queste anteprime denominate icone attive.</span><span class="sxs-lookup"><span data-stu-id="dac9a-109">You might hear these thumbnails referred to as Live Icons.</span></span>

 

<span data-ttu-id="dac9a-110">Le anteprime della risoluzione a 32 bit e le dimensioni di 256x256 pixel vengono spesso utilizzate nell'interfaccia utente di Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="dac9a-110">Thumbnails of 32-bit resolution and as large as 256x256 pixels are often used in Windows Vista UI.</span></span> <span data-ttu-id="dac9a-111">I proprietari del formato di file devono essere preparati per visualizzare le anteprime a tale dimensione.</span><span class="sxs-lookup"><span data-stu-id="dac9a-111">File format owners should be prepared to display their thumbnails at that size.</span></span> <span data-ttu-id="dac9a-112">Devono inoltre fornire immagini non statiche per le anteprime che riflettono il contenuto del file specifico.</span><span class="sxs-lookup"><span data-stu-id="dac9a-112">They should also provide non-static images for their thumbnails that reflect the particular file's contents.</span></span> <span data-ttu-id="dac9a-113">Ad esempio, l'anteprima di un file di testo dovrebbe mostrare una versione in miniatura del documento, incluso il testo.</span><span class="sxs-lookup"><span data-stu-id="dac9a-113">For example, a text file's thumbnail should show a miniature version of the document, including its text.</span></span>

<span data-ttu-id="dac9a-114">L'interfaccia [**IThumbnailProvider**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) è stata introdotta in modo da rendere più semplice e intuitiva la visualizzazione di un'anteprima, quando sarebbe stato usato [**IExtractImage**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iextractimage) .</span><span class="sxs-lookup"><span data-stu-id="dac9a-114">The [**IThumbnailProvider**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) interface has been introduced to make providing a thumbnail easier and more straightforward than in the past, when [**IExtractImage**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iextractimage) would have been used instead.</span></span> <span data-ttu-id="dac9a-115">Si noti che il codice esistente che usa **IExtractImage** è ancora valido in Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="dac9a-115">Note, that existing code that uses **IExtractImage** is still valid under Windows Vista.</span></span> <span data-ttu-id="dac9a-116">Tuttavia, **IExtractImage** non è supportato nel riquadro dei **Dettagli** .</span><span class="sxs-lookup"><span data-stu-id="dac9a-116">However, **IExtractImage** is not supported in the **Details** pane.</span></span>

<span data-ttu-id="dac9a-117">In questo argomento vengono trattati i seguenti temi:</span><span class="sxs-lookup"><span data-stu-id="dac9a-117">This topic discusses the following:</span></span>

-   [<span data-ttu-id="dac9a-118">Processi di anteprima</span><span class="sxs-lookup"><span data-stu-id="dac9a-118">Thumbnail Processes</span></span>](#thumbnail-processes)
-   [<span data-ttu-id="dac9a-119">Dimensioni e cache delle anteprime</span><span class="sxs-lookup"><span data-stu-id="dac9a-119">Thumbnail Cache and Sizing</span></span>](#thumbnail-cache-and-sizing)
-   [<span data-ttu-id="dac9a-120">Sovrimpressioni anteprima</span><span class="sxs-lookup"><span data-stu-id="dac9a-120">Thumbnail Overlays</span></span>](#thumbnail-overlays)
-   [<span data-ttu-id="dac9a-121">Aree di visualizzazione delle anteprime</span><span class="sxs-lookup"><span data-stu-id="dac9a-121">Thumbnail Adornments</span></span>](#thumbnail-adornments)
-   [<span data-ttu-id="dac9a-122">Registrazione del gestore di anteprime</span><span class="sxs-lookup"><span data-stu-id="dac9a-122">Registering Your Thumbnail Handler</span></span>](#registering-your-thumbnail-handler)
-   [<span data-ttu-id="dac9a-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="dac9a-123">Related topics</span></span>](#related-topics)

## <a name="thumbnail-processes"></a><span data-ttu-id="dac9a-124">Processi di anteprima</span><span class="sxs-lookup"><span data-stu-id="dac9a-124">Thumbnail Processes</span></span>

<span data-ttu-id="dac9a-125">I gestori, inclusi i gestori di anteprime, vengono eseguiti per impostazione predefinita in un processo separato.</span><span class="sxs-lookup"><span data-stu-id="dac9a-125">Handlers, including thumbnail handlers, run by default in a separate process.</span></span> <span data-ttu-id="dac9a-126">È possibile forzare l'esecuzione in-process del gestore passando un valore **null** come contesto di associazione in una chiamata a [**IShellItem:: BindToHandler**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-bindtohandler) come illustrato di seguito:</span><span class="sxs-lookup"><span data-stu-id="dac9a-126">You can force the handler to run in-process by passing a **NULL** value as the bind context in a call to [**IShellItem::BindToHandler**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-bindtohandler) as shown here:</span></span>


```
IShellItem::BindToHandler(NULL, BHID_ThumbnailHandler,..)
```



<span data-ttu-id="dac9a-127">Per impostazione predefinita, è anche possibile rifiutare esplicitamente l'esecuzione out-of-process impostando la voce DisableProcessIsolation nel registro di sistema, come illustrato in questo esempio.</span><span class="sxs-lookup"><span data-stu-id="dac9a-127">You can also opt out of running out of process by default by setting the DisableProcessIsolation entry in the registry as shown in this example.</span></span> <span data-ttu-id="dac9a-128">L'identificatore di classe (CLSID) {E357FCCD-A995-4576-B01F-234630154E96} è il CLSID per le implementazioni di [**IThumbnailProvider**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) .</span><span class="sxs-lookup"><span data-stu-id="dac9a-128">The class identifier (CLSID) {E357FCCD-A995-4576-B01F-234630154E96} is the CLSID for [**IThumbnailProvider**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) implementations.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {E357FCCD-A995-4576-B01F-234630154E96}
         DisableProcessIsolation = 1
```

## <a name="thumbnail-cache-and-sizing"></a><span data-ttu-id="dac9a-129">Dimensioni e cache delle anteprime</span><span class="sxs-lookup"><span data-stu-id="dac9a-129">Thumbnail Cache and Sizing</span></span>

<span data-ttu-id="dac9a-130">Quando è necessaria un'anteprima, Windows controlla prima di tutto la cache delle anteprime per l'immagine.</span><span class="sxs-lookup"><span data-stu-id="dac9a-130">When a thumbnail is needed, Windows first checks the thumbnail cache for the image.</span></span> <span data-ttu-id="dac9a-131">L'estrazione dell'anteprima viene chiamata se l'immagine non viene trovata nella cache.</span><span class="sxs-lookup"><span data-stu-id="dac9a-131">The thumbnail extractor is called if the image is not found in the cache.</span></span> <span data-ttu-id="dac9a-132">Viene anche chiamato quando l'ora dell'Ultima modifica dell'immagine è successiva a quella della copia nella cache.</span><span class="sxs-lookup"><span data-stu-id="dac9a-132">It is also called when the last modified time of the image is later than that of the copy in the cache.</span></span>

<span data-ttu-id="dac9a-133">Le immagini di anteprima in questa cache vengono archiviate in un set di dimensioni discrete.</span><span class="sxs-lookup"><span data-stu-id="dac9a-133">The thumbnail images in this cache are stored in a set of discrete sizes.</span></span> <span data-ttu-id="dac9a-134">Tutte le dimensioni vengono specificate in pixel.</span><span class="sxs-lookup"><span data-stu-id="dac9a-134">All sizes are given in pixels.</span></span>

-   <span data-ttu-id="dac9a-135">32x32</span><span class="sxs-lookup"><span data-stu-id="dac9a-135">32x32</span></span>
-   <span data-ttu-id="dac9a-136">96x96</span><span class="sxs-lookup"><span data-stu-id="dac9a-136">96x96</span></span>
-   <span data-ttu-id="dac9a-137">256x256</span><span class="sxs-lookup"><span data-stu-id="dac9a-137">256x256</span></span>
-   <span data-ttu-id="dac9a-138">1024x1024</span><span class="sxs-lookup"><span data-stu-id="dac9a-138">1024x1024</span></span>

> [!Note]  
> <span data-ttu-id="dac9a-139">Questi valori sono soggetti a modifiche.</span><span class="sxs-lookup"><span data-stu-id="dac9a-139">These values are subject to change.</span></span> <span data-ttu-id="dac9a-140">Il codice non deve presupporre che vengano sempre utilizzate dimensioni specifiche.</span><span class="sxs-lookup"><span data-stu-id="dac9a-140">You code should not assume that any particular size will always be used.</span></span>

 

<span data-ttu-id="dac9a-141">Se un'immagine non è quadrata, non è necessario riempirla manualmente.</span><span class="sxs-lookup"><span data-stu-id="dac9a-141">If an image is not square, you should not pad it yourself.</span></span> <span data-ttu-id="dac9a-142">Windows è responsabile del rispetto delle proporzioni originali e del riempimento dell'immagine a una dimensione quadrata.</span><span class="sxs-lookup"><span data-stu-id="dac9a-142">Windows is responsible for respecting the original aspect ratio and padding the image to a square size.</span></span>

<span data-ttu-id="dac9a-143">Quando viene richiesta un'immagine di una determinata dimensione, a meno che non venga rilevata una corrispondenza esatta, Windows Vista recupera sempre l'immagine più grande successiva e la ridimensiona fino alla dimensione richiesta.</span><span class="sxs-lookup"><span data-stu-id="dac9a-143">When an image of a particular size is asked for, unless an exact match is found, Windows Vista always retrieves the next largest image and scales it down to the requested size.</span></span> <span data-ttu-id="dac9a-144">Le dimensioni di un'immagine non vengono mai ridimensionate come nel caso delle versioni precedenti di Windows.</span><span class="sxs-lookup"><span data-stu-id="dac9a-144">An image is never scaled up in size as was the case in previous versions of Windows.</span></span>

<span data-ttu-id="dac9a-145">Nella tabella seguente vengono forniti alcuni esempi della relazione tra le dimensioni richieste e le dimensioni disponibili.</span><span class="sxs-lookup"><span data-stu-id="dac9a-145">The following table gives some examples of the relationship between requested size and available size.</span></span>



| <span data-ttu-id="dac9a-146">Dimensioni massime dell'immagine fornite</span><span class="sxs-lookup"><span data-stu-id="dac9a-146">Maximum Image Size You Provide</span></span> | <span data-ttu-id="dac9a-147">Dimensioni richieste dall'estrattore</span><span class="sxs-lookup"><span data-stu-id="dac9a-147">Size Requested by the Extractor</span></span> | <span data-ttu-id="dac9a-148">Fornire</span><span class="sxs-lookup"><span data-stu-id="dac9a-148">You Provide</span></span>                                 |
|--------------------------------|---------------------------------|---------------------------------------------|
| <span data-ttu-id="dac9a-149">156x120</span><span class="sxs-lookup"><span data-stu-id="dac9a-149">156x120</span></span>                        | <span data-ttu-id="dac9a-150">256x256</span><span class="sxs-lookup"><span data-stu-id="dac9a-150">256x256</span></span>                         | <span data-ttu-id="dac9a-151">156x120 (non riempire, mantenere le proporzioni)</span><span class="sxs-lookup"><span data-stu-id="dac9a-151">156x120 (Do not pad, maintain aspect ratio)</span></span> |
| <span data-ttu-id="dac9a-152">2048x1024</span><span class="sxs-lookup"><span data-stu-id="dac9a-152">2048x1024</span></span>                      | <span data-ttu-id="dac9a-153">256x256</span><span class="sxs-lookup"><span data-stu-id="dac9a-153">256x256</span></span>                         | <span data-ttu-id="dac9a-154">con dimensioni 256x128 (non riempire, mantenere le proporzioni)</span><span class="sxs-lookup"><span data-stu-id="dac9a-154">256x128 (Do not pad, maintain aspect ratio)</span></span> |



 

<span data-ttu-id="dac9a-155">È possibile dichiarare un punto di interruzione come parte della voce dell'ID programma dell'app associata nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="dac9a-155">You can declare a cutoff point as part of the program ID entry of the associated app in the registry.</span></span> <span data-ttu-id="dac9a-156">Al di sotto di questa dimensione, le anteprime non vengono usate.</span><span class="sxs-lookup"><span data-stu-id="dac9a-156">Below this size, thumbnails are not used.</span></span>

```
HKEY_CLASSES_ROOT
   .{ProgId}
      ThumbnailCutoff
```

<span data-ttu-id="dac9a-157">La voce ThumbnailCutoff è uno dei \_ valori DWORD reg.</span><span class="sxs-lookup"><span data-stu-id="dac9a-157">The ThumbnailCutoff entry is one of these REG\_DWORD values.</span></span>

| <span data-ttu-id="dac9a-158">Valore</span><span class="sxs-lookup"><span data-stu-id="dac9a-158">Value</span></span> | <span data-ttu-id="dac9a-159">Cambio data</span><span class="sxs-lookup"><span data-stu-id="dac9a-159">Cutoff</span></span> | <span data-ttu-id="dac9a-160">HighDPI sensibile</span><span class="sxs-lookup"><span data-stu-id="dac9a-160">HighDPI Sensitive</span></span> |
|-------|--------|-------------------|
| <span data-ttu-id="dac9a-161">0</span><span class="sxs-lookup"><span data-stu-id="dac9a-161">0</span></span>     | <span data-ttu-id="dac9a-162">32x32</span><span class="sxs-lookup"><span data-stu-id="dac9a-162">32x32</span></span>  | <span data-ttu-id="dac9a-163">Sì</span><span class="sxs-lookup"><span data-stu-id="dac9a-163">Yes</span></span>               |
| <span data-ttu-id="dac9a-164">1</span><span class="sxs-lookup"><span data-stu-id="dac9a-164">1</span></span>     | <span data-ttu-id="dac9a-165">16x16</span><span class="sxs-lookup"><span data-stu-id="dac9a-165">16x16</span></span>  | <span data-ttu-id="dac9a-166">Sì</span><span class="sxs-lookup"><span data-stu-id="dac9a-166">Yes</span></span>               |
| <span data-ttu-id="dac9a-167">2</span><span class="sxs-lookup"><span data-stu-id="dac9a-167">2</span></span>     | <span data-ttu-id="dac9a-168">48x48</span><span class="sxs-lookup"><span data-stu-id="dac9a-168">48x48</span></span>  | <span data-ttu-id="dac9a-169">Sì</span><span class="sxs-lookup"><span data-stu-id="dac9a-169">Yes</span></span>               |
| <span data-ttu-id="dac9a-170">3</span><span class="sxs-lookup"><span data-stu-id="dac9a-170">3</span></span>     | <span data-ttu-id="dac9a-171">16x16</span><span class="sxs-lookup"><span data-stu-id="dac9a-171">16x16</span></span>  | <span data-ttu-id="dac9a-172">Sì</span><span class="sxs-lookup"><span data-stu-id="dac9a-172">Yes</span></span>               |


<span data-ttu-id="dac9a-173">Una sensibilità di punti per pollice (dpi) elevata indica che le dimensioni in pixel dell'anteprima vengono regolate automaticamente per il valore dpi maggiore.</span><span class="sxs-lookup"><span data-stu-id="dac9a-173">High dots per inch (dpi) sensitivity means that the pixel dimensions of the thumbnail automatically adjust for the greater dpi.</span></span> <span data-ttu-id="dac9a-174">Ad esempio, un'immagine di 32x32 a 96 dpi sarà un'immagine 40x40 a 120 dpi.</span><span class="sxs-lookup"><span data-stu-id="dac9a-174">For instance, a 32x32 image at 96 dpi would be a 40x40 image at 120 dpi.</span></span>

<span data-ttu-id="dac9a-175">Se la voce ThumbnailCutoff non è specificata, il valore predefinito di cutoff è 20x20 (non con distinzione dpi).</span><span class="sxs-lookup"><span data-stu-id="dac9a-175">If the ThumbnailCutoff entry is not specified, the default cutoff is 20x20 (not dpi-sensitive).</span></span>

## <a name="thumbnail-overlays"></a><span data-ttu-id="dac9a-176">Sovrimpressioni anteprima</span><span class="sxs-lookup"><span data-stu-id="dac9a-176">Thumbnail Overlays</span></span>

<span data-ttu-id="dac9a-177">Le sovrapposizioni di anteprime, una piccola immagine visualizzata sull'angolo inferiore destro dell'anteprima, offrono agli sviluppatori la possibilità di applicare l'identificazione del marchio alle anteprime.</span><span class="sxs-lookup"><span data-stu-id="dac9a-177">Thumbnail overlays, a small image displayed over the lower right corner of the thumbnail, provide an opportunity for developers to apply brand identification to their thumbnails.</span></span> <span data-ttu-id="dac9a-178">Le sovrimpressioni vengono dichiarate nel registro di sistema come parte della voce dell'ID programma dell'app associata, come illustrato di seguito:</span><span class="sxs-lookup"><span data-stu-id="dac9a-178">Overlays are declared in the registry as part of the program ID entry of the associated app, as shown here:</span></span>

```
HKEY_CLASSES_ROOT
   .{ProgId}
      TypeOverlay
```

<span data-ttu-id="dac9a-179">La voce TypeOverlay contiene un \_ valore reg SZ interpretato nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="dac9a-179">The TypeOverlay entry contains a REG\_SZ value interpreted as follows:</span></span>

-   <span data-ttu-id="dac9a-180">Se il valore è un riferimento a una risorsa (un file con estensione **ico** incorporato nella dll) `ISVComponent.dll,-155` , ad esempio, tale immagine viene usata come sovrapposizione per i file con l'estensione di tale file.</span><span class="sxs-lookup"><span data-stu-id="dac9a-180">If the value is a resource reference (a **.ico** file embedded in the DLL) such as `ISVComponent.dll,-155`, that image is used as the overlay for files with that file name extension.</span></span> <span data-ttu-id="dac9a-181">Si noti che in questo esempio **155** è l'ID resouce e se la dll non è presente in un percorso standard, ad esempio **C:/Windows/system32**, il percorso completo è obbligatorio anziché solo il nome della dll.</span><span class="sxs-lookup"><span data-stu-id="dac9a-181">Note that in this example, **155** is the resouce ID, and if the DLL is not present in a standard path (such as **C:/Windows/System32**), the full path is required instead of just the DLL name.</span></span>
-   <span data-ttu-id="dac9a-182">Se il valore è una stringa vuota, non viene applicata alcuna sovrapposizione all'immagine.</span><span class="sxs-lookup"><span data-stu-id="dac9a-182">If the value is an empty string, no overlay is applied to the image.</span></span>
-   <span data-ttu-id="dac9a-183">Se il valore non è presente, viene utilizzata l'icona predefinita dell'applicazione associata.</span><span class="sxs-lookup"><span data-stu-id="dac9a-183">If the value is not present, the default icon of the associated application is used.</span></span>

<span data-ttu-id="dac9a-184">Le sovrimpressioni per le anteprime devono essere fornite solo tramite questo meccanismo e applicate da Windows.</span><span class="sxs-lookup"><span data-stu-id="dac9a-184">Overlays for your thumbnails should only be provided through this mechanism and applied by Windows.</span></span> <span data-ttu-id="dac9a-185">Non applicare sovrapposizioni.</span><span class="sxs-lookup"><span data-stu-id="dac9a-185">Do not apply overlays yourself.</span></span>

## <a name="thumbnail-adornments"></a><span data-ttu-id="dac9a-186">Aree di visualizzazione delle anteprime</span><span class="sxs-lookup"><span data-stu-id="dac9a-186">Thumbnail Adornments</span></span>

<span data-ttu-id="dac9a-187">Le aree di visualizzazione, ad esempio le ombreggiature, vengono applicate alle anteprime basate sul tema attualmente selezionato dell'utente.</span><span class="sxs-lookup"><span data-stu-id="dac9a-187">Adornments such as drop shadows are applied to thumbnails based on the user's currently selected theme.</span></span> <span data-ttu-id="dac9a-188">Le aree di strumenti sono fornite da Windows; non crearli manualmente.</span><span class="sxs-lookup"><span data-stu-id="dac9a-188">Adornments are provided by Windows; do not create them yourself.</span></span> <span data-ttu-id="dac9a-189">Windows potrebbe modificare l'aspetto di particolari aree di specializzazione in qualsiasi momento, pertanto se si ha la proprietà si rischia di non essere sincronizzati con il sistema.</span><span class="sxs-lookup"><span data-stu-id="dac9a-189">Windows could change the look of particular adornments at any time, so if you provided you own you would risk falling out of sync with the system.</span></span> <span data-ttu-id="dac9a-190">È possibile che le anteprime si trovino in un punto qualsiasi.</span><span class="sxs-lookup"><span data-stu-id="dac9a-190">Your thumbnails could wind up looking dated or out of place.</span></span>

<span data-ttu-id="dac9a-191">Le aree di visualizzazione potenziali sono dichiarate nel registro di sistema come parte della voce dell'ID programma dell'app associata, come illustrato di seguito:</span><span class="sxs-lookup"><span data-stu-id="dac9a-191">Potential adornments are declared in the registry as part of the program ID entry of the associated app, as shown here:</span></span>

```
HKEY_CLASSES_ROOT
   .{ProgId}
      Treatment
```

<span data-ttu-id="dac9a-192">La voce relativa al trattamento contiene uno dei \_ valori DWORD reg seguenti:</span><span class="sxs-lookup"><span data-stu-id="dac9a-192">The Treatment entry contains one of these REG\_DWORD values:</span></span>



| <span data-ttu-id="dac9a-193">Valore</span><span class="sxs-lookup"><span data-stu-id="dac9a-193">Value</span></span> | <span data-ttu-id="dac9a-194">Significato</span><span class="sxs-lookup"><span data-stu-id="dac9a-194">Meaning</span></span>         |
|-------|-----------------|
| <span data-ttu-id="dac9a-195">0</span><span class="sxs-lookup"><span data-stu-id="dac9a-195">0</span></span>     | <span data-ttu-id="dac9a-196">Nessun ornamento</span><span class="sxs-lookup"><span data-stu-id="dac9a-196">No Adornment</span></span>    |
| <span data-ttu-id="dac9a-197">1</span><span class="sxs-lookup"><span data-stu-id="dac9a-197">1</span></span>     | <span data-ttu-id="dac9a-198">Ombreggiatura</span><span class="sxs-lookup"><span data-stu-id="dac9a-198">Drop Shadow</span></span>     |
| <span data-ttu-id="dac9a-199">2</span><span class="sxs-lookup"><span data-stu-id="dac9a-199">2</span></span>     | <span data-ttu-id="dac9a-200">Bordo foto</span><span class="sxs-lookup"><span data-stu-id="dac9a-200">Photo Border</span></span>    |
| <span data-ttu-id="dac9a-201">3</span><span class="sxs-lookup"><span data-stu-id="dac9a-201">3</span></span>     | <span data-ttu-id="dac9a-202">Pignoni video</span><span class="sxs-lookup"><span data-stu-id="dac9a-202">Video Sprockets</span></span> |


<span data-ttu-id="dac9a-203">Per impostazione predefinita, un'ombreggiatura viene applicata alle immagini.</span><span class="sxs-lookup"><span data-stu-id="dac9a-203">A drop shadow is applied to images by default.</span></span>

## <a name="registering-your-thumbnail-handler"></a><span data-ttu-id="dac9a-204">Registrazione del gestore di anteprime</span><span class="sxs-lookup"><span data-stu-id="dac9a-204">Registering Your Thumbnail Handler</span></span>

<span data-ttu-id="dac9a-205">La registrazione di un gestore di anteprime è basata sulle associazioni di file standard.</span><span class="sxs-lookup"><span data-stu-id="dac9a-205">Registration of a thumbnail handler is based on standard file associations.</span></span>

<span data-ttu-id="dac9a-206">Il GUID dell'estensione della shell del gestore di anteprime è `E357FCCD-A995-4576-B01F-234630154E96` .</span><span class="sxs-lookup"><span data-stu-id="dac9a-206">The GUID for the thumbnail handler Shell extension is `E357FCCD-A995-4576-B01F-234630154E96`.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dac9a-207">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="dac9a-207">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dac9a-208">**IThumbnailProvider**</span><span class="sxs-lookup"><span data-stu-id="dac9a-208">**IThumbnailProvider**</span></span>](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider)
</dt> <dt>

[<span data-ttu-id="dac9a-209">Compilazione di gestori di anteprime</span><span class="sxs-lookup"><span data-stu-id="dac9a-209">Building Thumbnail Handlers</span></span>](building-thumbnail-providers.md)
</dt> <dt>

[<span data-ttu-id="dac9a-210">Linee guida per gestore anteprime</span><span class="sxs-lookup"><span data-stu-id="dac9a-210">Thumbnail Handler Guidelines</span></span>](thumbnail-provider-guidelines.md)
</dt> </dl>

 

 



