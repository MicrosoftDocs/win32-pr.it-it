---
description: In questo argomento viene descritto come utilizzare le interfacce che consentono l'accesso ai riferimenti a pagine in un OM XPS.
ms.assetid: bb227536-3b29-4221-b2d5-bab5e9d91448
title: Uso delle interfacce IXpsOMPageReference
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f4526e6c561a962b77fa3f2fc62d56431359aa6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882509"
---
# <a name="working-with-ixpsompagereference-interfaces"></a><span data-ttu-id="552ae-103">Uso delle interfacce IXpsOMPageReference</span><span class="sxs-lookup"><span data-stu-id="552ae-103">Working with IXpsOMPageReference Interfaces</span></span>

<span data-ttu-id="552ae-104">In questo argomento viene descritto come utilizzare le interfacce che consentono l'accesso ai riferimenti a pagine in un OM XPS.</span><span class="sxs-lookup"><span data-stu-id="552ae-104">This topic describes how to use the interfaces that provide access to page references in an XPS OM.</span></span>



| <span data-ttu-id="552ae-105">Nome interfaccia</span><span class="sxs-lookup"><span data-stu-id="552ae-105">Interface name</span></span>                                                  | <span data-ttu-id="552ae-106">Interfacce figlio logiche</span><span class="sxs-lookup"><span data-stu-id="552ae-106">Logical child interfaces</span></span>                    | <span data-ttu-id="552ae-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="552ae-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------|---------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="552ae-108">**IXpsOMPageReference**</span><span class="sxs-lookup"><span data-stu-id="552ae-108">**IXpsOMPageReference**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)<br/>   | [<span data-ttu-id="552ae-109">**IXpsOMPage**</span><span class="sxs-lookup"><span data-stu-id="552ae-109">**IXpsOMPage**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage)<br/> | <span data-ttu-id="552ae-110">Virtualizza il contenuto di una pagina del documento.</span><span class="sxs-lookup"><span data-stu-id="552ae-110">Virtualizes the content of a document page.</span></span> <br/> <span data-ttu-id="552ae-111">Un riferimento alla pagina contiene informazioni di base sulla pagina, alcune proprietà della pagina e un collegamento al contenuto della pagina.</span><span class="sxs-lookup"><span data-stu-id="552ae-111">A page reference contains basic information about the page, some page properties, and a link to the page contents.</span></span> <span data-ttu-id="552ae-112">L'interfaccia [**IXpsOMPage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage) che comprende il contenuto della pagina viene restituita dal metodo [**IXpsOMPageReference:: GetPage**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-getpage) .</span><span class="sxs-lookup"><span data-stu-id="552ae-112">The [**IXpsOMPage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage) interface that comprises page contents is returned by the [**IXpsOMPageReference::GetPage**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-getpage) method.</span></span><br/> |
| [<span data-ttu-id="552ae-113">**IXpsOMNameCollection**</span><span class="sxs-lookup"><span data-stu-id="552ae-113">**IXpsOMNameCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomnamecollection)<br/> | <span data-ttu-id="552ae-114">nessuno</span><span class="sxs-lookup"><span data-stu-id="552ae-114">None</span></span><br/>                             | <span data-ttu-id="552ae-115">Contiene un elenco di elementi della pagina che sono destinazioni di collegamento ipertestuale.</span><span class="sxs-lookup"><span data-stu-id="552ae-115">Contains a list of page items that are hyperlink targets.</span></span> <span data-ttu-id="552ae-116">L'elenco viene restituito dal metodo [**IXpsOMPageReference:: CollectLinkTargets**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-collectlinktargets) .</span><span class="sxs-lookup"><span data-stu-id="552ae-116">The list is returned by the [**IXpsOMPageReference::CollectLinkTargets**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-collectlinktargets) method.</span></span><br/>                                                                                                                                                               |
| [<span data-ttu-id="552ae-117">**IXpsOMPartResources**</span><span class="sxs-lookup"><span data-stu-id="552ae-117">**IXpsOMPartResources**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompartresources)<br/>   | <span data-ttu-id="552ae-118">nessuno</span><span class="sxs-lookup"><span data-stu-id="552ae-118">None</span></span><br/>                             | <span data-ttu-id="552ae-119">Contiene un elenco di risorse basate sulla parte associate alla pagina.</span><span class="sxs-lookup"><span data-stu-id="552ae-119">Contains a list of the part-based resources that are associated with the page.</span></span> <span data-ttu-id="552ae-120">Questo elenco viene restituito dal metodo [**IXpsOMPageReference:: CollectPartResources**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-collectpartresources) .</span><span class="sxs-lookup"><span data-stu-id="552ae-120">This list is returned by the [**IXpsOMPageReference::CollectPartResources**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-collectpartresources) method.</span></span><br/>                                                                                                                                     |



 

