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
# <a name="working-with-ixpsompagereference-interfaces"></a>Uso delle interfacce IXpsOMPageReference

In questo argomento viene descritto come utilizzare le interfacce che consentono l'accesso ai riferimenti a pagine in un OM XPS.



| Nome interfaccia                                                  | Interfacce figlio logiche                    | Descrizione                                                                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------|---------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IXpsOMPageReference**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)<br/>   | [**IXpsOMPage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage)<br/> | Virtualizza il contenuto di una pagina del documento. <br/> Un riferimento alla pagina contiene informazioni di base sulla pagina, alcune proprietà della pagina e un collegamento al contenuto della pagina. L'interfaccia [**IXpsOMPage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage) che comprende il contenuto della pagina viene restituita dal metodo [**IXpsOMPageReference:: GetPage**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-getpage) .<br/> |
| [**IXpsOMNameCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomnamecollection)<br/> | nessuno<br/>                             | Contiene un elenco di elementi della pagina che sono destinazioni di collegamento ipertestuale. L'elenco viene restituito dal metodo [**IXpsOMPageReference:: CollectLinkTargets**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-collectlinktargets) .<br/>                                                                                                                                                               |
| [**IXpsOMPartResources**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompartresources)<br/>   | nessuno<br/>                             | Contiene un elenco di risorse basate sulla parte associate alla pagina. Questo elenco viene restituito dal metodo [**IXpsOMPageReference:: CollectPartResources**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-collectpartresources) .<br/>                                                                                                                                     |



 

## <a name="code-examples"></a>Esempi di codice

Negli esempi di codice seguenti viene illustrato come utilizzare le interfacce di riferimento della pagina in un programma.

-   [Ottenere il contenuto della pagina](#get-the-page-contents)
-   [Ottiene l'elenco delle destinazioni dei collegamenti ipertestuali in questa pagina](#get-the-list-of-hyperlink-targets-on-this-page)
-   [Ottenere le risorse della parte associate a questa pagina](#get-the-part-resources-that-are-associated-with-this-page)

### <a name="get-the-page-contents"></a>Ottenere il contenuto della pagina

Nell'esempio di codice seguente viene ottenuto un puntatore all'interfaccia [**IXpsOMPage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage) che comprende il contenuto della pagina. Se la pagina non è stata caricata in XPS OM, come avviene quando il modello OM XPS viene inizializzato chiamando [**IXpsOMObjectFactory:: CreatePackageFromFile**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagefromfile), la chiamata a [**IXpsOMPageReference:: GetPage**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-getpage) CARICHERÀ la pagina in XPS om.


```C++
    {
    HRESULT        hr = S_OK;
    IXpsOMPage     *page = NULL;

    // pageRef contains the current page reference
    // and is passed in as a parameter

    // get the page content of this page reference
    hr = pageRef->GetPage (&page);
```



### <a name="get-the-list-of-hyperlink-targets-on-this-page"></a>Ottiene l'elenco delle destinazioni dei collegamenti ipertestuali in questa pagina

Nell'esempio di codice seguente viene ottenuto un puntatore all'interfaccia [**IXpsOMNameCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomnamecollection) che contiene l'elenco di elementi della pagina che sono destinazioni di collegamento ipertestuale. Se la pagina non è stata caricata in XPS OM, l'elenco di destinazioni dei collegamenti ipertestuali viene letto dal markup **PageContent. LinkTargets** . Se la pagina è stata caricata, [**CollectLinkTargets**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompagereference-collectlinktargets) controlla ogni elemento nella pagina e restituisce un elenco di elementi il cui attributo **IsHyperlinkTarget** è **true**.


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



### <a name="get-the-part-resources-that-are-associated-with-this-page"></a>Ottenere le risorse della parte associate a questa pagina

Nell'esempio di codice seguente vengono recuperati gli elenchi delle diverse risorse utilizzate da questa pagina.


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IXpsOMNameCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomnamecollection)
</dt> <dt>

[**IXpsOMPage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage)
</dt> <dt>

[**IXpsOMPageReference**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)
</dt> <dt>

[**IXpsOMPartResources**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompartresources)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 




