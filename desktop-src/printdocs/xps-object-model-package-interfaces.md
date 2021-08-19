---
description: Le interfacce del pacchetto rappresentano il livello superiore del sistema operativo XPS, che corrisponde a un file di documento XPS.
ms.assetid: 9e269b18-e5b1-4801-b8e7-473750443c6d
title: Interfacce del pacchetto OM XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6732531e3874046bbd174c363db24e304da95b9596b810014abb52a795e720c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119886141"
---
# <a name="xps-om-package-interfaces"></a>Interfacce del pacchetto OM XPS

Le interfacce del pacchetto rappresentano il livello superiore del sistema operativo XPS, che corrisponde a un file di documento XPS. Queste interfacce contengono metodi che serializzano un sistema operativo XPS in un documento o un flusso XPS e deserializzano un pacchetto XPS per creare un sistema operativo XPS che consente a un programma di accedere al contenuto di un documento.



| Nome dell'interfaccia                                                  | Interfacce figlio logiche                                                                                                            | Descrizione                                                                                    |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [**IXpsOMPackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage)<br/>               | [**IXpsOMDocumentSequence**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence)<br/> [**IXpsOMCoreProperties**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcoreproperties)<br/> | OM XPS completo che corrisponde al pacchetto che contiene il documento XPS.<br/> |
| [**IXpsOMPackageWriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter)<br/>   | Nessuno<br/>                                                                                                                     | Abilita la serializzazione incrementale delle pagine del documento in un pacchetto.<br/>                   |
| [**IXpsOMCoreProperties**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcoreproperties)<br/> | Nessuno<br/>                                                                                                                     | Accede ai metadati del documento. <br/>                                                    |



 

## <a name="code-examples"></a>Esempi di codice

Gli esempi di codice seguenti illustrano come alcune delle interfacce del pacchetto vengono usate da un programma. Se non diversamente specificato, tutti gli elementi in corsivo sono nomi di parametro.

-   [Leggere un documento XPS in un sistema operativo XPS](#read-an-xps-document-into-an-xps-om)
-   [Scrivere un file di documento XPS OM in un file di documento XPS](#write-an-xps-om-to-an-xps-document-file)
-   [Accedere alla sequenza di documenti di XPS OM](#access-the-document-sequence-of-the-xps-om)
-   [Accedere alle CoreProperties del documento](#access-the-documents-coreproperties)

### <a name="read-an-xps-document-into-an-xps-om"></a>Leggere un documento XPS in un sistema operativo XPS

Da un documento XPS esistente il cui nome file è archiviato in *xpsDocumentFilename*, questo esempio di codice crea un file OM XPS a cui fa riferimento *xpsPackage*.


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



### <a name="write-an-xps-om-to-an-xps-document-file"></a>Scrivere un file di documento XPS OM in un file di documento XPS

Nell'esempio di codice seguente viene scritto il sistema operativo XPS a cui fa riferimento *xpsPackage*. Nell'esempio viene creato un documento XPS nel file il cui nome è archiviato in *fileName*.


```C++
    HRESULT hr = S_OK;

    hr = xpsPackage->WriteToFile(
        xpsDocumentFilename,
        NULL,                    // LPSECURITY_ATTRIBUTES
        FILE_ATTRIBUTE_NORMAL,
        FALSE);                  // optimizeMarkupSize
```



### <a name="access-the-document-sequence-of-the-xps-om"></a>Accedere alla sequenza di documenti di XPS OM

L'esempio di codice seguente ottiene un [**puntatore all'interfaccia IXpsOMDocumentSequence,**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence) che contiene la sequenza di documenti del sistema operativo XPS rappresentato da *xpsPackage*.


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



### <a name="access-the-documents-coreproperties"></a>Accedere alle CoreProperties del documento

L'esempio di codice seguente ottiene un puntatore [**all'interfaccia IXpsOMCoreProperties,**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcoreproperties) consentendo al programma di accedere al contenuto della parte CoreProperties. Nell'esempio si presuppone che il documento sia stato letto in un sistema operativo XPS rappresentato *da xpsPackage*.


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

[Esplorare xps OM](navigate-the-xps-om.md)
</dt> <dt>

[**Interfaccia IXpsOMDocumentSequence**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence)
</dt> <dt>

[**Interfaccia IXpsOMPackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage)
</dt> <dt>

[**Interfaccia IXpsOMPackageWriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter)
</dt> <dt>

[**Interfaccia IXpsOMCoreProperties**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcoreproperties)
</dt> </dl>

 

 




