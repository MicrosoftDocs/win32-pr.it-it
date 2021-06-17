---
title: Accesso ai servizi voce (controllo di Microsoft Agent)
description: Informazioni sull'accesso ai servizi voce con Il controllo di Microsoft Agent. Microsoft Agent è deprecato a livello di Windows 7.
ms.assetid: c6c10f2a-a433-4a8e-a069-48e3c2032fb8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 035bde03d18b77ce43c47375f2075bba02416c39
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262713"
---
# <a name="accessing-speech-services-microsoft-agent-control"></a>Accesso ai servizi voce (controllo di Microsoft Agent)

\[Microsoft Agent è deprecato a livello di Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

Anche se i servizi di Microsoft Agent includono il supporto per l'input vocale, è necessario installare un motore di riconoscimento vocale compatibile per accedere ai servizi di input vocale di Agent. Analogamente, se si vogliono usare i servizi voce di Microsoft Agent per supportare l'output vocale sintetizzato per un carattere, è necessario installare un motore di sintesi vocale (TTS) compatibile per il carattere.

Per abilitare il supporto dell'input vocale nell'applicazione, definire un [**oggetto Command**](https://www.bing.com/search?q=**Command**) e impostarne la [**proprietà Voice.**](https://www.bing.com/search?q=**Voice**) Agent carica automaticamente i servizi voce, in modo che quando l'utente preme il tasto ascolto o si chiama Listen [**,**](https://www.bing.com/search?q=**Listen**)verrà caricato il motore di riconoscimento vocale. Per impostazione predefinita, [**languageID del**](https://www.bing.com/search?q=**LanguageID**) carattere determinerà quale motore viene caricato. Agent tenta di caricare il primo motore restituito da Microsoft Speech API (SAPI) come corrispondente a questo linguaggio. Usare [**SRModeID**](https://www.bing.com/search?q=**SRModeID**) se si vuole caricare un motore specifico.

Per abilitare l'output della sintesi vocale, usare il [**metodo Speak.**](https://www.bing.com/search?q=**Speak**) Agent tenterà automaticamente di caricare un motore che corrisponde al [**LanguageID del carattere**](https://www.bing.com/search?q=**LanguageID**). Se la definizione del carattere include un ID specifico della modalità motore TTS e tale motore è disponibile e corrisponde al **LanguageID** del carattere, Agent carica il motore per il carattere. In caso contrario, carica il primo motore TTS restituito da SAPI come corrispondente all'impostazione della lingua del carattere. È anche possibile usare [**TTSModeID**](https://www.bing.com/search?q=**TTSModeID**) per caricare un motore specifico.

In genere, Agent carica il riconoscimento vocale quando viene avviata la modalità di ascolto e un motore di sintesi vocale quando [**viene chiamato speak**](https://www.bing.com/search?q=**Speak**) per la prima volta. Tuttavia, se si vuole precaricare il motore di riconoscimento vocale, eseguire una query delle proprietà correlate alle interfacce vocali. Ad esempio, l'esecuzione di query [**su SRModeID**](https://www.bing.com/search?q=**SRModeID**) o [**TTSModeID**](https://www.bing.com/search?q=**TTSModeID**) tenterà di caricare il tipo di motore.

Poiché i servizi voce di Microsoft Agent sono basati su Microsoft Speech API, è possibile usare qualsiasi motore che supporti le interfacce vocali necessarie.

 

 




