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
# <a name="event-schema"></a>Schema di eventi

Lo schema dell'evento definisce gli elementi e i tipi seguenti che identificano gli elementi e gli attributi di un evento registrato:

-   [Elementi EventSchema](eventschema-elements.md)
-   [Tipi semplici EventSchema](eventschema-simple-types.md)
-   [Tipi complessi EventSchema](eventschema-complex-types.md)

La sezione Elements contiene i nomi degli elementi che si trovano in un evento registrato; Tuttavia, per ottenere i dettagli per ogni elemento, vedere il tipo complesso che contiene l'elemento.

Il Windows SDK include lo schema nel \\ file di inclusione \\ Event. xsd.

È possibile utilizzare questo schema per identificare gli elementi e gli attributi quando si chiama la funzione [**EvtRender**](/windows/desktop/api/WinEvt/nf-winevt-evtrender) per eseguire il rendering di sezioni o proprietà specifiche dell'evento. Per un esempio in cui viene illustrato come utilizzare questo schema durante il rendering degli eventi, vedere [rendering degli eventi](rendering-events.md).

Oltre allo schema di eventi, nel registro eventi di Windows vengono definiti anche gli schemi seguenti:

-   [Schema EventManifest](eventmanifestschema-schema.md): definisce gli elementi e i tipi utilizzati per scrivere un manifesto di strumentazione.
-   [Schema di query](queryschema-schema.md): definisce gli elementi e i tipi utilizzati per scrivere una query per recuperare gli eventi da uno o più canali.

 

 




