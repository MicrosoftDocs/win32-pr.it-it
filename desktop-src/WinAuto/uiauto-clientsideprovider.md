---
title: Implementazione di Client-Side provider di Automazione interfaccia utente (proxy)
description: In questo argomento viene descritto come scrivere un provider proxy per un controllo non supportato e aggiungerlo all'elenco di proxy utilizzati dalle applicazioni client.
ms.assetid: c66f4a7b-0a12-4c65-a3e9-1c826d54ac6b
keywords:
- Automazione interfaccia utente,implementazione del provider sul lato client
- Automazione interfaccia utente,implementazione del provider
- Automazione interfaccia utente,implementazione di provider sul lato client
- Automazione interfaccia utente,implementazione di provider
- Automazione interfaccia utente,proxy
- Proxy
- provider sul lato client
- provider, implementazione
- implementazione di provider sul lato client
- implementazione di provider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c8724f0761b5d7e5d361742734901990136a7a98c1b2f541b4fadb69c31a92d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119861301"
---
# <a name="implementing-a-client-side-proxy-ui-automation-provider"></a>Implementazione di Client-Side provider di Automazione interfaccia utente (proxy)

Microsoft Automazione interfaccia utente fornisce un set di proxy per la maggior parte dei controlli standard, ad esempio quelli usati nelle applicazioni Microsoft Win32, Windows Forms e Windows Presentation Foundation (WPF). Tuttavia, molti controlli personalizzati e di terze parti non implementano provider Automazione interfaccia utente nativi. Per essere accessibili Automazione interfaccia utente applicazioni client, questi controlli devono essere forniti con provider lato client, noti anche come provider *proxy* o *proxy.*

In questo argomento viene descritto come scrivere un provider proxy per un controllo non supportato e aggiungerlo all'elenco di proxy utilizzati dalle applicazioni client. Essa comprende i seguenti argomenti:

