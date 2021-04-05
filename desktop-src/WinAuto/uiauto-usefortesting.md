---
title: Utilizzo di automazione interfaccia utente per il test automatico
description: Questa panoramica descrive il modo in cui l'automazione interfaccia utente Microsoft può essere utile come Framework per l'accesso a livello di codice in scenari di test automatici.
ms.assetid: 192162f9-55bf-4111-9f15-c0d3b5af2ab7
keywords:
- client, test automatizzati di automazione interfaccia utente
- client, test automatizzati
- client, test
- client, strumenti per test automatizzati
- client, strumenti di automazione interfaccia utente per test automatizzati
- client, test di automazione interfaccia utente
- Automazione interfaccia utente, test automatizzati
- Automazione interfaccia utente, test
- Automazione interfaccia utente, strumenti per test automatizzati
- test automatizzato
- strumenti per test automatizzati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 269ff32cae26f8bb8ea6bb5b55ac91f1e0486685
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044722"
---
# <a name="using-ui-automation-for-automated-testing"></a>Utilizzo di automazione interfaccia utente per il test automatico

Questa panoramica descrive il modo in cui l'automazione interfaccia utente Microsoft può essere utile come Framework per l'accesso a livello di codice in scenari di test automatici.

Automazione interfaccia utente fornisce un modello a oggetti unificato che consente a tutti i Framework dell'interfaccia utente di esporre funzionalità complesse e complete in modo accessibile e automatizzato.

Automazione interfaccia utente è stato sviluppato come successore di Microsoft Active Accessibility, un Framework progettato per offrire una soluzione per rendere accessibili controlli e applicazioni. Microsoft Active Accessibility non è stata progettata con l'automazione di test, anche se si è evoluta in questo ruolo a causa dei requisiti simili di accessibilità e automazione. L'automazione interfaccia utente è progettata appositamente per fornire funzionalità affidabili per i test automatizzati, oltre a offrire soluzioni più raffinate per l'accessibilità. Microsoft Active Accessibility, ad esempio, si basa su una singola interfaccia per esporre informazioni sull'interfaccia utente e per raccogliere le informazioni necessarie ai prodotti di Assistive Technology. Automazione interfaccia utente separa i due modelli.

È necessario che un provider e un client implementino l'automazione dell'interfaccia utente affinché risulti utile come strumento di test automatizzato. I provider di automazione interfaccia utente sono applicazioni come Microsoft Word, Microsoft Excel e altre applicazioni di terze parti o controlli basati sul sistema operativo Windows. I client di automazione interfaccia utente includono script di test automatizzati e applicazioni di assistive technology.

In questo argomento sono contenute le sezioni seguenti.

