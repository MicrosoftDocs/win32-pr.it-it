---
description: Questo argomento descrive come spostarsi in un OM XPS e accedere a diverse parti del documento in memoria.
ms.assetid: 90b726aa-29da-4cfb-9c69-f471c2acb678
title: Esplorare XPS OM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0ec33543867f66dd4da65ef95aab0cdfd8cfe0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315986"
---
# <a name="navigate-the-xps-om"></a><span data-ttu-id="69d9e-103">Esplorare XPS OM</span><span class="sxs-lookup"><span data-stu-id="69d9e-103">Navigate the XPS OM</span></span>

<span data-ttu-id="69d9e-104">Questo argomento descrive come spostarsi in un OM XPS e accedere a diverse parti del documento in memoria.</span><span class="sxs-lookup"><span data-stu-id="69d9e-104">This topic describes how to navigate an XPS OM and to access different parts of the in-memory document.</span></span>

<span data-ttu-id="69d9e-105">L'organizzazione dell'API del documento XPS rispecchia l'organizzazione di un documento XPS.</span><span class="sxs-lookup"><span data-stu-id="69d9e-105">The organization of the XPS Document API mirrors the organization of an XPS document.</span></span> <span data-ttu-id="69d9e-106">Nella tabella seguente viene illustrato il modo in cui le interfacce dell'API del documento XPS sono correlate ai componenti di un documento XPS.</span><span class="sxs-lookup"><span data-stu-id="69d9e-106">The following table illustrates how the interfaces of the XPS Document API relate to the components of an XPS document.</span></span>



