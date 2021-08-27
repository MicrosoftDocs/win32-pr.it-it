---
description: Questi argomenti descrivono i documenti e le funzionalità di stampa Windows che consentono alle applicazioni di salvare, visualizzare e stampare.
ms.assetid: 20e56af6-9598-4d6a-a2bf-454cef8a3368
title: 'Documenti e stampa '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87d7af92af0615dcb11d2623be8f2e21ae813aa1
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472367"
---
# <a name="documents-and-printing"></a>Documenti e stampa 

Questi argomenti descrivono i documenti e le funzionalità di stampa Windows che consentono alle applicazioni di salvare, visualizzare e stampare.

## <a name="in-this-section"></a>Contenuto della sezione




| Argomento | Descrizione | 
|-------|-------------|
| <a href="/windows/desktop/printdocs/what-s-new-for-printing-in-windows-vnext">Novità per la stampa</a><br /> | Windows 8 supporta la stampa per le app Windows Store usando <a href="/previous-versions/windows/apps/hh465225(v=win.10)">JavaScript</a> e HTML e la stampa per le app di Windows Store con <a href="/previous-versions/windows/apps/hh465196(v=win.10)">C#/VB/C++ e XAML.</a><br /> Windows 8 include anche una nuova API basata su COM che offre il supporto completo per Open XPS e l'accesso a parti dei nuovi driver della stampante supportati Windows 8. Per altre informazioni sulla nuova API, vedere <a href="/windows/desktop/printdocs/tailored-app-printing-api">Print Document Package API</a>.<br /> Il Windows posta in arrivo del driver di stampa assicura che Windows 8 il supporto per una percentuale elevata delle stampanti più diffusi.<br /> | 
| <a href="/windows/desktop/printdocs/jobbindalldocuments">Documenti XPS</a><br /> | Informazioni sull'API documento XPS firme digitali XPS.<br /><ul><li><a href="/previous-versions/windows/desktop/dd316976(v=vs.85)">API documento XPS</a><br /> L'API documento XPS è un'API Windows nativa che supporta xps OM. L'API documento XPS è stata introdotta Windows 7 e può essere usata nei programmi in modalità utente e nei driver della stampante XPSDrv.<br /></li><li><a href="/previous-versions/windows/desktop/ff819108(v=vs.85)">API di firma digitale XPS</a><br /> Le firme digitali XPS consentono la firma dei documenti, la verifica dell'identità del firmatario e l'indicazione se un documento XPS è stato modificato dopo la firma.<br /></li></ul> | 
| <a href="printdocs-printing.md">Stampa</a><br /> | Informazioni sulle funzionalità di stampa supportate da Windows. Queste funzionalità includono:<br /><ul><li><a href="/windows/desktop/printdocs/tailored-app-printing-api">API per la stampa di pacchetti di documenti</a><br /> Fornisce alle app un'interfaccia che consente la gestione del <strong>pacchetto PrintDocument.</strong><br /></li><li><a href="print-spooler-api.md">API Spooler di stampa</a><br /> Fornisce un'interfaccia per lo spooler di stampa in modo che le applicazioni possano gestire stampanti e processi di stampa.<br /></li><li><a href="print-ticket-api.md">Print Ticket API</a><br /> Fornisce alle applicazioni funzioni per gestire e convertire i ticket di stampa.<br /></li><li><a href="gdi-printing.md">API di stampa GDI</a><br /> Fornisce alle applicazioni un'interfaccia di stampa indipendente dal dispositivo. <br /></li><li><p><a href="xps-printing.md">API di stampa XPS</a><br /> Fornisce un'interfaccia per lo spooler di stampa che le applicazioni possono usare per inviare documenti XPS a una stampante.</p><blockquote>[!Note]<br />L'API di stampa XPS non è supportata e potrebbe essere modificata o non disponibile in futuro. Le applicazioni client devono usare invece <a href="/windows/desktop/printdocs/tailored-app-printing-api">l'API Stampa pacchetto</a> documento.</blockquote><p><br /><br /></p></li></ul> | 
| <a href="/windows/desktop/printdocs/printschema">Stampare lo schema</a><br /> | Lo schema di stampa e le tecnologie correlate descrivono le funzionalità di una stampante e specificano le preferenze di stampa di un documento per le stampanti e la visualizzazione delle applicazioni. Print <a href="https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip">Schema Specification è</a> un documento scaricabile che contiene informazioni sullo schema di stampa e su come usarlo nei documenti e nella stampa. Le informazioni online disponibili in questa sezione vengono fornite solo per le informazioni e potrebbero non riflettere in modo accurato la versione corrente di <a href="https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip">Print Schema Specification</a>.<br /> Per le informazioni <a href="https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip">di progettazione più aggiornate,</a> vedere Print Schema Specification (Specifica dello schema di stampa).<br /> | 




 

## <a name="additional-resources"></a>Risorse aggiuntive

[L'app di esempio Print Sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/Print%20sample%20(Windows%208)) illustra come stampare da un'app Windows Store a partire da Windows 8.

Le funzionalità descritte in questa sezione sono per la programmazione Windows nativa. Per usare funzionalità simili nella programmazione .NET (gestita), vedere [Windows Presentation Foundation Documenti](/previous-versions/dotnet/netframework-3.0/ms749165(v=vs.85)).

I documenti XPS sono basati sull'API [Di creazione pacchetti.](/previous-versions/windows/desktop/opc/packaging) Per un accesso di livello inferiore al contenuto di un documento XPS, vedere l'API Di creazione pacchetti.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Comunicazioni bidirezionali della stampante (Hardware Dev Center)](/windows-hardware/drivers/print/bidirectional-communication)
</dt> </dl>
