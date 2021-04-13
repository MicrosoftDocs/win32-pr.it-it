---
title: Le applicazioni desktop potrebbero non essere visibili dopo l'avvio del Web browser predefinito o delle app di Windows Store
description: Le applicazioni desktop potrebbero non essere visibili dopo l'avvio del Web browser predefinito o delle app di Windows Store
ms.assetid: 5D2CE14B-111D-4987-A9AA-B04AC030F9F0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20c80541a860bd29f207ab99eba6ab4cb629a666
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/01/2020
ms.locfileid: "104339406"
---
# <a name="desktop-apps-may-not-be-visible-after-launching-the-default-web-browser-or-windows-store-apps"></a>Le applicazioni desktop potrebbero non essere visibili dopo l'avvio del Web browser predefinito o delle app di Windows Store

## <a name="platforms"></a>Piattaforme

**Client** -Windows 8  
**Server** : Windows Server 2012  


## <a name="description"></a>Descrizione

L'esperienza utente dell'app di Windows Store è incentrata su una singola app alla volta, con il multitasking, il cambio di app e le notifiche fornite dall'interfaccia utente di Windows. Le app di Windows Store sono dimensionate per riempire lo spazio disponibile sullo schermo, con la visualizzazione più comune a schermo intero. Pertanto, quando viene avviata un'altra app nel sistema, non è più possibile presupporre che la nuova app verrà aperta in una finestra del desktop insieme all'app desktop. Questo è sempre vero per le app di Windows Store e i browser che scelgono di partecipare alla nuova esperienza dell'interfaccia utente di Windows. È possibile continuare a visualizzare altre app allo stesso tempo, ad esempio se si è sul desktop e avviare un'altra applicazione desktop o se si dispone di applicazioni in uno stato bloccato.

## <a name="manifestation"></a>Manifestazione

Quando un'app desktop usa tecniche comuni di attivazione dell'app, ad esempio l'uso dell'API ShellExecute in un file o un protocollo, Windows avvia l'app associata a tale registrazione, che può essere un'app di Windows Store e/o il Web browser predefinito dell'utente. il Web browser predefinito può scegliere di partecipare al desktop o alla nuova interfaccia utente di Windows. Le app di Windows Store vengono avviate usando l'intero schermo, nascondendo il desktop e l'app desktop da cui è stata avviata.

> [!Note]  
> In Windows 8, Internet Explorer 10 è configurato come browser predefinito dell'utente, ma l'utente può scegliere di installare e impostare un altro browser come predefinito (nessuna modifica da Windows 7). In Internet Explorer 10, quando un collegamento viene aperto da un'applicazione desktop, viene aperto Internet Explorer sul desktop. Questa impostazione può tuttavia essere modificata dagli utenti in modo che Internet Explorer venga aperto come app di Windows Store. I fornitori di browser sono stati invitati ad adottare un'esperienza di "avvio contestuale" simile. Tuttavia, gli sviluppatori devono pianificare il fatto che non tutti i browser si comporteranno in modo analogo.

 

## <a name="mitigation"></a>Strategia di riduzione del rischio

Sebbene non vi siano modifiche che gli sviluppatori possono apportare alle proprie app per attenuare questo comportamento, è possibile che l'utente finale possa comunicare con essi. Provare a usare le informazioni raccolte dall'API estesa ShellExecuteEx () per popolare una finestra di dialogo opportunamente appropriata. In tale finestra di dialogo indicare all'utente quale app verrà avviata e se tale app è un'app di Windows Store o un'app desktop. Il CLSID può essere usato per distinguere le app di Windows Store dalle applicazioni desktop. Opzioni utente:

-   Gli utenti che dispongono di un monitor a schermo intero possono bloccare l'app di Windows Store sul bordo dello schermo per esporre il desktop e quindi visualizzare contemporaneamente l'app di Windows Store e l'app desktop.
-   Se Internet Explorer è configurato come browser predefinito dell'utente, gli utenti possono modificarne il comportamento cambiando le opzioni Internet nel pannello di controllo. Nella scheda programmi gli utenti possono modificare il modo in cui Internet Explorer gestisce i collegamenti. Altri browser possono offrire un'impostazione simile.

 

 




