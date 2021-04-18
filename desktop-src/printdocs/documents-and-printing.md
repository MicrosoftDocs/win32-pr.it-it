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
# <a name="documents-and-printing"></a>Documenti e stampa 

In questi argomenti vengono descritti i documenti e le funzionalità di stampa di Windows che consentono alle applicazioni di salvare, visualizzare e stampare.

## <a name="in-this-section"></a>Contenuto della sezione



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Argomento</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/printdocs/what-s-new-for-printing-in-windows-vnext">Novità relative alla stampa</a><br/></td>
<td>Windows 8 supporta <a href="/previous-versions/windows/apps/hh465225(v=win.10)">la stampa per le app di Windows Store scritte in JavaScript e HTML</a> e <a href="/previous-versions/windows/apps/hh465196(v=win.10)">la stampa per le app di Windows Store con C#/VB/C + + e XAML</a>.<br/> Windows 8 include anche una nuova API basata su COM che offre supporto completo per l'accesso XPS aperto e per l'accesso a parti dei nuovi driver della stampante supportati da Windows 8. Per altre informazioni sulla nuova API, vedere <a href="/windows/desktop/printdocs/tailored-app-printing-api">Print Document Package API</a>.<br/> Il programma Windows Print Driver Inbox garantisce che Windows 8 includa il supporto per un'alta percentuale delle stampanti più diffuse.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/printdocs/jobbindalldocuments">Documenti XPS</a><br/></td>
<td>Informazioni sulle firme digitali XPS per l'API documento XPS.<br/>
<ul>
<li><a href="/previous-versions/windows/desktop/dd316976(v=vs.85)">API documenti XPS</a><br/> L'API documento XPS è un'API Windows nativa che supporta XPS OM. L'API documento XPS è stata introdotta in Windows 7 e può essere utilizzata nei programmi in modalità utente e nei driver della stampante XPSDrv.<br/></li>
<li><a href="/previous-versions/windows/desktop/ff819108(v=vs.85)">API di firma digitale XPS</a><br/> Le firme digitali XPS consentono la firma dei documenti, la verifica dell'identità del firmatario e l'indicazione se un documento XPS è stato modificato dopo la firma.<br/></li>
</ul></td>
</tr>
<tr class="odd">
<td><a href="printdocs-printing.md">Stampa</a><br/></td>
<td>Informazioni sulle funzionalità di stampa supportate da Windows. Queste funzionalità includono:<br/>
<ul>
<li><a href="/windows/desktop/printdocs/tailored-app-printing-api">API di stampa del pacchetto di documenti</a><br/> Fornisce app con un'interfaccia che consente la gestione del pacchetto <strong>PrintDocument</strong> .<br/></li>
<li><a href="print-spooler-api.md">API spooler di stampa</a><br/> Fornisce un'interfaccia per lo spooler di stampa in modo che le applicazioni possano gestire stampanti e processi di stampa.<br/></li>
<li><a href="print-ticket-api.md">API Print Ticket</a><br/> Fornisce le applicazioni con funzioni per gestire e convertire i ticket di stampa.<br/></li>
<li><a href="gdi-printing.md">API di stampa GDI</a><br/> Fornisce le applicazioni con un'interfaccia di stampa indipendente dal dispositivo. <br/></li>
<li><p><a href="xps-printing.md">API di stampa XPS</a><br/> Fornisce un'interfaccia allo spooler di stampa che le applicazioni possono utilizzare per inviare documenti XPS a una stampante.</p>
<blockquote>
[!Note]<br />
L'API di stampa XPS non è supportata e può essere modificata o non disponibile in futuro. Le applicazioni client devono invece usare l' <a href="/windows/desktop/printdocs/tailored-app-printing-api">API del pacchetto di stampa del documento</a> .
</blockquote>
<p><br/> <br/></p></li>
</ul></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/printdocs/printschema">Stampa schema</a><br/></td>
<td>Lo schema di stampa e le tecnologie correlate descrivono le funzionalità di una stampante e specificano le preferenze di stampa di un documento per le stampanti e la visualizzazione delle applicazioni. La <a href="https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip">specifica dello schema di stampa</a> è un documento scaricabile che contiene informazioni sullo schema di stampa e su come usarlo in documenti e stampa. Le informazioni online disponibili in questa sezione vengono fornite solo per le informazioni e potrebbero non riflettere accuratamente la versione corrente della specifica dello schema di <a href="https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip">stampa</a>.<br/> Per informazioni sulla progettazione più aggiornate, vedere la <a href="https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip">specifica dello schema di stampa</a> .<br/></td>
</tr>
</tbody>
</table>



 

## <a name="additional-resources"></a>Risorse aggiuntive

L' [app di esempio di stampa](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/Print%20sample%20(Windows%208)) di esempio illustra come stampare da un'app di Windows Store a partire da Windows 8.

Le funzionalità descritte in questa sezione sono destinate alla programmazione nativa di Windows. Per usare funzionalità simili nella programmazione .NET (gestita), vedere [Windows Presentation Foundation Documents](/previous-versions/dotnet/netframework-3.0/ms749165(v=vs.85)).

I documenti XPS sono basati sull'API per la creazione di [pacchetti](/previous-versions/windows/desktop/opc/packaging) . Vedere l'API per la creazione di pacchetti, per un accesso di livello inferiore al contenuto di un documento XPS.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Comunicazione bidirezionale stampanti (hardware Dev Center)](/windows-hardware/drivers/print/bidirectional-communication)
</dt> </dl>
