---
title: Stampa guidata foto
description: La stampa guidata foto consente agli utenti di stampare le foto fornendo un'interfaccia di facile utilizzo della procedura guidata.
ms.assetid: 9cc2c7d4-a2aa-4abc-9c63-b091e044804f
keywords:
- Stampa guidata foto
- IDropTarget, stampa guidata foto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 708f051f658739cebd08e4f8643e5dd7fc0c6f7f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104399001"
---
# <a name="photo-printing-wizard"></a><span data-ttu-id="d8a75-105">Stampa guidata foto</span><span class="sxs-lookup"><span data-stu-id="d8a75-105">Photo Printing Wizard</span></span>

<span data-ttu-id="d8a75-106">La stampa guidata foto consente agli utenti di stampare le foto fornendo un'interfaccia di facile utilizzo della procedura guidata.</span><span class="sxs-lookup"><span data-stu-id="d8a75-106">The Photo Printing Wizard helps users print photos by providing an easy-to-use wizard interface.</span></span> <span data-ttu-id="d8a75-107">La procedura guidata consente all'utente di specificare le dimensioni di stampa foto e altre opzioni di stampa, quindi di inviare le foto alla stampante.</span><span class="sxs-lookup"><span data-stu-id="d8a75-107">The wizard enables the user to specify photo print sizes and other print options, and then sends the photos to the printer.</span></span> <span data-ttu-id="d8a75-108">La procedura guidata è progettata in modo da poter essere richiamata a livello di codice da qualsiasi applicazione che desideri offrire agli utenti la possibilità di stampare foto e specificare il ridimensionamento e altre opzioni di stampa.</span><span class="sxs-lookup"><span data-stu-id="d8a75-108">The wizard is designed so that it can be invoked programmatically by any application that wants to offer users the ability to print photos and specify sizing and other print options.</span></span> <span data-ttu-id="d8a75-109">La stampa guidata foto è disponibile in Windows XP e Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="d8a75-109">The Photo Printing Wizard is available on Windows XP and Windows Vista.</span></span>

