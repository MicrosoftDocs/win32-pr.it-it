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
# <a name="xps-om-package-interfaces"></a><span data-ttu-id="72087-103">Interfacce del pacchetto XPS OM</span><span class="sxs-lookup"><span data-stu-id="72087-103">XPS OM Package Interfaces</span></span>

<span data-ttu-id="72087-104">Le interfacce del pacchetto rappresentano il primo livello di XPS OM, che corrisponde a un file di documento XPS.</span><span class="sxs-lookup"><span data-stu-id="72087-104">The package interfaces represent the top level of the XPS OM, which corresponds to an XPS document file.</span></span> <span data-ttu-id="72087-105">Queste interfacce contengono metodi che serializzano XPS OM in un documento o flusso XPS e deserializzano un pacchetto XPS per creare un OM XPS che consente a un programma di accedere al contenuto di un documento.</span><span class="sxs-lookup"><span data-stu-id="72087-105">These interfaces contain methods that serialize an XPS OM to an XPS document or stream, and deserialize an XPS package to create an XPS OM that enables a program to access the contents of a document.</span></span>



| <span data-ttu-id="72087-106">Nome interfaccia</span><span class="sxs-lookup"><span data-stu-id="72087-106">Interface name</span></span>                                                  | <span data-ttu-id="72087-107">Interfacce figlio logiche</span><span class="sxs-lookup"><span data-stu-id="72087-107">Logical child interfaces</span></span>                                                                                                            | <span data-ttu-id="72087-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="72087-108">Description</span></span>                                                                                    |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="72087-109">**IXpsOMPackage**</span><span class="sxs-lookup"><span data-stu-id="72087-109">**IXpsOMPackage**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage)<br/>               | [<span data-ttu-id="72087-110">**IXpsOMDocumentSequence**</span><span class="sxs-lookup"><span data-stu-id="72087-110">**IXpsOMDocumentSequence**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence)<br/> [<span data-ttu-id="72087-111">**IXpsOMCoreProperties**</span><span class="sxs-lookup"><span data-stu-id="72087-111">**IXpsOMCoreProperties**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcoreproperties)<br/> | <span data-ttu-id="72087-112">OM XPS completo che corrisponde al pacchetto che contiene il documento XPS.</span><span class="sxs-lookup"><span data-stu-id="72087-112">The complete XPS OM that corresponds to the package that contains the XPS document.</span></span><br/> |
| [<span data-ttu-id="72087-113">**IXpsOMPackageWriter**</span><span class="sxs-lookup"><span data-stu-id="72087-113">**IXpsOMPackageWriter**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter)<br/>   | <span data-ttu-id="72087-114">nessuno</span><span class="sxs-lookup"><span data-stu-id="72087-114">None</span></span><br/>                                                                                                                     | <span data-ttu-id="72087-115">Consente la serializzazione incrementale delle pagine documento in un pacchetto.</span><span class="sxs-lookup"><span data-stu-id="72087-115">Enables incremental serialization of document pages to a package.</span></span><br/>                   |
| [<span data-ttu-id="72087-116">**IXpsOMCoreProperties**</span><span class="sxs-lookup"><span data-stu-id="72087-116">**IXpsOMCoreProperties**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcoreproperties)<br/> | <span data-ttu-id="72087-117">nessuno</span><span class="sxs-lookup"><span data-stu-id="72087-117">None</span></span><br/>                                                                                                                     | <span data-ttu-id="72087-118">Accede ai metadati del documento.</span><span class="sxs-lookup"><span data-stu-id="72087-118">Accesses the document metadata.</span></span> <br/>                                                    |



 

## <a name="code-examples"></a><span data-ttu-id="72087-119">Esempi di codice</span><span class="sxs-lookup"><span data-stu-id="72087-119">Code Examples</span></span>

<span data-ttu-id="72087-120">Negli esempi di codice seguenti viene illustrato il modo in cui alcune interfacce del pacchetto vengono utilizzate da un programma.</span><span class="sxs-lookup"><span data-stu-id="72087-120">The code examples that follow illustrate how some of the package interfaces are used by a program.</span></span> <span data-ttu-id="72087-121">Se non specificato diversamente, tutti gli elementi in corsivo sono nomi di parametro.</span><span class="sxs-lookup"><span data-stu-id="72087-121">Unless noted otherwise, all italicized items are parameter names.</span></span>

