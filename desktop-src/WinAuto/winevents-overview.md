---
title: Panoramica di WinEvents e Active Accessibility
description: I server Microsoft Active Accessibility generano WinEvents per notificare ai client quando un oggetto accessibile viene modificato.
ms.assetid: a2d486ee-84ef-4c44-a832-dbc0dae81542
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b351b1ce7b6337c4ca0ac0827daff2978c6611af
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "103956139"
---
# <a name="winevents-and-active-accessibility"></a>WinEvents e Active Accessibility

I server Microsoft Active Accessibility generano *winEvents* per notificare ai client quando un oggetto accessibile viene modificato. Esistono numerose condizioni in cui un server invia una notifica a un client di una modifica. Ogni [costante di evento](event-constants.md) definita da Microsoft Active Accessibility descrive una condizione per cui un client riceve una notifica. Ad esempio, WinEvents può segnalare:

- Quando un oggetto viene creato o eliminato definitivamente.
- Quando un oggetto riceve o perde lo stato attivo.
- Quando viene modificato lo stato o la posizione di un oggetto.
- Quando viene modificata una proprietà di un oggetto.

Le applicazioni client non ricevono automaticamente le notifiche degli eventi; devono specificare gli eventi che vogliono ricevere chiamando la funzione [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook) . Con **SetWinEventHook**, un client esegue la registrazione per ricevere uno o più eventi e imposta una funzione hook per la gestione degli eventi specificati. I client possono usare la stessa funzione hook per gestire più tipi di eventi oppure possono usare funzioni hook multipe. I client chiamano **SetWinEventHook** una volta per ogni funzione hook che deve registrare.

Le funzioni hook si trovano all'interno del corpo del codice del client, in una DLL mappata al processo del client o in una DLL mappata al processo del server. Ognuno di questi metodi presenta vantaggi e svantaggi. Per altre informazioni, vedere [funzioni hook nel contesto e out-of-Context](in-context-and-out-of-context-hook-functions.md).

Per notificare ai client l'occorrenza di un evento, i server chiamano [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent). Il sistema controlla se le applicazioni client dispongono di funzioni hook impostate per l'evento e chiama le funzioni hook appropriate in base alle esigenze.

Quando viene chiamata la funzione hook del client, riceve un numero di parametri che descrivono l'evento e l'oggetto che ha generato l'evento. Per ottenere l'accesso all'oggetto che ha generato l'evento, la funzione di hook client chiama [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent).

> [!NOTE]
> Se nessun client è stato registrato per la ricezione di WinEvents, l'effetto sulle prestazioni di un server per chiamare [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) è irrilevante.
>
> I server chiamano [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) per le modifiche solo nei propri oggetti accessibili; non chiamano **NotifyWinEvent** per le modifiche negli elementi dell'interfaccia utente forniti dal sistema.

## <a name="event-driven-communication"></a>Comunicazione Event-Driven

Per poter ricevere notifiche WinEvent, i client devono registrare un hook WinEvent. Per evitare callback superflui e migliorare le prestazioni, è consigliabile che i client si registrino solo per gli eventi che devono ricevere.

All'interno della routine hook, il client può chiamare [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent) per recuperare un oggetto [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) per l'elemento a cui si applica l'evento. Con questo oggetto, il client può iniziare a chiamare i metodi **IAccessible** per recuperare informazioni o interagire con l'elemento dell'interfaccia utente.

## <a name="related-topics"></a>Argomenti correlati

[WinEvents](winevents-infrastructure.md)
