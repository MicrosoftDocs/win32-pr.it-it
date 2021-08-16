---
title: Eventi di input vocale
description: Eventi di input vocale
ms.assetid: d7b621fe-9274-4b16-af8a-664b0b296c89
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3babdfb38f302bd2ca5934fec4d8b54a84f7452befbec0dfba45b078747f532
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118746262"
---
# <a name="speech-input-events"></a>Eventi di input vocale

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

Inoltre, per la notifica degli eventi [**Command,**](command-event.md) Agent notifica anche al client attivo di input quando il server attiva o disattiva la modalità di ascolto, usando gli eventi [**ListenStart**](listenstart-event.md) e [**ListenComplete**](listencomplete-event.md) ([**IAgentNotifySinkEx::ListeningState**](iagentnotifysinkex--listeningstate.md)). Tuttavia, se l'utente preme il tasto modalità di ascolto e non è disponibile alcun motore di riconoscimento vocale corrispondente per il carattere più in alto del client attivo di input, il server avvia il timeout della modalità tasto di scelta rapida Ascolto, ma non genera un evento **ListenStart** per il client attivo del carattere. Se, prima del completamento del timeout, l'utente attiva un altro carattere con il supporto del motore di riconoscimento vocale, il server tenta di attivare l'input vocale e genera **l'evento ListenStart.**

Analogamente, se un client tenta di attivare la modalità di ascolto usando il metodo [**Listen**](listen-method.md) e non è disponibile alcun motore di riconoscimento vocale corrispondente, la chiamata non riesce e il server non genera un [**evento ListenStart.**](listenstart-event.md) Nel controllo Microsoft Agent il metodo **Listen** restituisce **False,** ma la chiamata non genera un errore.

Quando la modalità tasto di ascolto è attivata e l'utente passa a un carattere che usa un motore di riconoscimento vocale diverso, il server passa a tale motore e lo attiva e attiva un evento [**ListenComplete**](listencomplete-event.md) e quindi un evento [**ListenStart.**](listenstart-event.md) Se il carattere attivato non dispone di un motore di riconoscimento vocale disponibile (perché uno non è installato o nessuno corrisponde all'impostazione dell'ID lingua del carattere attivato), il server attiverà l'evento **ListenComplete** per il carattere attivato in precedenza e passerà un valore nel **parametro Causa.** Tuttavia, il server non genera eventi **ListenStart** o **ListenComplete** per i client che non dispongono del supporto per il riconoscimento vocale.

Se un client chiama correttamente il metodo [**Listen**](listen-method.md) e un carattere senza supporto del motore di riconoscimento vocale diventa attivo per l'input prima del completamento del timeout della modalità di ascolto e quindi l'utente torna al carattere del client originale, il server genererà un evento [**ListenStart**](listenstart-event.md) per tale client.

Se il client attivo per l'input cambia i motori di riconoscimento vocale modificando [**SRModeID**](srmodeid-property.md) in modalità di ascolto, il server passa a tale motore e lo attiva senza riattivare [**l'evento ListenStart.**](listenstart-event.md) Tuttavia, se il motore specificato non è disponibile, la chiamata non riesce (genera un errore nel controllo) e il server chiama anche [**l'evento ListenComplete.**](listencomplete-event.md)

 

 




