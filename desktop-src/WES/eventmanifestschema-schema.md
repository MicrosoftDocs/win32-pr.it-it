---
title: Schema EventManifest
ms.assetid: 89acbc43-739b-4e89-a96a-cc3438ec8ecc
description: 'Altre informazioni su: schema EventManifest'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 67e1c2e9b769cd26e81a71853037655220a27d1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311845"
---
# <a name="eventmanifest-schema"></a><span data-ttu-id="53492-103">Schema EventManifest</span><span class="sxs-lookup"><span data-stu-id="53492-103">EventManifest Schema</span></span>

<span data-ttu-id="53492-104">Lo schema EventManifest definisce gli elementi e i tipi seguenti usati per scrivere un manifesto di strumentazione:</span><span class="sxs-lookup"><span data-stu-id="53492-104">The EventManifest schema defines the following elements and types that you use to write an instrumentation manifest:</span></span>

-   [<span data-ttu-id="53492-105">Elementi EventManifestSchema</span><span class="sxs-lookup"><span data-stu-id="53492-105">EventManifestSchema Elements</span></span>](eventmanifestschema-elements.md)
-   [<span data-ttu-id="53492-106">Tipi semplici EventManifestSchema</span><span class="sxs-lookup"><span data-stu-id="53492-106">EventManifestSchema Simple Types</span></span>](eventmanifestschema-simple-types.md)
-   [<span data-ttu-id="53492-107">Tipi complessi EventManifestSchema</span><span class="sxs-lookup"><span data-stu-id="53492-107">EventManifestSchema Complex Types</span></span>](eventmanifestschema-complex-types.md)

<span data-ttu-id="53492-108">La sezione Elements contiene i nomi degli elementi usati nel manifesto. Tuttavia, per ottenere i dettagli per ogni elemento, vedere il tipo complesso che contiene l'elemento.</span><span class="sxs-lookup"><span data-stu-id="53492-108">The elements section contains the names of the elements that you use in your manifest; however, to get the details for each element, see the complex type that contains the element.</span></span>

<span data-ttu-id="53492-109">Un manifesto di strumentazione è un file XML che definisce un provider di eventi, i canali in cui vengono scritti gli eventi, gli eventi stessi, i criteri di filtro degli eventi quali i livelli, le attività e i codici operativi e le stringhe localizzate utilizzate durante il rendering degli eventi.</span><span class="sxs-lookup"><span data-stu-id="53492-109">An instrumentation manifest is an XML file that defines an event provider, the channels to which the events are written, the events themselves, the event filtering criteria such as levels, tasks, and opcodes, and the localized strings used when rendering the events.</span></span> <span data-ttu-id="53492-110">La convenzione prevede l'uso di. Man come estensione per i file manifesto.</span><span class="sxs-lookup"><span data-stu-id="53492-110">The convention is to use .man as the extension for manifest files.</span></span> <span data-ttu-id="53492-111">Per informazioni dettagliate sulla scrittura di un manifesto, vedere [scrittura di un manifesto di strumentazione](writing-an-instrumentation-manifest.md).</span><span class="sxs-lookup"><span data-stu-id="53492-111">For details on writing a manifest, see [Writing an Instrumentation Manifest](writing-an-instrumentation-manifest.md).</span></span>

<span data-ttu-id="53492-112">Il Windows SDK include lo schema nel \\ file include \\ eventIn. xsd.</span><span class="sxs-lookup"><span data-stu-id="53492-112">The Windows SDK includes the schema in the \\Include\\Eventman.xsd file.</span></span> <span data-ttu-id="53492-113">È possibile utilizzare XSD per convalidare il manifesto.</span><span class="sxs-lookup"><span data-stu-id="53492-113">You can use the XSD to validate your manifest.</span></span>

<span data-ttu-id="53492-114">Oltre allo schema EventManifest, il registro eventi di Windows definisce anche gli schemi seguenti:</span><span class="sxs-lookup"><span data-stu-id="53492-114">In addition to the EventManifest schema, Windows Event Log also defines the following schemas:</span></span>

-   <span data-ttu-id="53492-115">[Schema dell'evento](eventschema-schema.md): definisce gli elementi e i tipi utilizzati per il rendering di un evento.</span><span class="sxs-lookup"><span data-stu-id="53492-115">[Event Schema](eventschema-schema.md)—defines the elements and types used to render an event.</span></span>
-   <span data-ttu-id="53492-116">[Schema di query](queryschema-schema.md): definisce gli elementi e i tipi utilizzati per scrivere una query per recuperare gli eventi da uno o più canali.</span><span class="sxs-lookup"><span data-stu-id="53492-116">[Query Schema](queryschema-schema.md)—defines the elements and types used to write a query to retrieve events from one or more channels.</span></span>

 

 




