---
description: OpenXPS è il formato Open XML Paper Specification per i documenti ed è basato sulla specifica standard ECMA (European Carton Maker Association).
ms.assetid: 52FB5B3F-BEBF-4851-8BE9-5DC7AE535313
title: Supporto delle app per la stampa OpenXPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 914d8c365209ea3486bedd5e0352e63a8e31086f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311562"
---
# <a name="app-support-for-openxps-printing"></a>Supporto delle app per la stampa OpenXPS

OpenXPS è il formato Open XML Paper Specification per i documenti ed è basato sulla specifica standard ECMA (European Computer Manufacturers Association).

Windows 8 fornisce supporto completo per la stampa OpenXPS tramite il modello di driver di stampa v4, affiancato con supporto continuo per il formato Microsoft XPS. Questo argomento è incentrato sulla parte di questo supporto rilevante per gli sviluppatori di applicazioni Windows. Per informazioni sui requisiti dei driver per il supporto di OpenXPS, vedere [supporto driver per OpenXPS](/windows-hardware/drivers/print/printer-driver-overview).

## <a name="sending-xps-data-to-the-print-system"></a>Invio di dati XPS al sistema di stampa

Si consiglia di utilizzare [**IPrintDocumentPackageTarget**](/windows/win32/api/documenttarget/nn-documenttarget-iprintdocumentpackagetarget) per l'invio di tutti i processi di stampa XPS al sistema di stampa. **IPrintDocumentPackageTarget** accetta il modello a oggetti XPS (OM) senza serializzazione e consente di migliorare le prestazioni complessive.

Ecco un breve riepilogo dell'interfaccia **IPrintDocumentPackageTarget** :

-   Questa interfaccia supporta la stampa da soluzioni personalizzate e da applicazioni desktop.

-   Per le app desktop, questo può essere usato al posto di [**StartXpsPrintJob1**](/windows/win32/api/xpsprint/nf-xpsprint-startxpsprintjob1).

-   Disponibile in Windows 7 con Service Pack 1 (SP1) + aggiornamento della piattaforma e Windows 8.

-   Includere *DocumentTarget. h* nei progetti per usare queste API.

Le applicazioni che utilizzano documenti OpenXPS devono tenere presente che il tipo MIME per OpenXPS è il seguente:

<dl> \\oxps applicazione  
</dl>

## <a name="sending-openxps-data-to-the-xps-print-api"></a>Invio di dati OpenXPS all'API di stampa XPS

Specifico di OpenXPS, XPS OM accetta sia MSXPS che OpenXPS e fornisce metodi per la conversione e la serializzazione in uno dei due formati. Ciò consente agli sviluppatori di applicazioni di essere indipendenti dal driver di destinazione, se necessario. Ciò significa anche che gli sviluppatori di app possono sempre inviare processi di stampa come XPS OM a StartXpsPrintJob1 o IDocumentPackageTarget, sapendo che il sistema di stampa gestirà qualsiasi conversione necessaria.

Naturalmente, impedire la conversione tra i formati XPS consente di migliorare le prestazioni end-to-end. Dall'applicazione, lo sviluppatore può controllare la seguente chiave del registro di sistema per determinare il formato XPS preferito del driver di stampa di destinazione:

``` syntax
HKLM\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Print\Printers\[PrintDriverName]\PrintDriverData\XpsFormat
```

Una volta determinato il formato XPS preferito, l'applicazione può fornire oggetti XPS OM che non richiedono la conversione. In particolare, si noti che l'uso della foto HD in MSXPS e JPEGXR in OpenXPS. La conversione da JPEGXR a Photo HD è relativamente leggera perché la differenza principale in questa conversione è che la foto HD ignora 4 bit di controllo richiesti da JPEGXR. Tuttavia, per la conversione da HD Photo a JPEGXR è necessario ricodificare l'intera immagine per generare i bit di controllo richiesti. Pertanto, fornire immagini JPEGXR per le immagini ad alta risoluzione garantirà la compatibilità con OpenXPS e ridurrà al minimo il costo di conversione dell'immagine per MSXPS.

