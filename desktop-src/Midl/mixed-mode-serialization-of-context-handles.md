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
# <a name="mixed-mode-serialization-of-context-handles"></a><span data-ttu-id="aec7e-106">Serializzazione in modalità mista di handle di contesto</span><span class="sxs-lookup"><span data-stu-id="aec7e-106">Mixed Mode Serialization of Context Handles</span></span>

<span data-ttu-id="aec7e-107">A partire da Windows XP, una singola interfaccia può supportare sia gli handle di contesto serializzati che quelli non serializzati, consentendo a un metodo su un'interfaccia di accedere a un handle di contesto esclusivamente (serializzato), mentre altri metodi accedono a tale handle di contesto in modalità condivisa (non serializzato).</span><span class="sxs-lookup"><span data-stu-id="aec7e-107">Starting with Windows XP, a single interface can accommodate both serialized and nonserialized context handles, enabling one method on an interface to access a context handle exclusively (serialized), while other methods access that context handle in shared mode (nonserialized).</span></span> <span data-ttu-id="aec7e-108">Per ulteriori informazioni sugli handle di contesto, vedere i seguenti attributi:</span><span class="sxs-lookup"><span data-stu-id="aec7e-108">For more information about context handles, see the following attributes:</span></span>

-   [<span data-ttu-id="aec7e-109">**handle di contesto \_**</span><span class="sxs-lookup"><span data-stu-id="aec7e-109">**context\_handle**</span></span>](context-handle.md)
-   [<span data-ttu-id="aec7e-110">**\_serializzazione handle di contesto \_**</span><span class="sxs-lookup"><span data-stu-id="aec7e-110">**context\_handle\_serialize**</span></span>](context-handle-serialize.md)
-   [<span data-ttu-id="aec7e-111">**gestore del contesto \_ \_ noserialize**</span><span class="sxs-lookup"><span data-stu-id="aec7e-111">**context\_handle\_noserialize**</span></span>](context-handle-noserialize.md)

<span data-ttu-id="aec7e-112">Le funzionalità di accesso in modalità condivisa e serializzata sono paragonabili ai meccanismi di blocco in lettura/scrittura. i metodi che usano un handle di contesto serializzato sono utenti esclusivi (writer), mentre i metodi che usano un handle di contesto non serializzato sono utenti condivisi (lettori).</span><span class="sxs-lookup"><span data-stu-id="aec7e-112">Serialized and shared mode access capabilities are comparable to read/write locking mechanisms; methods using a serialized context handle are exclusive users (writers), whereas methods using a nonserialized context handle are shared users (readers).</span></span> <span data-ttu-id="aec7e-113">I metodi che eliminano o modificano lo stato di un handle di contesto devono essere serializzati.</span><span class="sxs-lookup"><span data-stu-id="aec7e-113">Methods that destroy or modify the state of a context handle must be serialized.</span></span> <span data-ttu-id="aec7e-114">I metodi che non modificano lo stato di un handle di contesto, ad esempio i metodi che leggono semplicemente da un handle di contesto, possono essere non serializzati.</span><span class="sxs-lookup"><span data-stu-id="aec7e-114">Methods that do not modify the state of a context handle, such as those methods that simply read from a context handle, can be nonserialized.</span></span> <span data-ttu-id="aec7e-115">L'utilizzo di un handle di contesto in modalità mista può migliorare notevolmente la scalabilità di un server, soprattutto quando più thread effettuano chiamate simultanee allo stesso handle di contesto.</span><span class="sxs-lookup"><span data-stu-id="aec7e-115">Using a context handle in mixed mode can substantially improve the scalability of a server, especially when multiple threads make simultaneous calls to the same context handle.</span></span>

<span data-ttu-id="aec7e-116">RPC non impone il "blocco di scrittura" nei metodi che usano un handle di contesto in modalità condivisa, quindi le applicazioni devono garantire che gli handle del contesto in modalità condivisa non vengano modificati.</span><span class="sxs-lookup"><span data-stu-id="aec7e-116">RPC does not enforce "write lock" on methods using a context handle in shared mode, which means applications must ensure that shared mode context handles are not modified.</span></span> <span data-ttu-id="aec7e-117">La modifica di un handle di contesto utilizzato in modalità condivisa può comportare un lieve danneggiamento del contenuto della gestione del contesto, che non è possibile eseguire il debug.</span><span class="sxs-lookup"><span data-stu-id="aec7e-117">Modification of a context handle used in shared mode can result in subtle corruptions of context handle contents, which are impossible to debug.</span></span>

