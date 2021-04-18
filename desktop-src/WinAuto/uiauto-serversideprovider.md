---
title: Implementare un provider di automazione interfaccia utente Server-Side
description: Questo argomento descrive come implementare un provider di automazione interfaccia utente Microsoft sul lato server per un controllo personalizzato scritto in C++.
ms.assetid: c3a919b2-8b8c-4dde-ad71-587f3845a9f5
keywords:
- Automazione interfaccia utente, implementazione del provider lato server
- Automazione interfaccia utente, implementazione del provider
- Automazione interfaccia utente, implementazione di provider lato server
- Automazione interfaccia utente, implementazione di provider
- provider lato server, implementazione
- provider lato server, interfacce
- provider lato server, valori delle proprietà
- provider lato server, eventi
- provider lato server, assegnazione di un nuovo elemento padre
- eventi, provider lato server
- interfacce, provider lato server
- provider, implementazione
- implementazione di provider lato server
- implementazione di provider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7fafbb9d03a25eb2e4713330c0622c25d17f9ff
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300266"
---
# <a name="implement-a-server-side-ui-automation-provider"></a>Implementare un provider di automazione interfaccia utente Server-Side

Questo argomento descrive come implementare un provider di automazione interfaccia utente Microsoft sul lato server per un controllo personalizzato scritto in C++. Contiene le sezioni seguenti:

