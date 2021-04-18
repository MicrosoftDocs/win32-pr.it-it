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
# <a name="printing-documents-and-printing"></a><span data-ttu-id="a23c3-103">Stampa (documenti e stampa)</span><span class="sxs-lookup"><span data-stu-id="a23c3-103">Printing (Documents and Printing)</span></span>

<span data-ttu-id="a23c3-104">Windows offre alle applicazioni un set completo di funzioni che consentono la stampa su vari dispositivi, ad esempio stampanti laser, plotter di vettori, stampanti raster e fax.</span><span class="sxs-lookup"><span data-stu-id="a23c3-104">Windows provides applications with a complete set of functions that allow printing to various devices, such as laser printers, vector plotters, raster printers, and fax machines.</span></span>

## <a name="desktop-app-printing"></a><span data-ttu-id="a23c3-105">Stampa di app desktop</span><span class="sxs-lookup"><span data-stu-id="a23c3-105">Desktop App Printing</span></span>

<span data-ttu-id="a23c3-106">I programmatori Windows possono scegliere tra diverse tecnologie da stampare dalla propria applicazione.</span><span class="sxs-lookup"><span data-stu-id="a23c3-106">Windows programmers can select from several different technologies to print from their application.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a23c3-107">Tecnologia</span><span class="sxs-lookup"><span data-stu-id="a23c3-107">Technology</span></span></th>
<th><span data-ttu-id="a23c3-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a23c3-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a23c3-109"><a href="/windows/desktop/printdocs/tailored-app-printing-api">API di stampa del pacchetto di documenti</a></span><span class="sxs-lookup"><span data-stu-id="a23c3-109"><a href="/windows/desktop/printdocs/tailored-app-printing-api">Print Document Package API</a></span></span><br/></td>
<td><span data-ttu-id="a23c3-110">Fornisce un'interfaccia che consente a un'applicazione di accedere e gestire il pacchetto del documento di stampa.</span><span class="sxs-lookup"><span data-stu-id="a23c3-110">Provides an interface that allows an application to access and manage the print document package.</span></span> <span data-ttu-id="a23c3-111">Questa API è disponibile con Windows 8 e versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="a23c3-111">This API is available with Windows 8 and later versions of Windows.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a23c3-112"><a href="print-spooler-api.md">API spooler di stampa</a></span><span class="sxs-lookup"><span data-stu-id="a23c3-112"><a href="print-spooler-api.md">Print Spooler API</a></span></span><br/></td>
<td><span data-ttu-id="a23c3-113">Fornisce un'interfaccia per lo spooler di stampa in modo che le applicazioni possano gestire stampanti e processi di stampa.</span><span class="sxs-lookup"><span data-stu-id="a23c3-113">Provides an interface to the print spooler so that applications can manage printers and print jobs.</span></span><br/> <span data-ttu-id="a23c3-114">Le applicazioni utilizzano l' <a href="print-spooler-api.md">API spooler di stampa</a> per avviare, arrestare, controllare e configurare i processi di stampa gestiti dallo spooler di stampa, indipendentemente dal fatto che utilizzino l' <a href="/windows/desktop/printdocs/tailored-app-printing-api">API del pacchetto</a> di stampa del documento o l' <a href="gdi-printing.md">API di stampa GDI</a> per stampare il contenuto.</span><span class="sxs-lookup"><span data-stu-id="a23c3-114">Applications use the <a href="print-spooler-api.md">Print Spooler API</a> to start, stop, control, and configure print jobs managed by the print spooler whether they use the <a href="/windows/desktop/printdocs/tailored-app-printing-api">Print Document Package API</a> or the <a href="gdi-printing.md">GDI Print API</a> to print the content.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a23c3-115"><a href="print-ticket-api.md">API Print Ticket</a></span><span class="sxs-lookup"><span data-stu-id="a23c3-115"><a href="print-ticket-api.md">Print Ticket API</a></span></span><br/></td>
<td><span data-ttu-id="a23c3-116">Fornisce le applicazioni con funzioni per gestire e convertire i ticket di stampa.</span><span class="sxs-lookup"><span data-stu-id="a23c3-116">Provides applications with functions to manage and convert print tickets.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a23c3-117"><a href="gdi-printing.md">API di stampa GDI</a></span><span class="sxs-lookup"><span data-stu-id="a23c3-117"><a href="gdi-printing.md">GDI Print API</a></span></span><br/></td>
<td><span data-ttu-id="a23c3-118">Fornisce le applicazioni con un'interfaccia di stampa indipendente dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a23c3-118">Provides applications with a device-independent printing interface.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="a23c3-119">Gli sviluppatori che scrivono applicazioni per Windows Vista e versioni successive di Windows dovrebbero prendere in considerazione l'uso dell' <a href="/previous-versions/windows/desktop/dd316976(v=vs.85)">API Document XPS</a> nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a23c3-119">Developers who are writing applications for Windows Vista and later versions of Windows should consider using the <a href="/previous-versions/windows/desktop/dd316976(v=vs.85)">XPS Document API</a> in their application.</span></span>
</blockquote>
<br/> <span data-ttu-id="a23c3-120">L' <a href="gdi-printing.md">API di stampa GDI</a> è adatta per le applicazioni che devono essere eseguite in Windows XP e nelle versioni precedenti di Windows.</span><span class="sxs-lookup"><span data-stu-id="a23c3-120">The <a href="gdi-printing.md">GDI Print API</a> is suitable for applications that must run on Windows XP and earlier versions of Windows.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="a23c3-121">Nell'illustrazione seguente viene fornita una panoramica di alto livello del modo in cui sono correlate le diverse API di stampa.</span><span class="sxs-lookup"><span data-stu-id="a23c3-121">The following illustration provides a high-level view of how the different printing APIs are related.</span></span>