<span data-ttu-id="aec7e-118">La modifica della logica di serializzazione di un handle di contesto influiscono solo sul server.</span><span class="sxs-lookup"><span data-stu-id="aec7e-118">Changing the serialization logic of a context handle affects only the server.</span></span> <span data-ttu-id="aec7e-119">Inoltre, la modifica della logica di serializzazione di un handle di contesto non influisce sul formato wire e pertanto le modifiche apportate alla logica di serializzazione in un server non influiscono sulla capacità dei client esistenti di interagire con il server.</span><span class="sxs-lookup"><span data-stu-id="aec7e-119">Also, changing the serialization logic of a context handle does not affect the wire format, and therefore, changes to serialization logic on a server do not affect existing clients' capability to interact with the server.</span></span>

<span data-ttu-id="aec7e-120">Non è consigliabile usare solo handle di contesto non serializzati.</span><span class="sxs-lookup"><span data-stu-id="aec7e-120">Using only nonserialized context handles is not recommended.</span></span> <span data-ttu-id="aec7e-121">I server che utilizzano handle non serializzati devono passare all'accesso serializzato per il metodo che chiude l'handle del contesto.</span><span class="sxs-lookup"><span data-stu-id="aec7e-121">Servers that use nonserialized handles are should switch to serialized access for the method that closes the context handle.</span></span>

<span data-ttu-id="aec7e-122">Gli handle di contesto \[ \] solo in uscita vengono in genere utilizzati dai metodi di creazione e non richiedono alcuna serializzazione.</span><span class="sxs-lookup"><span data-stu-id="aec7e-122">Context handles that are \[out\]-only are typically used by creation methods, and do not require any serialization.</span></span> <span data-ttu-id="aec7e-123">Pertanto, qualsiasi attributo di serializzazione applicato agli \[ \] handle del contesto di sola uscita, ad esempio la [**\_ \_ serializzazione**](context-handle-serialize.md) dell'handle del contesto o l' [**handle di contesto \_ \_ noserialize**](context-handle-noserialize.md), viene ignorato da RPC.</span><span class="sxs-lookup"><span data-stu-id="aec7e-123">Therefore, any serialization attribute applied to \[out\]-only context handles, such as [**context\_handle\_serialize**](context-handle-serialize.md) or [**context\_handle\_noserialize**](context-handle-noserialize.md), is ignored by RPC.</span></span>

> [!Note]  
> <span data-ttu-id="aec7e-124">I metodi di creazione vengono serializzati in modo implicito.</span><span class="sxs-lookup"><span data-stu-id="aec7e-124">Creation methods are implicitly serialized.</span></span>

 

## <a name="examples"></a><span data-ttu-id="aec7e-125">Esempio</span><span class="sxs-lookup"><span data-stu-id="aec7e-125">Examples</span></span>

<span data-ttu-id="aec7e-126">Nei due esempi seguenti viene illustrato come abilitare la serializzazione in modalità mista degli handle di contesto.</span><span class="sxs-lookup"><span data-stu-id="aec7e-126">The following two examples show how to enable mixed mode serialization of context handles.</span></span>

<span data-ttu-id="aec7e-127">Nel primo esempio viene illustrato come eseguire questa operazione nel file IDL:</span><span class="sxs-lookup"><span data-stu-id="aec7e-127">The first example shows how to do so in the IDL file:</span></span>

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

<span data-ttu-id="aec7e-128">Nel secondo esempio viene illustrato come abilitare la serializzazione in modalità mista degli handle di contesto nel file ACF:</span><span class="sxs-lookup"><span data-stu-id="aec7e-128">The second example shows how to enable mixed mode serialization of context handles in the ACF file:</span></span>

``` syntax
typedef [context_handle_serialize] TestContextHandleExclusive;

typedef [context_handle_noserialize] TestContextHandleShared;
```

## <a name="related-topics"></a><span data-ttu-id="aec7e-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="aec7e-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aec7e-130">**handle di contesto \_**</span><span class="sxs-lookup"><span data-stu-id="aec7e-130">**context\_handle**</span></span>](context-handle.md)
</dt> <dt>

[<span data-ttu-id="aec7e-131">**\_serializzazione handle di contesto \_**</span><span class="sxs-lookup"><span data-stu-id="aec7e-131">**context\_handle\_serialize**</span></span>](context-handle-serialize.md)
</dt> <dt>

[<span data-ttu-id="aec7e-132">**gestore del contesto \_ \_ noserialize**</span><span class="sxs-lookup"><span data-stu-id="aec7e-132">**context\_handle\_noserialize**</span></span>](context-handle-noserialize.md)
</dt> </dl>

 

 