-   [Interfacce del provider](#provider-interfaces)
-   [Funzionalità richiesta per i provider di automazione interfaccia utente](#required-functionality-for-ui-automation-providers)
-   [Valori delle proprietà](#property-values)
-   [Eventi dai provider](#events-from-providers)
-   [Navigazione del provider](#provider-navigation)
-   [Assegnazione di un nuovo elemento padre](#assigning-a-new-parent)
-   [Riposizionamento del provider](#provider-repositioning)
-   [Disconnessione di provider](#disconnecting-providers)
-   [Argomenti correlati](#related-topics)

Per esempi di codice che illustrano come implementare i provider lato server, vedere procedure [per i provider di automazione interfaccia utente](uiauto-howto-topics-for-uiautomation-providers.md).

## <a name="provider-interfaces"></a>Interfacce del provider

Le seguenti interfacce di Component Object Model (COM) forniscono funzionalità per i controlli personalizzati. Per fornire funzionalità di base, ogni provider di automazione interfaccia utente deve implementare almeno l'interfaccia [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) . Le interfacce [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment) e [**IRawElementProviderFragmentRoot**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragmentroot) sono facoltative, ma devono essere implementate per gli elementi in un controllo complesso per fornire funzionalità aggiuntive.



| Interfaccia                                                                         | Descrizione                                                                                                                                                                   |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple)             | Fornisce funzionalità di base per un controllo ospitato in una finestra, incluso il supporto per pattern di controllo e proprietà.                                                         |
| [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment)         | Aggiunge la funzionalità per un elemento in un controllo complesso, inclusa la navigazione nel frammento, l'impostazione dello stato attivo e la restituzione del rettangolo di delimitazione dell'elemento.             |
| [**IRawElementProviderFragmentRoot**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragmentroot) | Aggiunge la funzionalità per l'elemento radice in un controllo complesso, inclusi l'individuazione di un elemento figlio in corrispondenza delle coordinate specificate e l'impostazione dello stato attivo per l'intero controllo. |



 

> [!Note]  
> Nell'API di automazione interfaccia utente per il codice gestito, queste interfacce formano una gerarchia di ereditarietà. Questo non avviene in C++, in cui le interfacce sono completamente separate.

 

Le interfacce seguenti forniscono funzionalità aggiunte, ma l'implementazione è facoltativa.



| Interfaccia                                                                         | Descrizione                                                                             |
|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [**IRawElementProviderAdviseEvents**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovideradviseevents) | Consente al provider di tenere traccia delle richieste per eventi.                                      |
| [**IRawElementProviderHwndOverride**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderhwndoverride) | Abilita il riposizionamento degli elementi basati su finestra nell'albero di automazione interfaccia utente di un frammento. |



 

## <a name="required-functionality-for-ui-automation-providers"></a>Funzionalità richiesta per i provider di automazione interfaccia utente

Per comunicare con l'automazione interfaccia utente, il controllo deve implementare le aree di funzionalità principali descritte nella tabella seguente.



| Funzionalità                                              | Implementazione                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Esporre il provider all'automazione interfaccia utente.                      | In risposta a un messaggio [**WM \_ GetObject**](wm-getobject.md) inviato alla finestra del controllo, restituire l'oggetto che implementa [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple). Per i frammenti, deve trattarsi del provider per la radice del frammento.                                           |
| Specificare i valori delle proprietà.                                   | Implementare [**IRawElementProviderSimple:: GetPropertyValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpropertyvalue) per fornire o eseguire l'override di valori.                                                                                                                                                             |
| Consentire al client di interagire con il controllo.            | Implementare le interfacce che supportano ogni pattern di controllo appropriato, ad esempio [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider). Restituire questi provider di pattern di controllo nell'implementazione di [**IRawElementProviderSimple:: GetPatternProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpatternprovider). |
| Generare eventi.                                              | [**UiaRaiseAutomationEvent**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaraiseautomationevent), metodi di [**IProxyProviderWinEventSink**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iproxyproviderwineventsink).                                                                                                                                                |
| Abilitare lo spostamento e la messa a fuoco in un frammento.              | Implementare [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment) per ogni elemento all'interno del frammento. Non necessario per gli elementi che non fanno parte di un frammento.                                                                                                                         |
| Abilitare la messa a fuoco e individuare gli elementi figlio in un frammento. | Implementare [**IRawElementProviderFragmentRoot**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragmentroot). Non necessario per gli elementi che non sono radici di frammenti.                                                                                                                                                          |



 

## <a name="property-values"></a>Valori della proprietà

I provider di automazione interfaccia utente per i controlli personalizzati devono supportare determinate proprietà che possono essere usate dall'automazione interfaccia utente e dalle applicazioni client. Per gli elementi ospitati in Windows, l'automazione interfaccia utente può recuperare alcune proprietà dal provider di finestra predefinito, ma deve ottenerne altre dal provider personalizzato.

In genere, i provider per i controlli basati su finestra non devono fornire le proprietà seguenti identificate da **PROPERTYID**:

-   [**\_BOUNDINGRECTANGLEPROPERTYID UIA**](uiauto-automation-element-propids.md)
-   [**\_CLICKABLEPOINTPROPERTYID UIA**](uiauto-automation-element-propids.md)
-   [**\_PROCESSIDPROPERTYID UIA**](uiauto-automation-element-propids.md)
-   [**\_CLASSNAMEPROPERTYID UIA**](uiauto-automation-element-propids.md)
-   [**\_HASKEYBOARDFOCUSPROPERTYID UIA**](uiauto-automation-element-propids.md)
-   [**\_ISENABLEDPROPERTYID UIA**](uiauto-automation-element-propids.md)
-   [**\_ISKEYBOARDFOCUSABLEPROPERTYID UIA**](uiauto-automation-element-propids.md)
-   [**\_ISPASSWORDPROPERTYID UIA**](uiauto-automation-element-propids.md)
-   [**\_NAMEPROPERTYID UIA**](uiauto-automation-element-propids.md)
-   [**\_RUNTIMEIDPROPERTYID UIA**](uiauto-automation-element-propids.md)

La proprietà IDruntime di un elemento semplice o di una radice di frammento ospitata in una finestra viene ottenuta dalla finestra. Tuttavia, gli elementi del frammento sotto la radice, ad esempio gli elementi di elenco in una casella di riepilogo, devono fornire i propri identificatori. Per ulteriori informazioni, vedere [**IRawElementProviderFragment:: GetRuntimeId**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-getruntimeid).

La proprietà IsKeyboardFocusable deve essere restituita per i provider ospitati in un controllo Windows Form. In questo caso, il provider di finestra predefinito potrebbe non essere in grado di recuperare il valore corretto.

La proprietà Name viene in genere fornita dal provider host.

## <a name="events-from-providers"></a>Eventi dai provider

I provider di automazione interfaccia utente devono generare eventi per notificare alle applicazioni client le modifiche allo stato dell'interfaccia utente. Le funzioni seguenti vengono utilizzate per generare eventi.



| Funzione                                                                                   | Descrizione                                                                                                              |
|--------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [**UiaRaiseAutomationEvent**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaraiseautomationevent)                  | Genera vari eventi, inclusi gli eventi attivati dai pattern di controllo.                                                   |
| [**UiaRaiseAutomationPropertyChangedEvent**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaraiseautomationpropertychangedevent) | Genera un evento quando viene modificata una proprietà di automazione interfaccia utente.                                                               |
| [**UiaRaiseStructureChangedEvent**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaraisestructurechangedevent)      | Genera un evento quando la struttura dell'albero di automazione interfaccia utente è cambiata, ad esempio rimuovendo o aggiungendo un elemento. |



 

Lo scopo di un evento è informare il client di qualcosa che si verifica nell'interfaccia utente. I provider devono generare un evento indipendentemente dal fatto che la modifica sia stata attivata dall'input dell'utente o da un'applicazione client che usa l'automazione interfaccia utente. Ad esempio, l'evento identificato da [**UIA \_ Invoke \_ InvokedEventId**](uiauto-event-ids.md) deve essere generato ogni volta che viene richiamato il controllo, tramite input utente diretto o dall'applicazione client che chiama [**IUIAutomationInvokePattern:: Invoke**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationinvokepattern-invoke).

Per ottimizzare le prestazioni, un provider può generare eventi in modo selettivo o non generarne affatto se nessuna applicazione client è registrata per riceverli. Per l'ottimizzazione vengono usati gli elementi API seguenti.



| Elemento API                                                                       | Descrizione                                                                                                                                                       |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UiaClientsAreListening**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaclientsarelistening)           | Questa funzione verifica se le applicazioni client hanno sottoscritto eventi di automazione interfaccia utente.                                                                 |
| [**IRawElementProviderAdviseEvents**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovideradviseevents) | L'implementazione di questa interfaccia in una radice di frammento consente al provider di essere avvisati quando i client registrano e annullano la registrazione dei gestori eventi per gli eventi nel frammento. |



 

> [!Note]  
> Analogamente all'implementazione del conteggio dei riferimenti nella programmazione COM, è importante per i provider di automazione interfaccia utente trattare i metodi [**IRawElementProviderAdviseEvents:: AdviseEventAdded**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovideradviseevents-adviseeventadded) e [**AdviseEventRemoved**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovideradviseevents-adviseeventremoved) , come i metodi [**IUnknown:: AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) e [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) dell'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . Fino a quando **AdviseEventAdded** è stato chiamato più volte rispetto a **AdviseEventRemoved** per un evento o una proprietà specifica, il provider deve continuare a generare eventi corrispondenti, perché alcuni client sono ancora in ascolto. In alternativa, i provider di automazione interfaccia utente possono utilizzare la funzione [**UiaClientsAreListening**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaclientsarelistening) per determinare se almeno un client è in ascolto e, in caso affermativo, generare tutti gli eventi appropriati.

 

## <a name="provider-navigation"></a>Navigazione del provider

I provider per controlli semplici, ad esempio un pulsante personalizzato ospitato in una finestra, non devono supportare la navigazione nell'albero di automazione interfaccia utente. La navigazione verso e dall'elemento viene gestita dal provider predefinito per la finestra host, specificata nell'implementazione di [**IRawElementProviderSimple:: HostRawElementProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-get_hostrawelementprovider). Quando si implementa un provider per un controllo personalizzato complesso, tuttavia, è necessario supportare la navigazione tra il nodo radice del frammento e i relativi discendenti, nonché tra nodi di pari livello.

> [!Note]  
> Gli elementi di un frammento diversi dalla radice devono restituire **null** da [**HostRawElementProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-get_hostrawelementprovider), perché non sono ospitati direttamente in una finestra e nessun provider predefinito può supportare lo spostamento verso e da essi.

 

La struttura del frammento è determinata dall'implementazione di [**IRawElementProviderFragment:: Navigate**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate). Per ogni possibile direzione da ogni frammento, questo metodo restituisce l'oggetto provider per l'elemento in quella direzione. Se non è presente alcun elemento in tale direzione, il metodo restituisce **null**.

La radice del frammento supporta la navigazione solo verso gli elementi figlio. Ad esempio, una casella di riepilogo restituisce il primo elemento nell'elenco quando la direzione è **NavigateDirection \_ FirstChild** e restituisce l'ultimo elemento quando la direzione è **NavigateDirection \_ LastChild**. La radice del frammento non supporta la navigazione verso un elemento padre o per gli elementi di pari livello. Questa operazione viene gestita dal provider della finestra host.

Gli elementi di un frammento non radice devono supportare la navigazione verso l'elemento padre e verso eventuali elementi di pari livello e figli.

## <a name="assigning-a-new-parent"></a>Assegnazione di un nuovo elemento padre

Le finestre popup sono in effetti finestre di primo livello e, per impostazione predefinita, vengono visualizzate nell'albero di automazione interfaccia utente come elementi figlio del desktop. In molti casi, tuttavia, le finestre popup sono logicamente elementi figlio di un altro controllo. Ad esempio, l'elenco a discesa di una casella combinata è logicamente un elemento figlio della casella combinata. Analogamente, una finestra popup di menu è logicamente un elemento figlio del menu. Automazione interfaccia utente fornisce supporto per assegnare un nuovo elemento padre a una finestra popup in modo che sembri essere un elemento figlio del controllo associato.

Per assegnare un nuovo elemento padre a una finestra popup:

1.  Creare un provider per la finestra popup. A tale scopo, è necessario che la classe della finestra popup sia nota in anticipo.
2.  Implementare tutte le proprietà e i pattern di controllo come di consueto per tale popup, come se si trattasse di un controllo in un proprio diritto.
3.  Implementare la proprietà [**IRawElementProviderSimple:: HostRawElementProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-get_hostrawelementprovider) in modo che restituisca il valore ottenuto da [**UiaHostProviderFromHwnd**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiahostproviderfromhwnd), dove il parametro è l'handle della finestra popup.
4.  Implementare [**IRawElementProviderFragment:: Navigate**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate) per la finestra popup e il relativo elemento padre in modo che la navigazione venga gestita correttamente dall'elemento padre logico agli elementi figlio logici e tra gli elementi figlio di pari livello.

Quando automazione interfaccia utente rileva la finestra popup, riconosce che è in corso l'override della navigazione rispetto all'impostazione predefinita e ignora la finestra popup quando viene rilevata come figlio del desktop. Al contrario, il nodo è raggiungibile solo tramite il frammento.

L'assegnazione di un nuovo elemento padre non è adatta ai casi in cui un controllo può ospitare una finestra di qualsiasi classe. Ad esempio, un controllo Rebar può ospitare qualsiasi tipo di finestra nelle bande. Per gestire questi casi, l'automazione interfaccia utente supporta un tipo alternativo di rilocazione della finestra, come descritto nella sezione successiva.

## <a name="provider-repositioning"></a>Riposizionamento del provider

I frammenti di automazione interfaccia utente possono contenere due o più elementi ognuno contenuti in una finestra. Poiché ogni finestra ha il proprio provider predefinito che considera la finestra come figlio di una finestra che lo contiene, l'albero di automazione interfaccia utente per impostazione predefinita mostrerà le finestre nel frammento come elementi figlio della finestra padre. Nella maggior parte dei casi si tratta di un comportamento auspicabile, ma a volte può causare confusione perché non corrisponde alla struttura logica dell'interfaccia utente.

Un esempio valido è un controllo Rebar. Un controllo Rebar contiene bande, ognuna delle quali può contenere a sua volta un controllo basato su finestra, ad esempio una barra degli strumenti, una casella di modifica o una casella combinata. Il provider di finestra predefinito per la finestra Rebar Visualizza le finestre di controllo della banda come elementi figlio e il provider Rebar Visualizza le bande come elementi figlio. Poiché il provider della finestra e il provider Rebar operano in tandem e combinano i rispettivi elementi figlio, sia le bande che i controlli basati su finestra vengono visualizzati come elementi figlio del controllo Rebar. Logicamente, tuttavia, solo le bande devono apparire come elementi figlio del controllo Rebar e ogni provider di banda deve essere abbinato al provider di finestra predefinito per il controllo che contiene.

A tale scopo, il provider di radice del frammento per il controllo Rebar espone un set di elementi figlio che rappresentano le bande. Ogni banda ha un singolo provider che può esporre le proprietà e i pattern di controllo. Nell'implementazione di [**IRawElementProviderSimple:: HostRawElementProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-get_hostrawelementprovider), il provider di bande restituisce il provider di finestra predefinito per la finestra di controllo, che ottiene chiamando [**UiaHostProviderFromHwnd**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiahostproviderfromhwnd), passando l'handle di finestra (**HWND**) del controllo. Infine, il provider di radice del frammento per il controllo Rebar implementa l'interfaccia [**IRawElementProviderHwndOverride**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderhwndoverride) e, nell'implementazione di [**IRawElementProviderHwndOverride:: GetOverrideProviderForHwnd**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderhwndoverride-getoverrideproviderforhwnd), restituisce il provider di bande appropriato per il controllo contenuto nella finestra specificata.

## <a name="disconnecting-providers"></a>Disconnessione di provider

Le applicazioni in genere creano controlli quando sono necessari e li eliminano successivamente. Dopo l'eliminazione di un controllo, le risorse del provider di automazione interfaccia utente associate al controllo devono essere rilasciate chiamando [**UiaDisconnectProvider**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiadisconnectprovider).

Analogamente, un'applicazione deve usare la funzione [**UiaDisconnectAllProviders**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiadisconnectallproviders) per rilasciare tutte le risorse di automazione interfaccia utente mantenute da tutti i provider nell'applicazione prima di arrestarsi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida per programmatori del provider di automazione interfaccia utente](uiauto-providerportal.md)
</dt> </dl>

 

 