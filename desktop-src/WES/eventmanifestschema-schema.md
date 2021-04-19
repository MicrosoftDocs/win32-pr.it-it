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
# <a name="eventmanifest-schema"></a>Schema EventManifest

Lo schema EventManifest definisce gli elementi e i tipi seguenti usati per scrivere un manifesto di strumentazione:

-   [Elementi EventManifestSchema](eventmanifestschema-elements.md)
-   [Tipi semplici EventManifestSchema](eventmanifestschema-simple-types.md)
-   [Tipi complessi EventManifestSchema](eventmanifestschema-complex-types.md)

La sezione Elements contiene i nomi degli elementi usati nel manifesto. Tuttavia, per ottenere i dettagli per ogni elemento, vedere il tipo complesso che contiene l'elemento.

Un manifesto di strumentazione è un file XML che definisce un provider di eventi, i canali in cui vengono scritti gli eventi, gli eventi stessi, i criteri di filtro degli eventi quali i livelli, le attività e i codici operativi e le stringhe localizzate utilizzate durante il rendering degli eventi. La convenzione prevede l'uso di. Man come estensione per i file manifesto. Per informazioni dettagliate sulla scrittura di un manifesto, vedere [scrittura di un manifesto di strumentazione](writing-an-instrumentation-manifest.md).

Il Windows SDK include lo schema nel \\ file include \\ eventIn. xsd. È possibile utilizzare XSD per convalidare il manifesto.

Oltre allo schema EventManifest, il registro eventi di Windows definisce anche gli schemi seguenti:

-   [Schema dell'evento](eventschema-schema.md): definisce gli elementi e i tipi utilizzati per il rendering di un evento.
-   [Schema di query](queryschema-schema.md): definisce gli elementi e i tipi utilizzati per scrivere una query per recuperare gli eventi da uno o più canali.

 

 




