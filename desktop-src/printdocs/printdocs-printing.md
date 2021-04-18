---
description: Windows offre alle applicazioni un set completo di funzioni che consentono la stampa su vari dispositivi, ad esempio stampanti laser, plotter di vettori, stampanti raster e fax.
ms.assetid: e5c115b0-9c1e-46e7-8fb5-eddbc2c75298
title: Stampa (documenti e stampa)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 607e845ffc525701489a53c2a6b4628eceb5840d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314011"
---
# <a name="printing-documents-and-printing"></a>Stampa (documenti e stampa)

Windows offre alle applicazioni un set completo di funzioni che consentono la stampa su vari dispositivi, ad esempio stampanti laser, plotter di vettori, stampanti raster e fax.

## <a name="desktop-app-printing"></a>Stampa di app desktop

I programmatori Windows possono scegliere tra diverse tecnologie da stampare dalla propria applicazione.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Tecnologia</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/printdocs/tailored-app-printing-api">API di stampa del pacchetto di documenti</a><br/></td>
<td>Fornisce un'interfaccia che consente a un'applicazione di accedere e gestire il pacchetto del documento di stampa. Questa API è disponibile con Windows 8 e versioni successive di Windows.<br/></td>
</tr>
<tr class="even">
<td><a href="print-spooler-api.md">API spooler di stampa</a><br/></td>
<td>Fornisce un'interfaccia per lo spooler di stampa in modo che le applicazioni possano gestire stampanti e processi di stampa.<br/> Le applicazioni utilizzano l' <a href="print-spooler-api.md">API spooler di stampa</a> per avviare, arrestare, controllare e configurare i processi di stampa gestiti dallo spooler di stampa, indipendentemente dal fatto che utilizzino l' <a href="/windows/desktop/printdocs/tailored-app-printing-api">API del pacchetto</a> di stampa del documento o l' <a href="gdi-printing.md">API di stampa GDI</a> per stampare il contenuto.<br/></td>
</tr>
<tr class="odd">
<td><a href="print-ticket-api.md">API Print Ticket</a><br/></td>
<td>Fornisce le applicazioni con funzioni per gestire e convertire i ticket di stampa.<br/></td>
</tr>
<tr class="even">
<td><a href="gdi-printing.md">API di stampa GDI</a><br/></td>
<td>Fornisce le applicazioni con un'interfaccia di stampa indipendente dal dispositivo. <br/>
<blockquote>
[!Note]<br />
Gli sviluppatori che scrivono applicazioni per Windows Vista e versioni successive di Windows dovrebbero prendere in considerazione l'uso dell' <a href="/previous-versions/windows/desktop/dd316976(v=vs.85)">API Document XPS</a> nell'applicazione.
</blockquote>
<br/> L' <a href="gdi-printing.md">API di stampa GDI</a> è adatta per le applicazioni che devono essere eseguite in Windows XP e nelle versioni precedenti di Windows.<br/></td>
</tr>
</tbody>
</table>



 

Nell'illustrazione seguente viene fornita una panoramica di alto livello del modo in cui sono correlate le diverse API di stampa.

![diagramma che illustra come un'applicazione Windows nativa può usare le API di stampa](images/print-apis.png)

 

Le [API del pacchetto di documenti di stampa](./tailored-app-printing-api.md)in questa sezione descrivono le interfacce del pacchetto di documenti di stampa e dell'anteprima di stampa che è possibile usare con Windows 8 e le versioni successive di Windows desktop.

Per ulteriori informazioni sulla stampa da app di Windows Store scritte in JavaScript e HTML, vedere la pagina relativa alla [stampa (app di Windows Store scritte in JavaScript e HTML)](/previous-versions/windows/apps/hh465225(v=win.10)). Per altre informazioni sulla stampa da app di Windows Store scritte in C#, Microsoft Visual Basic o C++ e XAML, vedere la pagina relativa alla [stampa (app di Windows Store con C)](/previous-versions/windows/apps/hh465196(v=win.10)).

> [!Note]  
> Vedere [Win32 e com per app di Windows Store (stampa e documenti)](/uwp/win32-and-com/win32-and-com-for-uwp-apps) per l'elenco delle API di stampa di app desktop che possono essere usate anche nelle app di Windows Store.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[API documenti XPS](/previous-versions/windows/desktop/dd316976(v=vs.85))
</dt> <dt>

[Comunicazione bidirezionale stampanti (hardware Dev Center)](/windows-hardware/drivers/print/bidirectional-communication)
</dt> </dl>

