---
title: Implementazione di un provider di automazione interfaccia utente Client-Side (proxy)
description: Questo argomento descrive come scrivere un provider proxy per un controllo non supportato e aggiungerlo all'elenco di proxy usati dalle applicazioni client.
ms.assetid: c66f4a7b-0a12-4c65-a3e9-1c826d54ac6b
keywords:
- Automazione interfaccia utente, implementazione del provider lato client
- Automazione interfaccia utente, implementazione del provider
- Automazione interfaccia utente, implementazione di provider lato client
- Automazione interfaccia utente, implementazione di provider
- Automazione interfaccia utente, proxy
- Proxy
- provider lato client
- provider, implementazione
- implementazione di provider lato client
- implementazione di provider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e2bdb4a94ba6e693792508de5c573317299b0d3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104046832"
---
# <a name="implementing-a-client-side-proxy-ui-automation-provider"></a>Implementazione di un provider di automazione interfaccia utente Client-Side (proxy)

Automazione interfaccia utente Microsoft fornisce un set di proxy per la maggior parte dei controlli standard, ad esempio quelli usati nelle applicazioni Microsoft Win32, Windows Form e Windows Presentation Foundation (WPF). Tuttavia, molti controlli personalizzati e controlli di terze parti non implementano i provider di automazione interfaccia utente nativi. Per essere accessibili alle applicazioni client di automazione interfaccia utente, questi controlli devono essere forniti con provider lato client, noti anche come *provider proxy* o *proxy*.

Questo argomento descrive come scrivere un provider proxy per un controllo non supportato e aggiungerlo all'elenco di proxy usati dalle applicazioni client. Essa comprende i seguenti argomenti:

