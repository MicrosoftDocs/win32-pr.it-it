---
description: L'API Print Ticket consente alle applicazioni di gestire e convertire i ticket di stampa.
ms.assetid: 4f854c1a-f2e1-48c4-9cc1-8a0fcf1bebed
title: API Print Ticket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e19cfd8d624a1390b8afacd625e92fcee2704dd
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "104058478"
---
# <a name="print-ticket-api"></a><span data-ttu-id="4dae3-103">API Print Ticket</span><span class="sxs-lookup"><span data-stu-id="4dae3-103">Print Ticket API</span></span>

<span data-ttu-id="4dae3-104">L'API Print Ticket consente alle applicazioni di gestire e convertire i ticket di stampa.</span><span class="sxs-lookup"><span data-stu-id="4dae3-104">The Print Ticket API provides enables applications to manage and convert print tickets.</span></span>

<span data-ttu-id="4dae3-105">Un Print Ticket è un componente del documento XPS che contiene le impostazioni della stampante preferite per una pagina in un documento o per un intero documento o per un processo di stampa che contiene uno o più documenti.</span><span class="sxs-lookup"><span data-stu-id="4dae3-105">A print ticket is an XPS document component that contains the preferred printer settings for a page in a document, or for an entire document, or for a print job that contains one or more documents.</span></span> <span data-ttu-id="4dae3-106">Si noti che i ticket di stampa sono disponibili solo nei documenti XPS.</span><span class="sxs-lookup"><span data-stu-id="4dae3-106">Note that print tickets are only found in XPS documents.</span></span>

<span data-ttu-id="4dae3-107">Prima che la stampante possa utilizzare il ticket di stampa, il ticket di stampa deve essere convalidato in base alle caratteristiche della stampante, definite nelle funzionalità di stampa della stampante.</span><span class="sxs-lookup"><span data-stu-id="4dae3-107">Before the printer can use the print ticket, the print ticket must be validated against the printer's characteristics, which are defined in the printer's Print Capabilities.</span></span> <span data-ttu-id="4dae3-108">L'applicazione esegue tale convalida chiamando l'API del ticket di stampa.</span><span class="sxs-lookup"><span data-stu-id="4dae3-108">The application performs that validation by calling the Print Ticket API.</span></span>

<span data-ttu-id="4dae3-109">PrintTicket e PrintCapabilities vengono descritti utilizzando gli elementi dello schema di stampa, definito dalla [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="4dae3-109">The PrintTicket and PrintCapabilities are described by using elements of the Print Schema, which is defined by the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="4dae3-110">Questo argomento contiene informazioni sugli elementi API seguenti:</span><span class="sxs-lookup"><span data-stu-id="4dae3-110">This topic contains information about the following API elements:</span></span>

-   [<span data-ttu-id="4dae3-111">Funzioni API del ticket di stampa</span><span class="sxs-lookup"><span data-stu-id="4dae3-111">Print Ticket API Functions</span></span>](print-ticket-api-functions.md)
-   [<span data-ttu-id="4dae3-112">Enumerazioni API del ticket di stampa</span><span class="sxs-lookup"><span data-stu-id="4dae3-112">Print Ticket API Enumerations</span></span>](print-ticket-api-enumerations.md)

<span data-ttu-id="4dae3-113">Il diagramma seguente mostra la relazione tra l'API del ticket di stampa e le altre API di stampa che un'applicazione Windows nativa può usare.</span><span class="sxs-lookup"><span data-stu-id="4dae3-113">The following diagram shows the relationship of the Print Ticket API to the other Print APIs that a native Windows application can use.</span></span>

![diagramma che mostra la relazione tra l'API del ticket di stampa e le altre API di stampa che possono essere utilizzate da un'applicazione Windows nativa](images/print-apis-pt.png)

## <a name="related-topics"></a><span data-ttu-id="4dae3-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4dae3-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4dae3-116">API di stampa XPS</span><span class="sxs-lookup"><span data-stu-id="4dae3-116">XPS Print API</span></span>](xps-printing.md)
</dt> <dt>

[<span data-ttu-id="4dae3-117">API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="4dae3-117">Print Spooler API</span></span>](print-spooler-api.md)
</dt> <dt>

[<span data-ttu-id="4dae3-118">API di stampa GDI</span><span class="sxs-lookup"><span data-stu-id="4dae3-118">GDI Print API</span></span>](gdi-printing.md)
</dt> <dt>

[<span data-ttu-id="4dae3-119">Specifica dello schema di stampa</span><span class="sxs-lookup"><span data-stu-id="4dae3-119">Print Schema Specification</span></span>](https://go.microsoft.com/fwlink/?linkid=2022117)
</dt> <dt>

[<span data-ttu-id="4dae3-120">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="4dae3-120">XML Paper Specification</span></span>](https://go.microsoft.com/fwlink/?linkid=2022122)
</dt> </dl>

 

 