-   [<span data-ttu-id="72087-122">Leggere un documento XPS in un OM XPS</span><span class="sxs-lookup"><span data-stu-id="72087-122">Read an XPS document into an XPS OM</span></span>](#read-an-xps-document-into-an-xps-om)
-   [<span data-ttu-id="72087-123">Scrivere un oggetto XPS OM in un file di documento XPS</span><span class="sxs-lookup"><span data-stu-id="72087-123">Write an XPS OM to an XPS document file</span></span>](#write-an-xps-om-to-an-xps-document-file)
-   [<span data-ttu-id="72087-124">Accedere alla sequenza di documenti di XPS OM</span><span class="sxs-lookup"><span data-stu-id="72087-124">Access the document sequence of the XPS OM</span></span>](#access-the-document-sequence-of-the-xps-om)
-   [<span data-ttu-id="72087-125">Accedere al CoreProperties del documento</span><span class="sxs-lookup"><span data-stu-id="72087-125">Access the document's CoreProperties</span></span>](#access-the-documents-coreproperties)

### <a name="read-an-xps-document-into-an-xps-om"></a><span data-ttu-id="72087-126">Leggere un documento XPS in un OM XPS</span><span class="sxs-lookup"><span data-stu-id="72087-126">Read an XPS document into an XPS OM</span></span>

<span data-ttu-id="72087-127">Da un documento XPS esistente il cui nome file è archiviato in *xpsDocumentFilename*, in questo esempio di codice viene creato un OM XPS a cui fa riferimento *xpsPackage*.</span><span class="sxs-lookup"><span data-stu-id="72087-127">From an existing XPS document whose file name is stored in *xpsDocumentFilename*, this code example creates an XPS OM that is referenced by *xpsPackage*.</span></span>


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



### <a name="write-an-xps-om-to-an-xps-document-file"></a><span data-ttu-id="72087-128">Scrivere un oggetto XPS OM in un file di documento XPS</span><span class="sxs-lookup"><span data-stu-id="72087-128">Write an XPS OM to an XPS document file</span></span>

<span data-ttu-id="72087-129">Nell'esempio di codice seguente viene scritto il codice OM XPS a cui fa riferimento *xpsPackage*.</span><span class="sxs-lookup"><span data-stu-id="72087-129">The following code example writes the XPS OM that is referenced by *xpsPackage*.</span></span> <span data-ttu-id="72087-130">Nell'esempio viene creato un documento XPS nel file il cui nome è archiviato in *filename*.</span><span class="sxs-lookup"><span data-stu-id="72087-130">The example creates an XPS document in the file whose name is stored in *fileName*.</span></span>


```C++
    HRESULT hr = S_OK;

    hr = xpsPackage->WriteToFile(
        xpsDocumentFilename,
        NULL,                    // LPSECURITY_ATTRIBUTES
        FILE_ATTRIBUTE_NORMAL,
        FALSE);                  // optimizeMarkupSize
```



### <a name="access-the-document-sequence-of-the-xps-om"></a><span data-ttu-id="72087-131">Accedere alla sequenza di documenti di XPS OM</span><span class="sxs-lookup"><span data-stu-id="72087-131">Access the document sequence of the XPS OM</span></span>

<span data-ttu-id="72087-132">Nell'esempio di codice seguente viene ottenuto un puntatore all'interfaccia [**IXpsOMDocumentSequence**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence) , che contiene la sequenza di documenti dell'OM XPS che è rappresentata da *xpsPackage*.</span><span class="sxs-lookup"><span data-stu-id="72087-132">The following code example obtains a pointer to the [**IXpsOMDocumentSequence**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence) interface, which contains the document sequence of the XPS OM that is represented by *xpsPackage*.</span></span>


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



### <a name="access-the-documents-coreproperties"></a><span data-ttu-id="72087-133">Accedere al CoreProperties del documento</span><span class="sxs-lookup"><span data-stu-id="72087-133">Access the document's CoreProperties</span></span>

<span data-ttu-id="72087-134">Nell'esempio di codice seguente viene ottenuto un puntatore all'interfaccia [**IXpsOMCoreProperties**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcoreproperties) , consentendo al programma di accedere al contenuto della parte CoreProperties.</span><span class="sxs-lookup"><span data-stu-id="72087-134">The following is code example obtains a pointer to the [**IXpsOMCoreProperties**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcoreproperties) interface, allowing the program to access the contents of the CoreProperties part.</span></span> <span data-ttu-id="72087-135">Nell'esempio si presuppone che il documento sia stato letto in un OM XPS che è rappresentato da *xpsPackage*.</span><span class="sxs-lookup"><span data-stu-id="72087-135">In the example, the document is assumed to have been read into an XPS OM that is represented by *xpsPackage*.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="72087-136">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="72087-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="72087-137">Uso dell'interfaccia IXpsOMPackageWriter</span><span class="sxs-lookup"><span data-stu-id="72087-137">Using the IXpsOMPackageWriter Interface</span></span>](using-the-ixpsompackagewriter-interface.md)
</dt> <dt>

[<span data-ttu-id="72087-138">Esplorare XPS OM</span><span class="sxs-lookup"><span data-stu-id="72087-138">Navigate the XPS OM</span></span>](navigate-the-xps-om.md)
</dt> <dt>

[<span data-ttu-id="72087-139">**Interfaccia IXpsOMDocumentSequence**</span><span class="sxs-lookup"><span data-stu-id="72087-139">**IXpsOMDocumentSequence Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence)
</dt> <dt>

[<span data-ttu-id="72087-140">**Interfaccia IXpsOMPackage**</span><span class="sxs-lookup"><span data-stu-id="72087-140">**IXpsOMPackage Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage)
</dt> <dt>

[<span data-ttu-id="72087-141">**Interfaccia IXpsOMPackageWriter**</span><span class="sxs-lookup"><span data-stu-id="72087-141">**IXpsOMPackageWriter Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter)
</dt> <dt>

[<span data-ttu-id="72087-142">**Interfaccia IXpsOMCoreProperties**</span><span class="sxs-lookup"><span data-stu-id="72087-142">**IXpsOMCoreProperties Interface**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcoreproperties)
</dt> </dl>

 

 




