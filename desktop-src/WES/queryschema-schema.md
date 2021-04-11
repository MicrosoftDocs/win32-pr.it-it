---
title: Schema di query
ms.assetid: 5710231b-5195-413e-8953-e47a411897a6
description: 'Altre informazioni su: schema di query'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: aa9b6c842ff7acd874e8e467d07c31e298a63564
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232920"
---
# <a name="query-schema"></a><span data-ttu-id="0476c-103">Schema di query</span><span class="sxs-lookup"><span data-stu-id="0476c-103">Query Schema</span></span>

<span data-ttu-id="0476c-104">Lo schema della query definisce gli elementi e i tipi seguenti che è possibile utilizzare per scrivere una query XML strutturata per recuperare eventi da un canale o un file di log:</span><span class="sxs-lookup"><span data-stu-id="0476c-104">The Query Schema defines the following elements and types that you can use to write a structured XML query to retrieve events from a channel or log file:</span></span>

-   [<span data-ttu-id="0476c-105">Elementi QuerySchema</span><span class="sxs-lookup"><span data-stu-id="0476c-105">QuerySchema Elements</span></span>](queryschema-elements.md)
-   [<span data-ttu-id="0476c-106">Tipi complessi QuerySchema</span><span class="sxs-lookup"><span data-stu-id="0476c-106">QuerySchema Complex Types</span></span>](queryschema-complex-types.md)

<span data-ttu-id="0476c-107">La sezione Elements contiene i nomi degli elementi utilizzati nella query. Tuttavia, per ottenere i dettagli per ogni elemento, vedere il tipo complesso che contiene l'elemento.</span><span class="sxs-lookup"><span data-stu-id="0476c-107">The elements section contains the names of the elements that you use in your query; however, to get the details for each element, see the complex type that contains the element.</span></span>

<span data-ttu-id="0476c-108">Una query può contenere una o più espressioni XPath utilizzate per includere o escludere l'evento nel set di risultati della query.</span><span class="sxs-lookup"><span data-stu-id="0476c-108">A query can contain one or more XPath expressions that are used to include or exclude event in the query result set.</span></span> <span data-ttu-id="0476c-109">È possibile eseguire una query per gli eventi da più canali o file di log, ma non è possibile combinare canali e file di log.</span><span class="sxs-lookup"><span data-stu-id="0476c-109">You can query for events from multiple channels or log files but you cannot mix channels and log files.</span></span> <span data-ttu-id="0476c-110">È possibile utilizzare una query in qualsiasi funzione che accetta un XPath (ad esempio, le funzioni [**EvtQuery**](/windows/desktop/api/WinEvt/nf-winevt-evtquery) o [**EvtSubscribe**](/windows/desktop/api/WinEvt/nf-winevt-evtsubscribe) ).</span><span class="sxs-lookup"><span data-stu-id="0476c-110">You can use a query in any function that takes an XPath (for example, the [**EvtQuery**](/windows/desktop/api/WinEvt/nf-winevt-evtquery) or [**EvtSubscribe**](/windows/desktop/api/WinEvt/nf-winevt-evtsubscribe) functions).</span></span> <span data-ttu-id="0476c-111">Ogni XPath specificato è limitato a 32 espressioni.</span><span class="sxs-lookup"><span data-stu-id="0476c-111">Each XPath that you specify is limited to 32 expressions.</span></span> <span data-ttu-id="0476c-112">Per un esempio, vedere [utilizzo degli eventi](consuming-events.md).</span><span class="sxs-lookup"><span data-stu-id="0476c-112">For an example, see [Consuming Events](consuming-events.md).</span></span>

<span data-ttu-id="0476c-113">Il Windows SDK include lo schema nel \\ file di inclusione \\ query. xsd.</span><span class="sxs-lookup"><span data-stu-id="0476c-113">The Windows SDK includes the schema in the \\Include\\Query.xsd file.</span></span>

<span data-ttu-id="0476c-114">Oltre allo schema di query, nel registro eventi di Windows vengono definiti anche gli schemi seguenti:</span><span class="sxs-lookup"><span data-stu-id="0476c-114">In addition to the Query schema, Windows Event Log also defines the following schemas:</span></span>

-   <span data-ttu-id="0476c-115">[Schema EventManifest](eventmanifestschema-schema.md): definisce gli elementi e i tipi utilizzati per scrivere un manifesto di strumentazione.</span><span class="sxs-lookup"><span data-stu-id="0476c-115">[EventManifest Schema](eventmanifestschema-schema.md)—defines the elements and types used to write an instrumentation manifest.</span></span>
-   <span data-ttu-id="0476c-116">[Schema dell'evento](eventschema-schema.md): definisce gli elementi e i tipi utilizzati per il rendering di un evento.</span><span class="sxs-lookup"><span data-stu-id="0476c-116">[Event Schema](eventschema-schema.md)—defines the elements and types used to render an event.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0476c-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0476c-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0476c-118">Utilizzo di eventi</span><span class="sxs-lookup"><span data-stu-id="0476c-118">Consuming Events</span></span>](consuming-events.md)
</dt> </dl>

 

 




