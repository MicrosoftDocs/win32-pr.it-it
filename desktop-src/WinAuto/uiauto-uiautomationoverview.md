---
title: Cenni preliminari su automazione interfaccia utente
description: Microsoft Automazione interfaccia utente è un framework di accessibilità per Windows.
ms.assetid: 99610542-761c-432d-a4ac-4cd3812577a8
keywords:
- Automazione interfaccia utente,about
- Automazione interfaccia utente,accessibilità
- Automazione interfaccia utente,components
- Automazione interfaccia utente, API provider
- Automazione interfaccia utente,API client
- Automazione interfaccia utente,file di intestazione
- Automazione interfaccia utente,model
- components
- accessibilità
- Provider API
- API client
- file di intestazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3664866280d570f9fa5f07acc6245ca2b4c1bff7
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122470058"
---
# <a name="ui-automation-overview"></a>Cenni preliminari su automazione interfaccia utente

Microsoft Automazione interfaccia utente è un framework di accessibilità per Windows. Fornisce l'accesso a livello di codice alla maggior parte degli elementi dell'interfaccia utente sul desktop. Consente ai assistive technology, ad esempio le utilità per la lettura dello schermo, di fornire informazioni sull'interfaccia utente agli utenti finali e di modificare l'interfaccia utente con mezzi diversi dall'input standard. Automazione interfaccia utente consente anche agli script di test automatizzati di interagire con l'interfaccia utente.

Automazione interfaccia utente è stato disponibile per la prima volta in Windows XP come parte di Microsoft .NET Framework. Anche se in quel momento è stata pubblicata anche un'API C++ non gestita, l'utilità delle funzioni client è stata limitata a causa di problemi di interoperabilità. Per Windows 7, l'API è stata riscritta nel Component Object Model (COM).

> [!Note]  
> Anche se le funzioni di libreria introdotte nella versione precedente di Automazione interfaccia utente sono ancora documentate, non devono essere usate nelle nuove applicazioni.

 

Automazione interfaccia utente applicazioni client possono essere scritte con la certezza che funzionino su più framework di controllo Windows Microsoft. Il Automazione interfaccia utente principale maschera eventuali differenze nei framework alla base di varie parti dell'interfaccia utente. Ad esempio, la proprietà **Content** di un pulsante Windows Presentation Foundation (WPF), la proprietà **Caption** di un pulsante Microsoft Win32 e la proprietà **ALT** di un'immagine HTML sono tutte mappate a una singola proprietà, **Name**, nella visualizzazione Automazione interfaccia utente.

Automazione interfaccia utente offre funzionalità complete in Windows XP, Windows Server 2003 e versioni successive.

Automazione interfaccia utente provider di servizi sono componenti che implementano il supporto Automazione interfaccia utente per i controlli e offrono supporto per le applicazioni client Microsoft Active Accessibility, tramite un servizio di bridging predefinito.

> [!Note]  
> Automazione interfaccia utente non consente la comunicazione tra processi avviati da utenti diversi tramite il **comando Esegui come.**

 

In questo argomento sono contenute le sezioni seguenti.