![diagramma che illustra come un'applicazione Windows nativa può usare le API di stampa](images/print-apis.png)

 

<span data-ttu-id="a23c3-123">Le [API del pacchetto di documenti di stampa](./tailored-app-printing-api.md)in questa sezione descrivono le interfacce del pacchetto di documenti di stampa e dell'anteprima di stampa che è possibile usare con Windows 8 e le versioni successive di Windows desktop.</span><span class="sxs-lookup"><span data-stu-id="a23c3-123">The [Print Document Package API](./tailored-app-printing-api.md)s in this section describe the print document package and print preview interfaces that you can use with Windows 8 and later versions of Windows desktop.</span></span>

<span data-ttu-id="a23c3-124">Per ulteriori informazioni sulla stampa da app di Windows Store scritte in JavaScript e HTML, vedere la pagina relativa alla [stampa (app di Windows Store scritte in JavaScript e HTML)](/previous-versions/windows/apps/hh465225(v=win.10)).</span><span class="sxs-lookup"><span data-stu-id="a23c3-124">For more info about printing from Windows Store apps that are written in JavaScript and HTML, see [Printing (Windows Store apps using JavaScript and HTML)](/previous-versions/windows/apps/hh465225(v=win.10)).</span></span> <span data-ttu-id="a23c3-125">Per altre informazioni sulla stampa da app di Windows Store scritte in C#, Microsoft Visual Basic o C++ e XAML, vedere la pagina relativa alla [stampa (app di Windows Store con C)](/previous-versions/windows/apps/hh465196(v=win.10)).</span><span class="sxs-lookup"><span data-stu-id="a23c3-125">For more info about printing from Windows Store apps that are written in C#, Microsoft Visual Basic, or C++ and XAML, see [Printing (Windows Store apps using C)](/previous-versions/windows/apps/hh465196(v=win.10)).</span></span>

> [!Note]  
> <span data-ttu-id="a23c3-126">Vedere [Win32 e com per app di Windows Store (stampa e documenti)](/uwp/win32-and-com/win32-and-com-for-uwp-apps) per l'elenco delle API di stampa di app desktop che possono essere usate anche nelle app di Windows Store.</span><span class="sxs-lookup"><span data-stu-id="a23c3-126">See [Win32 and COM for Windows Store apps (printing and documents)](/uwp/win32-and-com/win32-and-com-for-uwp-apps) for the list of the Desktop App Printing APIs that can also be used in Windows Store apps.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="a23c3-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a23c3-127">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="a23c3-128">[API documenti XPS](/previous-versions/windows/desktop/dd316976(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a23c3-128">[XPS Document API](/previous-versions/windows/desktop/dd316976(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="a23c3-129">Comunicazione bidirezionale stampanti (hardware Dev Center)</span><span class="sxs-lookup"><span data-stu-id="a23c3-129">Bidirectional printer communications (Hardware Dev Center)</span></span>](/windows-hardware/drivers/print/bidirectional-communication)
</dt> </dl>