## <a name="code-examples"></a><span data-ttu-id="552ae-121">Esempi di codice</span><span class="sxs-lookup"><span data-stu-id="552ae-121">Code Examples</span></span>

<span data-ttu-id="552ae-122">Negli esempi di codice seguenti viene illustrato come utilizzare le interfacce di riferimento della pagina in un programma.</span><span class="sxs-lookup"><span data-stu-id="552ae-122">The following code examples illustrate how to work with the page reference interfaces in a program.</span></span>

-   [<span data-ttu-id="552ae-123">Ottenere il contenuto della pagina</span><span class="sxs-lookup"><span data-stu-id="552ae-123">Get the page contents</span></span>](#get-the-page-contents)
-   [<span data-ttu-id="552ae-124">Ottiene l'elenco delle destinazioni dei collegamenti ipertestuali in questa pagina</span><span class="sxs-lookup"><span data-stu-id="552ae-124">Get the list of hyperlink targets on this page</span></span>](#get-the-list-of-hyperlink-targets-on-this-page)
-   [<span data-ttu-id="552ae-125">Ottenere le risorse della parte associate a questa pagina</span><span class="sxs-lookup"><span data-stu-id="552ae-125">Get the part resources that are associated with this page</span></span>](#get-the-part-resources-that-are-associated-with-this-page)

### <a name="get-the-page-contents"></a><span data-ttu-id="552ae-126">Ottenere il contenuto della pagina</span><span class="sxs-lookup"><span data-stu-id="552ae-126">Get the page contents</span></span>

<span data-ttu-id="552ae-127">Nell'esempio di codice seguente viene ottenuto un puntatore all'interfaccia [**IXpsOMPage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage) che comprende il contenuto della pagina.</span><span class="sxs-lookup"><span data-stu-id="552ae-127">The following code example gets a pointer to the [**IXpsOMPage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage) interface that comprises the page contents.</span></span> <span data-ttu-id="552ae-128">Se la pagina non è stata caricata in XPS OM, come avviene quando il modello OM XPS viene inizializzato chiamando [**IXpsOMObjectFactory:: CreatePackageFromFile**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagefromfile), la chiamata a [**IXpsOMPageReference:: GetPage**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-getpage) CARICHERÀ la pagina in XPS om.</span><span class="sxs-lookup"><span data-stu-id="552ae-128">If the page has not been loaded into the XPS OM, as happens when the XPS OM is initialized by calling [**IXpsOMObjectFactory::CreatePackageFromFile**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagefromfile), calling [**IXpsOMPageReference::GetPage**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-getpage) will load the page into the XPS OM.</span></span>


```C++
    {
    HRESULT        hr = S_OK;
    IXpsOMPage     *page = NULL;

    // pageRef contains the current page reference
    // and is passed in as a parameter

    // get the page content of this page reference
    hr = pageRef->GetPage (&page);
```



### <a name="get-the-list-of-hyperlink-targets-on-this-page"></a><span data-ttu-id="552ae-129">Ottiene l'elenco delle destinazioni dei collegamenti ipertestuali in questa pagina</span><span class="sxs-lookup"><span data-stu-id="552ae-129">Get the list of hyperlink targets on this page</span></span>

<span data-ttu-id="552ae-130">Nell'esempio di codice seguente viene ottenuto un puntatore all'interfaccia [**IXpsOMNameCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomnamecollection) che contiene l'elenco di elementi della pagina che sono destinazioni di collegamento ipertestuale.</span><span class="sxs-lookup"><span data-stu-id="552ae-130">The following code example gets a pointer to the [**IXpsOMNameCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomnamecollection) interface that contains the list of page items that are hyperlink targets.</span></span> <span data-ttu-id="552ae-131">Se la pagina non è stata caricata in XPS OM, l'elenco di destinazioni dei collegamenti ipertestuali viene letto dal markup **PageContent. LinkTargets** .</span><span class="sxs-lookup"><span data-stu-id="552ae-131">If the page has not been loaded into the XPS OM, the list of hyperlink targets is read from the **PageContent.LinkTargets** markup.</span></span> <span data-ttu-id="552ae-132">Se la pagina è stata caricata, [**CollectLinkTargets**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-collectlinktargets) controlla ogni elemento nella pagina e restituisce un elenco di elementi il cui attributo **IsHyperlinkTarget** è **true**.</span><span class="sxs-lookup"><span data-stu-id="552ae-132">If the page has been loaded, [**CollectLinkTargets**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-collectlinktargets) checks each element in the page and returns a list of elements whose **IsHyperlinkTarget** attribute is **TRUE**.</span></span>


```C++
    HRESULT                         hr = S_OK;
    IXpsOMPage                      *page = NULL;
    IXpsOMNameCollection            *linkTargets = NULL;

    UINT32 numTargets = 0;
    UINT32 thisTarget = 0;
    LPWSTR thisTargetName = NULL;

    // pageRef contains the current page reference 

    // if the page hasn't been loaded yet, for example, if the XPS OM 
    //  was loaded from an XPS document, CollectLinkTargets obtains the
    //  list of link targets from the <PageContent.LinkTargets> markup
    hr = pageRef->CollectLinkTargets(&linkTargets);

    // get the page content of this page reference
    hr = pageRef->GetPage (&page);

    // after the page object has been loaded and calling GetPage or 
    //  by creating a page in the XPS OM, CollectLinkTargets will now check
    //  each of the page elements to return the list so this call to
    //  CollectLinkTargets might take longer to return than the previous
    //  call above if the XPS OM was created from a file
    linkTargets->Release(); // release previous collection
    hr = pageRef->CollectLinkTargets(&linkTargets);
    
    // walk the list of link targets returned
    hr = linkTargets->GetCount( &numTargets );
    thisTarget = 0;
    while (thisTarget < numTargets) {
        hr = linkTargets->GetAt (thisTarget, &thisTargetName);
        printf ("%s\n", thisTargetName);
        // release the target string returned to prevent memory leaks
        CoTaskMemFree (thisTargetName);
        // get next target in list
        thisTarget++;
    }
    // release page and the link target collection
    page->Release();
    linkTargets->Release();
```



### <a name="get-the-part-resources-that-are-associated-with-this-page"></a><span data-ttu-id="552ae-133">Ottenere le risorse della parte associate a questa pagina</span><span class="sxs-lookup"><span data-stu-id="552ae-133">Get the part resources that are associated with this page</span></span>

<span data-ttu-id="552ae-134">Nell'esempio di codice seguente vengono recuperati gli elenchi delle diverse risorse utilizzate da questa pagina.</span><span class="sxs-lookup"><span data-stu-id="552ae-134">The following code example gets the lists of the different resources that are used by this page.</span></span>


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
```



## <a name="related-topics"></a><span data-ttu-id="552ae-135">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="552ae-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="552ae-136">**IXpsOMNameCollection**</span><span class="sxs-lookup"><span data-stu-id="552ae-136">**IXpsOMNameCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomnamecollection)
</dt> <dt>

[<span data-ttu-id="552ae-137">**IXpsOMPage**</span><span class="sxs-lookup"><span data-stu-id="552ae-137">**IXpsOMPage**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage)
</dt> <dt>

[<span data-ttu-id="552ae-138">**IXpsOMPageReference**</span><span class="sxs-lookup"><span data-stu-id="552ae-138">**IXpsOMPageReference**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)
</dt> <dt>

[<span data-ttu-id="552ae-139">**IXpsOMPartResources**</span><span class="sxs-lookup"><span data-stu-id="552ae-139">**IXpsOMPartResources**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompartresources)
</dt> <dt>

[<span data-ttu-id="552ae-140">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="552ae-140">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 