-   [Automazione interfaccia utente componenti](#ui-automation-components)
-   [Automazione interfaccia utente di intestazione](#ui-automation-header-files)
-   [Modello di automazione interfaccia utente](#ui-automation-model)
-   [Argomenti correlati](#related-topics)

## <a name="ui-automation-components"></a>Automazione interfaccia utente componenti

Automazione interfaccia utente include quattro componenti principali, come illustrato nella tabella seguente.




| Componente | Descrizione | 
|-----------|-------------|
| Provider API | Set di interfacce COM implementate dai provider Automazione interfaccia utente com. Automazione interfaccia utente provider sono oggetti che forniscono informazioni sugli elementi dell'interfaccia utente e rispondono all'input a livello di codice. | 
| API client | Set di interfacce COM che consentono alle applicazioni client di ottenere informazioni sull'interfaccia utente e di inviare input ai controlli.<blockquote>[!Note]<br />Le funzioni descritte in <a href="uiauto-entry-cpfunctions.md">Deprecated Control Pattern Functions</a> (Funzioni del pattern di controllo deprecate) <a href="uiauto-entry-uianodefunctions.md">e Deprecated Node Functions</a> (Funzioni del nodo deprecate) sono deprecate. Le applicazioni client devono invece usare le Automazione interfaccia utente COM descritte in Automazione interfaccia utente <a href="uiauto-entry-uiautoclientinterfaces.md">Element Interfaces for Clients</a>.</blockquote><br /> | 
| UIAutomationCore.dll | La libreria di runtime, talvolta denominata Automazione interfaccia utente core, che gestisce la comunicazione tra provider e client. | 
| Oleacc.dll | Libreria di runtime per Microsoft Active Accessibility e gli oggetti proxy. La libreria fornisce anche oggetti proxy usati da Microsoft Microsoft Active Accessibility per Automazione interfaccia utente proxy per supportare i controlli Win32. | 




 

Esistono due modi per usare Automazione interfaccia utente: per creare il supporto per i controlli personalizzati usando l'API del provider e per creare applicazioni client che usano il core Automazione interfaccia utente per comunicare e recuperare informazioni sugli elementi dell'interfaccia utente. In base allo stato attivo, è necessario fare riferimento a parti diverse della documentazione. Se è necessario creare il supporto per i controlli personalizzati, Automazione interfaccia utente [guida per programmatori del provider](uiauto-providerportal.md)di servizi . Se è necessario comunicare con o recuperare informazioni sugli elementi dell'interfaccia utente, Automazione interfaccia utente manuale del [programmatore del client.](uiauto-clientportal.md)

## <a name="ui-automation-header-files"></a>Automazione interfaccia utente di intestazione

L Automazione interfaccia utente API è definita in diversi file di intestazione C/C++ inclusi in Windows Software Development Kit (SDK). I Automazione interfaccia utente di intestazione sono descritti nella tabella seguente:



| File di intestazione           | Descrizione                                                                                                                                                                                                                                                                      |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| UIAutomationClient.h  | Definisce le interfacce e gli elementi di programmazione correlati usati Automazione interfaccia utente client.                                                                                                                                                                                           |
| UIAutomationCore.h    | Definisce le interfacce e gli elementi di programmazione correlati utilizzati Automazione interfaccia utente provider.                                                                                                                                                                                         |
| UIAutomationCoreApi.h | Definisce costanti generali, GUID, tipi di dati e strutture usate Automazione interfaccia utente client e provider. Contiene anche le definizioni per le funzioni deprecate del nodo e del pattern di controllo.                                                                                    |
| UIAutomation.h        | Include tutti gli altri file Automazione interfaccia utente di intestazione. Poiché la maggior Automazione interfaccia utente richiede elementi da tutti i file di intestazione Automazione interfaccia utente, è meglio includere UIAutomation.h nei progetti dell'applicazione Automazione interfaccia utente anziché includere ogni singolo file. |



 

Se si sviluppa un'applicazione che usa l'API Automazione interfaccia utente, è necessario includere UIAutomation.h nel progetto. Se l'applicazione supporta Microsoft Active Accessibility, includere il file di intestazione Oleacc.h. Automazione interfaccia utente applicazioni che usano GUID richiedono anche il file di intestazione Initguid.h. Se necessario, Initguid.h deve essere incluso prima di UIAutomation.h.

## <a name="ui-automation-model"></a>Modello di automazione interfaccia utente

Automazione interfaccia utente espone ogni elemento dell'interfaccia utente alle applicazioni client come oggetto rappresentato [**dall'interfaccia IUIAutomationElement.**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) Gli elementi sono contenuti in una struttura ad albero, con il desktop come elemento radice. I client possono filtrare la visualizzazione non elaborata della struttura ad albero come visualizzazione controlli o visualizzazione contenuto. Queste visualizzazioni standard della struttura possono essere facilmente visibili usando l'applicazione [Inspect](inspect-objects.md) inclusa in Windows SDK. Le applicazioni possono inoltre creare visualizzazioni personalizzate.

Un Automazione interfaccia utente elemento espone le proprietà del controllo o dell'elemento dell'interfaccia utente rappresentato. Una di queste proprietà è il tipo di controllo , che definisce l'aspetto e la funzionalità di base del controllo o dell'elemento dell'interfaccia utente come singola entità riconoscibile, ad esempio un pulsante o una casella di controllo. Per altre informazioni sui tipi di controllo, vedere [Cenni Automazione interfaccia utente cenni preliminari sui tipi di controllo.](uiauto-controltypesoverview.md)

Inoltre, un elemento Automazione interfaccia utente espone uno o più pattern di controllo. Un pattern di controllo fornisce un set di proprietà specifiche di un particolare tipo di controllo. Un pattern di controllo espone anche metodi che consentono alle applicazioni client di ottenere altre informazioni sull'elemento e di fornire l'input all'elemento. Per altre informazioni sui pattern di controllo, vedere [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).

> [!Note]  
> Non esiste alcuna corrispondenza uno-a-uno tra i tipi di controllo e i pattern di controllo. Un pattern di controllo può essere supportato da più tipi di controllo e un controllo può supportare più pattern di controllo, ognuno dei quali espone aspetti diversi del comportamento. Ad esempio, una casella combinata dispone di almeno due pattern di controllo: uno che rappresenta la possibilità di espansione e compressione e un altro che rappresenta il meccanismo di selezione. Tuttavia, un controllo può presentare un solo tipo di controllo.

 

Automazione interfaccia utente fornisce informazioni alle applicazioni client tramite eventi. A differenza di WinEvents, Automazione interfaccia utente eventi non sono basati su un meccanismo di trasmissione. Automazione interfaccia utente client si registrano per notifiche di eventi specifiche e possono richiedere che proprietà specifiche e informazioni sul pattern di controllo siano passate ai relativi gestori eventi. Inoltre, un evento Automazione interfaccia utente contiene un riferimento all'elemento che lo ha generato. I provider possono migliorare le prestazioni generando eventi in modo selettivo, a seconda dei client in ascolto. Per altre informazioni sugli eventi, vedere [UI Automation Events Overview](uiauto-eventsoverview.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Cenni preliminari sui tipi di controllo per l'automazione interfaccia utente](uiauto-controltypesoverview.md)
</dt> <dt>

[Cenni preliminari sui pattern di controllo per l'automazione interfaccia utente](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Cenni preliminari sugli eventi di automazione interfaccia utente](uiauto-eventsoverview.md)
</dt> </dl>

 

 





