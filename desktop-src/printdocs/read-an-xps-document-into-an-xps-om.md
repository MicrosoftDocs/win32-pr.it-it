---
description: Viene descritto come leggere un documento XPS esistente da un file in un OM XPS.
ms.assetid: 92a8d19f-1c9e-4e02-a3d4-f2869ec871df
title: Leggere un documento XPS in un OM XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5c3b703de24be58db875618b575cebf9c1c0b27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348221"
---
# <a name="read-an-xps-document-into-an-xps-om"></a><span data-ttu-id="953b7-103">Leggere un documento XPS in un OM XPS</span><span class="sxs-lookup"><span data-stu-id="953b7-103">Read an XPS Document into an XPS OM</span></span>

<span data-ttu-id="953b7-104">Viene descritto come leggere un documento XPS esistente da un file in un OM XPS.</span><span class="sxs-lookup"><span data-stu-id="953b7-104">Describes how to read an existing XPS document from a file into an XPS OM.</span></span>

<span data-ttu-id="953b7-105">Per creare un oggetto XPS OM da un documento XPS, chiamare il metodo [**IXpsOMObjectFactory:: CreatePackageFromFile**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagefromfile) .</span><span class="sxs-lookup"><span data-stu-id="953b7-105">To create an XPS OM from an XPS document, call the [**IXpsOMObjectFactory::CreatePackageFromFile**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagefromfile) method.</span></span>

