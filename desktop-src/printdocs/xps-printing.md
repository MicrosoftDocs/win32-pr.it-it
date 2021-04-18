---
description: Fornisce un'interfaccia per lo spooler di stampa. Le applicazioni possono utilizzare questa API per inviare documenti XPS a una stampante.
ms.assetid: df06ddcb-e573-461c-99a3-8f108fe2c143
title: API di stampa XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30c53322a8ae6a03c3ac4bb71fc680f719999546
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310141"
---
# <a name="xps-print-api"></a><span data-ttu-id="7e9bf-104">API di stampa XPS</span><span class="sxs-lookup"><span data-stu-id="7e9bf-104">XPS Print API</span></span>

<span data-ttu-id="7e9bf-105">\[L'API di stampa XPS non è supportata e può essere modificata o non disponibile in futuro.</span><span class="sxs-lookup"><span data-stu-id="7e9bf-105">\[The XPS Print API is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="7e9bf-106">Le applicazioni client devono invece usare l' [API del pacchetto di stampa del documento](./tailored-app-printing-api.md) .\]</span><span class="sxs-lookup"><span data-stu-id="7e9bf-106">Client applications should use the [Print Document Package API](./tailored-app-printing-api.md) instead.\]</span></span>

<span data-ttu-id="7e9bf-107">Fornisce un'interfaccia per lo spooler di stampa.</span><span class="sxs-lookup"><span data-stu-id="7e9bf-107">Provides an interface to the print spooler.</span></span> <span data-ttu-id="7e9bf-108">Le applicazioni possono utilizzare questa API per inviare documenti XPS a una stampante.</span><span class="sxs-lookup"><span data-stu-id="7e9bf-108">Applications can use this API to send XPS documents to a printer.</span></span>

<span data-ttu-id="7e9bf-109">In questa sezione vengono fornite informazioni sui seguenti argomenti.</span><span class="sxs-lookup"><span data-stu-id="7e9bf-109">This section contains information about the following topics.</span></span>

<dl>

[<span data-ttu-id="7e9bf-110">Informazioni sull'API di stampa XPS</span><span class="sxs-lookup"><span data-stu-id="7e9bf-110">About the XPS Print API</span></span>](about-xps-print-api.md)  
[<span data-ttu-id="7e9bf-111">Uso dell'API di stampa XPS</span><span class="sxs-lookup"><span data-stu-id="7e9bf-111">Using the XPS Print API</span></span>](using-the-xps-print-api.md)  
[<span data-ttu-id="7e9bf-112">Informazioni di riferimento sulle API di stampa XPS</span><span class="sxs-lookup"><span data-stu-id="7e9bf-112">XPS Print API Reference</span></span>](xpsprint-interfaces.md)  
</dl>

<span data-ttu-id="7e9bf-113">Le applicazioni Windows native che creano documenti XPS, ad esempio tramite l' [API Document XPS](/previous-versions/windows/desktop/dd316976(v=vs.85)), possono utilizzare l'API di stampa XPS per inviare contenuto del documento XPS a una stampante.</span><span class="sxs-lookup"><span data-stu-id="7e9bf-113">Native Windows applications that create XPS documents, such as by using the [XPS Document API](/previous-versions/windows/desktop/dd316976(v=vs.85)), can use the XPS Print API to send XPS document content to a printer.</span></span>

<span data-ttu-id="7e9bf-114">Nel diagramma seguente viene illustrata la relazione tra l'API di stampa XPS e le altre API di stampa che un'applicazione Windows nativa può utilizzare.</span><span class="sxs-lookup"><span data-stu-id="7e9bf-114">The following diagram shows the relationship of the XPS Print API to the other Print APIs that a native Windows application can use.</span></span>

![diagramma che mostra la relazione tra l'API di stampa XPS e le altre API di stampa che possono essere utilizzate da un'applicazione Windows nativa](images/print-apis-xps.png)

## <a name="related-topics"></a><span data-ttu-id="7e9bf-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7e9bf-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7e9bf-117">**AddJob**</span><span class="sxs-lookup"><span data-stu-id="7e9bf-117">**AddJob**</span></span>](addjob.md)
</dt> <dt>

[<span data-ttu-id="7e9bf-118">API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="7e9bf-118">Print Spooler API</span></span>](print-spooler-api.md)
</dt> <dt>

[<span data-ttu-id="7e9bf-119">API Print Ticket</span><span class="sxs-lookup"><span data-stu-id="7e9bf-119">Print Ticket API</span></span>](print-ticket-api.md)
</dt> <dt>

[<span data-ttu-id="7e9bf-120">API di stampa GDI</span><span class="sxs-lookup"><span data-stu-id="7e9bf-120">GDI Print API</span></span>](gdi-printing.md)
</dt> </dl>

 

 
