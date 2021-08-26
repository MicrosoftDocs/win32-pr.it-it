---
title: Schema di eventi
ms.assetid: 36037697-b777-4e5c-99af-77964200a3e4
description: 'Altre informazioni su: Schema di eventi'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c08e22ad44cb1eec461ebe70361a8ee4640a7fdf5a7eb7040b2774a520be7a05
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119904361"
---
# <a name="event-schema"></a>Schema di eventi

Lo schema Event definisce gli elementi e i tipi seguenti che identificano gli elementi e gli attributi di un evento registrato:

-   [Elementi EventSchema](eventschema-elements.md)
-   [Tipi semplici EventSchema](eventschema-simple-types.md)
-   [Tipi complessi EventSchema](eventschema-complex-types.md)

La sezione elements contiene i nomi degli elementi che si trovano in un evento registrato. Tuttavia, per ottenere i dettagli per ogni elemento, vedere il tipo complesso che contiene l'elemento.

L Windows SDK include lo schema nel \\ \\ file Event.xsd di inclusione.

È possibile usare questo schema per identificare gli elementi e gli attributi quando si chiama la [**funzione EvtRender**](/windows/desktop/api/WinEvt/nf-winevt-evtrender) per eseguire il rendering di sezioni o proprietà specifiche dell'evento. Per un esempio che illustra come usare questo schema durante il rendering degli eventi, vedere [Eventi di rendering](rendering-events.md).

Oltre allo schema di eventi, Windows registro eventi definisce anche gli schemi seguenti:

-   [Schema EventManifest:](eventmanifestschema-schema.md)definisce gli elementi e i tipi usati per scrivere un manifesto di strumentazione.
-   [Schema di query:](queryschema-schema.md)definisce gli elementi e i tipi usati per scrivere una query per recuperare gli eventi da uno o più canali.

 

 




