---
description: L'interfaccia IXpsOMPackageWriter crea un file di documento XPS in cui le applicazioni possono scrivere il contenuto delle interfacce IXpsOMPage di un sistema operativo XPS.
ms.assetid: eff1ab1e-2205-4f5c-9e32-199e073f5dbf
title: Uso dell'interfaccia IXpsOMPackageWriter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65a4437f939821b826fa0d5c30407777b7d44c5d03c236f4ef850d52145b4f8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119098703"
---
# <a name="using-the-ixpsompackagewriter-interface"></a>Uso dell'interfaccia IXpsOMPackageWriter

[**L'interfaccia IXpsOMPackageWriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) crea un file di documento XPS in cui le applicazioni possono scrivere il contenuto delle [**interfacce IXpsOMPage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage) di un sistema operativo XPS. [**L'interfaccia IXpsOMPackageWriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) è particolarmente utile quando il contenuto del documento viene elaborato o creato in sequenza. A differenza dei metodi [**WriteToFile**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-writetofile) e [**WriteToStream**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-writetostream) dell'interfaccia [**IXpsOMPackage,**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage) per l'interfaccia **IXpsOMPackageWriter** non è necessario completare né l'intero FixedDocument né FixedDocumentSequence.

## <a name="overview"></a>Panoramica

[**L'interfaccia IXpsOMPackageWriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) scrive una pagina alla volta, dalla prima pagina di un documento XPS all'ultima. L'interfaccia può essere usata per creare semplici file di documento XPS e anche file di documenti XPS complessi che contengono più di un FixedDocument in FixedDocumentSequence. Nei file di documento XPS complessi, vengono creati in sequenza anche fixedDocuments, a partire dal primo FixedDocument in FixedDocumentSequence. **L'interfaccia IXpsOMPackageWriter** non supporta la creazione del contenuto del documento in ordine casuale. Usarlo, ad esempio, per creare un report sequenziale o per eseguire l'elaborazione in un filtro del driver di dispositivo in cui il contenuto del documento viene alimentato al driver in sequenza.

## <a name="terminology-review"></a>Revisione della terminologia

Un *file di documento XPS* è un pacchetto Open Packaging Conventions (OPC) conforme alla XML Paper Specification. Tecnicamente, quindi, [**l'interfaccia IXpsOMPackageWriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) crea un pacchetto *OPC,* ma è un pacchetto OPC conforme alla XML Paper Specification. Per questo motivo, nelle discussioni sui documenti XPS, i termini documento e *pacchetto* *XPS* vengono spesso usati in modo intercambiabile.

Il *pacchetto* creato dall'interfaccia [**IXpsOMPackageWriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) conterrà i componenti del documento XPS necessari: FixedDocumentSequence, almeno un FixedDocument e almeno un fixedPage. FixedDocumentSequence viene creato quando viene creata **un'istanza dell'interfaccia IXpsOMPackageWriter.** Viene creato un oggetto FixedDocument ogni volta che viene chiamato [**IXpsOMPackageWriter::StartNewDocument**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-startnewdocument) e viene creato un oggetto FixedPage ogni volta che viene chiamato [**IXpsOMPackageWriter::AddPage.**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-addpage) Poiché l'interfaccia scrive il contenuto del documento in sequenza, il **metodo AddPage** aggiunge la pagina all'oggetto FixedDocument creato più di recente.

## <a name="using-the-ixpsompackagewriter-interface"></a>Uso dell'interfaccia IXpsOMPackageWriter

La procedura seguente descrive come creare un file di documento XPS usando [**l'interfaccia IXpsOMPackageWriter.**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) La procedura non descrive come creare un'istanza di [**un'interfaccia IXpsOMPage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage) e il relativo contenuto. Per altre informazioni **su IXpsOMPage** e sull'aggiunta di contenuto a una pagina, vedere [XpS OM Page Interfaces](xps-object-model-page-interfaces.md) e gli argomenti elencati nella sezione Vedere anche.

 **Creazione di un documento**

1.  Creare [**un'istanza di un'interfaccia IXpsOMPackageWriter.**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter)

    Verrà creato un oggetto FixedDocumentSequence vuoto nel pacchetto.

    -   Per creare un documento XPS in un file, chiamare [**IXpsOMObjectFactory::CreatePackageWriterOnFile**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagewriteronfile).
    -   Per creare un documento XPS in un flusso, chiamare [**IXpsOMObjectFactory::CreatePackageWriterOnStream**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagewriteronstream).

2.  Avviare un nuovo documento nel pacchetto chiamando [**IXpsOMPackageWriter::StartNewDocument**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-startnewdocument).

    Prima di aggiungere una pagina, chiamare [**IXpsOMPackageWriter::StartNewDocument**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-startnewdocument) per aggiungere un FixedDocument a FixedDocumentSequence creato nel passaggio 1.

3.  Aggiungere contenuto.
    -   Per aggiungere un nuovo oggetto FixedPage al documento, chiamare [**IXpsOMPackageWriter::AddPage**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-addpage), passando un puntatore all'interfaccia [**IXpsOMPage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage) con il contenuto dell'oggetto FixedPage da aggiungere.
    -   Per creare un nuovo FixedDocument in FixedDocumentSequence, chiamare [**IXpsOMPackageWriter::StartNewDocument**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-startnewdocument).
4.  Chiudere il pacchetto e il relativo contenuto chiamando [**IXpsOMPackageWriter::Close**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-close).

## <a name="advanced-features"></a>Funzionalità avanzate

I metodi [**dell'interfaccia IXpsOMPackageWriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) supportano anche l'aggiunta di risorse, anteprime e ticket di stampa. Questi componenti del documento possono essere aggiunti a livello di pacchetto, FixedDocumentSequence, FixedDocument e FixedPage. Per altre informazioni sull'uso di questa interfaccia per la stampa, vedere [Stampare un sistema operativo XPS.](print-an-xps-om.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso dell'API di firma digitale XPS](using-digital-signatures-in-xps-documents.md)
</dt> <dt>

[Interfacce di pagina OM XPS](xps-object-model-page-interfaces.md)
</dt> <dt>

[Esplorare il sistema operativo XPS](navigate-the-xps-om.md)
</dt> <dt>

[Uso delle interfacce canvas e visive di XPS OM](working-with-xpsomcanvas-interfaces.md)
</dt> <dt>

[Uso delle interfacce di percorso OM XPS](working-with-xps-object-model-path-interfaces.md)
</dt> <dt>

[Uso delle interfacce di testo, grafica e immagine di XPS OM](working-with-xps-object-model-text-and-image-interfaces.md)
</dt> <dt>

[Interfacce dei ticket di stampa OM XPS](xps-object-model-print-ticket-interfaces.md)
</dt> <dt>

[**IXpsOMThumbnailGenerator**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomthumbnailgenerator)
</dt> <dt>

[Informazioni di riferimento sulle API dei documenti XPS](xps-programming-reference.md)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 



