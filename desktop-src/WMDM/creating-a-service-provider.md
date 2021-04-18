---
title: Creazione di un provider di servizi
description: Creazione di un provider di servizi
ms.assetid: 7da27fe2-8a57-4adb-94b2-448b6362dc33
keywords:
- Windows Media Gestione dispositivi, creazione di provider di servizi
- Gestione dispositivi, creazione di provider di servizi
- Windows Media Gestione dispositivi, Guida alla programmazione
- Gestione dispositivi, Guida alla programmazione
- Guida per programmatori, provider di servizi
- Guida per programmatori, Windows Media Gestione dispositivi
- Guida per programmatori, creazione di provider di servizi
- Windows Media Gestione dispositivi, provider di servizi
- Gestione dispositivi, provider di servizi
- provider di servizi, creazione
- creazione di provider di servizi, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8469c3d656d151457ed818ea6b4192a3c79ed061
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106299890"
---
# <a name="creating-a-service-provider"></a>Creazione di un provider di servizi

Un provider di servizi è un componente che funge da intermediario tra un'applicazione e un dispositivo. Windows Media Gestione dispositivi instrada le richieste dall'applicazione al provider di servizi, che è quindi responsabile della comunicazione con il dispositivo o dell'esecuzione dell'azione richiesta. Un provider di servizi comunica in genere con un driver per consentire la comunicazione con il dispositivo. Un provider di servizi è un componente COM che implementa le interfacce chiamate da Windows Media Gestione dispositivi. L'interfaccia radice dell'oggetto provider di servizi è [**IMDServiceProvider**](/windows/desktop/api/mswmdm/nn-mswmdm-imdserviceprovider). Dopo aver ottenuto questa interfaccia, Windows Media Gestione dispositivi possibile ottenere altre interfacce tramite l'implementazione del provider di servizi di diversi metodi. Le interfacce che devono essere implementate da un provider di servizi sono elencate in [interfacce obbligatorie e facoltative](mandatory-and-optional-interfaces.md). La gerarchia delle interfacce viene visualizzata in [interfacce per i provider di servizi](interfaces-for-service-providers.md).

> [!Note]  
> Non provare a creare un provider di servizi MTP; è invece consigliabile usare il provider di servizi MTP e i driver forniti da Microsoft.

 

Prima di provare a creare un provider di servizi, è necessario comprendere in modo approfondito le chiamate effettuate da un'applicazione su un provider di servizi. Per informazioni sulle attività di base e sulle chiamate effettuate da un'applicazione su un provider di servizi durante il tentativo di comunicare con un dispositivo, vedere [creazione di un'applicazione Windows Media Gestione dispositivi](creating-a-windows-media-device-manager-application.md) .

Nell'elenco seguente vengono illustrati i passaggi principali per lo sviluppo di un provider di servizi:

1.  Includere (e, facoltativamente, compilare) i file di intestazione e di libreria necessari per il progetto. Per l'elenco dei file necessari, vedere le [librerie e le intestazioni obbligatorie per un provider di servizi](required-libraries-and-headers-for-a-service-provider.md) .
2.  Implementare tutte le altre interfacce del provider di servizi obbligatorie o facoltative (vedere [interfacce obbligatorie e facoltative](mandatory-and-optional-interfaces.md)). In genere, le interfacce verranno chiamate in questo ordine:
    -   [**IComponentAuthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate)
    -   [**IMDServiceProvider**](/windows/desktop/api/mswmdm/nn-mswmdm-imdserviceprovider)/2
    -   [**IMDSPEnumDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspenumdevice)
    -   [**IMDSPDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice)/2
    -   [**IMDSPEnumStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspenumstorage)
    -   [**IMDSPStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage)/2/3
3.  Verificare che il provider di servizi o il dispositivo installi le chiavi del registro di sistema appropriate durante l'installazione. Queste chiavi specificano i parametri del dispositivo, registrano il provider di servizi come plug-in e abilitano Plug and Play notifiche per l'arrivo e la rimozione dei dispositivi. Vedere [parametri del dispositivo](device-parameters.md), [registrazione del provider di servizi](registering-the-service-provider.md)e [Abilitazione di PNP per i dispositivi](enabling-pnp-for-devices.md).
4.  Quando si crea un'istanza della classe, autenticare il provider di servizi nel costruttore. A tale scopo, creare una classe [CSecureChannelServer](csecurechannelserver-class.md) e impostare il certificato. Implementare l'interfaccia [**IComponentAuthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) e chiamare i metodi della classe CSecureChannelServer di cui è stata creata un'istanza in precedenza. Per informazioni su come creare un'istanza della classe CSecureChannelServer e implementare i metodi IComponentAuthenticate, vedere [autenticazione del provider di servizi](authenticating-the-service-provider.md) .
5.  Windows Media Gestione dispositivi eseguirà una query sul provider di servizi per un elenco di dispositivi connessi chiamando [**IMDServiceProvider2:: CreateDevice**](/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider2-createdevice) o [**IMDServiceProvider:: EnumDevices**](/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider-enumdevices), a seconda che il provider di servizi gestisca plug and Play dispositivi. Il provider di servizi deve restituire un elenco di oggetti [**IMDSPDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice) che rappresentano i dispositivi connessi. Per altri dettagli, vedere [enumerazione dei dispositivi](enumerating-devices-service-provider.md) .
6.  Prima di gestire qualsiasi chiamata, verificare che sia stato stabilito un canale sicuro. Chiamare [**CSecureChannelServer:: fIsAuthenticated**](/previous-versions/bb231600(v=vs.85)) prima di eseguire qualsiasi azione. Se la chiamata ha esito negativo, restituire WMDM \_ E \_ NOTCERTIFIED.
7.  Per poter gestire il materiale protetto da DRM, sarà necessaria una coppia di certificati/chiavi rilasciata da Microsoft. Per ulteriori informazioni, vedere [gestione del contenuto protetto nel provider di servizi](handling-protected-content-in-the-service-provider.md) .
8.  Per consentire la sincronizzazione automatica del dispositivo con Windows Media Player, è necessario che soddisfi i requisiti indicati in [Abilitazione della sincronizzazione con windows media player](enabling-synchronization-with-windows-media-player.md).
9.  Per consentire la visualizzazione del dispositivo in Esplora risorse, è necessario eseguire alcuni passaggi speciali, descritti in dettaglio nei [requisiti per la visualizzazione dei lettori audio portatili in Esplora risorse](requirements-for-portable-audio-players-to-appear-in-windows-explorer.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Guida per programmatori**](programming-guide.md)
</dt> </dl>

 

 