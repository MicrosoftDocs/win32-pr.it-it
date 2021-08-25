---
description: I modelli di threading COM+ sono progettati in base a una raccolta di oggetti denominata apartment. Un apartment è una raccolta di contesti contenuti in un processo.
ms.assetid: c73fb4c5-20ae-4873-afd2-4f40eb47bade
title: Modelli di threading COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd0949a27291be43b5981f24f4985fac6911937b2c9fa85785b4d662bd1bf546
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119793677"
---
# <a name="com-threading-models"></a>Modelli di threading COM+

I modelli di threading COM+ sono progettati in base a una raccolta di oggetti denominata apartment. Un apartment è una raccolta di contesti contenuti in un processo, come illustrato nella figura seguente.

![Diagramma che mostra una raccolta di contesti in un'attività, all'interno di un apartment, all'interno di un processo.](images/6b86fe3b-262a-483a-a418-67d60f9a5d68.png)

Le chiamate all'interno di un apartment sono dirette, mentre le chiamate tra apartment (out-of-process) sono indirette e richiedono codice proxy e stub. Gli apartment consentono oggetti con proprietà di sincronizzazione e reentrancy diverse e hanno due categorie: a thread singolo e multithreading. Gli oggetti in un apartment a thread singolo (STA) vengono eseguiti nel thread specifico in cui sono stati creati. Gli stA consentono l'esecuzione di un solo metodo alla volta. Sono progettati per le interfacce utente e si basano su Microsoft Windows coda di messaggi per elaborare le chiamate in ingresso.

Gli oggetti in un apartment a thread multipla (MTA) vengono eseguiti su qualsiasi thread e consentono l'esecuzione simultanea di un numero qualsiasi di metodi. Gli mta supportano la reentrance in modo implicito.

Le classi COM+ sono contrassegnate con **una proprietà ThreadingModel** che consente a COM+ di creare l'oggetto nell'apartment appropriato. Per determinare in quale apartment viene creato un oggetto, [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) usa la **proprietà ThreadingModel.**

I thread devono [**chiamare CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) prima di poter usare COM+. In questo modo vengono creati all'interno dell'apartment e del contesto corretti. L'apartment del thread principale è determinato come il primo STA chiamato da **CoInitializeEx.** Questa operazione è in genere associata al thread principale di un processo. **CoInitializeEx** indica il tipo di apartment richiesto dal thread impostando i flag seguenti:

-   **COINIT \_ MULTITHREADED:** individua il thread nel singolo apartment multithreading.
-   **COINIT \_ APARTMENTTHREADED:** inserisce il thread in un nuovo sta.

Negli argomenti seguenti di questa sezione vengono fornite ulteriori informazioni sull'uso di modelli di threading e apartment in COM+:

-   [Attributo del modello di threading](threading-model-attribute.md)
-   [Neutral Apartment](neutral-apartments.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Processi, thread e apartment](/windows/desktop/com/processes--threads--and-apartments)
</dt> <dt>

[**Threadingmodel**](components.md)
</dt> </dl>

 

 
