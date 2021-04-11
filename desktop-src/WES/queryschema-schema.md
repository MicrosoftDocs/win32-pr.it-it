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
# <a name="query-schema"></a>Schema di query

Lo schema della query definisce gli elementi e i tipi seguenti che è possibile utilizzare per scrivere una query XML strutturata per recuperare eventi da un canale o un file di log:

-   [Elementi QuerySchema](queryschema-elements.md)
-   [Tipi complessi QuerySchema](queryschema-complex-types.md)

La sezione Elements contiene i nomi degli elementi utilizzati nella query. Tuttavia, per ottenere i dettagli per ogni elemento, vedere il tipo complesso che contiene l'elemento.

Una query può contenere una o più espressioni XPath utilizzate per includere o escludere l'evento nel set di risultati della query. È possibile eseguire una query per gli eventi da più canali o file di log, ma non è possibile combinare canali e file di log. È possibile utilizzare una query in qualsiasi funzione che accetta un XPath (ad esempio, le funzioni [**EvtQuery**](/windows/desktop/api/WinEvt/nf-winevt-evtquery) o [**EvtSubscribe**](/windows/desktop/api/WinEvt/nf-winevt-evtsubscribe) ). Ogni XPath specificato è limitato a 32 espressioni. Per un esempio, vedere [utilizzo degli eventi](consuming-events.md).

Il Windows SDK include lo schema nel \\ file di inclusione \\ query. xsd.

Oltre allo schema di query, nel registro eventi di Windows vengono definiti anche gli schemi seguenti:

-   [Schema EventManifest](eventmanifestschema-schema.md): definisce gli elementi e i tipi utilizzati per scrivere un manifesto di strumentazione.
-   [Schema dell'evento](eventschema-schema.md): definisce gli elementi e i tipi utilizzati per il rendering di un evento.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Utilizzo di eventi](consuming-events.md)
</dt> </dl>

 

 




