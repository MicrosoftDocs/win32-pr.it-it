---
title: Supporto per la sintesi vocale
description: Supporto per la sintesi vocale
ms.assetid: 38172e04-a5b6-41e4-9d7c-539d9d4117be
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c31fcb655ccb5a8fbb2ffbbb8d01d1da317209fbfa3e270a76d92208c06777df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118475323"
---
# <a name="synthesized-speech-support"></a>Supporto per la sintesi vocale

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

Se si usa la sintesi vocale, il carattere ha la possibilità di pronunciare quasi tutto, il che offre la massima flessibilità. Con l'audio registrato, è possibile assegnare al carattere una voce specifica o univoca. Per specificare l'output, specificare il testo parlato come parametro del [**metodo Speak.**](speak-method.md)

Poiché l'architettura di Microsoft Agent usa Microsoft SAPI per l'output vocale sintetizzato, è possibile usare qualsiasi motore conforme a questa specifica e supportare l'output IPA (International Phonetic Alphabet) usando il [**metodo visivo**](https://www.bing.com/search?q=**Visual**) dell'interfaccia [**ITTSNotifySinkW.**](ittsnotifysinkw.md) Per altre informazioni sui requisiti del motore, vedere [Requisiti di supporto del motore di riconoscimento vocale](requirements-for-text-to-speech-engines.md).

L'impostazione dell'ID lingua di un carattere ne determina l'output TTS. Se un client non specifica un ID lingua per il carattere, l'ID lingua del carattere viene impostato sull'ID lingua predefinito dell'utente. Se la definizione del carattere include un motore specifico e tale motore può essere caricato e corrisponde all'impostazione della lingua del carattere, verrà usato tale motore. In caso contrario, Microsoft Agent enumera gli altri motori disponibili e richiede una corrispondenza MIGLIORE SAPI in base alla lingua, al sesso e all'età (in questo ordine). Se non è disponibile alcun motore corrispondente, non è disponibile alcun output TTS per l'uso del carattere da parte del client. L'agente tenta di caricare il motore TTS alla prima chiamata [**Speak**](speak-method.md) o quando si esegue una query o si imposta correttamente il relativo ID modalità.

Un'applicazione client può anche specificare un motore TTS per il relativo carattere (usando la [**proprietà TTSModeID).**](ttsmodeid-property.md) In questo modo viene eseguito l'override del tentativo del server di trovare automaticamente un motore corrispondente in base all'ID della modalità TTS preferito del carattere o all'impostazione dell'ID lingua corrente del carattere. Tuttavia, se il motore non è installato o non può essere caricato in altro modo, la chiamata avrà esito negativo e genererà un errore nel controllo . Il server tenta quindi di caricare un altro motore in base all'ID lingua, all'impostazione TTS dei caratteri compilati e ai motori TTS disponibili. Se non è ancora presente alcuna corrispondenza, TTS non è disponibile per il client, ma il carattere può comunque pronunciare il relativo fumetto.

Rimangono caricati solo i motori TTS in uso da qualsiasi client. Ad esempio, se un carattere ha una preferenza definita per un motore specifico e tale motore è disponibile, ma l'applicazione client ha specificato un motore diverso (impostando l'ID lingua di un carattere in modo diverso dal motore o specificando un ID modalità diverso), rimane caricato solo il motore specificato dall'applicazione. Il motore che corrisponde alla preferenza definita del carattere per un'impostazione TTS viene scaricato (a meno che un altro client non utilizzi l'impostazione del motore compilato del carattere).

 

 




