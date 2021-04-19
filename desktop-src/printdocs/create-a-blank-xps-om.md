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
# <a name="create-a-blank-xps-om"></a><span data-ttu-id="c593e-103">Creazione di un OM XPS vuoto</span><span class="sxs-lookup"><span data-stu-id="c593e-103">Create a Blank XPS OM</span></span>

<span data-ttu-id="c593e-104">Questo argomento descrive come creare un OM XPS vuoto.</span><span class="sxs-lookup"><span data-stu-id="c593e-104">This topic describes how to create a blank XPS OM.</span></span> <span data-ttu-id="c593e-105">Vengono presentati gli esempi di codice che illustrano come utilizzare un oggetto XPS OM per compilare la struttura del documento di un documento XPS con una pagina vuota.</span><span class="sxs-lookup"><span data-stu-id="c593e-105">It presents the code examples that illustrate how to use an XPS OM to build the document structure of an XPS document that has one blank page.</span></span>

<span data-ttu-id="c593e-106">Per essere salvati come documento XPS, XPS OM richiede almeno i componenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="c593e-106">To be saved as an XPS document, the XPS OM requires at least the following components:</span></span>

-   <span data-ttu-id="c593e-107">Un [**IXpsOMPackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage) che descrive il pacchetto del documento XPS</span><span class="sxs-lookup"><span data-stu-id="c593e-107">An [**IXpsOMPackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage) that describes the XPS document package</span></span>
-   <span data-ttu-id="c593e-108">Oggetto [**IXpsOMDocumentSequence**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence) che contiene il Framework del contenuto del pacchetto</span><span class="sxs-lookup"><span data-stu-id="c593e-108">An [**IXpsOMDocumentSequence**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence) that contains the framework of the package contents</span></span>
-   <span data-ttu-id="c593e-109">Oggetto [**IXpsOMDocument**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument) che contiene il Framework di un documento all'interno del pacchetto</span><span class="sxs-lookup"><span data-stu-id="c593e-109">An [**IXpsOMDocument**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument) that contains the framework of a document within the package</span></span>
-   <span data-ttu-id="c593e-110">Oggetto [**IXpsOMPageReference**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference) che contiene la raccolta di pagine nel documento.</span><span class="sxs-lookup"><span data-stu-id="c593e-110">An [**IXpsOMPageReference**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference) that contains the collection of pages in the document</span></span>
-   <span data-ttu-id="c593e-111">Un [**IXpsOMPage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage) che contiene una pagina vuota</span><span class="sxs-lookup"><span data-stu-id="c593e-111">An [**IXpsOMPage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage) that contains a blank page</span></span>

<span data-ttu-id="c593e-112">Quando si usano queste interfacce, XPS OM conterrà un documento con una pagina vuota.</span><span class="sxs-lookup"><span data-stu-id="c593e-112">When these interfaces are used, the XPS OM will contain a document that has one blank page.</span></span> <span data-ttu-id="c593e-113">Per creare questo documento in un OM XPS, il programma deve prima creare i singoli componenti e quindi collegarli insieme.</span><span class="sxs-lookup"><span data-stu-id="c593e-113">To create this document in an XPS OM, the program must first create the individual components and then link them together.</span></span>

