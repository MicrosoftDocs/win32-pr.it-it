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
# <a name="app-support-for-openxps-printing"></a><span data-ttu-id="63616-103">Supporto delle app per la stampa OpenXPS</span><span class="sxs-lookup"><span data-stu-id="63616-103">App Support for OpenXPS Printing</span></span>

<span data-ttu-id="63616-104">OpenXPS è il formato Open XML Paper Specification per i documenti ed è basato sulla specifica standard ECMA (European Computer Manufacturers Association).</span><span class="sxs-lookup"><span data-stu-id="63616-104">OpenXPS is the Open XML Paper Specification format for documents, and it’s based on the European Computer Manufacturers Association (ECMA) standard specification.</span></span>

<span data-ttu-id="63616-105">Windows 8 fornisce supporto completo per la stampa OpenXPS tramite il modello di driver di stampa v4, affiancato con supporto continuo per il formato Microsoft XPS.</span><span class="sxs-lookup"><span data-stu-id="63616-105">Windows 8 provides full support for OpenXPS printing via the v4 print driver model, side-by-side with continued support for the Microsoft XPS format.</span></span> <span data-ttu-id="63616-106">Questo argomento è incentrato sulla parte di questo supporto rilevante per gli sviluppatori di applicazioni Windows.</span><span class="sxs-lookup"><span data-stu-id="63616-106">And this topic focuses on the portion of this support that is relevant to Windows application developers.</span></span> <span data-ttu-id="63616-107">Per informazioni sui requisiti dei driver per il supporto di OpenXPS, vedere [supporto driver per OpenXPS](/windows-hardware/drivers/print/printer-driver-overview).</span><span class="sxs-lookup"><span data-stu-id="63616-107">For information about driver requirements for OpenXPS support, see [Driver Support for OpenXPS](/windows-hardware/drivers/print/printer-driver-overview).</span></span>

## <a name="sending-xps-data-to-the-print-system"></a><span data-ttu-id="63616-108">Invio di dati XPS al sistema di stampa</span><span class="sxs-lookup"><span data-stu-id="63616-108">Sending XPS data to the Print System</span></span>

<span data-ttu-id="63616-109">Si consiglia di utilizzare [**IPrintDocumentPackageTarget**](/windows/win32/api/documenttarget/nn-documenttarget-iprintdocumentpackagetarget) per l'invio di tutti i processi di stampa XPS al sistema di stampa.</span><span class="sxs-lookup"><span data-stu-id="63616-109">We recommend that you use [**IPrintDocumentPackageTarget**](/windows/win32/api/documenttarget/nn-documenttarget-iprintdocumentpackagetarget) for sending all XPS print jobs to the print system.</span></span> <span data-ttu-id="63616-110">**IPrintDocumentPackageTarget** accetta il modello a oggetti XPS (OM) senza serializzazione e consente di migliorare le prestazioni complessive.</span><span class="sxs-lookup"><span data-stu-id="63616-110">**IPrintDocumentPackageTarget** accepts the XPS object model (OM) without serialization, and that helps to improve the overall performance.</span></span>

<span data-ttu-id="63616-111">Ecco un breve riepilogo dell'interfaccia **IPrintDocumentPackageTarget** :</span><span class="sxs-lookup"><span data-stu-id="63616-111">Here's a brief summary of the **IPrintDocumentPackageTarget** interface:</span></span>

-   <span data-ttu-id="63616-112">Questa interfaccia supporta la stampa da soluzioni personalizzate e da applicazioni desktop.</span><span class="sxs-lookup"><span data-stu-id="63616-112">This interface supports printing from tailored solutions as well as desktop applications.</span></span>

-   <span data-ttu-id="63616-113">Per le app desktop, questo può essere usato al posto di [**StartXpsPrintJob1**](/windows/win32/api/xpsprint/nf-xpsprint-startxpsprintjob1).</span><span class="sxs-lookup"><span data-stu-id="63616-113">For desktops apps, this can be used in place of [**StartXpsPrintJob1**](/windows/win32/api/xpsprint/nf-xpsprint-startxpsprintjob1).</span></span>

-   <span data-ttu-id="63616-114">Disponibile in Windows 7 con Service Pack 1 (SP1) + aggiornamento della piattaforma e Windows 8.</span><span class="sxs-lookup"><span data-stu-id="63616-114">Available on Windows 7 with Service Pack 1 (SP1) + Platform Update, and Windows 8.</span></span>

-   <span data-ttu-id="63616-115">Includere *DocumentTarget. h* nei progetti per usare queste API.</span><span class="sxs-lookup"><span data-stu-id="63616-115">Include *DocumentTarget.h* in projects to use these APIs.</span></span>