-   [Che cos'è un proxy?](#what-is-a-proxy)
-   [Che cos'è una factory proxy?](#what-is-a-proxy-factory)
-   [Mapping di Factory proxy](#proxy-factory-mapping)
-   [Gestione dei proxy predefiniti](#managing-default-proxies)
-   [Argomenti correlati](#related-topics)

Per esempi di codice che illustrano come implementare i provider proxy, vedere procedure [per i provider di automazione interfaccia utente](uiauto-howto-topics-for-uiautomation-providers.md).

## <a name="what-is-a-proxy"></a>Che cos'è un proxy?

Un provider lato client, o proxy, è un oggetto che implementa l'interfaccia [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) per conto di un controllo che non ha un'implementazione di **IRawElementProviderSimple** . Senza un proxy, questo controllo è in gran parte opaco per l'automazione dell'interfaccia utente, che può fornire solo le informazioni di base disponibili dall'handle di finestra (**HWND**), ad esempio la posizione del controllo.

## <a name="what-is-a-proxy-factory"></a>Che cos'è una factory proxy?

Ogni proxy richiede una *Factory proxy* corrispondente, ovvero un oggetto che espone l'interfaccia [**IUIAutomationProxyFactory**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactory) . Automazione interfaccia utente gestisce una tabella interna di *voci di Factory proxy*, ognuna delle quali contiene un riferimento alla Factory proxy per ogni proxy e un set di condizioni. Quando automazione interfaccia utente rileva un controllo che non ha un'implementazione [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) nativa, Cerca una voce di Factory proxy le cui condizioni indicano che supporta il controllo. Automazione interfaccia utente cerca la tabella dall'inizio e quando trova una voce corrispondente, l'automazione interfaccia utente chiama il metodo [**IUIAutomationProxyFactory:: CreateProvider**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationproxyfactory-createprovider) della factory. Se il proxy corrispondente viene creato correttamente, l'automazione interfaccia utente interrompe la ricerca e usa l'oggetto proxy appena creato. in caso contrario, l'automazione interfaccia utente continua la ricerca.

Un'applicazione client crea un'istanza di una voce di Factory proxy usando il metodo [**IUIAutomation:: CreateProxyFactoryEntry**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createproxyfactoryentry) , che restituisce un puntatore a interfaccia [**IUIAutomationProxyFactoryEntry**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactoryentry) . I client usano i metodi esposti da **IUIAutomationProxyFactoryEntry** per specificare il set di condizioni che la Factory proxy usa per la creazione del proxy.

Quando chiama [**IUIAutomationProxyFactory:: CreateProvider**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationproxyfactory-createprovider), l'automazione interfaccia utente passa i parametri che l'oggetto Factory proxy può usare per determinare se il proxy supporta adeguatamente il controllo personalizzato. In tal caso, la factory del proxy crea un'istanza del proxy e restituisce il puntatore all'interfaccia [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) ; in caso contrario, restituisce un puntatore **null** .

## <a name="proxy-factory-mapping"></a>Mapping di Factory proxy

Per impostazione predefinita, l'automazione interfaccia utente cerca nella tabella del proxy Factory nell'ordine seguente.



| JSON | Proxy                        | Descrizione                                                                      |
|-------|------------------------------|----------------------------------------------------------------------------------|
| 1     | Microsoft: proxy non di controllo | Per Windows con il nome della classe o il nome della classe di base "ComboBoxEx32".         |
| 2     | Microsoft: proxy non di controllo | Per Windows con il nome della classe o il nome della classe di base "WorkerW".              |
| 3     | Microsoft: proxy non di controllo | Per Windows con il nome della classe o il nome della classe di base "SHELLDLL \_ DefView".    |
| 4     | Microsoft: proxy contenitore   | Per Windows con il nome della classe o il nome della classe di base " \# 32770".              |
| 5     | Microsoft: proxy contenitore   | Per Windows con un nome di classe o un nome di classe di base contenente "AfxControlBar".     |
| 6     | Microsoft: TreeView proxy    | Per Windows con un nome di classe o un nome di classe di base contenente "SysTreeView32".     |
| 7     | Microsoft: proxy ListView    | Per Windows con un nome di classe o un nome di classe di base contenente "SysListView32" (1). |
| 8     | Microsoft: proxy ListView    | Per Windows con un nome di classe o un nome di classe di base che contiene "SysListView32" (2). |
| 9     | Microsoft: proxy MSAA        | Per qualsiasi finestra.                                                                  |



 

I proxy 7 e 8 sono voci duplicate per il controllo SysListView32. Senza modifiche, il proxy 7 viene sempre usato per il controllo SysListView32 e il proxy 8 non viene mai usato. Il proxy 8 viene usato solo per gli elementi di elenco visibili e viene in genere usato dalle applicazioni client che funzionano solo con gli elementi visibili o con requisiti di prestazioni rigidi. Questi client possono rimuovere il proxy 7.

Il proxy 9, il Active Accessibility Microsoft al proxy di automazione interfaccia utente, deve essere sempre l'ultima voce nella tabella. Questo consente la funzionalità di fallback di Microsoft Active Accessibility per i controlli che implementano Microsoft Active Accessibility, ma non l'automazione dell'interfaccia utente.

Quando si modificano le voci nella tabella del proxy Factory, è necessario valutare con attenzione la nuova posizione delle voci. Si consiglia di inserire le voci per i proxy personalizzati dopo i proxy del contenitore e non di controllo, ma prima che Microsoft Active Accessibility al proxy di automazione interfaccia utente. Inoltre, anche se è possibile che il codice nella chiamata a [**CreateProvider**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationproxyfactory-createprovider) determini se deve supportare un handle di finestra (**HWND**) specifico, è più efficiente consentire a automazione interfaccia utente di selezionare il proxy in base al nome della classe e mantenere il codice condizionale nel metodo **CreateProvider** come minimo.

Automazione interfaccia utente gestisce una tabella Factory proxy separata per ogni client. Quando un client modifica la tabella proxy, le modifiche interessano solo il client stesso; gli altri client non sono interessati.

## <a name="managing-default-proxies"></a>Gestione dei proxy predefiniti

Quando un'applicazione client crea l'oggetto [**CUIAutomation**](/previous-versions/windows/desktop/legacy/ff384838(v=vs.85)) , la tabella Factory proxy contiene inizialmente solo le voci per i provider di proxy predefiniti per i controlli standard. Usando l'interfaccia [**IUIAutomationProxyFactoryMapping**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactorymapping) , i client possono aggiungere nuove voci, rimuovere le voci indesiderate, modificare l'ordine delle voci e così via. Un client può recuperare un puntatore all'interfaccia **IUIAutomationProxyFactoryMapping** chiamando il metodo [**IUIAutomation::P roxyfactorymapping**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_proxyfactorymapping) .

La tabella dei proxy disponibili contiene un'interfaccia [**IUIAutomationProxyFactoryEntry**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactoryentry) per ogni proxy. Ogni **IUIAutomationProxyFactoryEntry** specifica il [**IUIAutomationProxyFactory**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactory) e la classe del controllo che il proxy serve e definisce il modo in cui devono essere gestiti gli eventi.

La tabella dei proxy è rappresentata da un'interfaccia [**IUIAutomationProxyFactoryMapping**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactorymapping) , che può essere ottenuta dalla proprietà [**IUIAutomation::P roxyfactorymapping**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_proxyfactorymapping) . Un'applicazione può usare i metodi **IUIAutomationProxyFactoryMapping** per aggiungere ed eliminare proxy. Per creare una nuova voce da aggiungere a questa tabella, usare [**IUIAutomation:: CreateProxyFactoryEntry**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createproxyfactoryentry) per ottenere l'interfaccia e quindi usare i metodi [**IUIAutomationProxyFactoryEntry**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactoryentry) per definire la classe del controllo applicabile e il comportamento del proxy.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Come creare un provider di automazione interfaccia utente di Client-Side (proxy)](uiauto-howto-create-clientside-provider.md)
</dt> <dt>

[Guida per programmatori del provider di automazione interfaccia utente](uiauto-providerportal.md)
</dt> </dl>

 

 