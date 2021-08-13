---
title: Accesso a un motore di riconoscimento vocale nel codice
description: Accesso a un motore di riconoscimento vocale nel codice
ms.assetid: ddfe0552-a29e-4ce4-b608-c131efbe300b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b9769e88437366b72fdff50dc0ab27918d1b21e4c0c317f230049a965629a03
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118753120"
---
# <a name="accessing-a-speech-engine-in-your-code"></a>Accesso a un motore di riconoscimento vocale nel codice

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

Per usare un motore di riconoscimento vocale specifico nel codice, usare l'API Agent per impostare il motore. Per i motori di input vocale, usare [**SRModeID,**](https://www.bing.com/search?q=**SRModeID**)specificando l'ID modalità per il motore. Si noti tuttavia che il motore deve essere installato. Per determinare se il motore è presente, è possibile eseguire una query **su SRModeID**. Il motore deve corrispondere all'impostazione [**LanguageID del**](https://www.bing.com/search?q=**LanguageID**) carattere. Ad esempio, non è possibile impostare **SRModeID** su un ID in modalità motore di riconoscimento vocale tedesco per un carattere il cui **LanguageID** è francese.

**ID modalità motore di input vocale**



| Chiamata vocale                                    | ID modalità                             |
|------------------------------------------|--------------------------------------|
| Motore di riconoscimento vocale Microsoft v4.0 | {D8905400-B5C8-11D0-B968020AFDB1B9C} |



 

