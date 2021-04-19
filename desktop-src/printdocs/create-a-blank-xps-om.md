---
description: Questo argomento descrive come creare un OM XPS vuoto.
ms.assetid: 5b6f12ba-9a41-4252-96c4-391bb8d75cd4
title: Creazione di un OM XPS vuoto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0588fc11deb4b3d980e978dfe8a5370bc170d506
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311828"
---
# <a name="create-a-blank-xps-om"></a>Creazione di un OM XPS vuoto

Questo argomento descrive come creare un OM XPS vuoto. Vengono presentati gli esempi di codice che illustrano come utilizzare un oggetto XPS OM per compilare la struttura del documento di un documento XPS con una pagina vuota.

Per essere salvati come documento XPS, XPS OM richiede almeno i componenti seguenti:

-   Un [**IXpsOMPackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage) che descrive il pacchetto del documento XPS
-   Oggetto [**IXpsOMDocumentSequence**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence) che contiene il Framework del contenuto del pacchetto
-   Oggetto [**IXpsOMDocument**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument) che contiene il Framework di un documento all'interno del pacchetto
-   Oggetto [**IXpsOMPageReference**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference) che contiene la raccolta di pagine nel documento.
-   Un [**IXpsOMPage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage) che contiene una pagina vuota

Quando si usano queste interfacce, XPS OM conterrà un documento con una pagina vuota. Per creare questo documento in un OM XPS, il programma deve prima creare i singoli componenti e quindi collegarli insieme.

Prima di usare gli esempi di codice seguenti, leggere la dichiarazione di non responsabilità nelle [attività comuni di programmazione dei documenti XPS](common-xps-document-tasks.md).

## <a name="code-examples"></a>Esempi di codice

Nell'esempio di codice seguente si presuppone che l'inizializzazione, descritta in [Initialize an XPS om](xps-object-model-initialization.md), abbia avuto esito positivo.


```C++
    // Declare the variables used in this section.
    HRESULT                       hr = S_OK;
    IOpcPartUri                   *opcPartUri = NULL;
    IXpsOMPackage                 *xpsPackage = NULL;
    IXpsOMDocumentSequence        *xpsFDS = NULL;
    IXpsOMDocumentCollection      *fixedDocuments = NULL;
    IXpsOMDocument                *xpsFD = NULL;
    IXpsOMPage                    *xpsPage = NULL;
    IXpsOMPageReferenceCollection *pageRefs = NULL;
    IXpsOMPageReference           *xpsPageRef = NULL;
    // These values are set outside of this code example.
    XPS_SIZE pageSize = {width, height}; 
    
    // Create the package.
    hr = xpsFactory->CreatePackage( &xpsPackage );

    // Create the URI for the fixed document sequence part and then  
    //  create the fixed document sequence
    hr = xpsFactory->CreatePartUri( 
        L"/FixedDocumentSequence.fdseq", &opcPartUri );
    hr = xpsFactory->CreateDocumentSequence( opcPartUri, &xpsFDS );
    // Release this URI to reuse the interface pointer.
    if (NULL != opcPartUri) {opcPartUri->Release(); opcPartUri = NULL;}

    // Create the URI for the document part and then create the document.
    hr = xpsFactory->CreatePartUri( 
        L"/Documents/1/FixedDocument.fdoc", &opcPartUri );
    hr = xpsFactory->CreateDocument( opcPartUri, &xpsFD );
    // Release this URI to reuse the interface pointer.
    if (NULL != opcPartUri) {opcPartUri->Release(); opcPartUri = NULL;}

    // Create a blank page.
    hr = xpsFactory->CreatePartUri( 
        L"/Documents/1/Pages/1.fpage", &opcPartUri );
    hr = xpsFactory->CreatePage(
        &pageSize,                  // Page size
        L"en-US",                   // Page language
        opcPartUri,                 // Page part name
        &xpsPage);                
    // Release this URI to reuse the interface pointer.
    if (NULL != opcPartUri) {opcPartUri->Release(); opcPartUri = NULL;}

    // Create a page reference for the page.
    hr = xpsFactory->CreatePageReference( &pageSize, &xpsPageRef );

    // Add the fixed document sequence to the package.
    hr = xpsPackage->SetDocumentSequence( xpsFDS );

    // Get the document collection of the fixed document sequence
    //  and then add the document to the collection.
    hr = xpsFDS->GetDocuments( &fixedDocuments );
    hr = fixedDocuments->Append( xpsFD );

    // Get the page reference collection from the document
    //  and add the page reference and blank page.
    hr = xpsFD->GetPageReferences( &pageRefs );
    hr = pageRefs->Append( xpsPageRef );
    hr = xpsPageRef->SetPage( xpsPage );

    // Release interface pointer
    if (NULL != xpsPage) xpsPage->Release();
    if (NULL != pageRefs) pageRefs->Release();
    if (NULL != fixedDocuments) fixedDocuments->Release();
    if (NULL != xpsPageRef) xpsPageRef->Release();
    if (NULL != xpsFD) xpsFD->Release();
    if (NULL != xpsFDS) xpsFDS->Release();
    if (NULL != xpsPackage) xpsPackage->Release();

```



## <a name="best-practices"></a>Procedure consigliate

Dopo avere usato un'interfaccia [**IOpcPartUri**](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi) per creare un componente, ad esempio dopo aver chiamato il metodo **CreateDocument** nell'esempio di codice, rilasciare il puntatore a tale interfaccia, a meno che non sia necessario per un'altra chiamata.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Passaggi successivi**
</dt> <dt>

[Esplorare XPS OM](navigate-the-xps-om.md)
</dt> <dt>

[Scrivere testo in un OM XPS](write-text-to-an-xps-om.md)
</dt> <dt>

[Creare grafica in un OM XPS](draw-graphics-in-an-xps-om.md)
</dt> <dt>

[Inserire immagini in un OM XPS](place-images-in-an-xps-om.md)
</dt> <dt>

**Usato in questa pagina**
</dt> <dt>

[**IOpcPartUri**](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi)
</dt> <dt>

[**IXpsOMObjectFactory**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory)
</dt> <dt>

[**IXpsOMPackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage)
</dt> <dt>

[**IXpsOMDocumentSequence**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence)
</dt> <dt>

[**IXpsOMDocumentCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentcollection)
</dt> <dt>

[**IXpsOMDocument**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument)
</dt> <dt>

[**IXpsOMPage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage)
</dt> <dt>

[**IXpsOMPageReference**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)
</dt> <dt>

[**IXpsOMPageReferenceCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereferencecollection)
</dt> <dt>

[**\_dimensioni XPS**](/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_size)
</dt> <dt>

**Per ulteriori informazioni**
</dt> <dt>

[Inizializzare un OM XPS](xps-object-model-initialization.md)
</dt> <dt>

[API per la creazione di pacchetti](/previous-versions/windows/desktop/opc/packaging)
</dt> <dt>

[Informazioni di riferimento sulle API documento XPS](xps-programming-reference.md)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
