---
title: Query Schema
ms.assetid: 5710231b-5195-413e-8953-e47a411897a6
description: 'Altre informazioni su: Schema di query'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 14beeaf8c4d739e490de972107fedf279e16e75b5401f63a709d43b03c338c79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120005171"
---
# <a name="query-schema"></a>Query Schema

Lo schema di query definisce gli elementi e i tipi seguenti che è possibile usare per scrivere una query XML strutturata per recuperare eventi da un canale o da un file di log:

-   [Elementi QuerySchema](queryschema-elements.md)
-   [Tipi complessi QuerySchema](queryschema-complex-types.md)

La sezione elements contiene i nomi degli elementi utilizzati nella query. Tuttavia, per ottenere i dettagli per ogni elemento, vedere il tipo complesso che contiene l'elemento.

Una query può contenere una o più espressioni XPath usate per includere o escludere eventi nel set di risultati della query. È possibile eseguire query per gli eventi da più canali o file di log, ma non è possibile combinare canali e file di log. È possibile usare una query in qualsiasi funzione che accetta un XPath,ad esempio le funzioni [**EvtQuery**](/windows/desktop/api/WinEvt/nf-winevt-evtquery) o [**EvtSubscribe.**](/windows/desktop/api/WinEvt/nf-winevt-evtsubscribe) Ogni XPath specificato è limitato a 32 espressioni. Per un esempio, vedere [Utilizzo di eventi](consuming-events.md).

L Windows SDK include lo schema nel \\ \\ file Include Query.xsd.

Oltre allo schema query, il Windows eventi definisce anche gli schemi seguenti:

-   [Schema EventManifest:](eventmanifestschema-schema.md)definisce gli elementi e i tipi usati per scrivere un manifesto di strumentazione.
-   [Schema eventi:](eventschema-schema.md)definisce gli elementi e i tipi usati per eseguire il rendering di un evento.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Utilizzo di eventi](consuming-events.md)
</dt> </dl>

 

 




