---
title: Implementare un provider di Server-Side Automazione interfaccia utente
description: Questo argomento descrive come implementare un provider microsoft Automazione interfaccia utente sul lato server per un controllo personalizzato scritto in C++.
ms.assetid: c3a919b2-8b8c-4dde-ad71-587f3845a9f5
keywords:
- Automazione interfaccia utente,implementazione del provider sul lato server
- Automazione interfaccia utente,implementazione del provider
- Automazione interfaccia utente,implementazione di provider sul lato server
- Automazione interfaccia utente,implementazione di provider
- provider sul lato server, implementazione
- provider sul lato server, interfacce
- provider sul lato server, valori delle proprietà
- provider sul lato server,eventi
- provider sul lato server, assegnazione di un nuovo elemento padre
- eventi, provider sul lato server
- interfacce, provider sul lato server
- provider, implementazione
- implementazione di provider sul lato server
- implementazione di provider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 583b9a5f91bb8be53a3e8b0e356ce558978b8ea28d5b726b56f52420cd7bff37
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119413441"
---
# <a name="implement-a-server-side-ui-automation-provider"></a>Implementare un provider di Server-Side Automazione interfaccia utente

Questo argomento descrive come implementare un provider microsoft Automazione interfaccia utente sul lato server per un controllo personalizzato scritto in C++. Contiene le sezioni seguenti:

-   [Interfacce del provider](#provider-interfaces)
-   [Funzionalità necessarie per Automazione interfaccia utente provider di servizi](#required-functionality-for-ui-automation-providers)
-   [Valori delle proprietà](#property-values)
-   [Eventi dai provider](#events-from-providers)
-   [Navigazione del provider](#provider-navigation)
-   [Assegnazione di un nuovo elemento padre](#assigning-a-new-parent)
-   [Riposizionamento del provider](#provider-repositioning)
-   [Disconnessione dei provider](#disconnecting-providers)
-   [Argomenti correlati](#related-topics)

Per esempi di codice che illustrano come implementare provider sul lato server, vedere Procedure per [Automazione interfaccia utente provider](uiauto-howto-topics-for-uiautomation-providers.md).

## <a name="provider-interfaces"></a>Interfacce del provider

Le interfacce Component Object Model (COM) seguenti forniscono funzionalità per i controlli personalizzati. Per fornire funzionalità di base, ogni provider Automazione interfaccia utente deve implementare almeno [**l'interfaccia IRawElementProviderSimple.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) Le [**interfacce IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment) e [**IRawElementProviderFragmentRoot**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragmentroot) sono facoltative, ma devono essere implementate per gli elementi in un controllo complesso per fornire funzionalità aggiuntive.



| Interfaccia                                                                         | Descrizione                                                                                                                                                                   |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple)             | Fornisce funzionalità di base per un controllo ospitato in una finestra, incluso il supporto per i pattern di controllo e le proprietà.                                                         |
| [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment)         | Aggiunge funzionalità per un elemento in un controllo complesso, tra cui lo spostamento nel frammento, l'impostazione dello stato attivo e la restituzione del rettangolo di delimitazione dell'elemento.             |
| [**IRawElementProviderFragmentRoot**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragmentroot) | Aggiunge la funzionalità per l'elemento radice in un controllo complesso, inclusi l'individuazione di un elemento figlio in corrispondenza delle coordinate specificate e l'impostazione dello stato attivo per l'intero controllo. |



 

> [!Note]  
> Nell'API Automazione interfaccia utente per il codice gestito, queste interfacce formano una gerarchia di ereditarietà. Questo non è il caso in C++, in cui le interfacce sono completamente separate.

 

Le interfacce seguenti forniscono funzionalità aggiuntive, ma l'implementazione è facoltativa.



| Interfaccia                                                                         | Descrizione                                                                             |
|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [**IRawElementProviderAdviseEvents**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovideradviseevents) | Consente al provider di tenere traccia delle richieste per eventi.                                      |
| [**IRawElementProviderHwndOverride**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderhwndoverride) | Consente il riposizionamento degli elementi basati su finestra nell'Automazione interfaccia utente albero di un frammento. |



 

## <a name="required-functionality-for-ui-automation-providers"></a>Funzionalità necessarie per Automazione interfaccia utente provider di servizi

Per comunicare con Automazione interfaccia utente, il controllo deve implementare le principali aree di funzionalità descritte nella tabella seguente.



| Funzionalità                                              | Implementazione                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Esporre il provider a Automazione interfaccia utente.                      | In risposta a un [**messaggio WM \_ GETOBJECT**](wm-getobject.md) inviato alla finestra di controllo, restituire l'oggetto che implementa [**IRawElementProviderSimple.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) Per i frammenti, deve trattarsi del provider per la radice del frammento.                                           |
| Specificare i valori delle proprietà.                                   | Implementare [**IRawElementProviderSimple::GetPropertyValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpropertyvalue) per fornire o eseguire l'override dei valori.                                                                                                                                                             |
| Abilitare il client per interagire con il controllo .            | Implementare interfacce che supportano ogni pattern di controllo appropriato, ad esempio [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider). Restituire questi provider di pattern di controllo nell'implementazione [**di IRawElementProviderSimple::GetPatternProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpatternprovider). |
| Generare eventi.                                              | [**UiaRaiseAutomationEvent**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaraiseautomationevent), metodi di [**IProxyProviderWinEventSink**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iproxyproviderwineventsink).                                                                                                                                                |
| Abilitare lo spostamento e la messa a fuoco in un frammento.              | Implementare [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment) per ogni elemento all'interno del frammento. Non necessario per gli elementi che non fanno parte di un frammento.                                                                                                                         |
| Abilitare l'attivazione e l'individuazione degli elementi figlio in un frammento. | Implementare [**IRawElementProviderFragmentRoot**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragmentroot). Non necessario per gli elementi che non sono radici di frammenti.                                                                                                                                                          |



 

## <a name="property-values"></a>Valori della proprietà

Automazione interfaccia utente provider per i controlli personalizzati devono supportare determinate proprietà che possono essere usate da Automazione interfaccia utente e dalle applicazioni client. Per gli elementi ospitati nelle finestre, Automazione interfaccia utente recuperare alcune proprietà dal provider di finestre predefinito, ma è necessario ottenerne altre dal provider personalizzato.

In genere, i provider per i controlli basati su finestra non devono fornire le proprietà seguenti identificate da **PROPERTYID**:

-   [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)
-   [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)
-   [**UIA \_ ProcessIdPropertyId**](uiauto-automation-element-propids.md)
-   [**UIA \_ ClassNamePropertyId**](uiauto-automation-element-propids.md)
-   [**UIA \_ HasKeyboardFocusPropertyId**](uiauto-automation-element-propids.md)
-   [**UIA \_ IsEnabledPropertyId**](uiauto-automation-element-propids.md)
-   [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)
-   [**UIA \_ IsPasswordPropertyId**](uiauto-automation-element-propids.md)
-   [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)
-   [**UIA \_ RuntimeIdPropertyId**](uiauto-automation-element-propids.md)

La proprietà RuntimeId di una radice di elemento o frammento semplice ospitata in una finestra viene ottenuta dalla finestra. Tuttavia, gli elementi frammento sotto la radice, ad esempio gli elementi di un elenco in una casella di riepilogo, devono fornire i propri identificatori. Per altre informazioni, vedere [**IRawElementProviderFragment::GetRuntimeId**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-getruntimeid).

La proprietà IsKeyboardFocusable deve essere restituita per i provider ospitati in un controllo Windows Form. In questo caso, il provider di finestra predefinito potrebbe non essere in grado di recuperare il valore corretto.

La proprietà Name viene in genere fornita dal provider host.

## <a name="events-from-providers"></a>Eventi dai provider

Automazione interfaccia utente provider devono generare eventi per notificare alle applicazioni client le modifiche apportate allo stato dell'interfaccia utente. Le funzioni seguenti vengono usate per generare eventi.



| Funzione                                                                                   | Descrizione                                                                                                              |
|--------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [**UiaRaiseAutomationEvent**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaraiseautomationevent)                  | Genera vari eventi, inclusi gli eventi attivati dai pattern di controllo.                                                   |
| [**UiaRaiseAutomationPropertyChangedEvent**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaraiseautomationpropertychangedevent) | Genera un evento quando una proprietà Automazione interfaccia utente modifica.                                                               |
| [**UiaRaiseStructureChangedEvent**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaraisestructurechangedevent)      | Genera un evento quando la struttura della struttura Automazione interfaccia utente albero è stata modificata, ad esempio rimuovendo o aggiungendo un elemento. |



 

Lo scopo di un evento è quello di inviare una notifica al client di un evento che si verifica nell'interfaccia utente. I provider devono generare un evento indipendentemente dal fatto che la modifica sia stata attivata dall'input dell'utente o da un'applicazione client Automazione interfaccia utente. Ad esempio, l'evento identificato da [**UIA \_ \_ InvokedEventId**](uiauto-event-ids.md) deve essere generato ogni volta che il controllo viene richiamato, tramite input diretto dell'utente o dall'applicazione client che chiama [**IUIAutomationInvokePattern::Invoke**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationinvokepattern-invoke).

Per ottimizzare le prestazioni, un provider può generare eventi in modo selettivo o non generarne affatto se nessuna applicazione client è registrata per riceverli. Per l'ottimizzazione vengono usati gli elementi API seguenti.



| Elemento API                                                                       | Descrizione                                                                                                                                                       |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UiaClientsAreListening**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaclientsarelistening)           | Questa funzione verifica se le applicazioni client hanno sottoscritto eventi Automazione interfaccia utente client.                                                                 |
| [**IRawElementProviderAdviseEvents**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovideradviseevents) | L'implementazione di questa interfaccia in una radice del frammento consente al provider di essere avvisato quando i client registrano e annullano la registrazione dei gestori eventi per gli eventi nel frammento. |



 

> [!Note]  
> Analogamente all'implementazione del conteggio dei riferimenti nella programmazione COM, è importante che i provider di Automazione interfaccia utente trattino i metodi [**IRawElementProviderAdviseEvents::AdviseEventAdded**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovideradviseevents-adviseeventadded) e [**AdviseEventRemoved**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovideradviseevents-adviseeventremoved) come i metodi [**IUnknown::AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) e [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) dell'interfaccia [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) Finché **AdviseEventAdded** è stato chiamato più volte rispetto a **AdviseEventRemoved** per un evento o una proprietà specifica, il provider deve continuare a generare eventi corrispondenti, perché alcuni client sono ancora in ascolto. In alternativa, Automazione interfaccia utente provider possono usare la [**funzione UiaClientsAreListening**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaclientsarelistening) per determinare se almeno un client è in ascolto e, in tal caso, generare tutti gli eventi appropriati.

 

## <a name="provider-navigation"></a>Navigazione del provider

I provider per controlli semplici, ad esempio un pulsante personalizzato ospitato in una finestra, non devono supportare la navigazione nell'Automazione interfaccia utente albero. Lo spostamento da e verso l'elemento viene gestito dal provider predefinito per la finestra host, specificato nell'implementazione di [**IRawElementProviderSimple::HostRawElementProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-get_hostrawelementprovider). Quando si implementa un provider per un controllo personalizzato complesso, tuttavia, è necessario supportare la navigazione tra il nodo radice del frammento e i relativi discendenti, nonché tra nodi di pari livello.

> [!Note]  
> Gli elementi di un frammento diverso dalla radice devono restituire **NULL** da [**HostRawElementProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-get_hostrawelementprovider), perché non sono ospitati direttamente in una finestra e nessun provider predefinito può supportare lo spostamento da e verso di essi.

 

La struttura del frammento è determinata dall'implementazione di [**IRawElementProviderFragment::Navigate.**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate) Per ogni possibile direzione da ogni frammento, questo metodo restituisce l'oggetto provider per l'elemento in quella direzione. Se non è presente alcun elemento in tale direzione, il metodo restituisce **NULL.**

La radice del frammento supporta la navigazione solo verso gli elementi figlio. Ad esempio, una casella di riepilogo restituisce il primo elemento dell'elenco quando la direzione è **NavigateDirection \_ FirstChild** e restituisce l'ultimo elemento quando la direzione è **NavigateDirection \_ LastChild**. La radice del frammento non supporta lo spostamento a un elemento padre o a elementi di pari livello. viene gestito dal provider della finestra host.

Gli elementi di un frammento non radice devono supportare la navigazione verso l'elemento padre e verso eventuali elementi di pari livello e figli.

## <a name="assigning-a-new-parent"></a>Assegnazione di un nuovo elemento padre

Le finestre popup sono in realtà finestre di primo livello e, per impostazione predefinita, vengono visualizzate nell'albero Automazione interfaccia utente come elementi figlio del desktop. In molti casi, tuttavia, le finestre popup sono logicamente elementi figlio di un altro controllo. Ad esempio, l'elenco a discesa di una casella combinata è logicamente un elemento figlio della casella combinata. Analogamente, una finestra popup di menu è logicamente un elemento figlio del menu. Automazione interfaccia utente fornisce il supporto per assegnare un nuovo elemento padre a una finestra popup in modo che sia un elemento figlio del controllo associato.

Per assegnare un nuovo elemento padre a una finestra popup:

1.  Creare un provider per la finestra popup. A questo scopo, è necessario che la classe della finestra popup sia nota in anticipo.
2.  Implementare tutte le proprietà e i pattern di controllo come di consueto per tale popup, come se fosse un controllo di per sé.
3.  Implementare la proprietà [**IRawElementProviderSimple::HostRawElementProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-get_hostrawelementprovider) in modo che restituisca il valore ottenuto da [**UiaHostProviderFromHwnd**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiahostproviderfromhwnd), dove il parametro è l'handle di finestra della finestra popup.
4.  Implementare [**IRawElementProviderFragment::Navigate**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate) per la finestra popup e il relativo elemento padre in modo che lo spostamento venga gestito correttamente dal padre logico agli elementi figlio logici e tra gli elementi figlio di pari livello.

Quando Automazione interfaccia utente rileva la finestra popup, riconosce che la navigazione viene sostituita dall'impostazione predefinita e ignora la finestra popup quando viene rilevata come figlio del desktop. Il nodo è invece raggiungibile solo tramite il frammento.

L'assegnazione di un nuovo elemento padre non è adatta nei casi in cui un controllo può ospitare una finestra di qualsiasi classe. Ad esempio, un controllo rebar può ospitare qualsiasi tipo di finestra nelle bande. Per gestire questi casi, Automazione interfaccia utente una forma alternativa di rilocazione della finestra, come descritto nella sezione successiva.

## <a name="provider-repositioning"></a>Riposizionamento del provider

Automazione interfaccia utente frammenti possono contenere due o più elementi contenuti in una finestra. Poiché ogni finestra ha un proprio provider predefinito che considera la finestra come figlio di una finestra contenitore, per impostazione predefinita l'albero Automazione interfaccia utente mostrerà le finestre nel frammento come elementi figlio della finestra padre. Nella maggior parte dei casi si tratta di un comportamento auspicabile, ma talvolta può causare confusione perché non corrisponde alla struttura logica dell'interfaccia utente.

Un esempio valido è un controllo Rebar. Un controllo rebar contiene bande, ognuna delle quali può a sua volta contenere un controllo basato su finestra, ad esempio una barra degli strumenti, una casella di modifica o una casella combinata. Il provider di finestre predefinito per la finestra rebar vede le finestre del controllo banda come elementi figlio e il provider rebar vede le bande come elementi figlio. Poiché il provider di finestre e il provider rebar funzionano in tandem e combinano i relativi elementi figlio, sia le bande che i controlli basati su finestra vengono visualizzati come elementi figlio del controllo rebar. Logicamente, tuttavia, solo le bande devono essere visualizzate come elementi figlio del controllo rebar e ogni provider di banda deve essere associato al provider di finestre predefinito per il controllo in esso contenuto.

A tale scopo, il provider radice del frammento per il controllo rebar espone un set di elementi figlio che rappresentano le bande. Ogni banda ha un singolo provider che può esporre proprietà e pattern di controllo. Nell'implementazione di [**IRawElementProviderSimple::HostRawElementProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-get_hostrawelementprovider), il provider di banda restituisce il provider di finestre predefinito per la finestra di controllo, ottenuto chiamando [**UiaHostProviderFromHwnd**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiahostproviderfromhwnd), passando l'handle di finestra del controllo (**HWND**). Infine, il provider radice del frammento per il rebar implementa l'interfaccia [**IRawElementProviderHwndOverride**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderhwndoverride) e nell'implementazione di [**IRawElementProviderHwndOverride::GetOverrideProviderForHwnd**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderhwndoverride-getoverrideproviderforhwnd)restituisce il provider di banda appropriato per il controllo contenuto nella finestra specificata.

## <a name="disconnecting-providers"></a>Disconnessione dei provider

Le applicazioni in genere creano i controlli in base alle esigenze e li eliminano in un secondo momento. Dopo aver eliminato un controllo, Automazione interfaccia utente le risorse del provider associate al controllo devono essere rilasciate chiamando [**UiaDisconnectProvider**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiadisconnectprovider).

Analogamente, un'applicazione deve usare la [**funzione UiaDisconnectAllProviders**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiadisconnectallproviders) per rilasciare tutte le risorse Automazione interfaccia utente utilizzate da tutti i provider nell'applicazione prima dell'arresto.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Automazione interfaccia utente per programmatori di provider](uiauto-providerportal.md)
</dt> </dl>

 

 