-   [Automazione interfaccia utente nei provider](#ui-automation-in-providers)
-   [Automazione interfaccia utente nei client](#ui-automation-in-clients)
    -   [Accesso a livello di codice](#programmatic-access)
-   [Proprietà chiave per l'automazione di test](#key-properties-for-test-automation)
-   [Strumenti e tecnologie correlati](#related-tools-and-technologies)
-   [Argomenti correlati](#related-topics)

## <a name="ui-automation-in-providers"></a>Automazione interfaccia utente nei provider

Per automatizzare un elemento dell'interfaccia utente, lo sviluppatore deve esaminare le azioni che un utente finale può eseguire sull'oggetto dell'interfaccia utente usando l'interazione standard con la tastiera e il mouse. Una volta identificate queste azioni chiave, i pattern di controllo di automazione interfaccia utente che riflettono le funzionalità e il comportamento dell'elemento dell'interfaccia utente devono essere implementati sul controllo. Ad esempio, l'interazione dell'utente con un controllo casella combinata comporta in genere l'espansione e la compressione della casella combinata per visualizzare o nascondere un elenco di elementi, la selezione di un elemento dall'elenco o l'aggiunta di un nuovo valore tramite input da tastiera.

Con altri modelli di accessibilità, è necessario che gli sviluppatori raccolgano le informazioni direttamente da singoli pulsanti, menu o altri controlli. Ogni tipo di controllo è costituito da decine di varianti secondarie. In altre parole, anche se 10 varianti di un pulsante funzionano allo stesso modo ed eseguono la stessa funzione, devono essere trattate come controlli univoci. Non è possibile sapere se tali controlli sono equivalenti a livello funzionale. I pattern di controllo di automazione interfaccia utente sono stati sviluppati per rappresentare questi comportamenti comuni del controllo. Per altre informazioni, vedere [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).

Senza il modello unificato dei pattern di controllo forniti dall'automazione interfaccia utente, gli strumenti di test e gli sviluppatori devono disporre di informazioni specifiche del Framework per esporre le proprietà e controllare i comportamenti in tale Framework. Poiché molti diversi framework dell'interfaccia utente possono essere presenti contemporaneamente nei sistemi operativi Windows, tra cui Microsoft Win32, Windows Form e Windows Presentation Foundation (WPF), può essere un'attività ardua testare più applicazioni con controlli simili. La tabella seguente elenca ad esempio i nomi delle proprietà specifiche del Framework necessari per recuperare il nome o il testo associato a un controllo Button e Mostra la proprietà di automazione interfaccia utente equivalente.



| Tipo di controllo | Framework dell'interfaccia utente | Proprietà specifica del Framework | Proprietà di automazione interfaccia utente |
|--------------|--------------|-----------------------------|------------------------|
| Pulsante       | WPF          | Content                     | Name (proprietà)          |
| Pulsante       | Win32        | Didascalia                     | Name (proprietà)          |
| Immagine        | HTML         | alt                         | Name (proprietà)          |



 

I provider di automazione interfaccia utente sono responsabili del mapping delle proprietà specifiche del Framework dei controlli alle proprietà di automazione interfaccia utente equivalenti. Per informazioni sull'implementazione di automazione interfaccia utente in un provider, vedere [UI Automation provider Programmer ' s Guide](uiauto-providerportal.md). Per informazioni sull'implementazione di pattern di controllo, vedere [implementazione dei pattern di controllo di automazione interfaccia utente](uiauto-implementinguiautocontrolpatterns.md).

## <a name="ui-automation-in-clients"></a>Automazione interfaccia utente nei client

L'obiettivo di scenari e strumenti di test automatizzati è la modifica coerente e ripetibile dell'interfaccia utente. Ad esempio, può comportare l'esecuzione di controlli specifici di unit test e la registrazione e l'esecuzione di script di test che eseguono l'iterazione di una serie di azioni generiche su un gruppo di controlli.

Una complicazione nelle applicazioni automatiche è la difficoltà di sincronizzare un test con una destinazione dinamica, ad esempio, un controllo casella di riepilogo, ad esempio Gestione attività di Windows, che visualizza un elenco di applicazioni attualmente in esecuzione. Poiché gli elementi nella casella di riepilogo vengono aggiornati dinamicamente all'esterno del controllo dell'applicazione di test, un tentativo di ripetere la selezione di un elemento specifico nella casella di riepilogo con qualsiasi coerenza è impossibile. Problemi simili possono verificarsi quando si tenta di ripetere semplici modifiche dello stato attivo in un'interfaccia utente esterna al controllo dell'applicazione di test.

### <a name="programmatic-access"></a>Accesso a livello di codice

L'accesso a livello di codice consente di imitare, tramite codice, qualsiasi interazione ed esperienza esposta dall'input tradizionale di mouse e tastiera. Automazione interfaccia utente consente l'accesso a livello di codice tramite cinque componenti:

-   L'albero di automazione interfaccia utente facilita la navigazione nella struttura dell'interfaccia utente. L'albero è compilato dalla raccolta di **HWND**. Per altre informazioni, vedere [Panoramica dell'albero di automazione interfaccia utente](uiauto-treeoverview.md).
-   Gli elementi di automazione sono singoli componenti dell'interfaccia utente. Spesso possono essere più granulari di un **HWND**.
-   Le proprietà di automazione forniscono informazioni specifiche sugli elementi dell'interfaccia utente. Per altre informazioni, vedere [UI Automation Properties Overview](uiauto-propertiesoverview.md).
-   I pattern di controllo definiscono un determinato aspetto della funzionalità di un controllo e possono essere costituiti da informazioni di proprietà, metodo, evento e struttura. Per altre informazioni, vedere [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).
-   Gli eventi di automazione forniscono notifiche e informazioni sugli eventi. Per altre informazioni, vedere [UI Automation Events Overview](uiauto-eventsoverview.md).

## <a name="key-properties-for-test-automation"></a>Proprietà chiave per l'automazione di test

La possibilità di identificare in modo univoco e di trovare successivamente qualsiasi controllo nell'interfaccia utente costituisce la base per le applicazioni di test automatizzate che operano su tale interfaccia utente. Nella tabella seguente sono descritte le proprietà di automazione interfaccia utente utilizzate da client e provider per identificare e individuare i controlli.



| Proprietà     | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AutomationId | Distingue in modo univoco un elemento di automazione dagli elementi di pari livello. Il supporto per la proprietà AutomationId non è obbligatorio. Quando è disponibile, la proprietà AutomationId di un elemento è la stessa in qualsiasi istanza dell'applicazione, indipendentemente dalla lingua locale. Anche se la proprietà AutomationId è univoca tra gli elementi di pari livello, potrebbe non essere univoca nell'intero desktop. Ad esempio, più istanze di un'applicazione o più visualizzazioni di cartelle in Microsoft Windows Explorer possono contenere elementi con lo stesso AutomationIdProperty, ad esempio "SystemMenuBar". I client non devono fare supposizioni sui AutomationIds esposti da altre applicazioni. AutomationId non è garantito che sia stabile in versioni o Build diverse di un'applicazione. |
| ControlType  | Identifica il tipo di controllo rappresentato da un elemento di automazione. La conoscenza del tipo di controllo consente di acquisire informazioni significative. Per altre informazioni, vedere [UI Automation Control Types Overview](uiauto-controltypesoverview.md).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Nome         | Stringa di testo che identifica o spiega lo scopo di un elemento di automazione. Deve essere usata con cautela perché può essere localizzata. La proprietà Name non è un identificatore univoco tra gli elementi di pari livello. Per l'automazione di test, i client devono invece usare la proprietà AutomationId o la proprietà IDruntime.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| IDruntime    | Matrice di numeri interi che rappresentano un identificatore per un elemento di automazione. L'identificatore è univoco sul desktop, ma è sicuramente univoco solo per l'interfaccia utente del desktop in cui è stato generato. Gli identificatori possono essere riutilizzati nel tempo. Usare [**IUIAutomation:: CompareElements**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-compareelements) per determinare se l'elemento che dispone attualmente di un determinato ID di runtime è lo stesso elemento che in precedenza aveva tale ID. Inoltre, il formato della proprietà IDruntime può cambiare. Deve essere trattato come un valore opaco e utilizzato solo per il confronto. ad esempio, per determinare se un elemento di automazione si trova nella cache.                                                                                                                       |



 

## <a name="related-tools-and-technologies"></a>Strumenti e tecnologie correlati

[Controllare](inspect-objects.md) (Inspect.exe) è uno strumento basato su Windows che è possibile utilizzare per raccogliere informazioni di automazione interfaccia utente per lo sviluppo e il debug di provider e client. Il controllo è incluso nel Software Development Kit (SDK) di Windows.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Considerazioni sulla sicurezza di automazione interfaccia utente](uiauto-securityoverview.md)
</dt> </dl>

 

 




