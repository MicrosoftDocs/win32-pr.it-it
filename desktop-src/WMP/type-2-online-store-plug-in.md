---
title: Plug-in per negozi online di tipo 2
description: Plug-in per negozi online di tipo 2
ms.assetid: 16e90a01-20be-49a6-96df-de81a7283f42
keywords:
- Windows Media Player store online, plug-in
- online store, plug-in
- store online di tipo 2, plug-in
- Windows Media Player store online, interfaccia IWMPSubscriptionService
- online store, interfaccia IWMPSubscriptionService
- Tipo 2 store online, interfaccia IWMPSubscriptionService
- plug-in, Windows Media Player online store
- plug-in, negozi online
- plug-in, tipo 2 negozi online
- plug-in, interfaccia IWMPSubscriptionService
- Windows Media Player plug-in, digitare 2 store online
- Windows Media Player plug-in, negozi online
- Windows Media Player plug-in, Windows Media Player store online
- Windows Media Player plug-in, interfaccia IWMPSubscriptionService
- IWMPSubscriptionService
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a254fe0aeed0d03f4437c408f4c00c181fdeb07cf75df8ff9d7a1139ea284150
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118117478"
---
# <a name="type-2-online-store-plug-in"></a>Plug-in per negozi online di tipo 2

Un plug-in dello store online di tipo 2 è un componente COM che implementa [l'interfaccia IWMPSubscriptionService](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice) e, facoltativamente, [l'interfaccia IWMPSubscriptionService2.](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice2) Windows Media Player 9 chiama i metodi **dell'interfaccia IWMPSubscriptionService.** Windows Media Player 10 o versioni successive chiama i metodi delle interfacce **IWMPSubscriptionService** e **IWMPSubscriptionService2.**

Un plug-in del negozio online di tipo 2 viene inserito in un pacchetto come server COM in-process. Ciò significa che il plug-in viene implementato in un file .dll mappato al Windows Media Player processo.

Windows Media Player attiva plug-in del negozio online di tipo 2 in base alle esigenze. Si supponga, ad esempio, che l'utente tenti di riprodurre un brano protetto e che non vi sia alcuna licenza corrente per riprodurlo. In tal caso, Windows Media Player **l'attributo ContentDistributor** nell'intestazione del file o nell'intestazione DRM. Se esiste un valore che corrisponde al nome della chiave di un negozio online, Windows Media Player controlla il Registro di sistema per verificare se tale negozio online ha fornito un plug-in di tipo 2. Se il plug-in esiste, Windows Media Player carica il plug-in e chiama i relativi metodi per determinare se l'utente dispone dei diritti per riprodurre il brano.

L'elenco seguente descrive alcuni degli scenari in cui Windows Media Player chiama un plug-in del negozio online di tipo 2.

-   **L'utente tenta di riprodurre il contenuto dello store online.** In questo caso, Windows Media Player chiama il metodo [IWMPSubscriptionService::allowPlay](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowplay) del plug-in, passando un puntatore all'elemento multimediale digitale che l'utente sta tentando di riprodurre. Lo Store online può usarlo come opportunità per aggiornare la licenza dell'utente per riprodurre il contenuto o per non consentire la riproduzione. Se il plug-in restituisce **TRUE** nel *parametro pfAllowPlay,* Windows Media Player prova a riprodurre il contenuto. La riproduzione avrà comunque esito negativo se non esiste una licenza valida. questo processo non elude la gestione dei diritti digitali (DRM).
-   **L'utente richiede l'autorizzazione per masterizzare il contenuto in un CD o DVD.** In questo caso, Windows Media Player chiama il metodo [IWMPSubscriptionService::allowCD Plugin del](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowcdburn) plug-in.
-   **L'utente tenta di sincronizzare il contenuto dello store online con un dispositivo o Windows Media Player è pronto per sincronizzare automaticamente il contenuto dello store online con un dispositivo.** In questo caso, Windows Media Player chiama il metodo [IWMPSubscriptionService2::p repareForSync](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice2-prepareforsync) del plug-in per avvisare lo store online che un elemento multimediale sta per essere sincronizzato con un particolare dispositivo, identificato dal nome canonico. Si tratta di un'opportunità per lo store online di determinare se l'utente è autorizzato a sincronizzare l'elemento multimediale con il dispositivo. Lo store online può anche preparare il dispositivo per la sincronizzazione e aggiornare i record, ad esempio i conteggi di sincronizzazione, associati al dispositivo o all'elemento multimediale. Il plug-in deve passare le attività di autorizzazione, preparazione e conservazione dei record a un thread separato e restituire immediatamente **da prepareForSync**. Al termine del lavoro, il thread separato deve inviare una notifica Windows Media Player chiamando [IWMPSubscriptionServiceCallback::onComplete.](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservicecallback-oncomplete)
-   **Un dispositivo diventa disponibile per l'elaborazione in background.** Quando un dispositivo è connesso, Windows Media Player segnala al negozio online che il dispositivo è disponibile e inattivo chiamando [IWMPSubscriptionService2::d eviceAvailable](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice2-deviceavailable).
-   **L'utente fa clic su un pulsante per attivare un negozio online in Windows Media Player.** In questo caso, Windows Media Player chiama il metodo [IWMPSubscriptionService2::serviceEvent del](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice2-serviceevent) plug-in. Windows Media Player chiama anche questo metodo quando l'utente passa a un altro servizio.
-   **Windows Media Player immette uno stato di attività bassa.** In questo caso, player chiama il metodo [IWMPSubscriptionService::startBackgroundProcessing del](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-startbackgroundprocessing) plug-in. Lo store online può usare questa opportunità per avviare o riattivare tutti i thread che eseguono attività in background, ad esempio il rinnovo delle licenze scadute o la compilazione di dati di conteggio di riproduzione.
-   **Windows Media Player immette uno stato di attività elevata.** In questo caso, Windows Media Player chiama il metodo [IWMPSubscriptionService2::stopBackgroundProcessing del](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice2-stopbackgroundprocessing) plug-in. In questo modo si informa il plug-in che deve sospendere tutti i thread che eseguono attività in background.

Windows Media Player rilascia il componente store online al termine della sessione del lettore. Al momento del rilascio, il componente deve interrompere qualsiasi elaborazione in background in corso e quindi arrestarsi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Interfaccia IWMPSubscriptionService**](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice)
</dt> <dt>

[**Interfaccia IWMPSubscriptionService2**](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice2)
</dt> <dt>

[**Interfaccia IWMPSubscriptionServiceCallback**](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservicecallback)
</dt> <dt>

[**Esempi di store online di tipo 2**](type-2-online-store-samples.md)
</dt> </dl>

 

 




