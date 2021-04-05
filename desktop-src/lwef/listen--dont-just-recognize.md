---
title: Ascolta, non solo riconosci
description: Ascolta, non solo riconosci
ms.assetid: 74bb2122-98c1-4a51-b894-93e1481aa46b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e972a8c98460e58d0f7080d7de7641fb856c8317
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103713873"
---
# <a name="listen-dont-just-recognize"></a>Ascolta, non solo riconosci

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

La comunicazione riuscita implica più del riconoscimento delle parole. Il processo di dialogo implica lo scambio di suggerimenti per il riscatto e la comprensione dei segnali. I caratteri possono migliorare le interfacce di conversazione fornendo segnali come inclinazioni della testa, Cenni o vibrazioni per indicare quando il motore vocale è nello stato di ascolto e quando viene riconosciuto un elemento. Ad esempio, l'agente Microsoft riproduce le animazioni assegnate allo stato di **ascolto** quando un utente preme il tasto ascolto push e le animazioni assegnate allo stato di **udito** quando viene rilevata un'espressione. Quando si definisce un carattere personalizzato, assicurarsi di creare e assegnare animazioni appropriate a questi Stati. Per ulteriori informazioni sulla progettazione di caratteri, vedere [progettazione di caratteri per Microsoft Agent](designing-characters-for-microsoft-agent.md).

Oltre ai segnali non verbali, una conversazione comporta un contesto comune tra le parti che si Conversano. Analogamente, è più probabile che gli scenari di input vocale con caratteri abbiano esito positivo quando il contesto è ben definito. La definizione del contesto consente di interpretare meglio frasi simili, ad esempio "check in the mail" e "Check My mail". È anche possibile consentire all'utente di eseguire una query sul contesto specificando un comando, ad esempio "Help" o "Where am I", a cui rispondere ridichiarando il contesto corrente, ad esempio l'ultima azione eseguita dall'applicazione.

Microsoft Agent fornisce interfacce che consentono di accedere alla migliore corrispondenza e alle due alternative migliori restituite dal motore di riconoscimento vocale. Inoltre, è possibile accedere ai punteggi di confidenza per tutte le corrispondenze. È possibile usare queste informazioni per determinare meglio ciò che è stato pronunciato. Se, ad esempio, i punteggi di confidenza della migliore corrispondenza e della prima alternativa sono vicini, può indicare che il motore vocale ha riscontrato difficoltà a discernere la differenza. In tal caso, potrebbe essere necessario chiedere all'utente di ripetere o riformulare la richiesta per migliorare le prestazioni. Tuttavia, se la corrispondenza migliore e la prima o la seconda alternativa restituiscono lo stesso comando, viene rafforzata l'indicazione del riconoscimento corretto.

La natura di una conversazione o di un dialogo implica la presenza di una risposta all'input parlato. Pertanto, l'input di un utente deve essere sempre risposto a con feedback verbale o visivo che indica che è stata eseguita un'azione o che si è verificato un problema oppure fornisce una risposta appropriata.

 

 




