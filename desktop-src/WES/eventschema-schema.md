---
title: Schema di eventi
ms.assetid: 36037697-b777-4e5c-99af-77964200a3e4
description: 'Altre informazioni su: schema di eventi'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bfb26f6c71d544e0c0a6a4d833b40a5d15ae5485
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881622"
---
# <a name="event-schema"></a><span data-ttu-id="e7824-103">Schema di eventi</span><span class="sxs-lookup"><span data-stu-id="e7824-103">Event Schema</span></span>

<span data-ttu-id="e7824-104">Lo schema dell'evento definisce gli elementi e i tipi seguenti che identificano gli elementi e gli attributi di un evento registrato:</span><span class="sxs-lookup"><span data-stu-id="e7824-104">The Event schema defines the following elements and types that identify the elements and attributes of a logged event:</span></span>

-   [<span data-ttu-id="e7824-105">Elementi EventSchema</span><span class="sxs-lookup"><span data-stu-id="e7824-105">EventSchema Elements</span></span>](eventschema-elements.md)
-   [<span data-ttu-id="e7824-106">Tipi semplici EventSchema</span><span class="sxs-lookup"><span data-stu-id="e7824-106">EventSchema Simple Types</span></span>](eventschema-simple-types.md)
-   [<span data-ttu-id="e7824-107">Tipi complessi EventSchema</span><span class="sxs-lookup"><span data-stu-id="e7824-107">EventSchema Complex Types</span></span>](eventschema-complex-types.md)

<span data-ttu-id="e7824-108">La sezione Elements contiene i nomi degli elementi che si trovano in un evento registrato; Tuttavia, per ottenere i dettagli per ogni elemento, vedere il tipo complesso che contiene l'elemento.</span><span class="sxs-lookup"><span data-stu-id="e7824-108">The elements section contains the names of the elements that you would find in a logged events; however, to get the details for each element, see the complex type that contains the element.</span></span>

<span data-ttu-id="e7824-109">Il Windows SDK include lo schema nel \\ file di inclusione \\ Event. xsd.</span><span class="sxs-lookup"><span data-stu-id="e7824-109">The Windows SDK includes the schema in the \\Include\\Event.xsd file.</span></span>

<span data-ttu-id="e7824-110">È possibile utilizzare questo schema per identificare gli elementi e gli attributi quando si chiama la funzione [**EvtRender**](/windows/desktop/api/WinEvt/nf-winevt-evtrender) per eseguire il rendering di sezioni o proprietà specifiche dell'evento.</span><span class="sxs-lookup"><span data-stu-id="e7824-110">You can use this schema to identify the elements and attributes when calling the [**EvtRender**](/windows/desktop/api/WinEvt/nf-winevt-evtrender) function to render specific sections or properties of the event.</span></span> <span data-ttu-id="e7824-111">Per un esempio in cui viene illustrato come utilizzare questo schema durante il rendering degli eventi, vedere [rendering degli eventi](rendering-events.md).</span><span class="sxs-lookup"><span data-stu-id="e7824-111">For an example that shows how to use this schema when rendering events, see [Rendering Events](rendering-events.md).</span></span>

<span data-ttu-id="e7824-112">Oltre allo schema di eventi, nel registro eventi di Windows vengono definiti anche gli schemi seguenti:</span><span class="sxs-lookup"><span data-stu-id="e7824-112">In addition to the Event schema, Windows Event Log also defines the following schemas:</span></span>

-   <span data-ttu-id="e7824-113">[Schema EventManifest](eventmanifestschema-schema.md): definisce gli elementi e i tipi utilizzati per scrivere un manifesto di strumentazione.</span><span class="sxs-lookup"><span data-stu-id="e7824-113">[EventManifest Schema](eventmanifestschema-schema.md)—defines the elements and types used to write an instrumentation manifest.</span></span>
-   <span data-ttu-id="e7824-114">[Schema di query](queryschema-schema.md): definisce gli elementi e i tipi utilizzati per scrivere una query per recuperare gli eventi da uno o più canali.</span><span class="sxs-lookup"><span data-stu-id="e7824-114">[Query Schema](queryschema-schema.md)—defines the elements and types used to write a query to retrieve events from one or more channels.</span></span>

 

 




