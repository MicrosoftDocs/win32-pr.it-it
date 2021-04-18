---
description: L'interfaccia IXpsOMPackageWriter crea un file di documento XPS in cui le applicazioni possono scrivere il contenuto delle interfacce IXpsOMPage di un OM XPS.
ms.assetid: eff1ab1e-2205-4f5c-9e32-199e073f5dbf
title: Uso dell'interfaccia IXpsOMPackageWriter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1e8a34a0538ff09cc050ac287d5314be93f0da8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317284"
---
# <a name="using-the-ixpsompackagewriter-interface"></a>Uso dell'interfaccia IXpsOMPackageWriter

L'interfaccia [**IXpsOMPackageWriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) crea un file di documento XPS in cui le applicazioni possono scrivere il contenuto delle interfacce [**IXPSOMPAGE**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage) di un OM XPS. L'interfaccia [**IXpsOMPackageWriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) è particolarmente utile quando il contenuto del documento viene elaborato o creato in modo sequenziale. A differenza dei metodi [**WriteToFile**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-writetofile) e [**WriteToStream**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-writetostream) dell'interfaccia [**IXpsOMPackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage) , per l'uso dell'interfaccia **IXpsOMPackageWriter** non è necessario che l'intero FixedDocument né il FixedDocumentSequence debbano essere completati.

## <a name="overview"></a>Panoramica

L'interfaccia [**IXpsOMPackageWriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) scrive una pagina alla volta, dalla prima pagina di un documento XPS fino all'ultima. L'interfaccia può essere utilizzata per creare semplici file di documento XPS e anche file di documenti XPS complessi che contengono più di un FixedDocument in FixedDocumentSequence. Nei file di documento XPS complessi, i FixedDocument vengono creati anche in sequenza, a partire dal primo FixedDocument in FixedDocumentSequence. L'interfaccia **IXpsOMPackageWriter** non supporta la creazione di contenuto del documento in ordine casuale. Usare, ad esempio, per creare un report sequenziale o per eseguire l'elaborazione in un filtro di driver di dispositivo in cui il contenuto del documento viene alimentato al driver in sequenza.

## <a name="terminology-review"></a>Revisione della terminologia

Un *file di documento XPS* è un pacchetto Open Packaging Conventions (OPC) che è conforme alla specifica del documento XML. Quindi, tecnicamente, l'interfaccia [**IXpsOMPackageWriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) crea un *pacchetto OPC*, ma è un pacchetto OPC che è conforme alla specifica del documento XML. Per questo motivo, nelle discussioni sui documenti XPS, i termini *documento* e *pacchetto* XPS vengono spesso usati in modo interscambiabile.

Il *pacchetto* creato dall'interfaccia [**IXpsOMPackageWriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) conterrà i componenti del documento XPS necessari, ovvero un elemento FixedDocumentSequence, almeno un FixedDocument e almeno un FixedPage. FixedDocumentSequence viene creato quando viene creata un'istanza dell'interfaccia **IXpsOMPackageWriter** . Un elemento FixedDocument viene creato ogni volta che viene chiamato [**IXpsOMPackageWriter:: StartNewDocument**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-startnewdocument) e viene creato un FixedPage ogni volta che viene chiamato [**IXpsOMPackageWriter:: AddPage**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-addpage) . Poiché l'interfaccia scrive il contenuto del documento in modo sequenziale, il metodo **AddPage** aggiunge la pagina all'oggetto FixedDocument creato più di recente.

## <a name="using-the-ixpsompackagewriter-interface"></a>Uso dell'interfaccia IXpsOMPackageWriter

Nella procedura riportata di seguito viene descritto come creare un file di documento XPS utilizzando l'interfaccia [**IXpsOMPackageWriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) . La procedura non descrive come creare un'istanza di un'interfaccia [**IXpsOMPage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage) e il relativo contenuto. Per ulteriori informazioni su **IXpsOMPage** e sull'aggiunta di contenuto a una pagina, vedere l'argomento relativo alle [interfacce di pagine XPS om](xps-object-model-page-interfaces.md) e gli argomenti elencati nella sezione vedere anche.

 **Creazione di un documento**

1.  Creare un'istanza di un'interfaccia [**IXpsOMPackageWriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) .

    Viene creato un FixedDocumentSequence vuoto nel pacchetto.

    -   Per creare un documento XPS in un file, chiamare [**IXpsOMObjectFactory:: CreatePackageWriterOnFile**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagewriteronfile).
    -   Per creare un documento XPS in un flusso, chiamare [**IXpsOMObjectFactory:: CreatePackageWriterOnStream**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagewriteronstream).

2.  Avviare un nuovo documento nel pacchetto chiamando [**IXpsOMPackageWriter:: StartNewDocument**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-startnewdocument).

    Prima di aggiungere una pagina, chiamare [**IXpsOMPackageWriter:: StartNewDocument**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-startnewdocument) per aggiungere un FixedDocument al FixedDocumentSequence creato nel passaggio 1.

3.  Aggiungere contenuto.
    -   Per aggiungere un nuovo elemento FixedPage al documento, chiamare [**IXpsOMPackageWriter:: AddPage**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-addpage), passandogli un puntatore all'interfaccia [**IXpsOMPage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage) che include il contenuto dell'elemento FixedPage che si desidera aggiungere.
    -   Per creare un nuovo FixedDocument in FixedDocumentSequence, chiamare [**IXpsOMPackageWriter:: StartNewDocument**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-startnewdocument).
4.  Chiudere il pacchetto e il relativo contenuto chiamando [**IXpsOMPackageWriter:: Close**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-close).

## <a name="advanced-features"></a>Funzionalità avanzate

I metodi dell'interfaccia [**IXpsOMPackageWriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) supportano anche l'aggiunta di risorse, anteprime e ticket di stampa. Questi componenti del documento possono essere aggiunti a livello di pacchetto, FixedDocumentSequence, FixedDocument e FixedPage. Per ulteriori informazioni sull'utilizzo di questa interfaccia per la stampa, vedere [Print an XPS om](print-an-xps-om.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso dell'API di firma digitale XPS](using-digital-signatures-in-xps-documents.md)
</dt> <dt>

[Interfacce di pagine XPS OM](xps-object-model-page-interfaces.md)
</dt> <dt>

[Esplorare XPS OM](navigate-the-xps-om.md)
</dt> <dt>

[Uso di Canvas e interfacce visive di XPS OM](working-with-xpsomcanvas-interfaces.md)
</dt> <dt>

[Utilizzo delle interfacce di percorso OM XPS](working-with-xps-object-model-path-interfaces.md)
</dt> <dt>

[Utilizzo di interfacce di testo, grafica e immagini XPS OM](working-with-xps-object-model-text-and-image-interfaces.md)
</dt> <dt>

[Interfacce del ticket di stampa XPS OM](xps-object-model-print-ticket-interfaces.md)
</dt> <dt>

[**IXpsOMThumbnailGenerator**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomthumbnailgenerator)
</dt> <dt>

[Informazioni di riferimento sulle API documento XPS](xps-programming-reference.md)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 



