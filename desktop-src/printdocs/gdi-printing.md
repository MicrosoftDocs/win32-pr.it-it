---
description: L'API di stampa GDI fornisce le applicazioni con un'interfaccia di stampa indipendente dal dispositivo.
ms.assetid: 3115c9e0-05c9-462d-8238-fc035ea32d4e
title: API di stampa GDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0239282543a68c6fe8b5d6503d085582fd9c20db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227468"
---
# <a name="gdi-print-api"></a><span data-ttu-id="4ac77-103">API di stampa GDI</span><span class="sxs-lookup"><span data-stu-id="4ac77-103">GDI Print API</span></span>

<span data-ttu-id="4ac77-104">L'API di stampa GDI fornisce le applicazioni con un'interfaccia di stampa indipendente dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4ac77-104">The GDI Print API provides applications with a device-independent printing interface.</span></span> <span data-ttu-id="4ac77-105">Utilizzare questa interfaccia se l'applicazione utilizza GDI per il rendering di testo e grafica.</span><span class="sxs-lookup"><span data-stu-id="4ac77-105">Use this interface if the application uses GDI to render text and graphics.</span></span>

<span data-ttu-id="4ac77-106">Se si scrivono applicazioni per Windows Vista o versioni successive di Windows, è consigliabile usare l' [API di documento XPS](/previous-versions/windows/desktop/dd316976(v=vs.85)) e l' [API di stampa XPS](xps-printing.md) per usare le interfacce grafiche a prestazioni elevate supportate dai driver di stampa XPSDrv.</span><span class="sxs-lookup"><span data-stu-id="4ac77-106">If you write applications for Windows Vista or later versions of Windows, consider using the [XPS Document API](/previous-versions/windows/desktop/dd316976(v=vs.85)) and the [XPS Print API](xps-printing.md) to use the higher-performance graphics interfaces that are supported by XPSDrv print drivers.</span></span>

<span data-ttu-id="4ac77-107">In questa sezione vengono fornite informazioni sui seguenti argomenti.</span><span class="sxs-lookup"><span data-stu-id="4ac77-107">This section provides information about the following topics.</span></span>



