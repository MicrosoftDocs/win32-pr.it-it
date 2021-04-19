---
description: Questo argomento descrive come usare le interfacce che forniscono l'accesso a FixedDocumentSequence, che è il livello principale della gerarchia dei documenti in un OM XPS.
ms.assetid: e7d01f21-0b5d-4385-89e8-14021800e234
title: Uso delle interfacce IXpsOMDocumentSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f108cbadf735b334f758102915abbda239a4e974
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313533"
---
# <a name="working-with-ixpsomdocumentsequence-interfaces"></a><span data-ttu-id="de078-103">Uso delle interfacce IXpsOMDocumentSequence</span><span class="sxs-lookup"><span data-stu-id="de078-103">Working with IXpsOMDocumentSequence Interfaces</span></span>

<span data-ttu-id="de078-104">Questo argomento descrive come usare le interfacce che forniscono l'accesso a FixedDocumentSequence, che è il livello principale della gerarchia dei documenti in un OM XPS.</span><span class="sxs-lookup"><span data-stu-id="de078-104">This topic describes how to use the interfaces that provide access to the FixedDocumentSequence, which is the top level of the document hierarchy in an XPS OM.</span></span>



| <span data-ttu-id="de078-105">Nome interfaccia</span><span class="sxs-lookup"><span data-stu-id="de078-105">Interface name</span></span>                                                          | <span data-ttu-id="de078-106">Interfacce figlio logiche</span><span class="sxs-lookup"><span data-stu-id="de078-106">Logical child interfaces</span></span>                            | <span data-ttu-id="de078-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="de078-107">Description</span></span>                                                              |
|-------------------------------------------------------------------------|-----------------------------------------------------|--------------------------------------------------------------------------|
| [<span data-ttu-id="de078-108">**IXpsOMDocumentSequence**</span><span class="sxs-lookup"><span data-stu-id="de078-108">**IXpsOMDocumentSequence**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence)<br/>     | [<span data-ttu-id="de078-109">**IXpsOMDocument**</span><span class="sxs-lookup"><span data-stu-id="de078-109">**IXpsOMDocument**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument)<br/> | <span data-ttu-id="de078-110">Raggruppa un set di FixedDocument in un elenco ordinato.</span><span class="sxs-lookup"><span data-stu-id="de078-110">Groups a set of FixedDocuments into an ordered list.</span></span><br/>          |
| [<span data-ttu-id="de078-111">**IXpsOMDocumentCollection**</span><span class="sxs-lookup"><span data-stu-id="de078-111">**IXpsOMDocumentCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentcollection)<br/> | <span data-ttu-id="de078-112">nessuno</span><span class="sxs-lookup"><span data-stu-id="de078-112">None</span></span><br/>                                     | <span data-ttu-id="de078-113">Raccolta di FixedDocument in una sequenza di documenti XPS.</span><span class="sxs-lookup"><span data-stu-id="de078-113">The collection of FixedDocuments in an XPS document sequence.</span></span><br/> |



 

## <a name="code-example"></a><span data-ttu-id="de078-114">Esempio di codice</span><span class="sxs-lookup"><span data-stu-id="de078-114">Code Example</span></span>

<span data-ttu-id="de078-115">Nell'esempio di codice seguente viene ottenuto un puntatore all'interfaccia [**IXpsOMDocumentSequence**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence) che contiene la sequenza di documenti dell'OM XPS che è rappresentata da *xpsPackage*.</span><span class="sxs-lookup"><span data-stu-id="de078-115">The following code example obtains a pointer to the [**IXpsOMDocumentSequence**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence) interface that contains the document sequence of the XPS OM that is represented by *xpsPackage*.</span></span> <span data-ttu-id="de078-116">Nell'esempio vengono quindi enumerati i documenti nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="de078-116">The example then enumerates the documents in the collection.</span></span>


```C++
    HRESULT                         hr = S_OK;

    IXpsOMDocumentSequence          *docSeq;
    IXpsOMDocumentCollection        *docs;
    IXpsOMDocument                  *doc;

    UINT32  numDocs = 0;
    UINT32  thisDoc = 0;

    // get the fixed document sequence of the package
    hr = xpsPackage->GetDocumentSequence(&docSeq);

    // get the collection of fixed documents in 
    //  the fixed document sequence
    hr = docSeq->GetDocuments(&docs);

    // walk the collection of documents;
    hr = docs->GetCount(&numDocs);
    thisDoc = 0;
    while (thisDoc < numDocs) {
        hr = docs->GetAt(thisDoc, &doc);
 
        // use this doc for something

        // release this doc and then go to the next one
        doc->Release();
        thisDoc++;
    }
    // release the document collection and
    // the document sequence
    docs->Release();
    docSeq->Release();
```



 

 