| <span data-ttu-id="69d9e-107">Componente documento XPS</span><span class="sxs-lookup"><span data-stu-id="69d9e-107">XPS document component</span></span>                                         | <span data-ttu-id="69d9e-108">Interfaccia API documenti XPS</span><span class="sxs-lookup"><span data-stu-id="69d9e-108">XPS Document API interface</span></span>                                          | <span data-ttu-id="69d9e-109">Metodo da chiamare per il livello successivo nella gerarchia</span><span class="sxs-lookup"><span data-stu-id="69d9e-109">Method to call for the next level down in the hierarchy</span></span>                                                                                       |
|----------------------------------------------------------------|---------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69d9e-110">File di documento XPS (contiene il pacchetto OPC)</span><span class="sxs-lookup"><span data-stu-id="69d9e-110">XPS document file (contains OPC package)</span></span><br/>            | [<span data-ttu-id="69d9e-111">**IXpsOMPackage**</span><span class="sxs-lookup"><span data-stu-id="69d9e-111">**IXpsOMPackage**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage)<br/>                   | [<span data-ttu-id="69d9e-112">**GetDocumentSequence**</span><span class="sxs-lookup"><span data-stu-id="69d9e-112">**GetDocumentSequence**</span></span>](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-getdocumentsequence)<br/>                                                                   |
| <span data-ttu-id="69d9e-113">Parte FixedDocumentSequence</span><span class="sxs-lookup"><span data-stu-id="69d9e-113">FixedDocumentSequence part</span></span><br/>                          | [<span data-ttu-id="69d9e-114">**IXpsOMDocumentSequence**</span><span class="sxs-lookup"><span data-stu-id="69d9e-114">**IXpsOMDocumentSequence**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence)<br/> | [<span data-ttu-id="69d9e-115">**GetDocuments**</span><span class="sxs-lookup"><span data-stu-id="69d9e-115">**GetDocuments**</span></span>](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomdocumentsequence-getdocuments)<br/>                                                                        |
| <span data-ttu-id="69d9e-116">Parte FixedDocument</span><span class="sxs-lookup"><span data-stu-id="69d9e-116">FixedDocument part</span></span><br/>                                  | [<span data-ttu-id="69d9e-117">**IXpsOMDocument**</span><span class="sxs-lookup"><span data-stu-id="69d9e-117">**IXpsOMDocument**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument)<br/>                 | [<span data-ttu-id="69d9e-118">**GetPageReferences**</span><span class="sxs-lookup"><span data-stu-id="69d9e-118">**GetPageReferences**</span></span>](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomdocument-getpagereferences)<br/>                                                                      |
| <span data-ttu-id="69d9e-119">Elemento **PageContent** nel markup FixedDocument</span><span class="sxs-lookup"><span data-stu-id="69d9e-119">**PageContent** element in the FixedDocument markup</span></span><br/> | [<span data-ttu-id="69d9e-120">**IXpsOMPageReference**</span><span class="sxs-lookup"><span data-stu-id="69d9e-120">**IXpsOMPageReference**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)<br/>       | [<span data-ttu-id="69d9e-121">**GetPage**</span><span class="sxs-lookup"><span data-stu-id="69d9e-121">**GetPage**</span></span>](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-getpage)<br/> [<span data-ttu-id="69d9e-122">**CollectPartResources**</span><span class="sxs-lookup"><span data-stu-id="69d9e-122">**CollectPartResources**</span></span>](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-collectpartresources)<br/> |
| <span data-ttu-id="69d9e-123">Parte FixedPage</span><span class="sxs-lookup"><span data-stu-id="69d9e-123">FixedPage part</span></span><br/>                                      | [<span data-ttu-id="69d9e-124">**IXpsOMPage**</span><span class="sxs-lookup"><span data-stu-id="69d9e-124">**IXpsOMPage**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage)<br/>                         | [<span data-ttu-id="69d9e-125">**Getoggetti visivi**</span><span class="sxs-lookup"><span data-stu-id="69d9e-125">**GetVisuals**</span></span>](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompage-getvisuals)<br/>                                                                                        |
| <span data-ttu-id="69d9e-126">Elemento **Canvas** nel markup FixedPage</span><span class="sxs-lookup"><span data-stu-id="69d9e-126">**Canvas** element in the FixedPage markup</span></span><br/>          | [<span data-ttu-id="69d9e-127">**IXpsOMCanvas**</span><span class="sxs-lookup"><span data-stu-id="69d9e-127">**IXpsOMCanvas**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas)<br/>                     | [<span data-ttu-id="69d9e-128">**Getoggetti visivi**</span><span class="sxs-lookup"><span data-stu-id="69d9e-128">**GetVisuals**</span></span>](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomcanvas-getvisuals)<br/>                                                                                      |
| <span data-ttu-id="69d9e-129">Elemento **path** nel markup FixedPage</span><span class="sxs-lookup"><span data-stu-id="69d9e-129">**Path** element in the FixedPage markup</span></span><br/>            | [<span data-ttu-id="69d9e-130">**IXpsOMPath**</span><span class="sxs-lookup"><span data-stu-id="69d9e-130">**IXpsOMPath**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath)<br/>                         | <span data-ttu-id="69d9e-131">Fine della gerarchia del documento.</span><span class="sxs-lookup"><span data-stu-id="69d9e-131">End of document hierarchy.</span></span><br/>                                                                                                         |
| <span data-ttu-id="69d9e-132">Elemento **Glyphs** nel markup FixedPage</span><span class="sxs-lookup"><span data-stu-id="69d9e-132">**Glyphs** element in the FixedPage markup</span></span><br/>          | [<span data-ttu-id="69d9e-133">**IXpsOMGlyphs**</span><span class="sxs-lookup"><span data-stu-id="69d9e-133">**IXpsOMGlyphs**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs)<br/>                     | <span data-ttu-id="69d9e-134">Fine della gerarchia del documento.</span><span class="sxs-lookup"><span data-stu-id="69d9e-134">End of document hierarchy.</span></span><br/>                                                                                                         |
| <span data-ttu-id="69d9e-135">Parte carattere</span><span class="sxs-lookup"><span data-stu-id="69d9e-135">Font part</span></span><br/>                                           | [<span data-ttu-id="69d9e-136">**IXpsOMFontResource**</span><span class="sxs-lookup"><span data-stu-id="69d9e-136">**IXpsOMFontResource**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomfontresource)<br/>         | <span data-ttu-id="69d9e-137">Fine della gerarchia del documento.</span><span class="sxs-lookup"><span data-stu-id="69d9e-137">End of document hierarchy.</span></span><br/>                                                                                                         |
| <span data-ttu-id="69d9e-138">Parte immagine</span><span class="sxs-lookup"><span data-stu-id="69d9e-138">Image part</span></span><br/>                                          | [<span data-ttu-id="69d9e-139">**IXpsOMImageResource**</span><span class="sxs-lookup"><span data-stu-id="69d9e-139">**IXpsOMImageResource**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimageresource)<br/>       | <span data-ttu-id="69d9e-140">Fine della gerarchia del documento.</span><span class="sxs-lookup"><span data-stu-id="69d9e-140">End of document hierarchy.</span></span><br/>                                                                                                         |



 