<span data-ttu-id="63616-116">Le applicazioni che utilizzano documenti OpenXPS devono tenere presente che il tipo MIME per OpenXPS è il seguente:</span><span class="sxs-lookup"><span data-stu-id="63616-116">Applications that consume OpenXPS documents should note that the MIME type for OpenXPS is as follows:</span></span>

<dl> <span data-ttu-id="63616-117">\\oxps applicazione</span><span class="sxs-lookup"><span data-stu-id="63616-117">application\\oxps</span></span>  
</dl>

## <a name="sending-openxps-data-to-the-xps-print-api"></a><span data-ttu-id="63616-118">Invio di dati OpenXPS all'API di stampa XPS</span><span class="sxs-lookup"><span data-stu-id="63616-118">Sending OpenXPS data to the XPS Print API</span></span>

<span data-ttu-id="63616-119">Specifico di OpenXPS, XPS OM accetta sia MSXPS che OpenXPS e fornisce metodi per la conversione e la serializzazione in uno dei due formati.</span><span class="sxs-lookup"><span data-stu-id="63616-119">Specific to OpenXPS, XPS OM accepts both MSXPS and OpenXPS, and provides methods for conversion and serialization to either format.</span></span> <span data-ttu-id="63616-120">Ciò consente agli sviluppatori di applicazioni di essere indipendenti dal driver di destinazione, se necessario.</span><span class="sxs-lookup"><span data-stu-id="63616-120">This allows application developers to be agnostic of the target driver, if they want.</span></span> <span data-ttu-id="63616-121">Ciò significa anche che gli sviluppatori di app possono sempre inviare processi di stampa come XPS OM a StartXpsPrintJob1 o IDocumentPackageTarget, sapendo che il sistema di stampa gestirà qualsiasi conversione necessaria.</span><span class="sxs-lookup"><span data-stu-id="63616-121">This also means that app developers can always submit print jobs as XPS OM to either StartXpsPrintJob1 or IDocumentPackageTarget, knowing that the print system will handle any necessary conversion.</span></span>

<span data-ttu-id="63616-122">Naturalmente, impedire la conversione tra i formati XPS consente di migliorare le prestazioni end-to-end.</span><span class="sxs-lookup"><span data-stu-id="63616-122">Of course, preventing conversion between XPS formats will improve end-to-end performance.</span></span> <span data-ttu-id="63616-123">Dall'applicazione, lo sviluppatore può controllare la seguente chiave del registro di sistema per determinare il formato XPS preferito del driver di stampa di destinazione:</span><span class="sxs-lookup"><span data-stu-id="63616-123">From the application, the developer can check the following registry key to determine the preferred XPS format of the targeted print driver:</span></span>

``` syntax
HKLM\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Print\Printers\[PrintDriverName]\PrintDriverData\XpsFormat
```

<span data-ttu-id="63616-124">Una volta determinato il formato XPS preferito, l'applicazione può fornire oggetti XPS OM che non richiedono la conversione.</span><span class="sxs-lookup"><span data-stu-id="63616-124">Once the preferred XPS format has been determined, the application can provide XPS OM objects that will not require conversion.</span></span> <span data-ttu-id="63616-125">In particolare, si noti che l'uso della foto HD in MSXPS e JPEGXR in OpenXPS.</span><span class="sxs-lookup"><span data-stu-id="63616-125">Of particular note is the use of HD Photo in MSXPS and JPEGXR in OpenXPS.</span></span> <span data-ttu-id="63616-126">La conversione da JPEGXR a Photo HD è relativamente leggera perché la differenza principale in questa conversione è che la foto HD ignora 4 bit di controllo richiesti da JPEGXR.</span><span class="sxs-lookup"><span data-stu-id="63616-126">Converting from JPEGXR to HD Photo is relatively lightweight since the primary difference in this conversion is that HD Photo ignores 4 control bits that JPEGXR requires.</span></span> <span data-ttu-id="63616-127">Tuttavia, per la conversione da HD Photo a JPEGXR è necessario ricodificare l'intera immagine per generare i bit di controllo richiesti.</span><span class="sxs-lookup"><span data-stu-id="63616-127">However, converting from HD Photo to JPEGXR requires the entire image to be re-encoded in order to generate the required control bits.</span></span> <span data-ttu-id="63616-128">Pertanto, fornire immagini JPEGXR per le immagini ad alta risoluzione garantirà la compatibilità con OpenXPS e ridurrà al minimo il costo di conversione dell'immagine per MSXPS.</span><span class="sxs-lookup"><span data-stu-id="63616-128">Thus, providing JPEGXR images for high-resolution images will ensure compatibility with OpenXPS and minimize the conversion cost of the image for MSXPS.</span></span>

