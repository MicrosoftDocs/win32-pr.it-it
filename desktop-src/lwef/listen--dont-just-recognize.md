---
title: Listen, Dont Just Recognize
description: Listen, Dont Just Recognize
ms.assetid: 74bb2122-98c1-4a51-b894-93e1481aa46b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b226b9172b10c70e4e699a98df49acc002dcd5add95986c9efbdf9e8f057648d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119888091"
---
# <a name="listen-dont-just-recognize"></a>Listen, Dont Just Recognize

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

La corretta comunicazione implica molto più del riconoscimento delle parole. Il processo di dialogo implica lo scambio di segnali per segnalare turni e comprensione. I caratteri possono migliorare le interfacce di conversazione fornendo segnali come inclinazioni della testa, accecamenti o frullati per indicare quando il motore vocale è in ascolto e quando viene riconosciuto un elemento. Ad esempio, Microsoft Agent riproduce  le animazioni assegnate allo stato Listening quando un utente preme il tasto di ascolto push-to-talk e le animazioni assegnate allo stato **Di** ascolto quando viene rilevata un'espressione. Quando si definisce un carattere personalizzato, assicurarsi di creare e assegnare animazioni appropriate a questi stati. Per altre informazioni sulla progettazione dei caratteri, vedere [Progettazione di caratteri per Microsoft Agent.](designing-characters-for-microsoft-agent.md)

Oltre ai segnali non verbali, una conversazione implica un contesto comune tra le parti conversanti. Analogamente, è più probabile che gli scenari di input vocale con caratteri riescano quando il contesto è ben stabilito. La definizione del contesto consente di interpretare meglio frasi simili, ad esempio "check's in the mail" e "check my mail". È anche possibile consentire all'utente di eseguire query sul contesto fornendo un comando, ad esempio "Help" o "Where am I", a cui si risponde rigenerando il contesto corrente, ad esempio l'ultima azione eseguita dall'applicazione.

Microsoft Agent offre interfacce che consentono di accedere alla corrispondenza migliore e alle due alternative migliori seguenti restituite dal motore di riconoscimento vocale. È anche possibile accedere ai punteggi di attendibilità per tutte le corrispondenze. È possibile usare queste informazioni per determinare meglio ciò che è stato pronunciato. Ad esempio, se i punteggi di attendibilità della corrispondenza migliore e della prima alternativa sono vicini, potrebbe indicare che il motore vocale ha avuto difficoltà a distinguere la differenza tra di essi. In tal caso, potrebbe essere necessario chiedere all'utente di ripetere o riform ripetere la richiesta nel tentativo di migliorare le prestazioni. Tuttavia, se la corrispondenza migliore e la prima o la seconda alternativa restituiscono lo stesso comando, potenzia l'indicazione del riconoscimento corretto.

La natura di una conversazione o di un dialogo implica che deve essere presente una risposta all'input parlato. Pertanto, l'input di un utente deve sempre essere risposto con feedback verbale o visivo che indica che è stata eseguita un'azione o si è verificato un problema o fornisce una risposta appropriata.

 

 