Controllare e impostare [**LanguageID**](https://www.bing.com/search?q=**LanguageID**) e [**SRModeID**](https://www.bing.com/search?q=**SRModeID**) del carattere nel codice prima di tentare di definire la grammatica per i parametri vocali degli oggetti **Command** dell'applicazione. È anche consigliabile controllare la lingua del browser o del sistema in modo da poter essere certi che corrisponda alla configurazione degli utenti. Il motore potrebbe non riuscire se si tenta di definire una grammatica per una lingua che non corrisponde al motore.

Un set di caratteri per l'output di sintesi vocale (TTS) può essere compilato con una preferenza ID modalità del motore di output vocale predefinito. Quando il carattere viene caricato, se il motore è installato e corrisponde a [**LanguageID**](https://www.bing.com/search?q=**LanguageID**)del carattere, Agent tenterà di caricare l'ID modalità per l'output vocale. Se il motore non è presente o ha un **LanguageID** diverso, Agent tenterà di caricare il primo ID modalità rilevato che corrisponde al **LanguageID** del carattere, ma imposta comunque l'impostazione di velocità e passo compilata del carattere.

Si noti che, poiché tutti i caratteri forniti da Microsoft Agent vengono compilati per usare il motore inglese americano Lernout & Hauspie TruVoice come motore di output vocale predefinito, l'impostazione di velocità e passo dei caratteri viene ottimizzata per questa lingua e motore. Pertanto, quando si usano altri motori TTS o motori di altre lingue, i caratteri potrebbero non parlare al passo o alla velocità ottimali. Anche se l'applicazione [](/previous-versions/ms809428(v=msdn.10)) o la pagina Web non è in grado di scrivere i valori delle proprietà Pitch e [**Speed,**](https://www.bing.com/search?q=**Speed**) è possibile includere i tag [Pit](pit-tag.md) (pitch) e [Spd](spd-tag.md) (speed) nel testo di output che modificheranno temporaneamente l'altezza e la velocità per una determinata espressione. Tuttavia, l'uso dei tag Pit e Spd non modificherà le **proprietà Pitch** **e Speed.** Per [informazioni dettagliate, vedere Programmazione del controllo Microsoft Agent](programming-the-microsoft-agent-control.md) e dei tag di output del riconoscimento vocale di Microsoft [Agent.](microsoft-agent-speech-output-tags.md)

È anche necessario installare i file binari di runtime SAPI 4.0a (SPCHAPI.exe) quando si usano altri motori TTS conformi a SAPI rispetto al motore L&H TruVoice American English con i caratteri forniti da Microsoft Agent in modo che i motori siano enumerati correttamente. Dalla pagina Web includere il tag Object seguente per installare automaticamente il componente:

``` syntax
<OBJECT width=0 height=0
CLASSID="CLSID:0C7F3F20-8BAB-11d2-9432-00C04F8EF48F"
CODEBASE="#VERSION=4,0,0,0">
</OBJECT>
```

Per eseguire una query per o impostare l'ID modalità di un motore, usare [**TTSModeID**](https://www.bing.com/search?q=**TTSModeID**). Con **TTSModeID** è possibile impostare un ID modalità diverso da [**LanguageID del carattere.**](https://www.bing.com/search?q=**LanguageID**) Ad esempio, è possibile impostare un carattere tedesco per parlare usando un ID in modalità francese. Gli ID della modalità motore di output vocale non solo definiscono il motore in uso, ma corrispondono anche a voci specifiche supportate per un motore. È anche possibile usare l'editor di caratteri di Microsoft Agent o gli strumenti inclusi nella documentazione di [Microsoft Speech SDK](https://msdn.microsoft.com/library/ee705648.aspx) per eseguire query sugli ID modalità dei motori TTS installati nel sistema.

**ID modalità di output vocale**



| Chiamata vocale                                       | ID modalità                               |
|---------------------------------------------|----------------------------------------|
| Adult Female \# 1, US English, L&H TruVoice  | {CA141FD0-AC7F-11D1-97A3-006008273008} |
| Adult Female \# 2, US English, L&H TruVoice  | {CA141FD0-AC7F-11D1-97A3-006008273009} |
| Adult Male \# 1, US English, L&H TruVoice    | {CA141FD0-AC7F-11D1-97A3-006008273000} |
| Adult Male \# 2, US English, L&H TruVoice    | {CA141FD0-AC7F-11D1-97A3-006008273001} |
| Adult Male \# 3, US English, L&H TruVoice    | {CA141FD0-AC7F-11D1-97A3-006008273002} |
| Adult Male \# 4, US English, L&H TruVoice    | {CA141FD0-AC7F-11D1-97A3-006008273003} |
| Adult Male \# 5, US English, L&H TruVoice    | {CA141FD0-AC7F-11D1-97A3-006008273004} |
| Adult Male \# 6, US English, L&H TruVoice    | {CA141FD0-AC7F-11D1-97A3-006008273005} |
| Adult Male \# 7, US English, L&H TruVoice    | {CA141FD0-AC7F-11D1-97A3-006008273006} |
| Adult Male \# 8, US English, L&H TruVoice    | {CA141FD0-AC7F-11D1-97A3-006008273007} |
| Carol, inglese inglese, L&H TTS3000         | {227A0E40-A92A-11d1-B17B-0020AFED142E} |
| Peter, inglese inglese, L&H TTS3000         | {227A0E41-A92A-11d1-B17B-0020AFED142E} |
| Linda, Olandese, L&H TTS3000                   | {A0DDCA40-A92C-11d1-B17B-0020AFED142E} |
| Alexander, Olandese, L&H TTS3000               | {A0DDCA41-A92C-11d1-B17B-0020AFED142E} |
| Véronique, francese, L&H TTS3000              | {0879A4E0-A92C-11d1-B17B-0020AFED142E} |
| Pierre, francese, L&H TTS3000                 | {0879A4E1-A92C-11d1-B17B-0020AFED142E} |
| Anna, tedesco, L&H TTS3000                   | {3A1FB760-A92B-11d1-B17B-0020AFED142E} |
| Stefan, Tedesco, L&H TTS3000                 | {3A1FB761-A92B-11d1-B17B-0020AFED142E} |
| Barbara, italiano, L&H TTS3000               | {7EF71700-A92D-11d1-B17B-0020AFED142E} |
| Stefano, italiano, L&H TTS3000               | {7EF71701-A92D-11d1-B17B-0020AFED142E} |
| Naoko, giapponese, L&H TTS3000                | {A778E060-A936-11d1-B17B-0020AFED142E} |
| Kenji, giapponese, L&H TTS3000                | {A778E061-A936-11d1-B17B-0020AFED142E} |
| Shin-Ah, coreano, L&H TTS3000                | {12E0B720-A936-11d1-B17B-0020AFED142E} |
| Jun-Ho, coreano, L&H TTS3000                 | {12E0B721-A936-11d1-B17B-0020AFED142E} |
| Giuliana, portoghese (Brasile), L&H TTS3000   | {8AA08CA0-A1AE-11d3-9BC5-00A0C967A2D1} |
| Alexandre, portoghese (Brasile), L&H TTS3000 | {8AA08CA1-A1AE-11d3-9BC5-00A0C967A2D1} |
| Svetlana, Russo, L&H TTS3000              | {06377F80-D48E-11d1-B17B-0020AFED142E} |
| Bob, Russo, L&H TTS3000                 | {06377F81-D48E-11d1-B17B-0020AFED142E} |
| Carmen, spagnolo, L&H TTS3000                | {2CE326E0-A935-11d1-B17B-0020AFED142E} |
| Julio, spagnolo, L&H TTS3000                 | {2CE326E1-A935-11d1-B17B-0020AFED142E} |



 

> [!Note]  
> Esiste una differenza tra il CLSID di installazione di un motore di riconoscimento vocale e il relativo ID modalità. Analogamente, un motore di riconoscimento vocale ha anche un ID motore, ma questo ID non è applicabile nell'API agent.

 

 

 