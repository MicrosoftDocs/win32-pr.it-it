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
# <a name="navigate-the-xps-om"></a>Esplorare XPS OM

Questo argomento descrive come spostarsi in un OM XPS e accedere a diverse parti del documento in memoria.

L'organizzazione dell'API del documento XPS rispecchia l'organizzazione di un documento XPS. Nella tabella seguente viene illustrato il modo in cui le interfacce dell'API del documento XPS sono correlate ai componenti di un documento XPS.



| Componente documento XPS                                         | Interfaccia API documenti XPS                                          | Metodo da chiamare per il livello successivo nella gerarchia                                                                                       |
|----------------------------------------------------------------|---------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| File di documento XPS (contiene il pacchetto OPC)<br/>            | [**IXpsOMPackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage)<br/>                   | [**GetDocumentSequence**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-getdocumentsequence)<br/>                                                                   |
| Parte FixedDocumentSequence<br/>                          | [**IXpsOMDocumentSequence**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence)<br/> | [**GetDocuments**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomdocumentsequence-getdocuments)<br/>                                                                        |
| Parte FixedDocument<br/>                                  | [**IXpsOMDocument**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument)<br/>                 | [**GetPageReferences**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomdocument-getpagereferences)<br/>                                                                      |
| Elemento **PageContent** nel markup FixedDocument<br/> | [**IXpsOMPageReference**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)<br/>       | [**GetPage**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-getpage)<br/> [**CollectPartResources**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-collectpartresources)<br/> |
| Parte FixedPage<br/>                                      | [**IXpsOMPage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage)<br/>                         | [**Getoggetti visivi**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompage-getvisuals)<br/>                                                                                        |
| Elemento **Canvas** nel markup FixedPage<br/>          | [**IXpsOMCanvas**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcanvas)<br/>                     | [**Getoggetti visivi**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomcanvas-getvisuals)<br/>                                                                                      |
| Elemento **path** nel markup FixedPage<br/>            | [**IXpsOMPath**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath)<br/>                         | Fine della gerarchia del documento.<br/>                                                                                                         |
| Elemento **Glyphs** nel markup FixedPage<br/>          | [**IXpsOMGlyphs**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs)<br/>                     | Fine della gerarchia del documento.<br/>                                                                                                         |
| Parte carattere<br/>                                           | [**IXpsOMFontResource**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomfontresource)<br/>         | Fine della gerarchia del documento.<br/>                                                                                                         |
| Parte immagine<br/>                                          | [**IXpsOMImageResource**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimageresource)<br/>       | Fine della gerarchia del documento.<br/>                                                                                                         |



 

Prima di usare gli esempi di codice seguenti nel programma, leggere la dichiarazione di non responsabilità nelle [attività comuni di programmazione dei documenti XPS](common-xps-document-tasks.md).

## <a name="code-example"></a>Esempio di codice

Nell'esempio di codice seguente si presuppone l'esistenza di un OM XPS inizializzato e il *pacchetto* punta a un'interfaccia [**IXpsOMPackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage) che rappresenta il modello om XPS. Per informazioni sulla creazione di un modello a oggetti XPS, vedere [leggere un documento XPS in un OM XPS](read-an-xps-document-into-an-xps-om.md) o [creare un OM XPS vuoto](create-a-blank-xps-om.md).


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Passaggi successivi**
</dt> <dt>

[Scrivere testo in un OM XPS](write-text-to-an-xps-om.md)
</dt> <dt>

[Creare grafica in un OM XPS](draw-graphics-in-an-xps-om.md)
</dt> <dt>

[Inserire immagini in un OM XPS](place-images-in-an-xps-om.md)
</dt> <dt>

**Usato in questa pagina**
</dt> <dt>

[**IXpsOMDocument**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument)
</dt> <dt>

[**IXpsOMDocumentCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentcollection)
</dt> <dt>

[**IXpsOMDocumentSequence**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence)
</dt> <dt>

[**IXpsOMFontResource**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomfontresource)
</dt> <dt>

[**IXpsOMFontResourceCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomfontresourcecollection)
</dt> <dt>

[**IXpsOMImageResource**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimageresource)
</dt> <dt>

[**IXpsOMImageResourceCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimageresourcecollection)
</dt> <dt>

[**IXpsOMPackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage)
</dt> <dt>

[**IXpsOMPage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage)
</dt> <dt>

[**IXpsOMPageReference**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)
</dt> <dt>

[**IXpsOMPageReferenceCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereferencecollection)
</dt> <dt>

[**IXpsOMVisual**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual)
</dt> <dt>

[**IXpsOMVisualCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualcollection)
</dt> <dt>

**Per ulteriori informazioni**
</dt> <dt>

[Inizializzare un OM XPS](xps-object-model-initialization.md)
</dt> <dt>

[Leggere un documento XPS in un OM XPS](read-an-xps-document-into-an-xps-om.md)
</dt> <dt>

[Creazione di un OM XPS vuoto](create-a-blank-xps-om.md)
</dt> <dt>

[API per la creazione di pacchetti](/previous-versions/windows/desktop/opc/packaging)
</dt> <dt>

[Informazioni di riferimento sulle API documento XPS](xps-programming-reference.md)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

