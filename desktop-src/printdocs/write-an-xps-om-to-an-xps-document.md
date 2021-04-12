---
description: Viene descritto come scrivere il contenuto di un oggetto XPS OM in un programma in un file di documento XPS.
ms.assetid: 8bee8059-b901-4a99-a7e4-60dad831c239
title: Scrivere un OM XPS in un documento XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 811f773394ee9dbbcf77dc75d1429322bb733631
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232372"
---
# <a name="write-an-xps-om-to-an-xps-document"></a><span data-ttu-id="d8d26-103">Scrivere un OM XPS in un documento XPS</span><span class="sxs-lookup"><span data-stu-id="d8d26-103">Write an XPS OM to an XPS Document</span></span>

<span data-ttu-id="d8d26-104">Viene descritto come scrivere il contenuto di un oggetto XPS OM in un programma in un file di documento XPS.</span><span class="sxs-lookup"><span data-stu-id="d8d26-104">Describes how to write the contents of an XPS OM in a program to an XPS document file.</span></span>

<span data-ttu-id="d8d26-105">Se un programma dispone di un OM XPS che contiene un documento completo, il programma può scrivere XPS OM in un file come documento XPS, chiamando il metodo [**WriteToFile**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-writetofile) dell'interfaccia [**IXpsOMPackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage) .</span><span class="sxs-lookup"><span data-stu-id="d8d26-105">If a program has an XPS OM that contains a complete document, the program can write the XPS OM to a file as an XPS document, by calling the [**WriteToFile**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-writetofile) method of the [**IXpsOMPackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage) interface.</span></span>

<span data-ttu-id="d8d26-106">Prima di usare questi esempi di codice in un programma, leggere la dichiarazione di non responsabilità nelle [attività comuni di programmazione dei documenti XPS](common-xps-document-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="d8d26-106">Before using these code examples in a program, read the disclaimer in [Common XPS Document Programming Tasks](common-xps-document-tasks.md).</span></span>

## <a name="writing-a-complete-xps-om-to-an-xps-document"></a><span data-ttu-id="d8d26-107">Scrittura di un OM XPS completo in un documento XPS</span><span class="sxs-lookup"><span data-stu-id="d8d26-107">Writing a complete XPS OM to an XPS document</span></span>

<span data-ttu-id="d8d26-108">Dopo aver impostato il contenuto di un OM XPS, è possibile salvare XPS OM in un file come documento XPS, chiamando il metodo [**WriteToFile**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-writetofile) dell'interfaccia [**IXpsOMPackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage) .</span><span class="sxs-lookup"><span data-stu-id="d8d26-108">After you set the contents of an XPS OM, you can save the XPS OM to a file as an XPS document, by calling the [**WriteToFile**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-writetofile) method of the [**IXpsOMPackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage) interface.</span></span>


```C++
    HRESULT hr = S_OK;

    hr = xpsPackage->WriteToFile(
        fileName,
        NULL,                    // LPSECURITY_ATTRIBUTES
        FILE_ATTRIBUTE_NORMAL,
        FALSE                    // Optimize Markup Size
        );

```



> [!Note]  
> <span data-ttu-id="d8d26-109">La scrittura di un modello OM XPS in un file o in un flusso non crea automaticamente un'anteprima per il documento XPS.</span><span class="sxs-lookup"><span data-stu-id="d8d26-109">Writing an XPS OM to a file or stream does not automatically create a thumbnail for the XPS document.</span></span> <span data-ttu-id="d8d26-110">Per creare un'anteprima del documento XPS, utilizzare l'interfaccia [**IXpsOMThumbnailGenerator**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomthumbnailgenerator) .</span><span class="sxs-lookup"><span data-stu-id="d8d26-110">To create a thumbnail of the XPS document, use the [**IXpsOMThumbnailGenerator**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomthumbnailgenerator) interface.</span></span>

 

## <a name="incrementally-writing-an-xps-document"></a><span data-ttu-id="d8d26-111">Scrittura incrementale di un documento XPS</span><span class="sxs-lookup"><span data-stu-id="d8d26-111">Incrementally writing an XPS document</span></span>

<span data-ttu-id="d8d26-112">L'interfaccia [**IXpsOMPackageWriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) può essere utilizzata per scrivere in modo incrementale le parti di un documento XPS. ad esempio, quando le parti del documento vengono create o elaborate in sequenza.</span><span class="sxs-lookup"><span data-stu-id="d8d26-112">The [**IXpsOMPackageWriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) interface can be used to write the parts of an XPS document incrementally; for example, when the document parts are created or processed in sequence.</span></span>

> [!Note]  
> <span data-ttu-id="d8d26-113">La scrittura di un modello OM XPS in un file o in un flusso non crea automaticamente un'anteprima per il documento XPS.</span><span class="sxs-lookup"><span data-stu-id="d8d26-113">Writing an XPS OM to a file or stream does not automatically create a thumbnail for the XPS document.</span></span> <span data-ttu-id="d8d26-114">Per creare un'anteprima del documento XPS, utilizzare l'interfaccia [**IXpsOMThumbnailGenerator**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomthumbnailgenerator) .</span><span class="sxs-lookup"><span data-stu-id="d8d26-114">To create a thumbnail of the XPS document, use the [**IXpsOMThumbnailGenerator**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomthumbnailgenerator) interface.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="d8d26-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d8d26-115">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="d8d26-116">**Passaggi successivi**</span><span class="sxs-lookup"><span data-stu-id="d8d26-116">**Next Steps**</span></span>
</dt> <dt>

[<span data-ttu-id="d8d26-117">Stampare un OM XPS</span><span class="sxs-lookup"><span data-stu-id="d8d26-117">Print an XPS OM</span></span>](print-an-xps-om.md)
</dt> <dt>

<span data-ttu-id="d8d26-118">**Usato in questa sezione**</span><span class="sxs-lookup"><span data-stu-id="d8d26-118">**Used in This Section**</span></span>
</dt> <dt>

[<span data-ttu-id="d8d26-119">**IOpcPartUri**</span><span class="sxs-lookup"><span data-stu-id="d8d26-119">**IOpcPartUri**</span></span>](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi)
</dt> <dt>

[<span data-ttu-id="d8d26-120">**IXpsOMPackage**</span><span class="sxs-lookup"><span data-stu-id="d8d26-120">**IXpsOMPackage**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage)
</dt> <dt>

[<span data-ttu-id="d8d26-121">**IXpsOMThumbnailGenerator**</span><span class="sxs-lookup"><span data-stu-id="d8d26-121">**IXpsOMThumbnailGenerator**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomthumbnailgenerator)
</dt> <dt>

<span data-ttu-id="d8d26-122">**Per ulteriori informazioni**</span><span class="sxs-lookup"><span data-stu-id="d8d26-122">**For More Information**</span></span>
</dt> <dt>

[<span data-ttu-id="d8d26-123">Inizializzare un OM XPS</span><span class="sxs-lookup"><span data-stu-id="d8d26-123">Initialize an XPS OM</span></span>](xps-object-model-initialization.md)
</dt> <dt>

[<span data-ttu-id="d8d26-124">Informazioni di riferimento sulle API documento XPS</span><span class="sxs-lookup"><span data-stu-id="d8d26-124">XPS Document API Reference</span></span>](xps-programming-reference.md)
</dt> <dt>

[<span data-ttu-id="d8d26-125">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="d8d26-125">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
