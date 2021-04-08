---
description: In questo argomento viene descritto come utilizzare le interfacce che consentono di accedere alle parti del documento XPS in un OM XPS.
ms.assetid: c52f7044-890d-47d1-83f8-bae1f8d83139
title: Interfacce della parte OM XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d81cbf17c26e4ba6c80199ee787b1ee11b28d260
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967374"
---
# <a name="xps-om-part-interfaces"></a>Interfacce della parte OM XPS

In questo argomento viene descritto come utilizzare le interfacce che consentono di accedere alle parti del documento XPS in un OM XPS.



| Nome interfaccia                                                                                                    | Interfacce figlio logiche                                                                                                                                                                                                                                                                                     | Descrizione                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**IXpsOMPart**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompart)<br/>                                                                       | [**IXpsOMDocumentSequence**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence)<br/> [**IXpsOMDocument**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument)<br/> [**IXpsOMPageReference**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)<br/> [**IXpsOMCoreProperties**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcoreproperties)<br/> [**IXpsOMResource**](/windows/win32/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomresource)<br/>    | Componenti del documento che costituiscono la struttura del documento.<br/>                                          |
| [**IXpsOMResource**](/windows/win32/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomresource)<br/> [**IXpsOMPartResources**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompartresources)<br/> | IXpsOMFontResource<br/> IXpsOMImageResource<br/> IXpsOMColorProfileResource<br/> IXpsOMPrintTicketResource<br/> IXpsOMRemoteDictionaryResource<br/> IXpsOMDocumentStructureResource<br/> IXpsOMStoryFragmentsResource<br/> IXpsOMSignatureBlockResource<br/> | Componenti del documento che contengono elementi utilizzati in o a cui fa riferimento una pagina o un documento.<br/> |
| [**IXpsOMPartUriCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomparturicollection)<br/>                                             | nessuno<br/>                                                                                                                                                                                                                                                                                              | Raccolta di URI di parte.<br/>                                                                        |



 

## <a name="code-examples"></a>Esempi di codice

Gli esempi di codice seguenti illustrano due esempi di come usare le interfacce di parte per accedere al contenuto XPS OM.

### <a name="get-the-name-of-a-document-part"></a>Ottenere il nome di una parte del documento

L'esempio di codice seguente consente di passare a una parte del documento e di ottenere il nome della parte.


```C++
    HRESULT                         hr = S_OK;
    
    IXpsOMDocumentSequence          *docSeq;
    IXpsOMDocumentCollection        *docs;
    IXpsOMDocument                  *doc;
    IXpsOMPageReferenceCollection   *pages;
    IXpsOMPageReference             *pageRef;
    IXpsOMPage                      *page;

    IOpcPartUri                     *thisDocPartUri;
    IOpcPartUri                     *thisPagePartUri;

    UINT32  numDocs = 0;
    UINT32  thisDoc = 0;

    UINT32  numPageRefs = 0;
    UINT32  thisPageRef = 0;

    // package points to the IXpsOMPackage interface to walk.

    // get the fixed document sequence of the package
    hr = package->GetDocumentSequence(&docSeq);

    // get the fixed documents in the fixed document sequence
    hr = docSeq->GetDocuments(&docs);

    // walk the collection of documents;
    hr = docs->GetCount(&numDocs);
    thisDoc = 0;
    while (thisDoc < numDocs) {
        hr = docs->GetAt(thisDoc, &doc);
        
        // get the part name (URI) of this document
        hr = doc->GetPartName ( &thisDocPartUri );

        // get the doc contents
        hr = doc->GetPageReferences(&pages);
        
        // walk the collection of page references
        hr = pages->GetCount(&numPageRefs);
        thisPageRef = 0;
        while (thisPageRef < numPageRefs) {
            // get this page reference
            hr = pages->GetAt(thisPageRef, &pageRef );

            // get the part name (URI) of this page
            hr = pageRef->GetPage (&page);
            hr = page->GetPartName ( &thisPagePartUri );

            // do something with the part name
 
            thisPagePartUri->Release();
            page->Release();
            pageRef->Release();

            thisPageRef++;
        }
        pages->Release();
        thisDocPartUri->Release();
        doc->Release();
        thisDoc++;
    }

    docs->Release();
    docSeq->Release();

```



### <a name="get-the-part-resources-that-are-associated-with-this-page"></a>Ottenere le risorse della parte associate a questa pagina

Nell'esempio di codice seguente vengono recuperati gli elenchi delle diverse risorse utilizzate da questa pagina.


```C++
    HRESULT                                   hr = S_OK;
    IXpsOMPartResources                       *resources;

    IXpsOMColorProfileResourceCollection      *colorProfileResources;
    IXpsOMFontResourceCollection              *fontResources;
    IXpsOMImageResourceCollection             *imageResources;
    IXpsOMRemoteDictionaryResourceCollection  *dictionaryResources; 

    // pageRef contains the current page reference 
    hr = pageRef->CollectPartResources ( &resources );

    // Get pointers to each type of resource
    hr = resources->GetColorProfileResources( &colorProfileResources );
    hr = resources->GetFontResources( &fontResources );
    hr = resources->GetImageResources( &imageResources );
    hr = resources->GetRemoteDictionaryResources( &dictionaryResources );

    // use resources

    dictionaryResources->Release();
    imageResources->Release();
    fontResources->Release();
    colorProfileResources->Release();
    resources->Release();
```



 

