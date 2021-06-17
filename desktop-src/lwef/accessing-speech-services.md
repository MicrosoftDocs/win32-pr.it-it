---
title: Accesso ai servizi Voce (interfaccia del server Microsoft Agent)
description: Informazioni sull'accesso ai servizi voce con l'interfaccia del server Microsoft Agent. Microsoft Agent è deprecato a livello di Windows 7.
ms.assetid: 99cf630d-3bd1-403a-833a-9173a84fe3c0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f87bf5cf88141344d5328592c9e823c7365c5d5
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262703"
---
# <a name="accessing-speech-services-microsoft-agent-server-interface"></a>Accesso ai servizi Voce (interfaccia del server Microsoft Agent)

\[Microsoft Agent è deprecato a livello di Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

Anche se i servizi di Microsoft Agent includono il supporto per l'input vocale, è necessario installare un motore di riconoscimento vocale compatibile per accedere ai servizi di input vocale di Agent. Analogamente, se si vogliono usare i servizi voce di Microsoft Agent per supportare l'output vocale sintetizzato per un carattere, è necessario installare un motore di sintesi vocale compatibile per il carattere. Poiché i servizi voce di Microsoft Agent sono basati su Microsoft Speech API (SAPI), è possibile usare qualsiasi motore compatibile che supporti le interfacce vocali necessarie.

Per abilitare il supporto dell'input vocale nell'applicazione, definire un [**oggetto Command**](https://www.bing.com/search?q=**Command**) e impostarne [**la proprietà**](https://www.bing.com/search?q=**Voice**) Voice. Microsoft Agent carica automaticamente i servizi voce, in modo che quando l'utente preme il tasto di ascolto o si chiama [**Listen**](https://www.bing.com/search?q=**Listen**), verrà caricato il motore di riconoscimento vocale. Per impostazione predefinita, l'ID lingua del carattere determinerà il motore caricato. Agent tenta di caricare il primo motore restituito da SAPI come corrispondente a questo linguaggio. Usare **IAgentCharacterEx::SetSRModeID** se si vuole caricare un motore specifico.

Per abilitare l'output della sintesi vocale, usare il [**metodo Speak.**](https://www.bing.com/search?q=**Speak**) Microsoft Agent tenterà automaticamente di caricare un motore che corrisponde all'ID lingua del carattere. Se la definizione del carattere include un ID della modalità del motore TTS specifico e tale motore è disponibile e corrisponde all'ID lingua del carattere, Agent carica tale motore per il carattere. In caso contrario, Agent carica il primo motore TTS restituito da SAPI come corrispondente all'impostazione della lingua del carattere. È anche possibile usare **IAgentCharacterEx::SetTTSModeID** per caricare un motore specifico.

In genere, Microsoft Agent carica un motore di riconoscimento vocale quando viene avviata la modalità di ascolto e carica un motore di sintesi vocale quando [**si chiama Speak**](https://www.bing.com/search?q=**Speak**) per la prima volta. Tuttavia, se si vuole precaricare il motore di riconoscimento vocale, è possibile eseguire una query delle proprietà correlate alle interfacce vocali. Ad esempio, la chiamata **di IAgentCharacterEx::GetSRModeID** o **IAgentCharacterEx::GetTTSModeID** tenterà di caricare tale tipo di motore.

 

 




