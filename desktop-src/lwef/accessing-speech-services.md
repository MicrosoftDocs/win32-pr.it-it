---
title: Accesso a servizi vocali (interfaccia server Microsoft Agent)
description: Accesso ai servizi di riconoscimento vocale
ms.assetid: 99cf630d-3bd1-403a-833a-9173a84fe3c0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fda1369fa83c5e8ffaf7f08317f69a2a569620f3
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "106300895"
---
# <a name="accessing-speech-services-microsoft-agent-server-interface"></a>Accesso a servizi vocali (interfaccia server Microsoft Agent)

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

Sebbene i servizi di Microsoft Agent includano il supporto per l'input vocale, è necessario installare un motore di riconoscimento vocale per i comandi e i controlli compatibili per accedere ai servizi di input vocale dell'agente. Analogamente, se si desidera utilizzare i servizi di riconoscimento vocale di Microsoft Agent per supportare l'output vocale sintetizzato per un carattere, è necessario installare un motore di sintesi vocale (TTS) compatibile per il carattere. Poiché i servizi di sintesi vocale di Microsoft Agent sono basati su Microsoft Speech API (SAPI), è possibile usare qualsiasi motore che supporta compatibilmente le interfacce vocali richieste.

Per abilitare il supporto dell'input vocale nell'applicazione, definire un oggetto [**Command**](https://www.bing.com/search?q=**Command**) e impostare la relativa proprietà [**Voice**](https://www.bing.com/search?q=**Voice**) . Microsoft Agent caricherà automaticamente i servizi di riconoscimento vocale, in modo che quando l'utente preme il tasto ascolto o si chiama [**Listen**](https://www.bing.com/search?q=**Listen**), il motore di riconoscimento vocale verrà caricato. Per impostazione predefinita, l'ID lingua del carattere determinerà il motore caricato. Agent tenta di caricare il primo motore restituito da SAPI come corrispondente a questa lingua. Usare [**IAgentCharacterEx:: SetSRModeID**](IAgentCharacterEx::SetSRModeID) se si vuole caricare un motore specifico.

Per abilitare l'output di sintesi vocale, usare il metodo [**Speak**](https://www.bing.com/search?q=**Speak**) . Microsoft Agent tenterà automaticamente di caricare un motore che corrisponde all'ID lingua del carattere. Se la definizione del carattere include un ID specifico della modalità del motore TTS e tale motore è disponibile e corrisponde all'ID lingua del carattere, Agent carica tale motore per il carattere. In caso contrario, Agent carica il primo motore TTS che SAPI restituisce come corrispondente all'impostazione della lingua del carattere. È anche possibile usare [**IAgentCharacterEx:: SetTTSModeID**](IAgentCharacterEx::SetTTSModeID) per caricare un motore specifico.

In genere, Microsoft Agent carica un motore di riconoscimento vocale quando viene avviata la modalità di ascolto e carica un motore di sintesi vocale quando viene [**chiamato per la prima volta.**](https://www.bing.com/search?q=**Speak**) Tuttavia, se si desidera precaricare il motore di riconoscimento vocale, è possibile eseguire una query sulle proprietà correlate alle interfacce vocali. Ad esempio, la chiamata di [**IAgentCharacterEx:: GetSRModeID**](IAgentCharacterEx::GetSRModeID) o [**IAgentCharacterEx:: GetTTSModeID**](IAgentCharacterEx::GetTTSModeID) tenterà di caricare tale tipo di motore.

 

 




