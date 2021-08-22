---
description: In questo argomento vengono descritte le interfacce che forniscono l'accesso ai componenti a livello di documento di un OM XPS.
ms.assetid: 96b92480-cc28-4a57-a184-c52d3ddc9b05
title: Uso delle interfacce IXpsOMDocument
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad7e8c0908382a731532f2697f03c8d67cb732ddf902f0c1ea181fe221d075fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119033759"
---
# <a name="working-with-ixpsomdocument-interfaces"></a>Uso delle interfacce IXpsOMDocument

In questo argomento vengono descritte le interfacce che forniscono l'accesso ai componenti a livello di documento di un OM XPS.



| Nome dell'interfaccia                                                                        | Interfacce figlio logiche                                      | Descrizione                                                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------|---------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IXpsOMDocument**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument)<br/>                                   | [**IXpsOMPageReference**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)<br/> | Rappresenta una singola parte FixedDocument e associa una raccolta di riferimenti alla pagina.<br/> [**IXpsOMPageReferenceCollection è**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereferencecollection) l'interfaccia di raccolta usata per scorrere le interfacce [**IXpsOMPageReference**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference) in un documento.<br/> |
| [**IXpsOMDocumentStructureResource**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentstructureresource)<br/> | Nessuno<br/>                                               | Rappresenta la parte DocumentStructure.<br/>                                                                                                                                                                                                                                                                           |



 

## <a name="code-examples"></a>Esempi di codice

Gli esempi di codice in questa sezione illustrano come alcune delle interfacce documento vengono usate in un programma.

### <a name="get-the-page-references-of-a-document"></a>Ottenere i riferimenti di pagina di un documento

L'esempio di codice seguente ottiene un puntatore a [**IXpsOMPageReferenceCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereferencecollection) che contiene l'elenco di interfacce [**IXpsOMPageReference**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference) per il documento a cui fa riferimento il parametro *doc.*


```C++
    HRESULT                               hr = S_OK;


    IXpsOMPageReferenceCollection         *pages;
    IXpsOMPageReference                   *pageRef;
    IXpsOMPage                            *page;

    UINT32  numPageRefs = 0;
    UINT32  thisPageRef = 0;

    // get the doc contents
    hr = doc->GetPageReferences(&pages);
        
    // walk the collection of page references
    hr = pages->GetCount(&numPageRefs);
    thisPageRef = 0;
    while (thisPageRef < numPageRefs) {
        // get this page reference
        hr = pages->GetAt(thisPageRef, &pageRef);

        // get the page content of this page reference
        hr = pageRef->GetPage (&page);

        // use the page

        // free this page & page reference and go to next
        page->Release();
        pageRef->Release();
        thisPageRef++;
    }

    pages->Release();
```



### <a name="get-the-document-structure-of-a-document"></a>Ottenere la struttura del documento di un documento

Nell'esempio di codice seguente viene recuperata la risorsa che contiene la struttura del documento.


```C++
    HRESULT                             hr = S_OK;
    
    IXpsOMDocumentStructureResource     *docStruct;
    IStream                             *docStructResStream;

    // doc is passed in as an argument
    // get the doc contents
    hr = doc->GetDocumentStructureResource(&docStruct);
   
    hr = docStruct->GetStream ( &docStructResStream );

    // access the document structure resource 
    //  contents by reading from the stream

    docStructResStream->Release();
    docStruct->Release();

```



 

 




