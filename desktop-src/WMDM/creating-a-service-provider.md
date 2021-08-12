---
title: Creazione di un provider di servizi
description: Creazione di un provider di servizi
ms.assetid: 7da27fe2-8a57-4adb-94b2-448b6362dc33
keywords:
- Windows Gestione dispositivi multimediali, creazione di provider di servizi
- Gestione dispositivi, creazione di provider di servizi
- Windows Gestione dispositivi multimediali, guida alla programmazione
- Gestione dispositivi, guida alla programmazione
- guida per programmatori, provider di servizi
- Guida per programmatori, Windows Gestione dispositivi multimediali
- guida per programmatori, creazione di provider di servizi
- Windows Gestione dispositivi multimediali, provider di servizi
- Gestione dispositivi, provider di servizi
- provider di servizi, creazione
- creazione di provider di servizi, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc1f5b6abfba6b143e0a8ab7913ed1c1f53bbdeb3104a6a8450e438843349598
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118585855"
---
# <a name="creating-a-service-provider"></a>Creazione di un provider di servizi

Un provider di servizi è un componente che funge da intermediario tra un'applicazione e un dispositivo. Windows Gestione dispositivi multimediali indirizza le richieste dall'applicazione al provider di servizi, che è quindi responsabile della comunicazione con il dispositivo o dell'esecuzione dell'azione richiesta. Un provider di servizi comunica in genere con un driver per abilitare la comunicazione con il dispositivo. Un provider di servizi è un componente COM che implementa le interfacce chiamate Windows Gestione dispositivi multimediali. L'interfaccia radice dell'oggetto provider di servizi è [**IMDServiceProvider.**](/windows/desktop/api/mswmdm/nn-mswmdm-imdserviceprovider) Dopo aver ottenuto questa interfaccia, Windows Gestione dispositivi multimediali può ottenere altre interfacce tramite l'implementazione di vari metodi da parte del provider di servizi. Le interfacce che un provider di servizi deve implementare sono elencate in [Interfacce obbligatorie e facoltative](mandatory-and-optional-interfaces.md). La gerarchia delle interfacce è illustrata in [Interfacce per i provider di servizi](interfaces-for-service-providers.md).

> [!Note]  
> Non è consigliabile provare a creare un provider di servizi MTP. è invece consigliabile usare il provider di servizi MTP e i driver forniti da Microsoft.

 

Prima di provare a creare un provider di servizi, è necessario comprendere in modo approfondito le chiamate che verranno effettuate da un'applicazione su un provider di servizi. Leggere [Creazione di un'applicazione](creating-a-windows-media-device-manager-application.md) di Gestione dispositivi multimediali Windows per avere un'idea delle attività di base e delle chiamate che un'applicazione farà su un provider di servizi quando tenta di comunicare con un dispositivo.

L'elenco seguente illustra i passaggi principali per lo sviluppo di un provider di servizi:

1.  Includere (e facoltativamente compilare) i file di intestazione e di libreria necessari per il progetto. Per [l'elenco dei file necessari, vedere](required-libraries-and-headers-for-a-service-provider.md) Librerie e intestazioni necessarie per un provider di servizi.
2.  Implementare tutte le altre interfacce del provider di servizi obbligatori o facoltative (vedere [Interfacce obbligatorie e facoltative](mandatory-and-optional-interfaces.md)). In genere, le interfacce vengono chiamate nell'ordine seguente:
    -   [**IComponentAuthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate)
    -   [**ImDServiceProvider**](/windows/desktop/api/mswmdm/nn-mswmdm-imdserviceprovider)/2
    -   [**IMDSPEnumDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspenumdevice)
    -   [**IMDSPDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice)/2
    -   [**IMDSPEnumStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspenumstorage)
    -   [**IMDSPStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage)/2/3
3.  Assicurarsi che il provider di servizi o il dispositivo installi le chiavi del Registro di sistema appropriate durante l'installazione. Queste chiavi specificano i parametri del dispositivo, registrano il provider di servizi come plug-in e Plug and Play notifiche per l'arrivo e la rimozione del dispositivo. Vedere [Parametri del dispositivo](device-parameters.md), Registrazione del provider di [servizi](registering-the-service-provider.md)e [Abilitazione di PnP per dispositivi](enabling-pnp-for-devices.md).
4.  Durante la creazione di un'istanza della classe , autenticare il provider di servizi nel costruttore. A tale scopo, creare una [classe CSecureChannelServer](csecurechannelserver-class.md) e impostare il certificato. Implementare [**l'interfaccia IComponentAuthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) e chiamare i metodi della classe CSecureChannelServer di cui è stata creata un'istanza in precedenza. Vedere [Autenticazione del provider di](authenticating-the-service-provider.md) servizi per informazioni su come creare un'istanza della classe CSecureChannelServer e implementare i metodi IComponentAuthenticate.
5.  Windows Gestione dispositivi multimediali esegue una query sul provider di servizi per un elenco di dispositivi connessi chiamando [**IMDServiceProvider2::CreateDevice**](/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider2-createdevice) o [**IMDServiceProvider::EnumDevices**](/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider-enumdevices), a seconda che il provider di servizi gestisca Plug and Play dispositivi. Il provider di servizi deve restituire un elenco di [**oggetti IMDSPDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice) che rappresentano i dispositivi connessi. Per [altri dettagli, vedere Enumerazione](enumerating-devices-service-provider.md) dei dispositivi.
6.  Prima di gestire qualsiasi chiamata, verificare che sia stato stabilito un canale sicuro. Chiamare [**CSecureChannelServer::fIsAuthenticated**](/previous-versions/bb231600(v=vs.85)) prima di eseguire qualsiasi azione. Se questa chiamata ha esito negativo, restituire WMDM \_ E \_ NOTCERTIFIED.
7.  Sarà necessaria una coppia di certificati/chiavi rilasciata da Microsoft per poter gestire il materiale protetto da DRM. Per [altre informazioni, vedere Gestione del contenuto protetto](handling-protected-content-in-the-service-provider.md) nel provider di servizi.
8.  Per consentire la sincronizzazione automatica del dispositivo con Windows Media Player, deve soddisfare i requisiti elencati in [Abilitazione della sincronizzazione con Windows Media Player](enabling-synchronization-with-windows-media-player.md).
9.  Per abilitare la visualizzazione del dispositivo in Windows Explorer, è necessario eseguire alcuni passaggi speciali, descritti in Requisiti per la visualizzazione dei lettori audio portatili [in Windows Explorer](requirements-for-portable-audio-players-to-appear-in-windows-explorer.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Guida per programmatori**](programming-guide.md)
</dt> </dl>

 

 