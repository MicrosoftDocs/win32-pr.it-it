---
title: Informazioni sui problemi di threading
description: Questo argomento descrive gli scenari di threading comuni per le implementazioni client di automazione interfaccia utente Microsoft e spiega come evitare i problemi che possono verificarsi se un client usa il threading in modo errato.
ms.assetid: 0772969a-da55-488e-8b21-7368434df8a9
keywords:
- client, problemi di threading di automazione interfaccia utente
- client, problemi di threading
- client, modello di threading del gestore eventi
- client, modello di threading del gestore eventi di automazione interfaccia utente
- client, affinità di automazione interfaccia utente
- client, affinità
- Automazione interfaccia utente, problemi di threading
- Automazione interfaccia utente, modello di threading del gestore eventi
- Automazione interfaccia utente, affinità
- problemi relativi al threading
- modello di threading del gestore eventi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a002132efe4055bb247c7d7290e271e153ac297e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104046797"
---
# <a name="understanding-threading-issues"></a>Informazioni sui problemi di threading

Questo argomento descrive gli scenari di threading comuni per le implementazioni client di automazione interfaccia utente Microsoft e spiega come evitare i problemi che possono verificarsi se un client usa il threading in modo errato.

In questo argomento sono incluse le sezioni seguenti:

-   [Automazione interfaccia utente e thread UI](#ui-automation-and-the-ui-thread)
-   [Modello di threading per i gestori eventi](#threading-model-for-event-handlers)
-   [Affinità di apartment COM in Windows a 64 bit](#com-apartment-affinity-on-64-bit-windows)
-   [Argomenti correlati](#related-topics)

## <a name="ui-automation-and-the-ui-thread"></a>Automazione interfaccia utente e thread UI

A causa del modo in cui automazione interfaccia utente usa i messaggi di Windows, i conflitti possono verificarsi quando un'applicazione client tenta di interagire con la propria interfaccia utente nel thread dell'interfaccia utente. Questi conflitti possono comportare prestazioni molto lente o addirittura causare l'interruzione della risposta da parte dell'applicazione.

Se l'applicazione client è progettata per interagire con tutti gli elementi sul desktop, inclusa la propria interfaccia utente, è necessario effettuare tutte le chiamate di automazione interfaccia utente da un thread separato. Ciò include l'individuazione di elementi, ad esempio, tramite [**IUIAutomationTreeWalker**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker) o il metodo [**IUIAutomationElement:: FindAll**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findall) e l'uso dei pattern di controllo. Questo thread non deve essere proprietario di alcuna finestra e deve essere un thread del modello di Component Object Model (COM) multithreading Apartment (MTA) (uno che inizializza COM chiamando [CoInitializeEx](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) con il flag **COinit \_ multithreading** ).

È possibile eseguire chiamate di automazione interfaccia utente in un gestore eventi di automazione interfaccia utente, poiché il gestore eventi viene sempre chiamato su un thread non dell'interfaccia utente. Tuttavia, quando si sottoscrive eventi che possono provenire dall'interfaccia utente dell'applicazione client, è necessario effettuare la chiamata a [**IUIAutomation:: AddAutomationEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addautomationeventhandler)o a un metodo correlato su un thread non dell'interfaccia utente (che deve essere anche un thread MTA). Rimuovere i gestori eventi sullo stesso thread.

Un client di automazione interfaccia utente non deve usare più thread per aggiungere o rimuovere i gestori eventi. Un comportamento imprevisto può verificarsi se un gestore eventi viene aggiunto o rimosso mentre un altro viene aggiunto o rimosso nello stesso processo client.

## <a name="threading-model-for-event-handlers"></a>Modello di threading per i gestori eventi

Un client di automazione interfaccia utente deve utilizzare il modello di threading MTA COM per i thread che implementano i gestori eventi. L'uso del modello STA (Single-Threaded Apartment) può causare problemi, ad esempio impedire ai client di rimuovere i gestori eventi dal thread.

## <a name="com-apartment-affinity-on-64-bit-windows"></a>Affinità di apartment COM in Windows a 64 bit

In base alla specifica COM, la durata di un oggetto remoto è regolata dalla durata dell'Apartment in cui viene chiamata la funzione [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) per creare l'oggetto. Quando l'Apartment originale viene arrestato, viene rilasciato anche l'oggetto remoto.

Per i client di automazione interfaccia utente, questo comportamento COM può indicare che la durata dell'helper 32/64 remoto (creata da UIAutomationCore.dll) usata da un elemento a 32 bit è regolata dalla durata dell'Apartment del thread che ha creato l'elemento. Se il client di automazione interfaccia utente esegue il marshalling dell'elemento in un altro thread, l'elemento può essere invalidato quando l'Apartment di origine si arresta. Il client di automazione interfaccia utente deve gestire correttamente questi problemi intercettando gli errori quando si usano gli elementi di automazione sottoposti a marshalling.

Lo stesso problema può verificarsi con un client di automazione interfaccia utente a 32 bit che contiene elementi a 64 bit.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Ottenere elementi di automazione interfaccia utente](uiauto-obtainingelements.md)
</dt> <dt>

[Sottoscrizione degli eventi di automazione interfaccia utente](uiauto-eventsforclients.md)
</dt> <dt>

[Cenni preliminari sugli eventi di automazione interfaccia utente](uiauto-eventsoverview.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[INFORMAZIONI: descrizioni e funzioni dei modelli di threading OLE](https://support.microsoft.com/kb/150777)
</dt> </dl>

 

 