L'intestazione *Xpsobjectmodel \_ 1. h* definisce gli oggetti e le API aggiuntivi per OpenXPS. E l'interfaccia IXpsOMObjectFactory1 fornisce metodi aggiuntivi per la conversione delle immagini. Ecco la sintassi:


```C++
IXpsOMObjectFactory1->ConvertHDPhotoToJpegXR(IXpsOMImageResource *imageResource);

IXpsOMObjectFactory1->ConvertJpegXRToHDPhoto(IXpsOMImageResource *imageResource);
```



Windows 8 fornisce le seguenti enumerazioni nuove e aggiornate.

Nuova enumerazione:

<dl>

[**\_tipo di documento XPS \_**](/windows/win32/api/xpsobjectmodel_1/ne-xpsobjectmodel_1-xps_document_type)  
</dl>

Enumerazione aggiornata

<dl>

[**\_tipo di immagine XPS \_**](/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_image_type)  
</dl>

I nuovi metodi GetDocumentType consentono a un'applicazione di determinare il formato XPS dei documenti. Sono disponibili in [**IXpsOMObjectFactory1**](/windows/desktop/api/XpsObjectModel_1/nn-xpsobjectmodel_1-ixpsomobjectfactory1), [**IXpsOMPackage1**](/windows/desktop/api/XpsObjectModel_1/nn-xpsobjectmodel_1-ixpsompackage1)e [**IXpsOMPage1**](/windows/desktop/api/XpsObjectModel_1/nn-xpsobjectmodel_1-ixpsompage1). Ecco un elenco dei metodi.

<dl>

[**IXpsOMObjectFactory1::GetDocumentTypeFromFile**](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsomobjectfactory1-getdocumenttypefromfile)  
[**IXpsOMObjectFactory1::GetDocumentTypeFromStream**](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsomobjectfactory1-getdocumenttypefromstream)  
[**IXpsOMPackage1:: GetDocumentType**](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsompackage1-getdocumenttype)  
[**IXpsOMPage1:: GetDocumentType**](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsompage1-getdocumenttype)  
</dl>

Windows 8 fornisce i nuovi codici di errore seguenti per il supporto di OpenXPS:

<dl> \_ \_ spazio dei nomi XPS E non corrispondente \_ . <dl> Questo errore viene restituito se è presente uno spazio dei nomi non corrispondente.  
</dl> </dd> XPS\_E\_ABSOLUTE\_REFERENCE. <dl> Questo errore viene restituito se MSXPS utilizza URI assoluti nei riferimenti interni oppure tenta di utilizzare riferimenti interni per la serializzazione nel flusso. Questo perché XPS OM genera gli URI relativi. Sebbene MSXPS supporti gli URI sia relativi che assoluti, OpenXPS richiede URI relativi.  
</dl> </dd> </dl>

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Supporto dei driver per OpenXPS](/windows-hardware/drivers/print/printer-driver-overview)
</dt> <dt>

[**IPrintDocumentPackageTarget**](/windows/win32/api/documenttarget/nn-documenttarget-iprintdocumentpackagetarget)
</dt> <dt>

[**IXpsOMObjectFactory1::GetDocumentTypeFromFile**](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsomobjectfactory1-getdocumenttypefromfile)
</dt> <dt>

[**IXpsOMObjectFactory1::GetDocumentTypeFromStream**](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsomobjectfactory1-getdocumenttypefromstream)
</dt> <dt>

[**IXpsOMPackage1:: GetDocumentType**](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsompackage1-getdocumenttype)
</dt> <dt>

[**IXpsOMPage1:: GetDocumentType**](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsompage1-getdocumenttype)
</dt> <dt>

[**\_tipo di documento XPS \_**](/windows/win32/api/xpsobjectmodel_1/ne-xpsobjectmodel_1-xps_document_type)
</dt> <dt>

[**\_tipo di immagine XPS \_**](/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_image_type)
</dt> </dl>

 

 