<span data-ttu-id="69d9e-141">Prima di usare gli esempi di codice seguenti nel programma, leggere la dichiarazione di non responsabilità nelle [attività comuni di programmazione dei documenti XPS](common-xps-document-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="69d9e-141">Before using the following code examples in your program, read the disclaimer in [Common XPS Document Programming Tasks](common-xps-document-tasks.md).</span></span>

## <a name="code-example"></a><span data-ttu-id="69d9e-142">Esempio di codice</span><span class="sxs-lookup"><span data-stu-id="69d9e-142">Code Example</span></span>

<span data-ttu-id="69d9e-143">Nell'esempio di codice seguente si presuppone l'esistenza di un OM XPS inizializzato e il *pacchetto* punta a un'interfaccia [**IXpsOMPackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage) che rappresenta il modello om XPS.</span><span class="sxs-lookup"><span data-stu-id="69d9e-143">The following code example assumes the existence of an initialized XPS OM, and *package* points to an [**IXpsOMPackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage) interface that represents that XPS OM.</span></span> <span data-ttu-id="69d9e-144">Per informazioni sulla creazione di un modello a oggetti XPS, vedere [leggere un documento XPS in un OM XPS](read-an-xps-document-into-an-xps-om.md) o [creare un OM XPS vuoto](create-a-blank-xps-om.md).</span><span class="sxs-lookup"><span data-stu-id="69d9e-144">For information about creating an XPS OM, see [Read an XPS Document into an XPS OM](read-an-xps-document-into-an-xps-om.md) or [Create a Blank XPS OM](create-a-blank-xps-om.md).</span></span>


```C++
    HRESULT                        hr = S_OK;

    IXpsOMDocumentSequence         *docSeq = NULL;
    IXpsOMDocumentCollection       *docs = NULL;
    IXpsOMDocument                 *doc = NULL;
    IXpsOMPageReferenceCollection  *pages = NULL;
    IXpsOMPageReference            *pageRef = NULL;
    IXpsOMPage                     *page = NULL;
    IXpsOMCanvas                   *canvas = NULL;
    IXpsOMPath                     *path = NULL;
    IXpsOMPartResources            *pageParts = NULL;
    IXpsOMGlyphs                   *glyphs = NULL;
    IXpsOMFontResourceCollection   *fonts = NULL; 
    IXpsOMFontResource             *font = NULL;
    IXpsOMImageResourceCollection  *images = NULL;
    IXpsOMImageResource            *image = NULL;
    IXpsOMVisualCollection         *visuals = NULL;
    IXpsOMVisual                   *visual = NULL;

    UINT32  numDocs = 0;
    UINT32  thisDoc = 0;

    UINT32  numPageRefs = 0;
    UINT32  thisPageRef = 0;

    UINT32  numVisuals = 0;
    UINT32  thisVisual = 0;

    UINT32  numFonts = 0;
    UINT32  thisFont = 0;

    UINT32  numImages = 0;
    UINT32  thisImage = 0;

    XPS_OBJECT_TYPE  visualType;
 
    // package points to the IXpsOMPackage interface to walk.

    // Get the fixed document sequence of the package.
    hr = package->GetDocumentSequence(&docSeq);

    // Get the fixed documents in the fixed document sequence.
    hr = docSeq->GetDocuments(&docs);

    // Walk the collection of documents.
    hr = docs->GetCount(&numDocs);
    thisDoc = 0;
    while (thisDoc < numDocs) {
        hr = docs->GetAt(thisDoc, &doc);
        
        // Get the doc contents.
        hr = doc->GetPageReferences(&pages);
        
        // Walk the collection of page references
        hr = pages->GetCount(&numPageRefs);
        thisPageRef = 0;
        while (thisPageRef < numPageRefs) {
            // Get this page reference.
            hr = pages->GetAt(thisPageRef, &pageRef);

            // Get the page content of this page reference.
            {
                hr = pageRef->GetPage (&page);

                // Get the visual tree of this page.
                hr = page->GetVisuals (&visuals);
                
                // Walk the visuals.
                hr = visuals->GetCount (&numVisuals);
                thisVisual = 0;
                while (thisVisual < numVisuals) {
                    hr = visuals->GetAt (thisVisual, &visual);
                    // Get visual type.
                    hr = visual->GetType( &visualType );
                    
                    // Do other stuff with the visual.

                    // Release the visual.
                    if (NULL != visual) {visual->Release(); visual = NULL;}
                    thisVisual++; // Get next visual in collection.
                }
                if (NULL != visuals) {visuals->Release(); visuals = NULL;}
                if (NULL != page) {page->Release(); page = NULL;}
            }
            // Get the part resources used by this page.
            hr = pageRef->CollectPartResources (&pageParts);

            // Get the font resources.
            {
                hr = pageParts->GetFontResources (&fonts);
                
                // Walk the fonts.
                hr = fonts->GetCount (&numFonts);
                thisFont = 0;
                while (thisFont < numFonts) {
                    hr = fonts->GetAt(thisFont, &font);
                    if (NULL != font) {font->Release(); font = NULL;}

                    thisFont++; // Get the next font in collection.
                }
                if (NULL != fonts) {fonts->Release(); fonts = NULL;}
            }

            // Get the image resources.
            {
                hr = pageParts->GetImageResources (&images);

                // walk the images
                hr = images->GetCount (&numImages);
                thisImage = 0;
                while (thisImage < numImages) {
                    hr = images->GetAt(thisImage, &image);
                    thisImage++;
                    if (NULL != image) {image->Release(); image = NULL;}
                }
                if (NULL != images) {images->Release(); images = NULL;}
            }
            if (NULL != pageRef) {pageRef->Release(); pageRef = NULL;}
            thisPageRef++; // Get next page in doc.
        }
        if (NULL != pages) {pages->Release(); pages = NULL;}
        if (NULL != doc) {doc->Release(); doc = NULL;}
        thisDoc++; // Get next doc in collection.
    }

    // Release interface pointers.
    if (NULL != docs) docs->Release();
    if (NULL != docSeq) docSeq->Release();

```



## <a name="related-topics"></a><span data-ttu-id="69d9e-145">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="69d9e-145">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="69d9e-146">**Passaggi successivi**</span><span class="sxs-lookup"><span data-stu-id="69d9e-146">**Next Steps**</span></span>
</dt> <dt>

[<span data-ttu-id="69d9e-147">Scrivere testo in un OM XPS</span><span class="sxs-lookup"><span data-stu-id="69d9e-147">Write Text to an XPS OM</span></span>](write-text-to-an-xps-om.md)
</dt> <dt>

[<span data-ttu-id="69d9e-148">Creare grafica in un OM XPS</span><span class="sxs-lookup"><span data-stu-id="69d9e-148">Draw Graphics in an XPS OM</span></span>](draw-graphics-in-an-xps-om.md)
</dt> <dt>

[<span data-ttu-id="69d9e-149">Inserire immagini in un OM XPS</span><span class="sxs-lookup"><span data-stu-id="69d9e-149">Place Images in an XPS OM</span></span>](place-images-in-an-xps-om.md)
</dt> <dt>

<span data-ttu-id="69d9e-150">**Usato in questa pagina**</span><span class="sxs-lookup"><span data-stu-id="69d9e-150">**Used in This Page**</span></span>
</dt> <dt>

[<span data-ttu-id="69d9e-151">**IXpsOMDocument**</span><span class="sxs-lookup"><span data-stu-id="69d9e-151">**IXpsOMDocument**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument)
</dt> <dt>

[<span data-ttu-id="69d9e-152">**IXpsOMDocumentCollection**</span><span class="sxs-lookup"><span data-stu-id="69d9e-152">**IXpsOMDocumentCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentcollection)
</dt> <dt>

[<span data-ttu-id="69d9e-153">**IXpsOMDocumentSequence**</span><span class="sxs-lookup"><span data-stu-id="69d9e-153">**IXpsOMDocumentSequence**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence)
</dt> <dt>

[<span data-ttu-id="69d9e-154">**IXpsOMFontResource**</span><span class="sxs-lookup"><span data-stu-id="69d9e-154">**IXpsOMFontResource**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomfontresource)
</dt> <dt>

[<span data-ttu-id="69d9e-155">**IXpsOMFontResourceCollection**</span><span class="sxs-lookup"><span data-stu-id="69d9e-155">**IXpsOMFontResourceCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomfontresourcecollection)
</dt> <dt>

[<span data-ttu-id="69d9e-156">**IXpsOMImageResource**</span><span class="sxs-lookup"><span data-stu-id="69d9e-156">**IXpsOMImageResource**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimageresource)
</dt> <dt>

[<span data-ttu-id="69d9e-157">**IXpsOMImageResourceCollection**</span><span class="sxs-lookup"><span data-stu-id="69d9e-157">**IXpsOMImageResourceCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimageresourcecollection)
</dt> <dt>

[<span data-ttu-id="69d9e-158">**IXpsOMPackage**</span><span class="sxs-lookup"><span data-stu-id="69d9e-158">**IXpsOMPackage**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage)
</dt> <dt>

[<span data-ttu-id="69d9e-159">**IXpsOMPage**</span><span class="sxs-lookup"><span data-stu-id="69d9e-159">**IXpsOMPage**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage)
</dt> <dt>

[<span data-ttu-id="69d9e-160">**IXpsOMPageReference**</span><span class="sxs-lookup"><span data-stu-id="69d9e-160">**IXpsOMPageReference**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)
</dt> <dt>

[<span data-ttu-id="69d9e-161">**IXpsOMPageReferenceCollection**</span><span class="sxs-lookup"><span data-stu-id="69d9e-161">**IXpsOMPageReferenceCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereferencecollection)
</dt> <dt>

[<span data-ttu-id="69d9e-162">**IXpsOMVisual**</span><span class="sxs-lookup"><span data-stu-id="69d9e-162">**IXpsOMVisual**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual)
</dt> <dt>

[<span data-ttu-id="69d9e-163">**IXpsOMVisualCollection**</span><span class="sxs-lookup"><span data-stu-id="69d9e-163">**IXpsOMVisualCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualcollection)
</dt> <dt>

<span data-ttu-id="69d9e-164">**Per ulteriori informazioni**</span><span class="sxs-lookup"><span data-stu-id="69d9e-164">**For More Information**</span></span>
</dt> <dt>

[<span data-ttu-id="69d9e-165">Inizializzare un OM XPS</span><span class="sxs-lookup"><span data-stu-id="69d9e-165">Initialize an XPS OM</span></span>](xps-object-model-initialization.md)
</dt> <dt>

[<span data-ttu-id="69d9e-166">Leggere un documento XPS in un OM XPS</span><span class="sxs-lookup"><span data-stu-id="69d9e-166">Read an XPS Document into an XPS OM</span></span>](read-an-xps-document-into-an-xps-om.md)
</dt> <dt>

[<span data-ttu-id="69d9e-167">Creazione di un OM XPS vuoto</span><span class="sxs-lookup"><span data-stu-id="69d9e-167">Create a Blank XPS OM</span></span>](create-a-blank-xps-om.md)
</dt> <dt>

[<span data-ttu-id="69d9e-168">API per la creazione di pacchetti</span><span class="sxs-lookup"><span data-stu-id="69d9e-168">Packaging API</span></span>](/previous-versions/windows/desktop/opc/packaging)
</dt> <dt>

[<span data-ttu-id="69d9e-169">Informazioni di riferimento sulle API documento XPS</span><span class="sxs-lookup"><span data-stu-id="69d9e-169">XPS Document API Reference</span></span>](xps-programming-reference.md)
</dt> <dt>

[<span data-ttu-id="69d9e-170">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="69d9e-170">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

