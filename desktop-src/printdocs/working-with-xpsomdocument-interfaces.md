---
description: In questo argomento vengono descritte le interfacce che consentono di accedere ai componenti a livello di documento di un OM XPS.
ms.assetid: 96b92480-cc28-4a57-a184-c52d3ddc9b05
title: Uso delle interfacce IXpsOMDocument
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5299452195dc8f14ebd08508c3fd9a6e198781a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311532"
---
# <a name="working-with-ixpsomdocument-interfaces"></a><span data-ttu-id="d834f-103">Uso delle interfacce IXpsOMDocument</span><span class="sxs-lookup"><span data-stu-id="d834f-103">Working with IXpsOMDocument Interfaces</span></span>

<span data-ttu-id="d834f-104">In questo argomento vengono descritte le interfacce che consentono di accedere ai componenti a livello di documento di un OM XPS.</span><span class="sxs-lookup"><span data-stu-id="d834f-104">This topic describes the interfaces that provide access to the document-level components of an XPS OM.</span></span>



| <span data-ttu-id="d834f-105">Nome interfaccia</span><span class="sxs-lookup"><span data-stu-id="d834f-105">Interface name</span></span>                                                                        | <span data-ttu-id="d834f-106">Interfacce figlio logiche</span><span class="sxs-lookup"><span data-stu-id="d834f-106">Logical child interfaces</span></span>                                      | <span data-ttu-id="d834f-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d834f-107">Description</span></span>                                                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------|---------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d834f-108">**IXpsOMDocument**</span><span class="sxs-lookup"><span data-stu-id="d834f-108">**IXpsOMDocument**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument)<br/>                                   | [<span data-ttu-id="d834f-109">**IXpsOMPageReference**</span><span class="sxs-lookup"><span data-stu-id="d834f-109">**IXpsOMPageReference**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)<br/> | <span data-ttu-id="d834f-110">Rappresenta una singola parte di FixedDocument e associa una raccolta di riferimenti a pagine.</span><span class="sxs-lookup"><span data-stu-id="d834f-110">Represents a single FixedDocument part and binds a collection of page references.</span></span><br/> <span data-ttu-id="d834f-111">[**IXpsOMPageReferenceCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereferencecollection) è l'interfaccia di raccolta usata per scorrere le interfacce [**IXpsOMPageReference**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference) in un documento.</span><span class="sxs-lookup"><span data-stu-id="d834f-111">[**IXpsOMPageReferenceCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereferencecollection) is the collection interface that is used to iterate through the [**IXpsOMPageReference**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference) interfaces in a document.</span></span><br/> |
| [<span data-ttu-id="d834f-112">**IXpsOMDocumentStructureResource**</span><span class="sxs-lookup"><span data-stu-id="d834f-112">**IXpsOMDocumentStructureResource**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentstructureresource)<br/> | <span data-ttu-id="d834f-113">nessuno</span><span class="sxs-lookup"><span data-stu-id="d834f-113">None</span></span><br/>                                               | <span data-ttu-id="d834f-114">Rappresenta la parte DocumentStructure.</span><span class="sxs-lookup"><span data-stu-id="d834f-114">Represents the DocumentStructure part.</span></span><br/>                                                                                                                                                                                                                                                                           |



 

## <a name="code-examples"></a><span data-ttu-id="d834f-115">Esempi di codice</span><span class="sxs-lookup"><span data-stu-id="d834f-115">Code Examples</span></span>

<span data-ttu-id="d834f-116">Negli esempi di codice di questa sezione viene illustrato il modo in cui alcune delle interfacce dei documenti vengono utilizzate in un programma.</span><span class="sxs-lookup"><span data-stu-id="d834f-116">The code examples in this section illustrate how some of the document interfaces are used in a program.</span></span>

### <a name="get-the-page-references-of-a-document"></a><span data-ttu-id="d834f-117">Ottenere i riferimenti di pagina di un documento</span><span class="sxs-lookup"><span data-stu-id="d834f-117">Get the page references of a document</span></span>

<span data-ttu-id="d834f-118">Nell'esempio di codice seguente viene ottenuto un puntatore a [**IXpsOMPageReferenceCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereferencecollection) che contiene l'elenco di interfacce [**IXpsOMPageReference**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference) per il documento a cui fa riferimento il parametro *doc* .</span><span class="sxs-lookup"><span data-stu-id="d834f-118">The following code example gets a pointer to the [**IXpsOMPageReferenceCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereferencecollection) that contains the list of [**IXpsOMPageReference**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference) interfaces for the document that is referenced by *doc* parameter.</span></span>


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



### <a name="get-the-document-structure-of-a-document"></a><span data-ttu-id="d834f-119">Ottenere la struttura del documento di un documento</span><span class="sxs-lookup"><span data-stu-id="d834f-119">Get the document structure of a document</span></span>

<span data-ttu-id="d834f-120">Nell'esempio di codice seguente viene ottenuta la risorsa che contiene la struttura del documento.</span><span class="sxs-lookup"><span data-stu-id="d834f-120">The following code example gets the resource that contains the document structure.</span></span>


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



 

 




