---
description: I modelli di threading COM+ sono progettati intorno a una raccolta di oggetti denominata Apartment. Un Apartment è una raccolta di contesti contenuti in un processo.
ms.assetid: c73fb4c5-20ae-4873-afd2-4f40eb47bade
title: Modelli di threading COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5f07b065861c042e68add633368a9c8b8ba41b2
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/05/2021
ms.locfileid: "103761116"
---
# <a name="com-threading-models"></a>Modelli di threading COM+

I modelli di threading COM+ sono progettati intorno a una raccolta di oggetti denominata Apartment. Un Apartment è una raccolta di contesti contenuti in un processo, come illustrato nella figura seguente.

![Diagramma che mostra una raccolta di contesti in un'attività, all'interno di un Apartment, all'interno di un processo.](images/6b86fe3b-262a-483a-a418-67d60f9a5d68.png)

Le chiamate all'interno di un Apartment sono dirette, mentre le chiamate tra gli appartamenti (out-of-process) sono indirette e richiedono codice del proxy e dello stub. Gli Apartment consentono oggetti con diverse proprietà di sincronizzazione e rientranza e hanno due categorie: a thread singolo e multithreading. Gli oggetti in un Apartment a thread singolo (STA) vengono eseguiti sul thread specifico in cui sono stati creati. STAs consente l'esecuzione di un solo metodo alla volta. Sono progettate per le interfacce utente e si basano sulla coda di messaggi di Microsoft Windows per elaborare le chiamate in ingresso.

Gli oggetti in un Apartment a thread multipli (MTA) vengono eseguiti su qualsiasi thread e consentono l'esecuzione simultanea di un numero qualsiasi di metodi. Gli MTA supportano il reingresso in modo implicito.

Le classi COM+ sono contrassegnate con una proprietà **ThreadingModel** che consente a com+ di creare l'oggetto nell'Apartment appropriato. Per determinare in quale Apartment viene creato un oggetto, [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) utilizza la proprietà **ThreadingModel** .

I thread devono chiamare [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) prima di poter usare com+. In questo modo vengono creati all'interno dell'Apartment e del contesto corretti. L'Apartment del thread principale è determinato come il primo STA chiamato da **CoInitializeEx**. Questa operazione è in genere associata al thread principale di un processo. **CoInitializeEx** indica il tipo di Apartment richiesto dal thread impostando i flag seguenti:

-   **COinit \_ Multithreading**: individua il thread nel singolo Apartment a thread multipli.
-   **COinit \_ APARTMENTTHREADED**: inserisce il thread in un nuovo sta.

Negli argomenti seguenti di questa sezione vengono fornite ulteriori informazioni sull'utilizzo di modelli di threading e di Apartment in COM+:

-   [Attributo del modello di threading](threading-model-attribute.md)
-   [Appartamenti neutri](neutral-apartments.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Processi, thread e Apartment](/windows/desktop/com/processes--threads--and-apartments)
</dt> <dt>

[**ThreadingModel**](components.md)
</dt> </dl>

 

 