| <span data-ttu-id="4ac77-108">Argomento</span><span class="sxs-lookup"><span data-stu-id="4ac77-108">Topic</span></span>                                                                                             | <span data-ttu-id="4ac77-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4ac77-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4ac77-110">Informazioni sull'API di stampa GDI</span><span class="sxs-lookup"><span data-stu-id="4ac77-110">About the GDI Print API</span></span>](about-the-gdi-print-api.md)<br/>                                 | <span data-ttu-id="4ac77-111">Panoramica della funzionalità di stampa GDI.</span><span class="sxs-lookup"><span data-stu-id="4ac77-111">An overview of the GDI printing functionality.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [<span data-ttu-id="4ac77-112">Uso dell'API di stampa GDI</span><span class="sxs-lookup"><span data-stu-id="4ac77-112">Using the GDI Print API</span></span>](using-the-printing-functions.md)<br/>                            | <span data-ttu-id="4ac77-113">Informazioni sull'utilizzo dell'API di stampa GDI in un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="4ac77-113">Information about using the GDI Print API in an application.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="4ac77-114">Informazioni di riferimento sulle API di stampa GDI</span><span class="sxs-lookup"><span data-stu-id="4ac77-114">GDI Print API Reference</span></span>](gdi-print-api-reference.md)<br/>                                 | <span data-ttu-id="4ac77-115">Descrizioni dettagliate delle funzioni, delle strutture e di altri elementi dell'API di stampa GDI.</span><span class="sxs-lookup"><span data-stu-id="4ac77-115">Detailed descriptions of the functions, structures, and other elements of the GDI Print API.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="4ac77-116">Microsoft XPS Document Converter (MXDC)</span><span class="sxs-lookup"><span data-stu-id="4ac77-116">Microsoft XPS Document Converter (MXDC)</span></span>](microsoft-xps-document-converter--mxdc-.md)<br/> | <span data-ttu-id="4ac77-117">[Microsoft XPS Document Converter (MXDC)](microsoft-xps-document-converter--mxdc-.md) è un componente che consente alle applicazioni di utilizzare l'API di stampa GDI con stampanti che dispongono di un driver di stampa XPSDrv.</span><span class="sxs-lookup"><span data-stu-id="4ac77-117">The [Microsoft XPS Document Converter (MXDC)](microsoft-xps-document-converter--mxdc-.md) is a component that enables applications to use the GDI Print API with printers that have an XPSDrv Print Driver.</span></span><br/>                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="4ac77-118">Microsoft XPS Document Writer (MXDW)</span><span class="sxs-lookup"><span data-stu-id="4ac77-118">Microsoft XPS Document Writer (MXDW)</span></span>](microsoft-xps-document-writer.md)<br/>              | <span data-ttu-id="4ac77-119">[Microsoft XPS Document Writer (MXDW)](microsoft-xps-document-writer.md) fornisce applicazioni con la funzionalità "Save As XPS" o "Export to XPS".</span><span class="sxs-lookup"><span data-stu-id="4ac77-119">The [Microsoft XPS Document Writer (MXDW)](microsoft-xps-document-writer.md) provides applications with "save as XPS" or "export to XPS" functionality.</span></span> <span data-ttu-id="4ac77-120">Le applicazioni che non creano in modo nativo contenuto del documento XPS possono usare MXDW per creare file di documento XPS senza usare l' [API documento XPS](/previous-versions/windows/desktop/dd316976(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="4ac77-120">Applications that do not natively create XPS document content can use the MXDW to create XPS document files without using the [XPS Document API](/previous-versions/windows/desktop/dd316976(v=vs.85)).</span></span> <span data-ttu-id="4ac77-121">L'API documenti XPS, tuttavia, fornisce a un'applicazione la possibilità di utilizzare le interfacce grafiche con prestazioni più elevate supportate dai driver di stampa XPSDrv.</span><span class="sxs-lookup"><span data-stu-id="4ac77-121">The XPS Document API, however, provides an application with the ability to use the higher-performance graphics interfaces that are supported by XPSDrv print drivers.</span></span><br/> |



 

<span data-ttu-id="4ac77-122">Nel diagramma seguente viene illustrata la relazione tra l'API di stampa GDI e le altre API di stampa che un'applicazione può utilizzare.</span><span class="sxs-lookup"><span data-stu-id="4ac77-122">The following diagram shows the relationship of the GDI Print API to the other print APIs that an application can use.</span></span>

![diagramma che mostra la relazione tra l'API di stampa GDI e le altre API di stampa che un'applicazione Win32 può utilizzare](images/print-apis-gdi.png)

## <a name="related-topics"></a><span data-ttu-id="4ac77-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4ac77-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4ac77-125">**AddJob**</span><span class="sxs-lookup"><span data-stu-id="4ac77-125">**AddJob**</span></span>](addjob.md)
</dt> <dt>

<span data-ttu-id="4ac77-126">[API documenti XPS](/previous-versions/windows/desktop/dd316976(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4ac77-126">[XPS Document API](/previous-versions/windows/desktop/dd316976(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="4ac77-127">API di stampa XPS</span><span class="sxs-lookup"><span data-stu-id="4ac77-127">XPS Print API</span></span>](xps-printing.md)
</dt> <dt>

[<span data-ttu-id="4ac77-128">API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="4ac77-128">Print Spooler API</span></span>](print-spooler-api.md)
</dt> <dt>

[<span data-ttu-id="4ac77-129">API Print Ticket</span><span class="sxs-lookup"><span data-stu-id="4ac77-129">Print Ticket API</span></span>](print-ticket-api.md)
</dt> </dl>

 