-   [<span data-ttu-id="d8a75-110">Funzionalità fornite dalla procedura guidata di stampa foto</span><span class="sxs-lookup"><span data-stu-id="d8a75-110">Features Provided by the Photo Print Wizard</span></span>](#features-provided-by-the-photo-print-wizard)
-   [<span data-ttu-id="d8a75-111">Formati di file di foto supportati</span><span class="sxs-lookup"><span data-stu-id="d8a75-111">Supported Photo File Formats</span></span>](#supported-photo-file-formats)
-   [<span data-ttu-id="d8a75-112">Avvio a livello di codice della procedura guidata di stampa foto</span><span class="sxs-lookup"><span data-stu-id="d8a75-112">Programmatically Launching the Photo Print Wizard</span></span>](#programmatically-launching-the-photo-print-wizard)

## <a name="features-provided-by-the-photo-print-wizard"></a><span data-ttu-id="d8a75-113">Funzionalità fornite dalla procedura guidata di stampa foto</span><span class="sxs-lookup"><span data-stu-id="d8a75-113">Features Provided by the Photo Print Wizard</span></span>

<span data-ttu-id="d8a75-114">La procedura guidata per la stampa fotografica offre diverse opzioni che potrebbero non essere disponibili nelle finestre di dialogo comuni della stampante, ad esempio modelli a più layout con dimensioni accurate.</span><span class="sxs-lookup"><span data-stu-id="d8a75-114">The Photo Printing Wizard offers several options that may not be available on common printer dialogs, such as multi-layout templates with accurate dimensions.</span></span> <span data-ttu-id="d8a75-115">I modelli di layout consentono agli utenti di sfruttare al meglio lo spazio disponibile su carta stampata fotografica.</span><span class="sxs-lookup"><span data-stu-id="d8a75-115">The layout templates enable users to make the most efficient use of the space available on photographic printing paper.</span></span> <span data-ttu-id="d8a75-116">Altre opzioni che è possibile specificare o a cui si accede tramite la procedura guidata di stampa foto includono:</span><span class="sxs-lookup"><span data-stu-id="d8a75-116">Other options that can be specified or accessed through the Photo Print Wizard include:</span></span>

-   <span data-ttu-id="d8a75-117">Selezione di una stampante da un elenco di stampanti disponibili o destinazioni di stampa virtuale (ad esempio, Microsoft XPS Document Writer).</span><span class="sxs-lookup"><span data-stu-id="d8a75-117">Selecting a printer from a list of available printers or virtual printing destinations (for example, Microsoft XPS Document Writer).</span></span> <span data-ttu-id="d8a75-118">In Windows Vista è possibile che siano disponibili le opzioni seguenti, a seconda delle funzionalità della stampante o della destinazione di stampa virtuale:</span><span class="sxs-lookup"><span data-stu-id="d8a75-118">On Windows Vista, the following options may be available, depending on the capabilities of the printer or virtual printing destination:</span></span>
    -   <span data-ttu-id="d8a75-119">Formato della carta.</span><span class="sxs-lookup"><span data-stu-id="d8a75-119">Paper size.</span></span> <span data-ttu-id="d8a75-120">Ad esempio, "Letter", "Legal", "a3".</span><span class="sxs-lookup"><span data-stu-id="d8a75-120">For example, "Letter", "Legal", "A3".</span></span>
    -   <span data-ttu-id="d8a75-121">Qualità di stampa, in termini di risoluzioni DPI (punti per pollice) supportati.</span><span class="sxs-lookup"><span data-stu-id="d8a75-121">Print quality, in terms of supported dots per inch (dpi) resolutions.</span></span>
    -   <span data-ttu-id="d8a75-122">Tipo di carta.</span><span class="sxs-lookup"><span data-stu-id="d8a75-122">Paper type.</span></span> <span data-ttu-id="d8a75-123">Ad esempio, "Plain" o "glossy".</span><span class="sxs-lookup"><span data-stu-id="d8a75-123">For example, "Plain" or "Glossy".</span></span>
-   <span data-ttu-id="d8a75-124">Avvio delle preferenze di stampa e delle proprietà per una particolare stampante.</span><span class="sxs-lookup"><span data-stu-id="d8a75-124">Launching the printing preferences and properties for a particular printer.</span></span>
-   <span data-ttu-id="d8a75-125">Impostazione delle **copie di ogni immagine** (in Windows Vista) o **numero di volte in cui utilizzare** i valori della casella di selezione di ogni immagine (in Windows XP).</span><span class="sxs-lookup"><span data-stu-id="d8a75-125">Setting the **Copies of each picture** (on Windows Vista) or **Number of times to use each picture** (on Windows XP) spin box values.</span></span>
-   <span data-ttu-id="d8a75-126">Specifica di un modello di layout di stampa.</span><span class="sxs-lookup"><span data-stu-id="d8a75-126">Specifying a print layout template.</span></span> <span data-ttu-id="d8a75-127">Ad esempio, vengono **stampate** **foto a pagina intera** o portafogli.</span><span class="sxs-lookup"><span data-stu-id="d8a75-127">For example, **Full page photo** or **Wallet prints**.</span></span>
-   <span data-ttu-id="d8a75-128">Selezione dell'opzione **Adatta immagine a frame** (disponibile solo in Windows Vista).</span><span class="sxs-lookup"><span data-stu-id="d8a75-128">Selecting the **Fit picture to frame** option (available on Windows Vista only).</span></span>
-   <span data-ttu-id="d8a75-129">Visualizzazione in anteprima della foto stampata con le opzioni attualmente specificate.</span><span class="sxs-lookup"><span data-stu-id="d8a75-129">Previewing the printed photo with the currently specified options.</span></span>
-   <span data-ttu-id="d8a75-130">Accesso a opzioni di stampa avanzate, ad esempio **nitidezza per la stampa e la** **gestione dei colori** (disponibile solo in Windows Vista).</span><span class="sxs-lookup"><span data-stu-id="d8a75-130">Accesssing advanced print options, such as **Sharpen for printing** and **Color management** (available on Windows Vista only).</span></span>

<span data-ttu-id="d8a75-131">Qualsiasi applicazione può trarre vantaggio dalle funzionalità e dalla funzionalità di stampa foto offerte dalla procedura guidata di stampa foto.</span><span class="sxs-lookup"><span data-stu-id="d8a75-131">Any application can benefit from the features and photo printing capability offered by the Photo Printing Wizard.</span></span> <span data-ttu-id="d8a75-132">Un'applicazione può passare i file da stampare.</span><span class="sxs-lookup"><span data-stu-id="d8a75-132">An application can pass in the files to be printed.</span></span> <span data-ttu-id="d8a75-133">La stampa guidata foto esegue quindi la preparazione del file per la stampa in base alle opzioni specificate dall'utente e invia i file preparati alla stampante.</span><span class="sxs-lookup"><span data-stu-id="d8a75-133">The Photo Printing Wizard then takes care of preparing the file for printing based on the options specified by the user and sends the prepared files to the printer.</span></span>

<span data-ttu-id="d8a75-134">Nella figura seguente è illustrata l'interfaccia della procedura guidata stampa foto in Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d8a75-134">The following figure shows the Photo Printing Wizard interface on Windows Vista</span></span>

![Creazione guidata foto in Windows Vista](images/ppw-vista.png)

<span data-ttu-id="d8a75-136">Nella figura seguente è illustrata l'interfaccia della procedura guidata stampa foto in Windows XP</span><span class="sxs-lookup"><span data-stu-id="d8a75-136">The following figure shows the Photo Printing Wizard interface on Windows XP</span></span>

![procedura guidata di stampa fotografica in Windows XP](images/ppw-xp.png)

## <a name="supported-photo-file-formats"></a><span data-ttu-id="d8a75-138">Formati di file di foto supportati</span><span class="sxs-lookup"><span data-stu-id="d8a75-138">Supported Photo File Formats</span></span>

<span data-ttu-id="d8a75-139">In Windows XP, la procedura guidata di stampa fotografica supporta tutti i formati di file grafici supportati da Windows GDI+.</span><span class="sxs-lookup"><span data-stu-id="d8a75-139">On Windows XP, the Photo Print Wizard supports all graphics file formats that are supported by Windows GDI+.</span></span> <span data-ttu-id="d8a75-140">Attualmente, questi formati di file includono:</span><span class="sxs-lookup"><span data-stu-id="d8a75-140">Currently, these file formats include:</span></span>

-   <span data-ttu-id="d8a75-141">Bitmap (BMP)</span><span class="sxs-lookup"><span data-stu-id="d8a75-141">Bitmap (BMP)</span></span>
-   <span data-ttu-id="d8a75-142">Graphics Interchange Format (GIF)</span><span class="sxs-lookup"><span data-stu-id="d8a75-142">Graphics Interchange Format (GIF)</span></span>
-   <span data-ttu-id="d8a75-143">Joint Photographic Experts Group (JPEG)</span><span class="sxs-lookup"><span data-stu-id="d8a75-143">Joint Photographic Experts Group (JPEG)</span></span>
-   <span data-ttu-id="d8a75-144">File di immagine scambiabile (EXIF)</span><span class="sxs-lookup"><span data-stu-id="d8a75-144">Exchangeable Image File (EXIF)</span></span>
-   <span data-ttu-id="d8a75-145">Portable Network Graphics (PNG)</span><span class="sxs-lookup"><span data-stu-id="d8a75-145">Portable Network Graphics (PNG)</span></span>
-   <span data-ttu-id="d8a75-146">Tagged Image File Format (TIFF)</span><span class="sxs-lookup"><span data-stu-id="d8a75-146">Tagged Image File Format (TIFF)</span></span>

<span data-ttu-id="d8a75-147">Per ulteriori informazioni sui formati di file grafici supportati da GDI+, vedere [tipi di bitmap](../gdiplus/-gdiplus-types-of-bitmaps-about.md).</span><span class="sxs-lookup"><span data-stu-id="d8a75-147">For more information about graphics file formats supported by GDI+, see [Types of Bitmaps](../gdiplus/-gdiplus-types-of-bitmaps-about.md).</span></span>

<span data-ttu-id="d8a75-148">In Windows Vista, la procedura guidata di stampa fotografica supporta qualsiasi formato di file di immagine per cui è installato un codec di Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="d8a75-148">On Windows Vista, the Photo Print Wizard supports any image file format for which a Windows Imaging Component (WIC) codec is installed.</span></span> <span data-ttu-id="d8a75-149">WIC fornisce diversi codec standard, tra cui:</span><span class="sxs-lookup"><span data-stu-id="d8a75-149">WIC provides several standard codecs, including:</span></span>

-   <span data-ttu-id="d8a75-150">Bitmap (BMP)</span><span class="sxs-lookup"><span data-stu-id="d8a75-150">Bitmap (BMP)</span></span>
-   <span data-ttu-id="d8a75-151">GIF</span><span class="sxs-lookup"><span data-stu-id="d8a75-151">GIF</span></span>
-   <span data-ttu-id="d8a75-152">Formato dell'icona (ICO)</span><span class="sxs-lookup"><span data-stu-id="d8a75-152">Icon Format (ICO)</span></span>
-   <span data-ttu-id="d8a75-153">JPEG</span><span class="sxs-lookup"><span data-stu-id="d8a75-153">JPEG</span></span>
-   <span data-ttu-id="d8a75-154">PNG</span><span class="sxs-lookup"><span data-stu-id="d8a75-154">PNG</span></span>
-   <span data-ttu-id="d8a75-155">TIFF</span><span class="sxs-lookup"><span data-stu-id="d8a75-155">TIFF</span></span>
-   <span data-ttu-id="d8a75-156">Formato foto Windows Media</span><span class="sxs-lookup"><span data-stu-id="d8a75-156">Windows Media Photo format</span></span>

<span data-ttu-id="d8a75-157">Per ulteriori informazioni sui codec WIC e WIC, vedere [componente Windows Imaging](https://msdn.microsoft.com/library/ms737408(VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="d8a75-157">For more information about WIC and WIC codecs, see [Windows Imaging Component](https://msdn.microsoft.com/library/ms737408(VS.85).aspx)</span></span>

## <a name="programmatically-launching-the-photo-print-wizard"></a><span data-ttu-id="d8a75-158">Avvio a livello di codice della procedura guidata di stampa foto</span><span class="sxs-lookup"><span data-stu-id="d8a75-158">Programmatically Launching the Photo Print Wizard</span></span>

<span data-ttu-id="d8a75-159">Per richiamare la stampa guidata foto, chiamare l'interfaccia [IDropTarget](/windows/win32/api/oleidl/nn-oleidl-idroptarget) con l'identificatore di classe seguente (CLSID):</span><span class="sxs-lookup"><span data-stu-id="d8a75-159">To invoke the Photo Printing Wizard, call the [IDropTarget](/windows/win32/api/oleidl/nn-oleidl-idroptarget) interface with the following class identifier (CLSID):</span></span>


```
static const CLSID CLSID_PrintPhotosDropTarget = 
  {0x60fd46de, 0xf830, 0x4894, {0xa6, 0x28, 0x6f, 0xa8, 0x1b, 0xc0, 0x19, 0x0d}};
```



<span data-ttu-id="d8a75-160">I file da elaborare tramite la procedura guidata di stampa foto sono specificati in un oggetto [IDataObject](/windows/win32/api/objidl/nn-objidl-idataobject) .</span><span class="sxs-lookup"><span data-stu-id="d8a75-160">The files to be processed by the Photo Printing Wizard are specified in an [IDataObject](/windows/win32/api/objidl/nn-objidl-idataobject) object.</span></span>

<span data-ttu-id="d8a75-161">Nell'esempio di codice riportato di seguito viene illustrato come richiamare la stampa guidata foto.</span><span class="sxs-lookup"><span data-stu-id="d8a75-161">The following code example demonstrates how to invoke the Photo Printing Wizard.</span></span>


```
static const CLSID CLSID_PrintPhotosDropTarget = 
  {0x60fd46de, 0xf830, 0x4894, {0xa6, 0x28, 0x6f, 0xa8, 0x1b, 0xc0, 0x19, 0x0d}};
            
// A data object that contains the list of photos to print.
IDataObject* pDataObject;

// Create the Photo Printing Wizard drop target.
CComPtr<IDropTarget> spDropTarget;
        
hr = CoCreateInstance(CLSID_PrintPhotosDropTarget,
                      NULL,
                      CLSCTX_INPROC_SERVER,
                      IID_PPV_ARGS(&spDropTarget));

// Drop the data object onto the drop target.
POINTL pt = {0};
DWORD dwEffect = DROPEFFECT_LINK | DROPEFFECT_MOVE | DROPEFFECT_COPY;

spDropTarget->DragEnter(pDataObject, MK_LBUTTON, pt, &dwEffect);

spDropTarget->Drop(pDataObject, MK_LBUTTON, pt, &dwEffect);}
```



 

 