<span data-ttu-id="953b7-106">Prima di usare questi esempi di codice nel programma, leggere la dichiarazione di non responsabilità nelle [attività comuni di programmazione dei documenti XPS](common-xps-document-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="953b7-106">Before using these code examples in your program, read the disclaimer in [Common XPS Document Programming Tasks](common-xps-document-tasks.md).</span></span>

## <a name="code-example"></a><span data-ttu-id="953b7-107">Esempio di codice</span><span class="sxs-lookup"><span data-stu-id="953b7-107">Code Example</span></span>

<span data-ttu-id="953b7-108">Nell'esempio di codice seguente si presuppone che l'inizializzazione descritta in [Initialize a XPS om](xps-object-model-initialization.md) abbia avuto esito positivo.</span><span class="sxs-lookup"><span data-stu-id="953b7-108">The following code example assumes that the initialization described in [Initialize an XPS OM](xps-object-model-initialization.md) has succeeded.</span></span>


```C++
    IXpsOMPackage *package = NULL;

    hr = xpsFactory->CreatePackageFromFile(
        xpsDocumentFilename,
        FALSE,
        &package);

    // package now contains a pointer to the IXpsOMPackage
    // object that has been populated with the contents
    // of the XPS document in xpsDocumentFilename.

    // When finished with the package, release the object.
    if (NULL != package) package->Release();
```



<span data-ttu-id="953b7-109">Per creare un oggetto XPS OM da un documento XPS archiviato come flusso, chiamare [**IXpsOMObjectFactory:: CreatePackageFromStream**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagefromstream).</span><span class="sxs-lookup"><span data-stu-id="953b7-109">To create an XPS OM from an XPS document that is stored as a stream, call [**IXpsOMObjectFactory::CreatePackageFromStream**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagefromstream).</span></span>

## <a name="remarks"></a><span data-ttu-id="953b7-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="953b7-110">Remarks</span></span>

<span data-ttu-id="953b7-111">Se si scrive un OM XPS immediatamente dopo aver letto un pacchetto XPS, è possibile che alcuni contenuti originali vengano persi o modificati.</span><span class="sxs-lookup"><span data-stu-id="953b7-111">If you write an XPS OM immediately after you have read an XPS package into it, some of the original content might be lost or changed.</span></span>

<span data-ttu-id="953b7-112">Alcune delle modifiche che possono verificarsi in questo caso sono elencate nella tabella seguente:</span><span class="sxs-lookup"><span data-stu-id="953b7-112">Some of the changes that can occur in such case are listed in the table that follows:</span></span>

| <span data-ttu-id="953b7-113">Funzionalità del documento</span><span class="sxs-lookup"><span data-stu-id="953b7-113">Document feature</span></span>                      | <span data-ttu-id="953b7-114">Azione</span><span class="sxs-lookup"><span data-stu-id="953b7-114">Action</span></span>                                                             |
|---------------------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="953b7-115">Firme digitali</span><span class="sxs-lookup"><span data-stu-id="953b7-115">Digital signatures</span></span><br/>         | <span data-ttu-id="953b7-116">Rimosso dal documento</span><span class="sxs-lookup"><span data-stu-id="953b7-116">Removed from the document</span></span><br/>                               |
| <span data-ttu-id="953b7-117">Parte DiscardControl</span><span class="sxs-lookup"><span data-stu-id="953b7-117">DiscardControl part</span></span><br/>        | <span data-ttu-id="953b7-118">Rimosso dal documento</span><span class="sxs-lookup"><span data-stu-id="953b7-118">Removed from the document</span></span><br/>                               |
| <span data-ttu-id="953b7-119">Parti del documento esterno</span><span class="sxs-lookup"><span data-stu-id="953b7-119">Foreign document parts</span></span><br/>     | <span data-ttu-id="953b7-120">Rimosso dal documento</span><span class="sxs-lookup"><span data-stu-id="953b7-120">Removed from the document</span></span><br/>                               |
| <span data-ttu-id="953b7-121">Markup FixedPage</span><span class="sxs-lookup"><span data-stu-id="953b7-121">FixedPage markup</span></span><br/>           | <span data-ttu-id="953b7-122">Modificato dall'originale</span><span class="sxs-lookup"><span data-stu-id="953b7-122">Modified from the original</span></span><br/>                              |
| <span data-ttu-id="953b7-123">Markup del dizionario risorse</span><span class="sxs-lookup"><span data-stu-id="953b7-123">Resource dictionary markup</span></span><br/> | <span data-ttu-id="953b7-124">Modificato dall'originale, se è impostato il flag di ottimizzazione</span><span class="sxs-lookup"><span data-stu-id="953b7-124">Modified from the original, if Optimization flag is set</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="953b7-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="953b7-125">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="953b7-126">**Passaggi successivi**</span><span class="sxs-lookup"><span data-stu-id="953b7-126">**Next Steps**</span></span>
</dt> <dt>

[<span data-ttu-id="953b7-127">Esplorare XPS OM</span><span class="sxs-lookup"><span data-stu-id="953b7-127">Navigate the XPS OM</span></span>](navigate-the-xps-om.md)
</dt> <dt>

[<span data-ttu-id="953b7-128">Scrivere testo in un OM XPS</span><span class="sxs-lookup"><span data-stu-id="953b7-128">Write Text to an XPS OM</span></span>](write-text-to-an-xps-om.md)
</dt> <dt>

[<span data-ttu-id="953b7-129">Creare grafica in un OM XPS</span><span class="sxs-lookup"><span data-stu-id="953b7-129">Draw Graphics in an XPS OM</span></span>](draw-graphics-in-an-xps-om.md)
</dt> <dt>

[<span data-ttu-id="953b7-130">Inserire immagini in un OM XPS</span><span class="sxs-lookup"><span data-stu-id="953b7-130">Place Images in an XPS OM</span></span>](place-images-in-an-xps-om.md)
</dt> <dt>

<span data-ttu-id="953b7-131">**Usato in questa sezione**</span><span class="sxs-lookup"><span data-stu-id="953b7-131">**Used in This Section**</span></span>
</dt> <dt>

[<span data-ttu-id="953b7-132">**IXpsOMObjectFactory**</span><span class="sxs-lookup"><span data-stu-id="953b7-132">**IXpsOMObjectFactory**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory)
</dt> <dt>

[<span data-ttu-id="953b7-133">**IXpsOMPackage**</span><span class="sxs-lookup"><span data-stu-id="953b7-133">**IXpsOMPackage**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage)
</dt> <dt>

<span data-ttu-id="953b7-134">**Per ulteriori informazioni**</span><span class="sxs-lookup"><span data-stu-id="953b7-134">**For More Information**</span></span>
</dt> <dt>

[<span data-ttu-id="953b7-135">Inizializzare un OM XPS</span><span class="sxs-lookup"><span data-stu-id="953b7-135">Initialize an XPS OM</span></span>](xps-object-model-initialization.md)
</dt> <dt>

[<span data-ttu-id="953b7-136">API per la creazione di pacchetti</span><span class="sxs-lookup"><span data-stu-id="953b7-136">Packaging API</span></span>](/previous-versions/windows/desktop/opc/packaging)
</dt> <dt>

[<span data-ttu-id="953b7-137">Informazioni di riferimento sulle API documento XPS</span><span class="sxs-lookup"><span data-stu-id="953b7-137">XPS Document API Reference</span></span>](xps-programming-reference.md)
</dt> <dt>

[<span data-ttu-id="953b7-138">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="953b7-138">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

