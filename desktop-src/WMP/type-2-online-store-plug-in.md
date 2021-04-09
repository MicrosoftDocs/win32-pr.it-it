---
title: Plug-in per negozi online di tipo 2
description: Plug-in per negozi online di tipo 2
ms.assetid: 16e90a01-20be-49a6-96df-de81a7283f42
keywords:
- Windows Media Player Online Stores, plug-in
- archivi online, plug-in
- digitare 2 archivi online, plug-in
- Windows Media Player Online Stores, interfaccia IWMPSubscriptionService
- negozi online, interfaccia IWMPSubscriptionService
- tipi 2 negozi online, interfaccia IWMPSubscriptionService
- plug-in, archivi Windows Media Player online
- plug-in, archivi online
- plug-in, digitare 2 archivi online
- plug-in, interfaccia IWMPSubscriptionService
- Plug-in di Windows Media Player, digitare 2 archivi online
- Plug-in di Windows Media Player, archivi online
- Plug-in di Windows Media Player, archivi Windows Media Player online
- Plug-in di Windows Media Player, interfaccia IWMPSubscriptionService
- IWMPSubscriptionService
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6d2f3aeeaa7456c3452b498a1a728e24c96783c
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2020
ms.locfileid: "104117466"
---
# <a name="type-2-online-store-plug-in"></a>Plug-in per negozi online di tipo 2

Un plug-in di archivio online di tipo 2 è un componente COM che implementa l'interfaccia [IWMPSubscriptionService](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice) e, facoltativamente, l'interfaccia [IWMPSubscriptionService2](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice2) . Windows Media Player 9 chiama i metodi dell'interfaccia **IWMPSubscriptionService** . Windows Media Player 10 o versioni successive chiama i metodi delle interfacce **IWMPSubscriptionService** e **IWMPSubscriptionService2** .

Un plug-in di archiviazione di tipo 2 è incluso in un pacchetto come server COM in-process. Ovvero, il plug-in viene implementato in un file con estensione dll mappato al processo di Media Player di Windows.

Windows Media Player attiva i plug-in di tipo 2 Store online in base alle esigenze. Si supponga, ad esempio, che l'utente tenti di riprodurre un brano protetto e che non esista una licenza corrente per riprodurlo. In tal caso, Windows Media Player controlla l'attributo **contentdistributor** nell'intestazione del file o nell'intestazione DRM. Se esiste un valore che corrisponde al nome della chiave di un archivio online, Windows Media Player controlla il registro di sistema per verificare se l'archivio online ha fornito un plug-in di tipo 2. Se il plug-in esiste, Windows Media Player carica il plug-in e chiama i relativi metodi per determinare se l'utente dispone dei diritti per riprodurre il brano.

Nell'elenco seguente vengono descritti alcuni scenari in cui Windows Media Player chiama un plug-in di archiviazione di tipo 2 online.

-   **L'utente tenta di riprodurre il contenuto del negozio online.** Quando si verifica questa situazione, Windows Media Player chiama il metodo [IWMPSubscriptionService:: allowPlay](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowplay) del plug-in, passando un puntatore all'elemento multimediale digitale che l'utente sta tentando di riprodurre. Il negozio online può usarlo come opportunità per aggiornare la licenza dell'utente per riprodurre il contenuto o per non consentire la riproduzione. Se il plug-in restituisce **true** nel parametro *pfAllowPlay* , Windows Media Player tenta di riprodurre il contenuto. La riproduzione avrà esito negativo anche se non esiste una licenza valida; Questo processo non elude Digital Rights Management (DRM).
-   **L'utente richiede l'autorizzazione per masterizzare contenuto in un CD o DVD.** Quando si verifica questa situazione, Windows Media Player chiama il metodo [IWMPSubscriptionService:: allowCDBurn](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowcdburn) del plug-in.
-   **L'utente tenta di sincronizzare il contenuto dell'archivio online con un dispositivo o Windows Media Player è pronto per sincronizzare automaticamente il contenuto di un negozio online con un dispositivo.** Quando si verifica questa situazione, Windows Media Player chiama il metodo [IWMPSubscriptionService2::P repareforsync](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice2-prepareforsync) del plug-in per avvisare l'archivio online che un elemento multimediale sta per essere sincronizzato con un determinato dispositivo, identificato dal nome canonico. Si tratta di un'opportunità per l'archivio online per determinare se l'utente è autorizzato a sincronizzare l'elemento multimediale con il dispositivo. È anche un'opportunità per il negozio online di preparare il dispositivo per la sincronizzazione e aggiornare i record, ad esempio i conteggi della sincronizzazione, associati al dispositivo o all'elemento multimediale. Il plug-in deve passare le attività di autorizzazione, preparazione e conservazione dei record a un thread separato e restituire immediatamente un risultato da **prepareForSync**. Al termine del lavoro, il thread separato deve notificare a Windows Media Player chiamando [IWMPSubscriptionServiceCallback:: OnComplete](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservicecallback-oncomplete).
-   **Un dispositivo diventa disponibile per l'elaborazione in background.** Quando un dispositivo è connesso, Windows Media Player avvisa l'archivio online che il dispositivo è disponibile e inattivo chiamando [IWMPSubscriptionService2::D eviceavailable](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice2-deviceavailable).
-   **L'utente fa clic su un pulsante per attivare un archivio online in Windows Media Player.** Quando si verifica questa situazione, Windows Media Player chiama il metodo [IWMPSubscriptionService2:: serviceEvent](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice2-serviceevent) del plug-in. Windows Media Player chiama inoltre questo metodo quando l'utente passa a un altro servizio.
-   **Windows Media Player entra in uno stato di bassa attività.** Quando si verifica questo problema, il lettore chiama il metodo [IWMPSubscriptionService:: startBackgroundProcessing](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-startbackgroundprocessing) del plug-in. Il negozio online può usare questa opportunità per avviare o riattivare tutti i thread che eseguono attività in background, ad esempio il rinnovo di licenze scadute o la compilazione di dati di conteggio dei Play.
-   **Windows Media Player entra in uno stato di attività elevata.** Quando si verifica questa situazione, Windows Media Player chiama il metodo [IWMPSubscriptionService2:: stopBackgroundProcessing](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice2-stopbackgroundprocessing) del plug-in. In questo modo si informa il plug-in che deve sospendere tutti i thread che eseguono attività in background.

Windows Media Player rilascia il componente negozio online al termine della sessione del lettore. Al rilascio, il componente deve interrompere l'elaborazione in background in corso e quindi arrestare.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Interfaccia IWMPSubscriptionService**](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice)
</dt> <dt>

[**Interfaccia IWMPSubscriptionService2**](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice2)
</dt> <dt>

[**Interfaccia IWMPSubscriptionServiceCallback**](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservicecallback)
</dt> <dt>

[**Digitare 2 esempi di archivio online**](type-2-online-store-samples.md)
</dt> </dl>

 

 




