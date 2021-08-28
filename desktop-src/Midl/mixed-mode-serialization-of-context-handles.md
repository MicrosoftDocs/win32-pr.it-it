---
title: Serializzazione in modalità mista di handle di contesto
description: In Microsoft Windows XP una singola interfaccia può contenere handle di contesto serializzati e non serializzati, denominati serializzazione in modalità mista.
ms.assetid: b52c1d6f-cdc5-4597-a36e-bb957e4aab01
keywords:
- MidL language reference MIDL , serializzazione in modalità mista di handle di contesto
- il contesto gestisce MIDL
- MIDL di serializzazione in modalità mista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0aaa35f02a939a50e2484ace29630783ee219d6313d7538cba54b1f54cd83007
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119787431"
---
# <a name="mixed-mode-serialization-of-context-handles"></a>Serializzazione in modalità mista di handle di contesto

A partire da Windows XP, una singola interfaccia può contenere handle di contesto serializzati e non serializzati, consentendo a un metodo in un'interfaccia di accedere esclusivamente a un handle di contesto (serializzato), mentre altri metodi accedono a tale handle di contesto in modalità condivisa (non serializzata). Per altre informazioni sugli handle di contesto, vedere gli attributi seguenti:

-   [**handle di \_ contesto**](context-handle.md)
-   [**serializzazione \_ dell'handle \_ di contesto**](context-handle-serialize.md)
-   [**handle \_ di contesto \_ noserialize**](context-handle-noserialize.md)

Le funzionalità di accesso in modalità serializzata e condivisa sono paragonabili ai meccanismi di blocco in lettura/scrittura. I metodi che usano un handle di contesto serializzato sono utenti esclusivi (writer), mentre i metodi che usano un handle di contesto non serializzato sono utenti condivisi (lettori). I metodi che eliminano o modificano lo stato di un handle di contesto devono essere serializzati. I metodi che non modificano lo stato di un handle di contesto, ad esempio i metodi che semplicemente leggono da un handle di contesto, possono essere nonserializzati. L'uso di un handle di contesto in modalità mista può migliorare notevolmente la scalabilità di un server, soprattutto quando più thread eserciteranno chiamate simultanee allo stesso handle di contesto.

RPC non applica il "blocco di scrittura" ai metodi che usano un handle di contesto in modalità condivisa, il che significa che le applicazioni devono garantire che gli handle di contesto in modalità condivisa non vengano modificati. La modifica di un handle di contesto usato in modalità condivisa può causare lievi danneggiamenti del contenuto dell'handle di contesto, che non è possibile eseguire il debug.

La modifica della logica di serializzazione di un handle di contesto influisce solo sul server. Inoltre, la modifica della logica di serializzazione di un handle di contesto non influisce sul formato wire e pertanto le modifiche alla logica di serializzazione in un server non influiscono sulla capacità dei client esistenti di interagire con il server.

Non è consigliabile usare solo handle di contesto nonserializzati. I server che usano handle non serializzati devono passare all'accesso serializzato per il metodo che chiude l'handle di contesto.

Gli handle di contesto che sono out -only vengono in genere usati dai metodi \[ di creazione e non richiedono alcuna \] serializzazione. Pertanto, qualsiasi attributo di serializzazione applicato agli handle di contesto out-only, ad esempio la serializzazione dell'handle di contesto o \[ \] [**l'handle di contesto \_ \_ noserialize,**](context-handle-noserialize.md)viene ignorato da RPC. [**\_ \_**](context-handle-serialize.md)

> [!Note]  
> I metodi di creazione vengono serializzati in modo implicito.

 

## <a name="examples"></a>Esempio

I due esempi seguenti illustrano come abilitare la serializzazione in modalità mista degli handle di contesto.

Il primo esempio illustra come eseguire questa operazione nel file IDL:

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

Il secondo esempio illustra come abilitare la serializzazione in modalità mista degli handle di contesto nel file ACF:

``` syntax
typedef [context_handle_serialize] TestContextHandleExclusive;

typedef [context_handle_noserialize] TestContextHandleShared;
```

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**handle di \_ contesto**](context-handle.md)
</dt> <dt>

[**serializzazione \_ dell'handle \_ di contesto**](context-handle-serialize.md)
</dt> <dt>

[**handle \_ di contesto \_ noserialize**](context-handle-noserialize.md)
</dt> </dl>

 

 




