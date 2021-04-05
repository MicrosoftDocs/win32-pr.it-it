---
title: Serializzazione in modalità mista di handle di contesto
description: In Microsoft Windows XP, una singola interfaccia può supportare sia gli handle di contesto serializzati che quelli non serializzati, denominati serializzazione in modalità mista.
ms.assetid: b52c1d6f-cdc5-4597-a36e-bb957e4aab01
keywords:
- Riferimento al linguaggio MIDL MIDL, serializzazione in modalità mista di handle di contesto
- gestione del contesto MIDL
- serializzazione in modalità mista MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0922b53bfc7ba2e30ad8df0764e3cf9a36f0f723
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856077"
---
# <a name="mixed-mode-serialization-of-context-handles"></a>Serializzazione in modalità mista di handle di contesto

A partire da Windows XP, una singola interfaccia può supportare sia gli handle di contesto serializzati che quelli non serializzati, consentendo a un metodo su un'interfaccia di accedere a un handle di contesto esclusivamente (serializzato), mentre altri metodi accedono a tale handle di contesto in modalità condivisa (non serializzato). Per ulteriori informazioni sugli handle di contesto, vedere i seguenti attributi:

-   [**handle di contesto \_**](context-handle.md)
-   [**\_serializzazione handle di contesto \_**](context-handle-serialize.md)
-   [**gestore del contesto \_ \_ noserialize**](context-handle-noserialize.md)

Le funzionalità di accesso in modalità condivisa e serializzata sono paragonabili ai meccanismi di blocco in lettura/scrittura. i metodi che usano un handle di contesto serializzato sono utenti esclusivi (writer), mentre i metodi che usano un handle di contesto non serializzato sono utenti condivisi (lettori). I metodi che eliminano o modificano lo stato di un handle di contesto devono essere serializzati. I metodi che non modificano lo stato di un handle di contesto, ad esempio i metodi che leggono semplicemente da un handle di contesto, possono essere non serializzati. L'utilizzo di un handle di contesto in modalità mista può migliorare notevolmente la scalabilità di un server, soprattutto quando più thread effettuano chiamate simultanee allo stesso handle di contesto.

RPC non impone il "blocco di scrittura" nei metodi che usano un handle di contesto in modalità condivisa, quindi le applicazioni devono garantire che gli handle del contesto in modalità condivisa non vengano modificati. La modifica di un handle di contesto utilizzato in modalità condivisa può comportare un lieve danneggiamento del contenuto della gestione del contesto, che non è possibile eseguire il debug.

La modifica della logica di serializzazione di un handle di contesto influiscono solo sul server. Inoltre, la modifica della logica di serializzazione di un handle di contesto non influisce sul formato wire e pertanto le modifiche apportate alla logica di serializzazione in un server non influiscono sulla capacità dei client esistenti di interagire con il server.

Non è consigliabile usare solo handle di contesto non serializzati. I server che utilizzano handle non serializzati devono passare all'accesso serializzato per il metodo che chiude l'handle del contesto.

Gli handle di contesto \[ \] solo in uscita vengono in genere utilizzati dai metodi di creazione e non richiedono alcuna serializzazione. Pertanto, qualsiasi attributo di serializzazione applicato agli \[ \] handle del contesto di sola uscita, ad esempio la [**\_ \_ serializzazione**](context-handle-serialize.md) dell'handle del contesto o l' [**handle di contesto \_ \_ noserialize**](context-handle-noserialize.md), viene ignorato da RPC.

> [!Note]  
> I metodi di creazione vengono serializzati in modo implicito.

 

## <a name="examples"></a>Esempio

Nei due esempi seguenti viene illustrato come abilitare la serializzazione in modalità mista degli handle di contesto.

Nel primo esempio viene illustrato come eseguire questa operazione nel file IDL:

``` syntax
typedef [context_handle] void *TestContextHandleExclusive;
typedef [context_handle] TestContextHandleExclusive TestContextHandleShared;

void
UseShared(...
          [in] TestContextHandleShared *Ctx,
          ...);

void
UseExclusive(...
             [in, out] TestContextHandleExclusive *Ctx,
             ...);
```

Nel secondo esempio viene illustrato come abilitare la serializzazione in modalità mista degli handle di contesto nel file ACF:

``` syntax
typedef [context_handle_serialize] TestContextHandleExclusive;

typedef [context_handle_noserialize] TestContextHandleShared;
```

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**handle di contesto \_**](context-handle.md)
</dt> <dt>

[**\_serializzazione handle di contesto \_**](context-handle-serialize.md)
</dt> <dt>

[**gestore del contesto \_ \_ noserialize**](context-handle-noserialize.md)
</dt> </dl>

 

 