-   [Che cos'è un proxy?](#what-is-a-proxy)
-   [Che cos'è una factory proxy?](#what-is-a-proxy-factory)
-   [Proxy Factory Mapping](#proxy-factory-mapping)
-   [Gestione dei proxy predefiniti](#managing-default-proxies)
-   [Argomenti correlati](#related-topics)

Per esempi di codice che illustrano come implementare i provider proxy, vedere [Procedure per Automazione interfaccia utente provider](uiauto-howto-topics-for-uiautomation-providers.md).

## <a name="what-is-a-proxy"></a>Che cos'è un proxy?

Un provider sul lato client, o proxy, è un oggetto che implementa l'interfaccia [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) per conto di un controllo che non ha un'implementazione **IRawElementProviderSimple** propria. Senza un proxy, tale controllo è in gran parte opaco per Automazione interfaccia utente, che può fornire solo le informazioni di base disponibili dall'handle della finestra (**HWND**), ad esempio la posizione del controllo.

## <a name="what-is-a-proxy-factory"></a>Che cos'è una factory proxy?

Ogni proxy richiede una *factory proxy corrispondente,* ovvero un oggetto che espone l'interfaccia [**IUIAutomationProxyFactory.**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactory) Automazione interfaccia utente gestisce una tabella interna di voci della *factory proxy,* ognuna delle quali contiene un riferimento alla factory proxy per ogni proxy e un set di condizioni. Quando Automazione interfaccia utente rileva un controllo che non ha un'implementazione [**nativa di IRawElementProviderSimple,**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) cerca una voce della factory proxy le cui condizioni indicano che supporta il controllo. Automazione interfaccia utente esegue la ricerca nella tabella dall'inizio e quando trova una voce corrispondente, Automazione interfaccia utente chiama il metodo [**IUIAutomationProxyFactory::CreateProvider**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationproxyfactory-createprovider) della factory. Se il proxy corrispondente viene creato correttamente, il Automazione interfaccia utente interrompe la ricerca e usa l'oggetto proxy appena creato. In caso contrario, Automazione interfaccia utente continua la ricerca.

Un'applicazione client crea un'istanza di una voce della factory proxy usando il metodo [**IUIAutomation::CreateProxyFactoryEntry,**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createproxyfactoryentry) che restituisce un puntatore a interfaccia [**IUIAutomationProxyFactoryEntry.**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactoryentry) I client usano i metodi esposti da **IUIAutomationProxyFactoryEntry** per specificare il set di condizioni usate dalla factory proxy per la creazione del proxy.

Quando chiama [**IUIAutomationProxyFactory::CreateProvider,**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationproxyfactory-createprovider)Automazione interfaccia utente passa i parametri che l'oggetto proxy factory può usare per determinare se il proxy supporta adeguatamente il controllo personalizzato. In questo caso, la factory proxy crea un'istanza del proxy e restituisce il puntatore di interfaccia [**IRawElementProviderSimple.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) In caso contrario, restituisce un **puntatore NULL.**

## <a name="proxy-factory-mapping"></a>Proxy Factory Mapping

Per impostazione predefinita, Automazione interfaccia utente ricerca nella tabella della factory proxy nell'ordine seguente.



| JSON | Proxy                        | Descrizione                                                                      |
|-------|------------------------------|----------------------------------------------------------------------------------|
| 1     | Microsoft: Proxy non di controllo | Per le finestre con il nome esatto della classe o il nome della classe di base "ComboBoxEx32".         |
| 2     | Microsoft: Proxy non di controllo | Per le finestre con il nome esatto della classe o il nome della classe di base "WorkerW".              |
| 3     | Microsoft: Proxy non di controllo | Per le finestre con il nome esatto della classe o il nome della classe di base "SHELLDLL \_ DefView".    |
| 4     | Microsoft: Proxy contenitore   | Per le finestre con il nome esatto della classe o il nome della classe di base " \# 32770".              |
| 5     | Microsoft: Proxy contenitore   | Per le finestre con un nome di classe o un nome di classe di base contenente "AfxControlBar".     |
| 6     | Microsoft: TreeView Proxy    | Per le finestre con un nome di classe o un nome di classe di base contenente "SysTreeView32".     |
| 7     | Microsoft: ListView Proxy    | Per le finestre con un nome di classe o un nome di classe di base contenente "SysListView32" (1). |
| 8     | Microsoft: ListView Proxy    | Per le finestre con un nome di classe o un nome di classe di base contenente "SysListView32" (2). |
| 9     | Microsoft: MSAA Proxy        | Per qualsiasi finestra.                                                                  |



 

I proxy 7 e 8 sono voci duplicate per il controllo SysListView32. Senza modifiche, il proxy 7 viene sempre usato per il controllo SysListView32 e il proxy 8 non viene mai usato. Proxy 8 viene usato solo per gli elementi elenco visibili e viene in genere usato dalle applicazioni client che funzionano solo con elementi visibili o che hanno requisiti di prestazioni rigorosi. Questi client possono rimuovere il proxy 7.

Proxy 9, il Microsoft Active Accessibility per Automazione interfaccia utente proxy, deve essere sempre l'ultima voce nella tabella. In questo modo Microsoft Active Accessibility funzionalità di fallback per i controlli che implementano Microsoft Active Accessibility, ma non Automazione interfaccia utente.

Quando si modificano le voci nella tabella della factory proxy, è necessario valutare attentamente la nuova posizione delle voci. È consigliabile inserire le voci per i proxy personalizzati dopo i proxy non di controllo e contenitore, ma prima dell'Microsoft Active Accessibility per Automazione interfaccia utente proxy. Inoltre, anche se è possibile che il codice nella chiamata a [**CreateProvider**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationproxyfactory-createprovider) determinerà se deve supportare un handle di finestra specifico **(HWND),** è più efficiente consentire Automazione interfaccia utente selezionare il proxy in base al nome della classe e mantenere minimo il codice condizionale nel metodo **CreateProvider.**

Automazione interfaccia utente gestisce una tabella di factory proxy separata per ogni client. Quando un client modifica la relativa tabella proxy, le modifiche interessano solo il client stesso. gli altri client non sono interessati.

## <a name="managing-default-proxies"></a>Gestione dei proxy predefiniti

Quando un'applicazione client crea l'oggetto [**CUIAutomation,**](/previous-versions/windows/desktop/legacy/ff384838(v=vs.85)) la tabella della factory proxy contiene inizialmente voci solo per i provider proxy predefiniti per i controlli standard. Usando [**l'interfaccia IUIAutomationProxyFactoryMapping,**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactorymapping) i client possono aggiungere nuove voci, rimuovere le voci indesiderate, modificare l'ordine delle voci e così via. Un client può recuperare un puntatore a interfaccia **IUIAutomationProxyFactoryMapping** chiamando il metodo [**IUIAutomation::P roxyFactoryMapping.**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_proxyfactorymapping)

La tabella dei proxy disponibili contiene [**un'interfaccia IUIAutomationProxyFactoryEntry**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactoryentry) per ogni proxy. Ogni **IUIAutomationProxyFactoryEntry** specifica [**IUIAutomationProxyFactory**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactory) e la classe di controllo gestita dal proxy e definisce la modalità di gestione degli eventi.

La tabella dei proxy è rappresentata da [**un'interfaccia IUIAutomationProxyFactoryMapping,**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactorymapping) che può essere ottenuta dalla proprietà [**IUIAutomation::P roxyFactoryMapping.**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_proxyfactorymapping) Un'applicazione può **usare i metodi IUIAutomationProxyFactoryMapping** per aggiungere ed eliminare proxy. Per creare una nuova voce da aggiungere a questa tabella, usare [**IUIAutomation::CreateProxyFactoryEntry**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createproxyfactoryentry) per ottenere l'interfaccia e quindi usare i metodi [**IUIAutomationProxyFactoryEntry**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationproxyfactoryentry) per definire la classe di controllo applicabile e il comportamento del proxy.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Come creare un provider Client-Side (proxy) Automazione interfaccia utente](uiauto-howto-create-clientside-provider.md)
</dt> <dt>

[Automazione interfaccia utente per programmatori di provider di servizi](uiauto-providerportal.md)
</dt> </dl>

 

 