<span data-ttu-id="63616-129">L'intestazione *Xpsobjectmodel \_ 1. h* definisce gli oggetti e le API aggiuntivi per OpenXPS.</span><span class="sxs-lookup"><span data-stu-id="63616-129">The *Xpsobjectmodel\_1.h* header defines the additional APIs and objects for OpenXPS.</span></span> <span data-ttu-id="63616-130">E l'interfaccia IXpsOMObjectFactory1 fornisce metodi aggiuntivi per la conversione delle immagini.</span><span class="sxs-lookup"><span data-stu-id="63616-130">And the IXpsOMObjectFactory1 interface provides additional methods for image conversion.</span></span> <span data-ttu-id="63616-131">Ecco la sintassi:</span><span class="sxs-lookup"><span data-stu-id="63616-131">Here's the syntax:</span></span>


```C++
IXpsOMObjectFactory1->ConvertHDPhotoToJpegXR(IXpsOMImageResource *imageResource);

IXpsOMObjectFactory1->ConvertJpegXRToHDPhoto(IXpsOMImageResource *imageResource);
```



<span data-ttu-id="63616-132">Windows 8 fornisce le seguenti enumerazioni nuove e aggiornate.</span><span class="sxs-lookup"><span data-stu-id="63616-132">Windows 8 provides the following new and updated enumerations.</span></span>

<span data-ttu-id="63616-133">Nuova enumerazione:</span><span class="sxs-lookup"><span data-stu-id="63616-133">New enumeration:</span></span>

<dl>

[<span data-ttu-id="63616-134">**\_tipo di documento XPS \_**</span><span class="sxs-lookup"><span data-stu-id="63616-134">**XPS\_DOCUMENT\_TYPE**</span></span>](/windows/win32/api/xpsobjectmodel_1/ne-xpsobjectmodel_1-xps_document_type)  
</dl>

<span data-ttu-id="63616-135">Enumerazione aggiornata</span><span class="sxs-lookup"><span data-stu-id="63616-135">Updated enumeration</span></span>

<dl>

[<span data-ttu-id="63616-136">**\_tipo di immagine XPS \_**</span><span class="sxs-lookup"><span data-stu-id="63616-136">**XPS\_IMAGE\_TYPE**</span></span>](/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_image_type)  
</dl>

<span data-ttu-id="63616-137">I nuovi metodi GetDocumentType consentono a un'applicazione di determinare il formato XPS dei documenti.</span><span class="sxs-lookup"><span data-stu-id="63616-137">The new GetDocumentType methods allow an application to determine the XPS format of documents.</span></span> <span data-ttu-id="63616-138">Sono disponibili in [**IXpsOMObjectFactory1**](/windows/desktop/api/XpsObjectModel_1/nn-xpsobjectmodel_1-ixpsomobjectfactory1), [**IXpsOMPackage1**](/windows/desktop/api/XpsObjectModel_1/nn-xpsobjectmodel_1-ixpsompackage1)e [**IXpsOMPage1**](/windows/desktop/api/XpsObjectModel_1/nn-xpsobjectmodel_1-ixpsompage1).</span><span class="sxs-lookup"><span data-stu-id="63616-138">These are available in [**IXpsOMObjectFactory1**](/windows/desktop/api/XpsObjectModel_1/nn-xpsobjectmodel_1-ixpsomobjectfactory1), [**IXpsOMPackage1**](/windows/desktop/api/XpsObjectModel_1/nn-xpsobjectmodel_1-ixpsompackage1), and [**IXpsOMPage1**](/windows/desktop/api/XpsObjectModel_1/nn-xpsobjectmodel_1-ixpsompage1).</span></span> <span data-ttu-id="63616-139">Ecco un elenco dei metodi.</span><span class="sxs-lookup"><span data-stu-id="63616-139">Here's a list of the methods.</span></span>

<dl>

[<span data-ttu-id="63616-140">**IXpsOMObjectFactory1::GetDocumentTypeFromFile**</span><span class="sxs-lookup"><span data-stu-id="63616-140">**IXpsOMObjectFactory1::GetDocumentTypeFromFile**</span></span>](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsomobjectfactory1-getdocumenttypefromfile)  
[<span data-ttu-id="63616-141">**IXpsOMObjectFactory1::GetDocumentTypeFromStream**</span><span class="sxs-lookup"><span data-stu-id="63616-141">**IXpsOMObjectFactory1::GetDocumentTypeFromStream**</span></span>](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsomobjectfactory1-getdocumenttypefromstream)  
[<span data-ttu-id="63616-142">**IXpsOMPackage1:: GetDocumentType**</span><span class="sxs-lookup"><span data-stu-id="63616-142">**IXpsOMPackage1::GetDocumentType**</span></span>](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsompackage1-getdocumenttype)  
[<span data-ttu-id="63616-143">**IXpsOMPage1:: GetDocumentType**</span><span class="sxs-lookup"><span data-stu-id="63616-143">**IXpsOMPage1::GetDocumentType**</span></span>](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsompage1-getdocumenttype)  
</dl>

