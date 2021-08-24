---
description: Questo argomento descrive come usare le interfacce che forniscono l'accesso a FixedDocumentSequence, ovvero il primo livello della gerarchia di documenti in un sistema operativo XPS.
ms.assetid: e7d01f21-0b5d-4385-89e8-14021800e234
title: Uso delle interfacce IXpsOMDocumentSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edac74809de63c1ae4e688bb99214d11b091ee4e877c921e9280abc9c6868121
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119098663"
---
# <a name="working-with-ixpsomdocumentsequence-interfaces"></a>Uso delle interfacce IXpsOMDocumentSequence

Questo argomento descrive come usare le interfacce che forniscono l'accesso a FixedDocumentSequence, ovvero il primo livello della gerarchia di documenti in un sistema operativo XPS.



| Nome dell'interfaccia                                                          | Interfacce figlio logiche                            | Descrizione                                                              |
|-------------------------------------------------------------------------|-----------------------------------------------------|--------------------------------------------------------------------------|
| [**IXpsOMDocumentSequence**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence)<br/>     | [**IXpsOMDocument**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument)<br/> | Raggruppa un set di FixedDocuments in un elenco ordinato.<br/>          |
| [**IXpsOMDocumentCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentcollection)<br/> | Nessuno<br/>                                     | Raccolta di FixedDocuments in una sequenza di documenti XPS.<br/> |



 

## <a name="code-example"></a>Esempio di codice

Nell'esempio di codice seguente viene ottenuto un puntatore all'interfaccia [**IXpsOMDocumentSequence**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence) che contiene la sequenza di documenti del sistema operativo XPS rappresentato da *xpsPackage*. Nell'esempio vengono quindi enumerati i documenti nella raccolta .


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



 

 




