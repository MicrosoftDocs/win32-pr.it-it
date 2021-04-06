---
title: Eventi di input vocale
description: Eventi di input vocale
ms.assetid: d7b621fe-9274-4b16-af8a-664b0b296c89
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0dc75bb010286b7645c206d192913017472829d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045384"
---
# <a name="speech-input-events"></a>Eventi di input vocale

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

Inoltre, per la notifica degli eventi di [**comando**](command-event.md) , Agent invia una notifica al client di input-Active anche quando il server attiva o disattiva la modalità di ascolto, usando gli eventi [**ListenStart**](listenstart-event.md) e [**ListenComplete**](listencomplete-event.md) ([**IAgentNotifySinkEx:: ListeningState**](iagentnotifysinkex--listeningstate.md)). Tuttavia, se l'utente preme il tasto modalità di ascolto e non è disponibile alcun motore di riconoscimento vocale corrispondente per il carattere di primo livello del client attivo di input, il server avvia il timeout della modalità di scelta rapida in ascolto, ma non genera un evento **ListenStart** per il client attivo del carattere. Se, prima del completamento del timeout, l'utente attiva un altro carattere con supporto del motore di riconoscimento vocale, il server tenta di attivare l'input vocale e genera l'evento **ListenStart** .

Analogamente, se un client tenta di attivare la modalità di ascolto utilizzando il metodo [**Listen**](listen-method.md) e non è disponibile alcun motore di riconoscimento vocale corrispondente, la chiamata ha esito negativo e il server non genera un evento [**ListenStart**](listenstart-event.md). Nel controllo Microsoft Agent il metodo **Listen** restituisce **false**, ma la chiamata non genera alcun errore.

Quando la modalità della chiave di ascolto è attiva e l'utente passa a un carattere che usa un motore di riconoscimento vocale diverso, il server passa a e attiva il motore e attiva un [**ListenComplete**](listencomplete-event.md) e quindi un evento [**ListenStart**](listenstart-event.md) . Se il carattere attivato non dispone di un motore di riconoscimento vocale disponibile (poiché non ne è installato uno oppure nessuno corrisponde all'impostazione dell'ID lingua del carattere attivato), il server attiverà l'evento **ListenComplete** per il carattere attivato in precedenza e passa di nuovo un valore nel parametro **causa** . Tuttavia, il server non genera eventi **ListenStart** o **ListenComplete** per i client che non dispongono del supporto per il riconoscimento vocale.

Se un client chiama correttamente il metodo [**Listen**](listen-method.md) e un carattere senza supporto del motore di riconoscimento vocale diventa input-attivo prima del completamento del timeout della modalità di ascolto, quindi l'utente torna al carattere del client originale, il server genererà un evento [**ListenStart**](listenstart-event.md) per quel client.

Se il client attivo di input passa i motori di riconoscimento vocale cambiando [**SRModeID**](srmodeid-property.md) in modalità di ascolto, il server passa a e attiva il motore senza riattivare l'evento [**ListenStart**](listenstart-event.md) . Tuttavia, se il motore specificato non è disponibile, la chiamata ha esito negativo (genera un errore nel controllo) e il server chiama anche l'evento [**ListenComplete**](listencomplete-event.md) .

 

 




