---
description: Interfacce DELL'API di stampa XPS
ms.assetid: f575109e-e9c4-4db5-945c-7c96b6b5d613
title: Interfacce DELL'API di stampa XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47cd01c169c82a9e3210f281ec6c44fa206c40b5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105189"
---
# <a name="xps-print-api-interfaces"></a><span data-ttu-id="e642c-103">Interfacce DELL'API di stampa XPS</span><span class="sxs-lookup"><span data-stu-id="e642c-103">XPS Print API Interfaces</span></span>

<span data-ttu-id="e642c-104">\[Le interfacce descritte in questa sezione sono deprecate.</span><span class="sxs-lookup"><span data-stu-id="e642c-104">\[The interfaces described in this section are deprecated.</span></span> <span data-ttu-id="e642c-105">Le applicazioni client devono invece usare [l'API print document package.](./tailored-app-printing-api.md)\]</span><span class="sxs-lookup"><span data-stu-id="e642c-105">Client applications should use the [Print Document Package API](./tailored-app-printing-api.md) instead.\]</span></span>

<span data-ttu-id="e642c-106">\[IXpsPrintJob non è supportato e potrebbe essere modificato o non disponibile in futuro.</span><span class="sxs-lookup"><span data-stu-id="e642c-106">\[IXpsPrintJob is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="e642c-107">\]</span><span class="sxs-lookup"><span data-stu-id="e642c-107">\]</span></span>

<span data-ttu-id="e642c-108">\[IXpsPrintJobStream non è supportato e potrebbe essere modificato o non disponibile in futuro.</span><span class="sxs-lookup"><span data-stu-id="e642c-108">\[IXpsPrintJobStream is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="e642c-109">\]</span><span class="sxs-lookup"><span data-stu-id="e642c-109">\]</span></span>

## <a name="in-this-section"></a><span data-ttu-id="e642c-110">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="e642c-110">In this section</span></span>



| <span data-ttu-id="e642c-111">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="e642c-111">Interface</span></span>                                                   | <span data-ttu-id="e642c-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e642c-112">Description</span></span>                                                                               |
|-------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e642c-113">**IXpsPrintJob**</span><span class="sxs-lookup"><span data-stu-id="e642c-113">**IXpsPrintJob**</span></span>](/windows/desktop/api/XpsPrint/nn-xpsprint-ixpsprintjob)<br/>             | <span data-ttu-id="e642c-114">Fornisce l'accesso a un processo di stampa attualmente in corso.</span><span class="sxs-lookup"><span data-stu-id="e642c-114">Provides access to a print job that is currently in progress.</span></span><br/>                  |
| [<span data-ttu-id="e642c-115">**IXpsPrintJobStream**</span><span class="sxs-lookup"><span data-stu-id="e642c-115">**IXpsPrintJobStream**</span></span>](/windows/desktop/api/XpsPrint/nn-xpsprint-ixpsprintjobstream)<br/> | <span data-ttu-id="e642c-116">Interfaccia di flusso di sola scrittura in cui un'applicazione scrive i dati del processo di stampa.</span><span class="sxs-lookup"><span data-stu-id="e642c-116">A write-only stream interface into which an application writes print job data.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="e642c-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e642c-117">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="e642c-118">[Documents](./jobbindalldocuments.md) (Documenti)</span><span class="sxs-lookup"><span data-stu-id="e642c-118">[Documents](./jobbindalldocuments.md)</span></span>
</dt> <dt>

[<span data-ttu-id="e642c-119">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="e642c-119">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

