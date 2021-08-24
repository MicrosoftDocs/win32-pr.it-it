---
title: Cenni preliminari sui Active Accessibility WinEvents
description: Microsoft Active Accessibility generano Eventi WinEvent per notificare ai client quando viene modificato un oggetto accessibile.
ms.assetid: a2d486ee-84ef-4c44-a832-dbc0dae81542
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95507ff1b6cd56451dd7f9acc04014c6013a7179d536565b3518bccb9137e689
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052179"
---
# <a name="winevents-and-active-accessibility"></a>Eventi WinEvent e Active Accessibility

Microsoft Active Accessibility generano *Eventi WinEvent per* notificare ai client quando viene modificato un oggetto accessibile. Esistono numerose condizioni in cui un server invia una notifica a un client di una modifica. Ogni [costante di](event-constants.md) evento definita da Microsoft Active Accessibility descrive una condizione per cui un client viene notificato. Ad esempio, WinEvents può segnalare:

- Quando un oggetto viene creato o eliminato.
- Quando un oggetto riceve o perde lo stato attivo.
- Quando lo stato o la posizione di un oggetto cambia.
- Quando una proprietà di un oggetto viene modificata.

Le applicazioni client non ricevono automaticamente le notifiche degli eventi. Devono specificare gli eventi che vogliono ricevere chiamando la [**funzione SetWinEventHook.**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook) Con **SetWinEventHook,** un client si registra per ricevere uno o più eventi e imposta una funzione hook per gestire gli eventi specificati. I client possono usare la stessa funzione hook per gestire più tipi di eventi oppure possono usare funzioni hook multipe. I client chiamano **SetWinEventHook una** volta per ogni funzione hook che deve registrare.

Le funzioni hook si trovano all'interno del corpo del codice del client, in una DLL mappata al processo del client o in una DLL mappata al processo del server. Ognuno di questi metodi presenta vantaggi e svantaggi. Per altre informazioni, vedere Funzioni hook nel contesto e [out-of-context.](in-context-and-out-of-context-hook-functions.md)

Per notificare ai client l'occorrenza di un evento, i server [**chiamano NotifyWinEvent.**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) Il sistema controlla se le applicazioni client hanno impostato funzioni hook per l'evento e chiama le funzioni hook appropriate in base alle esigenze.

Quando viene chiamata la funzione hook del client, riceve una serie di parametri che descrivono l'evento e l'oggetto che ha generato l'evento. Per ottenere l'accesso all'oggetto che ha generato l'evento, la funzione hook client chiama [**AccessibleObjectFromEvent.**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent)

> [!NOTE]
> Se nessun client si è registrato per ricevere WinEvent, l'impatto sulle prestazioni su un server per chiamare [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) è trascurabile.
>
> I server [**chiamano NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) per le modifiche solo nei propri oggetti accessibili; Non chiamano **NotifyWinEvent per le** modifiche negli elementi dell'interfaccia utente forniti dal sistema.

## <a name="event-driven-communication"></a>Event-Driven comunicazione

I client devono registrare un hook WinEvent prima di poter ricevere notifiche WinEvent. Per evitare callback non necessari e migliorare le prestazioni, è consigliabile registrare i client solo per gli eventi che devono ricevere.

All'interno della routine hook, il client può chiamare [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent) per recuperare un [**oggetto IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) per l'elemento a cui si applica l'evento. Con questo oggetto, il client può iniziare a chiamare i **metodi IAccessible** per recuperare informazioni o interagire con l'elemento dell'interfaccia utente.

## <a name="related-topics"></a>Argomenti correlati

[WinEvents](winevents-infrastructure.md)