<span data-ttu-id="63616-144">Windows 8 fornisce i nuovi codici di errore seguenti per il supporto di OpenXPS:</span><span class="sxs-lookup"><span data-stu-id="63616-144">Windows 8 provides the following new error codes in support of OpenXPS:</span></span>

<dl> <span data-ttu-id="63616-145">\_ \_ spazio dei nomi XPS E non corrispondente \_ .</span><span class="sxs-lookup"><span data-stu-id="63616-145">XPS\_E\_MISMATCHED\_NAMESPACE.</span></span> <dl> <span data-ttu-id="63616-146">Questo errore viene restituito se è presente uno spazio dei nomi non corrispondente.</span><span class="sxs-lookup"><span data-stu-id="63616-146">This error is returned, if there is a mismatched namespace.</span></span>  
</dl> </dd> XPS\_E\_ABSOLUTE\_REFERENCE. <dl> <span data-ttu-id="63616-147">Questo errore viene restituito se MSXPS utilizza URI assoluti nei riferimenti interni oppure tenta di utilizzare riferimenti interni per la serializzazione nel flusso.</span><span class="sxs-lookup"><span data-stu-id="63616-147">This error is returned if MSXPS uses absolute URIs in internal references, or attempts to use internal references to serialize in the stream.</span></span> <span data-ttu-id="63616-148">Questo perché XPS OM genera gli URI relativi.</span><span class="sxs-lookup"><span data-stu-id="63616-148">That is because XPS OM generates relative URIs.</span></span> <span data-ttu-id="63616-149">Sebbene MSXPS supporti gli URI sia relativi che assoluti, OpenXPS richiede URI relativi.</span><span class="sxs-lookup"><span data-stu-id="63616-149">And although MSXPS supports both relative and absolute URIs, OpenXPS requires relative URIs.</span></span>  
</dl> </dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="63616-150">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="63616-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="63616-151">Supporto dei driver per OpenXPS</span><span class="sxs-lookup"><span data-stu-id="63616-151">Driver Support for OpenXPS</span></span>](/windows-hardware/drivers/print/printer-driver-overview)
</dt> <dt>

[<span data-ttu-id="63616-152">**IPrintDocumentPackageTarget**</span><span class="sxs-lookup"><span data-stu-id="63616-152">**IPrintDocumentPackageTarget**</span></span>](/windows/win32/api/documenttarget/nn-documenttarget-iprintdocumentpackagetarget)
</dt> <dt>

[<span data-ttu-id="63616-153">**IXpsOMObjectFactory1::GetDocumentTypeFromFile**</span><span class="sxs-lookup"><span data-stu-id="63616-153">**IXpsOMObjectFactory1::GetDocumentTypeFromFile**</span></span>](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsomobjectfactory1-getdocumenttypefromfile)
</dt> <dt>

[<span data-ttu-id="63616-154">**IXpsOMObjectFactory1::GetDocumentTypeFromStream**</span><span class="sxs-lookup"><span data-stu-id="63616-154">**IXpsOMObjectFactory1::GetDocumentTypeFromStream**</span></span>](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsomobjectfactory1-getdocumenttypefromstream)
</dt> <dt>

[<span data-ttu-id="63616-155">**IXpsOMPackage1:: GetDocumentType**</span><span class="sxs-lookup"><span data-stu-id="63616-155">**IXpsOMPackage1::GetDocumentType**</span></span>](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsompackage1-getdocumenttype)
</dt> <dt>

[<span data-ttu-id="63616-156">**IXpsOMPage1:: GetDocumentType**</span><span class="sxs-lookup"><span data-stu-id="63616-156">**IXpsOMPage1::GetDocumentType**</span></span>](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsompage1-getdocumenttype)
</dt> <dt>

[<span data-ttu-id="63616-157">**\_tipo di documento XPS \_**</span><span class="sxs-lookup"><span data-stu-id="63616-157">**XPS\_DOCUMENT\_TYPE**</span></span>](/windows/win32/api/xpsobjectmodel_1/ne-xpsobjectmodel_1-xps_document_type)
</dt> <dt>

[<span data-ttu-id="63616-158">**\_tipo di immagine XPS \_**</span><span class="sxs-lookup"><span data-stu-id="63616-158">**XPS\_IMAGE\_TYPE**</span></span>](/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_image_type)
</dt> </dl>

 

 
