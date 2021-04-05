---
description: .
ms.assetid: f575109e-e9c4-4db5-945c-7c96b6b5d613
title: Interfacce API di stampa XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 828e999417354678d77ad1de8c29beb5956f7762
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755215"
---
# <a name="xps-print-api-interfaces"></a><span data-ttu-id="7fd4a-103">Interfacce API di stampa XPS</span><span class="sxs-lookup"><span data-stu-id="7fd4a-103">XPS Print API Interfaces</span></span>

<span data-ttu-id="7fd4a-104">\[Le interfacce descritte in questa sezione sono deprecate.</span><span class="sxs-lookup"><span data-stu-id="7fd4a-104">\[The interfaces described in this section are deprecated.</span></span> <span data-ttu-id="7fd4a-105">Le applicazioni client devono invece usare l' [API del pacchetto di stampa del documento](./tailored-app-printing-api.md) .\]</span><span class="sxs-lookup"><span data-stu-id="7fd4a-105">Client applications should use the [Print Document Package API](./tailored-app-printing-api.md) instead.\]</span></span>

<span data-ttu-id="7fd4a-106">\[IXpsPrintJob non è supportato e può essere modificato o non disponibile in futuro.</span><span class="sxs-lookup"><span data-stu-id="7fd4a-106">\[IXpsPrintJob is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="7fd4a-107">\]</span><span class="sxs-lookup"><span data-stu-id="7fd4a-107">\]</span></span>

<span data-ttu-id="7fd4a-108">\[IXpsPrintJobStream non è supportato e può essere modificato o non disponibile in futuro.</span><span class="sxs-lookup"><span data-stu-id="7fd4a-108">\[IXpsPrintJobStream is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="7fd4a-109">\]</span><span class="sxs-lookup"><span data-stu-id="7fd4a-109">\]</span></span>

## <a name="in-this-section"></a><span data-ttu-id="7fd4a-110">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="7fd4a-110">In this section</span></span>



| <span data-ttu-id="7fd4a-111">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="7fd4a-111">Interface</span></span>                                                   | <span data-ttu-id="7fd4a-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7fd4a-112">Description</span></span>                                                                               |
|-------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7fd4a-113">**IXpsPrintJob**</span><span class="sxs-lookup"><span data-stu-id="7fd4a-113">**IXpsPrintJob**</span></span>](/windows/desktop/api/XpsPrint/nn-xpsprint-ixpsprintjob)<br/>             | <span data-ttu-id="7fd4a-114">Consente di accedere a un processo di stampa attualmente in corso.</span><span class="sxs-lookup"><span data-stu-id="7fd4a-114">Provides access to a print job that is currently in progress.</span></span><br/>                  |
| [<span data-ttu-id="7fd4a-115">**IXpsPrintJobStream**</span><span class="sxs-lookup"><span data-stu-id="7fd4a-115">**IXpsPrintJobStream**</span></span>](/windows/desktop/api/XpsPrint/nn-xpsprint-ixpsprintjobstream)<br/> | <span data-ttu-id="7fd4a-116">Interfaccia di flusso di sola scrittura in cui un'applicazione scrive i dati del processo di stampa.</span><span class="sxs-lookup"><span data-stu-id="7fd4a-116">A write-only stream interface into which an application writes print job data.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="7fd4a-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7fd4a-117">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="7fd4a-118">[Documents](./jobbindalldocuments.md) (Documenti)</span><span class="sxs-lookup"><span data-stu-id="7fd4a-118">[Documents](./jobbindalldocuments.md)</span></span>
</dt> <dt>

[<span data-ttu-id="7fd4a-119">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="7fd4a-119">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