<span data-ttu-id="c593e-114">Prima di usare gli esempi di codice seguenti, leggere la dichiarazione di non responsabilità nelle [attività comuni di programmazione dei documenti XPS](common-xps-document-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="c593e-114">Before using the following code examples, read the disclaimer in [Common XPS Document Programming Tasks](common-xps-document-tasks.md).</span></span>

## <a name="code-examples"></a><span data-ttu-id="c593e-115">Esempi di codice</span><span class="sxs-lookup"><span data-stu-id="c593e-115">Code Examples</span></span>

<span data-ttu-id="c593e-116">Nell'esempio di codice seguente si presuppone che l'inizializzazione, descritta in [Initialize an XPS om](xps-object-model-initialization.md), abbia avuto esito positivo.</span><span class="sxs-lookup"><span data-stu-id="c593e-116">The following code example assumes that the initialization, described in [Initialize an XPS OM](xps-object-model-initialization.md), has succeeded.</span></span>


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



## <a name="best-practices"></a><span data-ttu-id="c593e-117">Procedure consigliate</span><span class="sxs-lookup"><span data-stu-id="c593e-117">Best Practices</span></span>

<span data-ttu-id="c593e-118">Dopo avere usato un'interfaccia [**IOpcPartUri**](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi) per creare un componente, ad esempio dopo aver chiamato il metodo **CreateDocument** nell'esempio di codice, rilasciare il puntatore a tale interfaccia, a meno che non sia necessario per un'altra chiamata.</span><span class="sxs-lookup"><span data-stu-id="c593e-118">After you have used an [**IOpcPartUri**](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi) interface to create a component (such as after calling the **CreateDocument** method in the code example), release the pointer to that interface—unless you need it for another call.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c593e-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c593e-119">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="c593e-120">**Passaggi successivi**</span><span class="sxs-lookup"><span data-stu-id="c593e-120">**Next Steps**</span></span>
</dt> <dt>

[<span data-ttu-id="c593e-121">Esplorare XPS OM</span><span class="sxs-lookup"><span data-stu-id="c593e-121">Navigate the XPS OM</span></span>](navigate-the-xps-om.md)
</dt> <dt>

[<span data-ttu-id="c593e-122">Scrivere testo in un OM XPS</span><span class="sxs-lookup"><span data-stu-id="c593e-122">Write Text to an XPS OM</span></span>](write-text-to-an-xps-om.md)
</dt> <dt>

[<span data-ttu-id="c593e-123">Creare grafica in un OM XPS</span><span class="sxs-lookup"><span data-stu-id="c593e-123">Draw Graphics in an XPS OM</span></span>](draw-graphics-in-an-xps-om.md)
</dt> <dt>

[<span data-ttu-id="c593e-124">Inserire immagini in un OM XPS</span><span class="sxs-lookup"><span data-stu-id="c593e-124">Place Images in an XPS OM</span></span>](place-images-in-an-xps-om.md)
</dt> <dt>

<span data-ttu-id="c593e-125">**Usato in questa pagina**</span><span class="sxs-lookup"><span data-stu-id="c593e-125">**Used in This Page**</span></span>
</dt> <dt>

[<span data-ttu-id="c593e-126">**IOpcPartUri**</span><span class="sxs-lookup"><span data-stu-id="c593e-126">**IOpcPartUri**</span></span>](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi)
</dt> <dt>

[<span data-ttu-id="c593e-127">**IXpsOMObjectFactory**</span><span class="sxs-lookup"><span data-stu-id="c593e-127">**IXpsOMObjectFactory**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory)
</dt> <dt>

[<span data-ttu-id="c593e-128">**IXpsOMPackage**</span><span class="sxs-lookup"><span data-stu-id="c593e-128">**IXpsOMPackage**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage)
</dt> <dt>

[<span data-ttu-id="c593e-129">**IXpsOMDocumentSequence**</span><span class="sxs-lookup"><span data-stu-id="c593e-129">**IXpsOMDocumentSequence**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence)
</dt> <dt>

[<span data-ttu-id="c593e-130">**IXpsOMDocumentCollection**</span><span class="sxs-lookup"><span data-stu-id="c593e-130">**IXpsOMDocumentCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentcollection)
</dt> <dt>

[<span data-ttu-id="c593e-131">**IXpsOMDocument**</span><span class="sxs-lookup"><span data-stu-id="c593e-131">**IXpsOMDocument**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument)
</dt> <dt>

[<span data-ttu-id="c593e-132">**IXpsOMPage**</span><span class="sxs-lookup"><span data-stu-id="c593e-132">**IXpsOMPage**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage)
</dt> <dt>

[<span data-ttu-id="c593e-133">**IXpsOMPageReference**</span><span class="sxs-lookup"><span data-stu-id="c593e-133">**IXpsOMPageReference**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)
</dt> <dt>

[<span data-ttu-id="c593e-134">**IXpsOMPageReferenceCollection**</span><span class="sxs-lookup"><span data-stu-id="c593e-134">**IXpsOMPageReferenceCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereferencecollection)
</dt> <dt>

[<span data-ttu-id="c593e-135">**\_dimensioni XPS**</span><span class="sxs-lookup"><span data-stu-id="c593e-135">**XPS\_SIZE**</span></span>](/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_size)
</dt> <dt>

<span data-ttu-id="c593e-136">**Per ulteriori informazioni**</span><span class="sxs-lookup"><span data-stu-id="c593e-136">**For More Information**</span></span>
</dt> <dt>

[<span data-ttu-id="c593e-137">Inizializzare un OM XPS</span><span class="sxs-lookup"><span data-stu-id="c593e-137">Initialize an XPS OM</span></span>](xps-object-model-initialization.md)
</dt> <dt>

[<span data-ttu-id="c593e-138">API per la creazione di pacchetti</span><span class="sxs-lookup"><span data-stu-id="c593e-138">Packaging API</span></span>](/previous-versions/windows/desktop/opc/packaging)
</dt> <dt>

[<span data-ttu-id="c593e-139">Informazioni di riferimento sulle API documento XPS</span><span class="sxs-lookup"><span data-stu-id="c593e-139">XPS Document API Reference</span></span>](xps-programming-reference.md)
</dt> <dt>

[<span data-ttu-id="c593e-140">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="c593e-140">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
