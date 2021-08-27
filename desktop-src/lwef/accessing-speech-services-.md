---
title: Accesso ai servizi Voce (controllo Microsoft Agent)
description: Informazioni sull'accesso ai servizi voce con Il controllo di Microsoft Agent. Microsoft Agent è deprecato a Windows 7.
ms.assetid: c6c10f2a-a433-4a8e-a069-48e3c2032fb8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 617da522912e2fbae361fb3addf569d5164894fc2b98a901686b2458d4d0a8e4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120114941"
---
# <a name="accessing-speech-services-microsoft-agent-control"></a>Accesso ai servizi Voce (controllo Microsoft Agent)

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

Anche se i servizi di Microsoft Agent includono il supporto per l'input vocale, è necessario installare un motore di riconoscimento vocale compatibile per accedere ai servizi di input vocale di Agent. Analogamente, se si vogliono usare i servizi voce di Microsoft Agent per supportare l'output vocale sintetizzato per un carattere, è necessario installare un motore di sintesi vocale compatibile per il carattere.

Per abilitare il supporto dell'input vocale nell'applicazione, definire un [**oggetto Command**](https://www.bing.com/search?q=**Command**) e impostarne [**la proprietà**](https://www.bing.com/search?q=**Voice**) Voice. Agent carica automaticamente i servizi voce, in modo che quando l'utente preme il tasto di ascolto o si chiama [**Listen**](https://www.bing.com/search?q=**Listen**), verrà caricato il motore di riconoscimento vocale. Per impostazione predefinita, il [**LanguageID del**](https://www.bing.com/search?q=**LanguageID**) carattere determinerà il motore caricato. Agent tenta di caricare il primo motore restituito da Microsoft Speech API (SAPI) come corrispondente a questo linguaggio. Usare [**SRModeID**](https://www.bing.com/search?q=**SRModeID**) se si vuole caricare un motore specifico.

Per abilitare l'output della sintesi vocale, usare il [**metodo Speak.**](https://www.bing.com/search?q=**Speak**) Agent tenterà automaticamente di caricare un motore che corrisponde al [**LanguageID del carattere**](https://www.bing.com/search?q=**LanguageID**). Se la definizione del carattere include un ID della modalità del motore TTS specifico e tale motore è disponibile e corrisponde al **LanguageID** del carattere, Agent carica tale motore per il carattere. In caso contrario, carica il primo motore TTS restituito da SAPI come corrispondente all'impostazione della lingua del carattere. È anche possibile usare [**TTSModeID**](https://www.bing.com/search?q=**TTSModeID**) per caricare un motore specifico.

In genere, Agent carica il riconoscimento vocale quando viene avviata la modalità di ascolto e un motore di sintesi vocale quando [**si chiama Speak**](https://www.bing.com/search?q=**Speak**) per la prima volta. Tuttavia, se si vuole precaricare il motore di riconoscimento vocale, eseguire una query delle proprietà correlate alle interfacce vocali. Ad esempio, l'esecuzione [**di query su SRModeID**](https://www.bing.com/search?q=**SRModeID**) o [**TTSModeID**](https://www.bing.com/search?q=**TTSModeID**) tenterà di caricare quel tipo di motore.

Poiché i servizi voce di Microsoft Agent sono basati su Microsoft Speech API, è possibile usare qualsiasi motore che supporti le interfacce vocali necessarie.

 

 




