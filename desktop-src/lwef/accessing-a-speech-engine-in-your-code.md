---
title: Accesso a un motore vocale nel codice
description: Accesso a un motore vocale nel codice
ms.assetid: ddfe0552-a29e-4ce4-b608-c131efbe300b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7d81841f6f287d36a6ac01fa77294b1754eeb9b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299653"
---
# <a name="accessing-a-speech-engine-in-your-code"></a>Accesso a un motore vocale nel codice

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

Per usare un particolare motore vocale nel codice, usare l'API dell'agente per impostare il motore. Per i motori di input vocale, usare [**SRModeID**](https://www.bing.com/search?q=**SRModeID**), specificando l'ID modalità per il motore. Si noti tuttavia che è necessario installare il motore. Per determinare se il motore è presente, è possibile eseguire una query su **SRModeID**. Il motore deve corrispondere all'impostazione [**LanguageID**](https://www.bing.com/search?q=**LanguageID**) del carattere. Ad esempio, non è possibile impostare **SRModeID** su un ID modalità del motore di riconoscimento vocale tedesco per un carattere il cui **LanguageID** è francese.

**ID modalità motore di input vocale**



| Chiamata vocale                                    | ID modalità                             |
|------------------------------------------|--------------------------------------|
| Motore di riconoscimento vocale Microsoft v 4.0 | {D8905400-B5C8-11D0-B968020AFDB1B9C} |



 

Prima di provare a definire la grammatica per i parametri vocali degli oggetti **Command** dell'applicazione, controllare e impostare [**LanguageID**](https://www.bing.com/search?q=**LanguageID**) e [**SRModeID**](https://www.bing.com/search?q=**SRModeID**) del carattere nel codice. Si consiglia inoltre di controllare la lingua del browser o del sistema in modo da essere certi di poter corrispondere alla configurazione degli utenti. Il motore potrebbe non riuscire se si tenta di definire una grammatica per una lingua non corrispondente al motore.

Un set di caratteri per l'output da sintesi vocale (TTS) può essere compilato con una preferenza ID modalità predefinita del motore di output vocale. Quando il carattere viene caricato, se il motore è installato e corrisponde al [**LanguageID**](https://www.bing.com/search?q=**LanguageID**)del carattere, Agent tenterà di caricare l'ID modalità per l'output vocale. Se il motore non è presente o ha un **LanguageID** diverso, Agent tenterà di caricare il primo ID modalità trovato che corrisponde al **LanguageID** del carattere, ma imposta comunque la velocità e l'impostazione del pitch compilate del carattere.

Si noti che poiché tutti i caratteri forniti da Microsoft Agent vengono compilati per l'uso di Lernout & Hauspie Speech TruVoice American English Engine come motore di output vocale predefinito, l'impostazione della velocità e del pitch dei caratteri viene ottimizzata per questo linguaggio e motore. Pertanto, quando si utilizzano altri motori di TTS o motori di altri linguaggi, è possibile che i caratteri non parlino con il pitch o la velocità ottimale. Anche se l'applicazione o la pagina Web non è in grado di scrivere i valori delle proprietà [**pitch**](/previous-versions/ms809428(v=msdn.10)) e [**Speed**](https://www.bing.com/search?q=**Speed**) , è possibile includere tag [Pit](pit-tag.md) (pitch) e [SPD](spd-tag.md) (Speed) nel testo di output che cambierà temporaneamente il pitch e la velocità per una particolare espressione. Tuttavia, se si usano i tag Pit e SPD, le proprietà **pitch** e **Speed** non vengono modificate. Per informazioni dettagliate, vedere la pagina relativa alla [programmazione del controllo Microsoft Agent](programming-the-microsoft-agent-control.md) e dei [tag di output vocale di Microsoft Agent](microsoft-agent-speech-output-tags.md) .

È necessario installare anche i file binari di runtime di SAPI 4.0 (SPCHAPI.exe) quando si usano altri motori TTS conformi a SAPI rispetto al motore di L&H TruVoice American English con i caratteri forniti dall'agente Microsoft, in modo che i motori vengano enumerati correttamente. Nella pagina Web includere il tag oggetto seguente per installare automaticamente il componente:

``` syntax
<OBJECT width=0 height=0
CLASSID="CLSID:0C7F3F20-8BAB-11d2-9432-00C04F8EF48F"
CODEBASE="#VERSION=4,0,0,0">
</OBJECT>
```

Per eseguire una query per o impostare l'ID modalità di un motore, utilizzare [**TTSModeID**](https://www.bing.com/search?q=**TTSModeID**). Con **TTSModeID** è possibile impostare un ID modalità diverso da [**LanguageID**](https://www.bing.com/search?q=**LanguageID**)del carattere. Ad esempio, è possibile impostare un carattere tedesco per parlare usando un ID in modalità francese. Gli ID modalità motore di output vocale non solo definiscono il motore usato, ma corrispondono anche a voci specifiche supportate per un motore. È anche possibile usare l'editor caratteri Microsoft Agent o gli strumenti inclusi nella [documentazione di Microsoft Speech SDK](https://msdn.microsoft.com/library/ee705648.aspx) per eseguire una query per gli ID modalità dei motori TTS installati nel sistema.

**ID modalità output vocale**



| Chiamata vocale                                       | ID modalità                               |
|---------------------------------------------|----------------------------------------|
| Adult Female \# 1, inglese Stati Uniti, L&H TruVoice  | {CA141FD0-AC7F-11D1-97A3-006008273008} |
| Adult Female \# 2, inglese Stati Uniti, L&H TruVoice  | {CA141FD0-AC7F-11D1-97A3-006008273009} |
| Adult male \# 1, inglese Stati Uniti, L&H TruVoice    | {CA141FD0-AC7F-11D1-97A3-006008273000} |
| Adult male \# 2, inglese Stati Uniti, L&H TruVoice    | {CA141FD0-AC7F-11D1-97A3-006008273001} |
| Adult male \# 3, inglese Stati Uniti, L&H TruVoice    | {CA141FD0-AC7F-11D1-97A3-006008273002} |
| Adult male \# 4, inglese Stati Uniti, L&H TruVoice    | {CA141FD0-AC7F-11D1-97A3-006008273003} |
| Adult male \# 5, inglese Stati Uniti, L&H TruVoice    | {CA141FD0-AC7F-11D1-97A3-006008273004} |
| Adult male \# 6, inglese Stati Uniti, L&H TruVoice    | {CA141FD0-AC7F-11D1-97A3-006008273005} |
| Adult male \# 7, inglese Stati Uniti, L&H TruVoice    | {CA141FD0-AC7F-11D1-97A3-006008273006} |
| Adult male \# 8, inglese Stati Uniti, L&H TruVoice    | {CA141FD0-AC7F-11D1-97A3-006008273007} |
| Carol, inglese britannico, L&H TTS3000         | {227A0E40-A92A-11d1-B17B-0020AFED142E} |
| Peter, inglese britannico, L&H TTS3000         | {227A0E41-A92A-11d1-B17B-0020AFED142E} |
| Linda, olandese, L&H TTS3000                   | {A0DDCA40-A92C-11d1-B17B-0020AFED142E} |
| Alessandro, olandese, L&H TTS3000               | {A0DDCA41-A92C-11d1-B17B-0020AFED142E} |
| Véronique, francese, L&H TTS3000              | {0879A4E0-A92C-11d1-B17B-0020AFED142E} |
| Pierre, francese, L&H TTS3000                 | {0879A4E1-A92C-11d1-B17B-0020AFED142E} |
| Anna, tedesco, L&H TTS3000                   | {3A1FB760-A92B-11d1-B17B-0020AFED142E} |
| Stefan, tedesco, L&H TTS3000                 | {3A1FB761-A92B-11d1-B17B-0020AFED142E} |
| Barbara, italiano, L&H TTS3000               | {7EF71700-A92D-11d1-B17B-0020AFED142E} |
| Stefano, italiano, L&H TTS3000               | {7EF71701-A92D-11d1-B17B-0020AFED142E} |
| Naoko, giapponese, L&H TTS3000                | {A778E060-A936-11d1-B17B-0020AFED142E} |
| Kenji, giapponese, L&H TTS3000                | {A778E061-A936-11d1-B17B-0020AFED142E} |
| Shin-ah, coreano, L&H TTS3000                | {12E0B720-A936-11d1-B17B-0020AFED142E} |
| Giu-ho, coreano, L&H TTS3000                 | {12E0B721-A936-11d1-B17B-0020AFED142E} |
| Juliana, portoghese (Brasile), L&H TTS3000   | {8AA08CA0-A1AE-11d3-9BC5-00A0C967A2D1} |
| Alexandre, portoghese (Brasile), L&H TTS3000 | {8AA08CA1-A1AE-11d3-9BC5-00A0C967A2D1} |
| Svetlana, russo, L&H TTS3000              | {06377F80-D48E-11d1-B17B-0020AFED142E} |
| Boris, russo, L&H TTS3000                 | {06377F81-D48E-11d1-B17B-0020AFED142E} |
| Carmen, spagnolo, L&H TTS3000                | {2CE326E0-A935-11d1-B17B-0020AFED142E} |
| Julio, spagnolo, L&H TTS3000                 | {2CE326E1-A935-11d1-B17B-0020AFED142E} |



 

> [!Note]  
> Esiste una differenza tra il CLSID di installazione di un motore vocale e il relativo ID modalità. Analogamente, un motore di riconoscimento vocale dispone anche di un ID del motore, ma questo ID non è applicabile nell'API dell'agente.

 

 

 