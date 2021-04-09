---
description: Le interfacce del pacchetto rappresentano il primo livello di XPS OM, che corrisponde a un file di documento XPS.
ms.assetid: 9e269b18-e5b1-4801-b8e7-473750443c6d
title: Interfacce del pacchetto XPS OM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1465f5d6782e29f9c37f899b59790302e21ebf1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880561"
---
# <a name="xps-om-package-interfaces"></a>Interfacce del pacchetto XPS OM

Le interfacce del pacchetto rappresentano il primo livello di XPS OM, che corrisponde a un file di documento XPS. Queste interfacce contengono metodi che serializzano XPS OM in un documento o flusso XPS e deserializzano un pacchetto XPS per creare un OM XPS che consente a un programma di accedere al contenuto di un documento.



| Nome interfaccia                                                  | Interfacce figlio logiche                                                                                                            | Descrizione                                                                                    |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [**IXpsOMPackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage)<br/>               | [**IXpsOMDocumentSequence**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence)<br/> [**IXpsOMCoreProperties**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcoreproperties)<br/> | OM XPS completo che corrisponde al pacchetto che contiene il documento XPS.<br/> |
| [**IXpsOMPackageWriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter)<br/>   | nessuno<br/>                                                                                                                     | Consente la serializzazione incrementale delle pagine documento in un pacchetto.<br/>                   |
| [**IXpsOMCoreProperties**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcoreproperties)<br/> | nessuno<br/>                                                                                                                     | Accede ai metadati del documento. <br/>                                                    |



 

## <a name="code-examples"></a>Esempi di codice

Negli esempi di codice seguenti viene illustrato il modo in cui alcune interfacce del pacchetto vengono utilizzate da un programma. Se non specificato diversamente, tutti gli elementi in corsivo sono nomi di parametro.

-   [Leggere un documento XPS in un OM XPS](#read-an-xps-document-into-an-xps-om)
-   [Scrivere un oggetto XPS OM in un file di documento XPS](#write-an-xps-om-to-an-xps-document-file)
-   [Accedere alla sequenza di documenti di XPS OM](#access-the-document-sequence-of-the-xps-om)
-   [Accedere al CoreProperties del documento](#access-the-documents-coreproperties)

### <a name="read-an-xps-document-into-an-xps-om"></a>Leggere un documento XPS in un OM XPS

Da un documento XPS esistente il cui nome file è archiviato in *xpsDocumentFilename*, in questo esempio di codice viene creato un OM XPS a cui fa riferimento *xpsPackage*.


```C++
    HRESULT                 hr = S_OK;
    IXpsOMPackage           *xpsPackage;

    hr = xpsFactory->CreatePackageFromFile(
        xpsDocumentFilename,
        FALSE,
        &xpsPackage);

    // xpsPackage now contains a pointer to the IXpsOMPackage
    // object that has been populated with the contents
    // of the XPS document in xpsDocumentFilename.
```



### <a name="write-an-xps-om-to-an-xps-document-file"></a>Scrivere un oggetto XPS OM in un file di documento XPS

Nell'esempio di codice seguente viene scritto il codice OM XPS a cui fa riferimento *xpsPackage*. Nell'esempio viene creato un documento XPS nel file il cui nome è archiviato in *filename*.


```C++
    HRESULT hr = S_OK;

    hr = xpsPackage->WriteToFile(
        xpsDocumentFilename,
        NULL,                    // LPSECURITY_ATTRIBUTES
        FILE_ATTRIBUTE_NORMAL,
        FALSE);                  // optimizeMarkupSize
```



### <a name="access-the-document-sequence-of-the-xps-om"></a>Accedere alla sequenza di documenti di XPS OM

Nell'esempio di codice seguente viene ottenuto un puntatore all'interfaccia [**IXpsOMDocumentSequence**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence) , che contiene la sequenza di documenti dell'OM XPS che è rappresentata da *xpsPackage*.


```C++
    HRESULT                         hr = S_OK;
    IXpsOMDocumentSequence          *docSeq;
    IXpsOMDocumentCollection        *docs;

    // get the fixed document sequence of the package
    hr = xpsPackage->GetDocumentSequence(&docSeq);

    // get the collection of fixed documents in 
    //  the fixed document sequence
    hr = docSeq->GetDocuments(&docs);
```



### <a name="access-the-documents-coreproperties"></a>Accedere al CoreProperties del documento

Nell'esempio di codice seguente viene ottenuto un puntatore all'interfaccia [**IXpsOMCoreProperties**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcoreproperties) , consentendo al programma di accedere al contenuto della parte CoreProperties. Nell'esempio si presuppone che il documento sia stato letto in un OM XPS che è rappresentato da *xpsPackage*.


```C++
    HRESULT                         hr = S_OK;
    IXpsOMCoreProperties            *coreProps;
    LPWSTR                          title;

    // get the fixed document sequence of the package
    hr = xpsPackage->GetCoreProperties(&coreProps);

    // get the title property 
    hr = coreProps->GetTitle(&title);

    // do something with the title property here...

    // free the string when finished with it
    CoTaskMemFree ( title );
    coreProps->Release();
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso dell'interfaccia IXpsOMPackageWriter](using-the-ixpsompackagewriter-interface.md)
</dt> <dt>

[Esplorare XPS OM](navigate-the-xps-om.md)
</dt> <dt>

[**Interfaccia IXpsOMDocumentSequence**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence)
</dt> <dt>

[**Interfaccia IXpsOMPackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage)
</dt> <dt>

[**Interfaccia IXpsOMPackageWriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter)
</dt> <dt>

[**Interfaccia IXpsOMCoreProperties**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcoreproperties)
</dt> </dl>

 

 




