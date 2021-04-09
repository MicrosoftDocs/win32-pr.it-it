---
title: Accesso ai servizi di riconoscimento vocale (controllo agente Microsoft)
description: Accesso ai servizi di riconoscimento vocale
ms.assetid: c6c10f2a-a433-4a8e-a069-48e3c2032fb8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83459cfd7ee478fca7d2cf2d25c4c1d590d8ed54
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "103739658"
---
# <a name="accessing-speech-services-microsoft-agent-control"></a>Accesso ai servizi di riconoscimento vocale (controllo agente Microsoft)

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

Sebbene i servizi di Microsoft Agent includano il supporto per l'input vocale, è necessario installare un motore di riconoscimento vocale per i comandi e i controlli compatibili per accedere ai servizi di input vocale dell'agente. Analogamente, se si desidera utilizzare i servizi di riconoscimento vocale di Microsoft Agent per supportare l'output vocale sintetizzato per un carattere, è necessario installare un motore di sintesi vocale (TTS) compatibile per il carattere.

Per abilitare il supporto dell'input vocale nell'applicazione, definire un oggetto [**Command**](https://www.bing.com/search?q=**Command**) e impostare la relativa proprietà [**Voice**](https://www.bing.com/search?q=**Voice**) . Agent caricherà automaticamente i servizi di riconoscimento vocale, in modo che quando l'utente preme il tasto di ascolto o si chiama [**Listen**](https://www.bing.com/search?q=**Listen**), il motore di riconoscimento vocale verrà caricato. Per impostazione predefinita, il [**LanguageID**](https://www.bing.com/search?q=**LanguageID**) del carattere determinerà il motore caricato. Agent tenta di caricare il primo motore restituito da Microsoft Speech API (SAPI) come corrispondente a questa lingua. Usare [**SRModeID**](https://www.bing.com/search?q=**SRModeID**) se si vuole caricare un motore specifico.

Per abilitare l'output di sintesi vocale, usare il metodo [**Speak**](https://www.bing.com/search?q=**Speak**) . Agent tenterà automaticamente di caricare un motore che corrisponde al [**LanguageID**](https://www.bing.com/search?q=**LanguageID**)del carattere. Se la definizione del carattere include un ID specifico della modalità del motore TTS e il motore è disponibile e corrisponde al **LanguageID** del carattere, Agent carica tale motore per il carattere. In caso contrario, carica il primo motore TTS restituito da SAPI come corrispondente all'impostazione della lingua del carattere. È anche possibile usare [**TTSModeID**](https://www.bing.com/search?q=**TTSModeID**) per caricare un motore specifico.

In genere, Agent carica il riconoscimento vocale quando viene avviata la modalità di ascolto e un motore di sintesi vocale quando [**parla**](https://www.bing.com/search?q=**Speak**) viene chiamato per la prima volta. Tuttavia, se si desidera precaricare il motore di riconoscimento vocale, è possibile eseguire una query sulle proprietà correlate alle interfacce di riconoscimento vocale. Ad esempio, se si esegue una query su [**SRModeID**](https://www.bing.com/search?q=**SRModeID**) o [**TTSModeID**](https://www.bing.com/search?q=**TTSModeID**) si tenterà di caricare tale tipo di motore.

Poiché i servizi di sintesi vocale di Microsoft Agent sono basati sulla Speech API Microsoft, è possibile usare qualsiasi motore che supporti le interfacce vocali richieste.

 

 




