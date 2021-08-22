---
title: Tag di output del riconoscimento vocale di Microsoft Agent
description: Tag di output del riconoscimento vocale di Microsoft Agent
ms.assetid: b7939974-bc54-4dd8-8e79-3ebd24e76215
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a27add35cc9be72a002cdb1a6fba60ef61d47cca61ef532a6d80fd6ed4a5794d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118747891"
---
# <a name="microsoft-agent-speech-output-tags"></a>Tag di output del riconoscimento vocale di Microsoft Agent

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

I servizi di Microsoft Agent supportano la modifica dell'output vocale tramite tag speciali inseriti nella stringa di testo vocale. Questi tag consentono di modificare le caratteristiche dell'espressione di output del carattere.

I tag di output vocale usano le regole di sintassi seguenti:

-   Tutti i tag iniziano e terminano con un carattere barra rovesciata ( \\ ).
-   Il singolo carattere barra rovesciata non è abilitato all'interno di un tag. Per includere un carattere barra rovesciata in un parametro di testo di un tag, usare una doppia barra rovesciata ( \\ \\ ).
-   Per i tag non viene distinzione tra maiuscole e minuscole. Ad esempio, \\ pit è uguale a PIT \\ \\ \\ .
-   I tag dipendono da spazi vuoti. Ad esempio, \\ Rst \\ non corrisponde a \\ Rst \\ .

Se non diversamente specificato o modificato da un altro tag, l'output vocale mantiene la caratteristica impostata dal tag all'interno del testo specificato in un singolo [**metodo Speak.**](speak-method.md) L'output vocale viene reimpostato automaticamente tramite i parametri definiti dall'utente dopo il completamento **di** un metodo Speak.

Alcuni tag includono stringhe tra virgolette. Per alcuni linguaggi di programmazione, ad esempio Visual Basic Scripting Edition (VBScript) e Visual Basic, potrebbe essere necessario usare due virgolette per designare il parametro del tag o concatenare un carattere tra virgolette doppie come parte della stringa. Quest'ultimo è illustrato in questo esempio Visual Basic seguente:


```
Agent1.Characters("Genie").Speak "This is \map=" + chr(34) + "Spoken text" _
+ chr(34) + "=" + chr(34) + "Balloon text" + chr(34) + "\."
```



Per la programmazione C, C++ e Java™, far precedere le barre rovesciate e le virgolette doppie con una barra rovesciata. Esempio:


```
BSTR bszSpeak = SysAllocString(L"This is \\map=\"Spoken text\"=\"Balloon text\"\\");

pCharacter->Speak(bszSpeak, ......);
```



Per le lingue estere che supportano caratteri DBCS (Double-Byte Character Set), è possibile usare caratteri a byte doppio per specificare i parametri stringa. Usare tuttavia caratteri a byte singolo per tutti gli altri parametri e caratteri usati per definire il tag, incluso il tag stesso.

I seguenti tag sono supportati:

-   [**Chr**](chr-tag.md)
-   [**Ctx**](ctx-tag.md)
-   [**Emp**](emp-tag.md)
-   [**Lst**](lst-tag.md)
-   [**Mappa**](map-tag.md)
-   [**Mrk**](mrk-tag.md)
-   [**Pau**](pau-tag.md)
-   [**fossa**](pit-tag.md)
-   [**Rst**](rst-tag.md)
-   [**Spd**](spd-tag.md)
-   [**Vol**](vol-tag.md)

I tag sono progettati principalmente per la regolazione dell'output generato dalla sintesi vocale (TTS). Solo i [**tag Mrk**](mrk-tag.md) [**e Map**](map-tag.md) possono essere usati con l'output parlato basato su file audio.

> [!Note]  
> Microsoft Agent non supporta tutti i tag documentati in Microsoft Speech SDK. I parametri possono anche variare a seconda del motore TTS selezionato. È possibile impostare un motore TTS specifico usando [**TTSModeID**](ttsmodeid-property.md).

 

 

 




