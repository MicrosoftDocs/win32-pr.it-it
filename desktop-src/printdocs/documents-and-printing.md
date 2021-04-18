---
description: In questi argomenti vengono descritti i documenti e le funzionalità di stampa di Windows che consentono alle applicazioni di salvare, visualizzare e stampare.
ms.assetid: 20e56af6-9598-4d6a-a2bf-454cef8a3368
title: 'Documenti e stampa '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19b23ae7040586d550c47f3fedc59104d83fe818
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106320973"
---
# <a name="documents-and-printing"></a><span data-ttu-id="aa475-103">Documenti e stampa </span><span class="sxs-lookup"><span data-stu-id="aa475-103">Documents and Printing</span></span>

<span data-ttu-id="aa475-104">In questi argomenti vengono descritti i documenti e le funzionalità di stampa di Windows che consentono alle applicazioni di salvare, visualizzare e stampare.</span><span class="sxs-lookup"><span data-stu-id="aa475-104">These topics describe the documents and printing features of Windows that enable applications to save, view, and print.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="aa475-105">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="aa475-105">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="aa475-106">Argomento</span><span class="sxs-lookup"><span data-stu-id="aa475-106">Topic</span></span></th>
<th><span data-ttu-id="aa475-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="aa475-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="aa475-108"><a href="/windows/desktop/printdocs/what-s-new-for-printing-in-windows-vnext">Novità relative alla stampa</a></span><span class="sxs-lookup"><span data-stu-id="aa475-108"><a href="/windows/desktop/printdocs/what-s-new-for-printing-in-windows-vnext">What's New for Printing</a></span></span><br/></td>
<td><span data-ttu-id="aa475-109">Windows 8 supporta <a href="/previous-versions/windows/apps/hh465225(v=win.10)">la stampa per le app di Windows Store scritte in JavaScript e HTML</a> e <a href="/previous-versions/windows/apps/hh465196(v=win.10)">la stampa per le app di Windows Store con C#/VB/C + + e XAML</a>.</span><span class="sxs-lookup"><span data-stu-id="aa475-109">Windows 8 supports <a href="/previous-versions/windows/apps/hh465225(v=win.10)">printing for Windows Store apps using JavaScript and HTML</a> and <a href="/previous-versions/windows/apps/hh465196(v=win.10)">printing for Windows Store apps using C#/VB/C++ and XAML</a>.</span></span><br/> <span data-ttu-id="aa475-110">Windows 8 include anche una nuova API basata su COM che offre supporto completo per l'accesso XPS aperto e per l'accesso a parti dei nuovi driver della stampante supportati da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="aa475-110">Windows 8 also includes a new COM-based API that provides full support for Open XPS and access to portions of the new printer drivers that Windows 8 supports.</span></span> <span data-ttu-id="aa475-111">Per altre informazioni sulla nuova API, vedere <a href="/windows/desktop/printdocs/tailored-app-printing-api">Print Document Package API</a>.</span><span class="sxs-lookup"><span data-stu-id="aa475-111">For more information about the new API, see <a href="/windows/desktop/printdocs/tailored-app-printing-api">Print Document Package API</a>.</span></span><br/> <span data-ttu-id="aa475-112">Il programma Windows Print Driver Inbox garantisce che Windows 8 includa il supporto per un'alta percentuale delle stampanti più diffuse.</span><span class="sxs-lookup"><span data-stu-id="aa475-112">The Windows Print Driver Inbox Program makes sure that Windows 8 includes support for a high percentage of the popular printers.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa475-113"><a href="/windows/desktop/printdocs/jobbindalldocuments">Documenti XPS</a></span><span class="sxs-lookup"><span data-stu-id="aa475-113"><a href="/windows/desktop/printdocs/jobbindalldocuments">XPS Documents</a></span></span><br/></td>
<td><span data-ttu-id="aa475-114">Informazioni sulle firme digitali XPS per l'API documento XPS.</span><span class="sxs-lookup"><span data-stu-id="aa475-114">Information about the XPS Document API an XPS Digital Signatures.</span></span><br/>
<ul>
<li><span data-ttu-id="aa475-115"><a href="/previous-versions/windows/desktop/dd316976(v=vs.85)">API documenti XPS</a></span><span class="sxs-lookup"><span data-stu-id="aa475-115"><a href="/previous-versions/windows/desktop/dd316976(v=vs.85)">XPS Document API</a></span></span><br/> <span data-ttu-id="aa475-116">L'API documento XPS è un'API Windows nativa che supporta XPS OM.</span><span class="sxs-lookup"><span data-stu-id="aa475-116">The XPS Document API is a native Windows API that supports the XPS OM.</span></span> <span data-ttu-id="aa475-117">L'API documento XPS è stata introdotta in Windows 7 e può essere utilizzata nei programmi in modalità utente e nei driver della stampante XPSDrv.</span><span class="sxs-lookup"><span data-stu-id="aa475-117">The XPS Document API was introduced in Windows 7 and can be used in user-mode programs and XPSDrv printer drivers.</span></span><br/></li>
<li><span data-ttu-id="aa475-118"><a href="/previous-versions/windows/desktop/ff819108(v=vs.85)">API di firma digitale XPS</a></span><span class="sxs-lookup"><span data-stu-id="aa475-118"><a href="/previous-versions/windows/desktop/ff819108(v=vs.85)">XPS Digital Signature API</a></span></span><br/> <span data-ttu-id="aa475-119">Le firme digitali XPS consentono la firma dei documenti, la verifica dell'identità del firmatario e l'indicazione se un documento XPS è stato modificato dopo la firma.</span><span class="sxs-lookup"><span data-stu-id="aa475-119">XPS Digital Signatures enable document signing, verification of the signer's identity, and indication of whether an XPS document has changed since it was signed.</span></span><br/></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="aa475-120"><a href="printdocs-printing.md">Stampa</a></span><span class="sxs-lookup"><span data-stu-id="aa475-120"><a href="printdocs-printing.md">Printing</a></span></span><br/></td>
<td><span data-ttu-id="aa475-121">Informazioni sulle funzionalità di stampa supportate da Windows.</span><span class="sxs-lookup"><span data-stu-id="aa475-121">Information about the printing features supported by Windows.</span></span> <span data-ttu-id="aa475-122">Queste funzionalità includono:</span><span class="sxs-lookup"><span data-stu-id="aa475-122">These features include:</span></span><br/>
<ul>
<li><span data-ttu-id="aa475-123"><a href="/windows/desktop/printdocs/tailored-app-printing-api">API di stampa del pacchetto di documenti</a></span><span class="sxs-lookup"><span data-stu-id="aa475-123"><a href="/windows/desktop/printdocs/tailored-app-printing-api">Print Document Package API</a></span></span><br/> <span data-ttu-id="aa475-124">Fornisce app con un'interfaccia che consente la gestione del pacchetto <strong>PrintDocument</strong> .</span><span class="sxs-lookup"><span data-stu-id="aa475-124">Provides apps with an interface that allows the management of the <strong>PrintDocument</strong> package.</span></span><br/></li>
<li><span data-ttu-id="aa475-125"><a href="print-spooler-api.md">API spooler di stampa</a></span><span class="sxs-lookup"><span data-stu-id="aa475-125"><a href="print-spooler-api.md">Print Spooler API</a></span></span><br/> <span data-ttu-id="aa475-126">Fornisce un'interfaccia per lo spooler di stampa in modo che le applicazioni possano gestire stampanti e processi di stampa.</span><span class="sxs-lookup"><span data-stu-id="aa475-126">Provides an interface to the print spooler so that applications can manage printers and print jobs.</span></span><br/></li>
<li><span data-ttu-id="aa475-127"><a href="print-ticket-api.md">API Print Ticket</a></span><span class="sxs-lookup"><span data-stu-id="aa475-127"><a href="print-ticket-api.md">Print Ticket API</a></span></span><br/> <span data-ttu-id="aa475-128">Fornisce le applicazioni con funzioni per gestire e convertire i ticket di stampa.</span><span class="sxs-lookup"><span data-stu-id="aa475-128">Provides applications with functions to manage and convert print tickets.</span></span><br/></li>
<li><span data-ttu-id="aa475-129"><a href="gdi-printing.md">API di stampa GDI</a></span><span class="sxs-lookup"><span data-stu-id="aa475-129"><a href="gdi-printing.md">GDI Print API</a></span></span><br/> <span data-ttu-id="aa475-130">Fornisce le applicazioni con un'interfaccia di stampa indipendente dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="aa475-130">Provides applications with a device-independent printing interface.</span></span> <br/></li>
<li><p><span data-ttu-id="aa475-131"><a href="xps-printing.md">API di stampa XPS</a></span><span class="sxs-lookup"><span data-stu-id="aa475-131"><a href="xps-printing.md">XPS Print API</a></span></span><br/> <span data-ttu-id="aa475-132">Fornisce un'interfaccia allo spooler di stampa che le applicazioni possono utilizzare per inviare documenti XPS a una stampante.</span><span class="sxs-lookup"><span data-stu-id="aa475-132">Provides an interface to the print spooler that applications can use to send XPS documents to a printer.</span></span></p>
<blockquote>
[!Note]<br />
<span data-ttu-id="aa475-133">L'API di stampa XPS non è supportata e può essere modificata o non disponibile in futuro.</span><span class="sxs-lookup"><span data-stu-id="aa475-133">The XPS Print API is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="aa475-134">Le applicazioni client devono invece usare l' <a href="/windows/desktop/printdocs/tailored-app-printing-api">API del pacchetto di stampa del documento</a> .</span><span class="sxs-lookup"><span data-stu-id="aa475-134">Client applications should use the <a href="/windows/desktop/printdocs/tailored-app-printing-api">Print Document Package API</a> instead.</span></span>
</blockquote>
<p><br/> <br/></p></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="aa475-135"><a href="/windows/desktop/printdocs/printschema">Stampa schema</a></span><span class="sxs-lookup"><span data-stu-id="aa475-135"><a href="/windows/desktop/printdocs/printschema">Print Schema</a></span></span><br/></td>
<td><span data-ttu-id="aa475-136">Lo schema di stampa e le tecnologie correlate descrivono le funzionalità di una stampante e specificano le preferenze di stampa di un documento per le stampanti e la visualizzazione delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="aa475-136">The Print Schema and related technologies describe a printer's features and specify the printing preferences of a document to printers and viewing applications.</span></span> <span data-ttu-id="aa475-137">La <a href="https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip">specifica dello schema di stampa</a> è un documento scaricabile che contiene informazioni sullo schema di stampa e su come usarlo in documenti e stampa.</span><span class="sxs-lookup"><span data-stu-id="aa475-137">The <a href="https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip">Print Schema Specification</a> is a downloadable document that contains information about the Print Schema and how to use it in documents and printing.</span></span> <span data-ttu-id="aa475-138">Le informazioni online disponibili in questa sezione vengono fornite solo per le informazioni e potrebbero non riflettere accuratamente la versione corrente della specifica dello schema di <a href="https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip">stampa</a>.</span><span class="sxs-lookup"><span data-stu-id="aa475-138">The online information that is found in this section is provided for your information only and might not accurately reflect the current version of the <a href="https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip">Print Schema Specification</a>.</span></span><br/> <span data-ttu-id="aa475-139">Per informazioni sulla progettazione più aggiornate, vedere la <a href="https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip">specifica dello schema di stampa</a> .</span><span class="sxs-lookup"><span data-stu-id="aa475-139">Refer to the <a href="https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip">Print Schema Specification</a> for the most current design information.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="additional-resources"></a><span data-ttu-id="aa475-140">Risorse aggiuntive</span><span class="sxs-lookup"><span data-stu-id="aa475-140">Additional resources</span></span>

