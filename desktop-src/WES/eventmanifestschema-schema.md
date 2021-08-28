---
title: EventManifest Schema
ms.assetid: 89acbc43-739b-4e89-a96a-cc3438ec8ecc
description: 'Altre informazioni su: Schema EventManifest'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8b282a3570c7ddc510f55c012a13b9438108693a3b6abba06de08ce1da59d734
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055849"
---
# <a name="eventmanifest-schema"></a>EventManifest Schema

Lo schema EventManifest definisce gli elementi e i tipi seguenti che si usano per scrivere un manifesto di strumentazione:

-   [Elementi EventManifestSchema](eventmanifestschema-elements.md)
-   [Tipi semplici EventManifestSchema](eventmanifestschema-simple-types.md)
-   [Tipi complessi EventManifestSchema](eventmanifestschema-complex-types.md)

La sezione elements contiene i nomi degli elementi che si usano nel manifesto. Tuttavia, per ottenere i dettagli per ogni elemento, vedere il tipo complesso che contiene l'elemento.

Un manifesto di strumentazione è un file XML che definisce un provider di eventi, i canali in cui vengono scritti gli eventi, gli eventi stessi, i criteri di filtro degli eventi come livelli, attività e codici operativo e le stringhe localizzate usate per il rendering degli eventi. La convenzione è usare .man come estensione per i file manifesto. Per informazioni dettagliate sulla scrittura di un manifesto, vedere [Scrittura di un manifesto di strumentazione.](writing-an-instrumentation-manifest.md)

L Windows SDK include lo schema nel \\ \\ file Include Eventman.xsd. È possibile usare lo schema XSD per convalidare il manifesto.

Oltre allo schema EventManifest, il Windows eventi definisce anche gli schemi seguenti:

-   [Schema di](eventschema-schema.md)eventi: definisce gli elementi e i tipi usati per eseguire il rendering di un evento.
-   [Schema di](queryschema-schema.md)query: definisce gli elementi e i tipi usati per scrivere una query per recuperare eventi da uno o più canali.

 

 




