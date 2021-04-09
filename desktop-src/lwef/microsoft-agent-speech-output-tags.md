---
title: Tag output sintesi vocale agente Microsoft
description: Tag output sintesi vocale agente Microsoft
ms.assetid: b7939974-bc54-4dd8-8e79-3ebd24e76215
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d365d4837df3e3a5afb57c355e229f21ade0b5a0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856213"
---
# <a name="microsoft-agent-speech-output-tags"></a>Tag output sintesi vocale agente Microsoft

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

I servizi di Microsoft Agent supportano la modifica dell'output vocale tramite tag speciali inseriti nella stringa di testo vocale. Questi tag consentono di modificare le caratteristiche dell'espressione di output del carattere.

I tag di output vocale utilizzano le regole di sintassi seguenti:

-   Tutti i tag iniziano e terminano con un carattere barra rovesciata ( \) .
-   Il carattere barra rovesciata singola non è abilitato in un tag. Per includere un carattere barra rovesciata in un parametro di testo di un tag, utilizzare una doppia barra rovesciata ( \\ \) .
-   I tag non fanno distinzione tra maiuscole e minuscole. Ad esempio, \\ Pit \\ è lo stesso di \\ Pit \\ .
-   I tag sono dipendenti da spazi vuoti. Ad esempio, \\ RST \\ non è uguale a \\ RST \\ .

Se non diversamente specificato o modificato da un altro tag, l'output vocale mantiene il set di caratteristiche dal tag all'interno del testo specificato in un singolo metodo [**Speak**](speak-method.md) . L'output vocale viene reimpostato automaticamente tramite i parametri definiti dall'utente dopo il completamento di un metodo **Speak** .

Alcuni tag includono stringhe tra virgolette. Per alcuni linguaggi di programmazione, ad esempio Visual Basic Scripting Edition (VBScript) e Visual Basic, ciò significa che potrebbe essere necessario utilizzare due virgolette per definire il parametro del tag o concatenare un carattere di virgolette doppie come parte della stringa. Il secondo è illustrato in questo Visual Basic esempio:


```
Agent1.Characters("Genie").Speak "This is \map=" + chr(34) + "Spoken text" _
+ chr(34) + "=" + chr(34) + "Balloon text" + chr(34) + "\."
```



Per la programmazione in C, C++ e Java™, precede le barre rovesciate e le virgolette doppie con una barra rovesciata. Ad esempio:


```
BSTR bszSpeak = SysAllocString(L"This is \\map=\"Spoken text\"=\"Balloon text\"\\");

pCharacter->Speak(bszSpeak, ......);
```



Per le lingue straniere che supportano i caratteri DBCS (Double-byte character set), è possibile utilizzare caratteri a byte doppio per specificare i parametri di stringa. Usare tuttavia caratteri a byte singolo per tutti gli altri parametri e caratteri usati per definire il tag, incluso il tag stesso.

I seguenti tag sono supportati:

-   [**Chr**](chr-tag.md)
-   [**CTX**](ctx-tag.md)
-   [**EMP**](emp-tag.md)
-   [**LST**](lst-tag.md)
-   [**Mappa**](map-tag.md)
-   [**MRK**](mrk-tag.md)
-   [**Pau**](pau-tag.md)
-   [**Pit**](pit-tag.md)
-   [**RST**](rst-tag.md)
-   [**SPD**](spd-tag.md)
-   [**Vol**](vol-tag.md)

I tag sono progettati principalmente per la regolazione dell'output generato da sintesi vocale (TTS). Solo i tag [**MRK**](mrk-tag.md) e [**Map**](map-tag.md) possono essere usati con l'output parlato basato su file audio.

> [!Note]  
> Microsoft Agent non supporta tutti i tag documentati in Microsoft Speech SDK. I parametri possono variare anche a seconda del motore TTS selezionato. È possibile impostare un motore TTS specifico usando [**TTSModeID**](ttsmodeid-property.md).

 

 

 