<span data-ttu-id="aa475-141">L' [app di esempio di stampa](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/Print%20sample%20(Windows%208)) di esempio illustra come stampare da un'app di Windows Store a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="aa475-141">The [Print Sample sample app](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/Print%20sample%20(Windows%208)) demonstrates how to print from a Windows Store app starting with Windows 8.</span></span>

<span data-ttu-id="aa475-142">Le funzionalità descritte in questa sezione sono destinate alla programmazione nativa di Windows.</span><span class="sxs-lookup"><span data-stu-id="aa475-142">The features described in this section are for native Windows programming.</span></span> <span data-ttu-id="aa475-143">Per usare funzionalità simili nella programmazione .NET (gestita), vedere [Windows Presentation Foundation Documents](/previous-versions/dotnet/netframework-3.0/ms749165(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="aa475-143">To use similar features in .NET (managed) programming, see [Windows Presentation Foundation Documents](/previous-versions/dotnet/netframework-3.0/ms749165(v=vs.85)).</span></span>

<span data-ttu-id="aa475-144">I documenti XPS sono basati sull'API per la creazione di [pacchetti](/previous-versions/windows/desktop/opc/packaging) .</span><span class="sxs-lookup"><span data-stu-id="aa475-144">XPS documents are built on the [Packaging](/previous-versions/windows/desktop/opc/packaging) API.</span></span> <span data-ttu-id="aa475-145">Vedere l'API per la creazione di pacchetti, per un accesso di livello inferiore al contenuto di un documento XPS.</span><span class="sxs-lookup"><span data-stu-id="aa475-145">See the Packaging API, for lower level access to the contents of an XPS document.</span></span>

## <a name="related-topics"></a><span data-ttu-id="aa475-146">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="aa475-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aa475-147">Comunicazione bidirezionale stampanti (hardware Dev Center)</span><span class="sxs-lookup"><span data-stu-id="aa475-147">Bidirectional printer communications (Hardware Dev Center)</span></span>](/windows-hardware/drivers/print/bidirectional-communication)
</dt> </dl>
