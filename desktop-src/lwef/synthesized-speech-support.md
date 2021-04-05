---
title: Supporto vocale sintetizzato
description: Supporto vocale sintetizzato
ms.assetid: 38172e04-a5b6-41e4-9d7c-539d9d4117be
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8a89610a912cf601724bc9a2153cba8343e6feb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044689"
---
# <a name="synthesized-speech-support"></a>Supporto vocale sintetizzato

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

Se si usa il riconoscimento vocale sintetizzato, il carattere è in grado di esprimere praticamente qualsiasi elemento, che offre la massima flessibilità. Con l'audio registrato, è possibile assegnare al carattere una voce specifica o univoca. Per specificare l'output, fornire il testo parlato come parametro del metodo [**Speak**](speak-method.md) .

Poiché l'architettura di Microsoft Agent USA Microsoft SAPI per l'output vocale sintetizzato, è possibile usare qualsiasi motore conforme a questa specifica e supporta l'output dell'alfabeto fonetico internazionale (IPA) usando il metodo [**visivo**](https://www.bing.com/search?q=**Visual**) dell'interfaccia [**ITTSNotifySinkW**](ittsnotifysinkw.md) . Per ulteriori informazioni sul motore, vedere requisiti di [supporto del motore vocale](requirements-for-text-to-speech-engines.md).

L'impostazione dell'ID lingua di un carattere determina l'output TTS. Se un client non specifica un ID lingua per il carattere, l'ID lingua del carattere viene impostato sull'ID lingua predefinito dell'utente. Se la definizione del carattere include un motore specifico e tale motore può essere caricato e corrisponde all'impostazione della lingua del carattere, verrà usato tale motore. In caso contrario, Microsoft Agent enumera gli altri motori disponibili e richiede una corrispondenza migliore di SAPI in base a lingua, sesso ed età (in questo ordine). Se non è disponibile alcun motore corrispondente, non è presente alcun output TTS per l'uso del carattere da parte del client. Agent tenta di caricare il motore TTS per la prima chiamata a [**Speak**](speak-method.md) o quando si esegue una query o si imposta correttamente l'ID modalità.

Un'applicazione client può anche specificare un motore TTS per il relativo carattere (usando la proprietà [**TTSModeID**](ttsmodeid-property.md) ). In questo modo viene eseguito l'override del tentativo del server di trovare automaticamente un motore corrispondente in base all'ID della modalità TTS preferita o all'impostazione dell'ID lingua corrente del carattere. Tuttavia, se il motore non è installato (o non può essere caricato altrimenti), la chiamata avrà esito negativo e genererà un errore nel controllo. Il server tenta quindi di caricare un altro motore in base all'ID lingua, all'impostazione di TTS dei caratteri compilata e ai motori TTS disponibili. Se non è ancora presente alcuna corrispondenza, TTS non è disponibile per quel client, ma il carattere può ancora pronunciare il suo fumetto di parole.

Rimangono caricati solo i motori TTS usati da qualsiasi client. Se, ad esempio, un carattere ha una preferenza definita per un motore specifico e tale motore è disponibile, ma l'applicazione client ha specificato un motore diverso (impostando un ID lingua del carattere diverso dal motore o specificando un ID modalità diverso), rimane caricato solo il motore specificato dall'applicazione. Il motore che corrisponde alla preferenza definita dal carattere per un'impostazione TTS viene scaricato (a meno che un altro client non usi l'impostazione del motore compilato del carattere).

 

 




