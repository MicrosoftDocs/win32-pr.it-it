---
title: Messaggi e stringhe di comando MCI
description: Messaggi e stringhe di comando MCI
ms.assetid: eb60c96b-e89e-4673-a8e0-98fabe4af7ca
keywords:
- Stringhe di comando MCI, informazioni
- Messaggi di comando MCI, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 107a317442280b8fb4c7afe7832205b1c7128513
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103872529"
---
# <a name="mci-command-strings-and-messages"></a>Messaggi e stringhe di comando MCI

MCI supporta le [stringhe di comando](command-strings.md) e [i messaggi di comando](command-messages.md). Nell'applicazione MCI è possibile usare stringhe o messaggi o entrambi.

-   L' *interfaccia del messaggio di comando* è costituita da costanti e strutture. Usare la funzione [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) per inviare messaggi a un dispositivo MCI.
-   L' *interfaccia della stringa di comando* fornisce una versione testuale dei messaggi di comando. Usare la funzione [**mciSendString**](/previous-versions//dd757161(v=vs.85)) per inviare stringhe a un dispositivo MCI. Le stringhe di comando duplicano la funzionalità dei messaggi di comando. Il sistema operativo converte le stringhe di comando in messaggi di comando prima di inviarli al driver MCI per l'elaborazione.

I messaggi di comando che recuperano informazioni consentono di eseguire questa operazione sotto forma di strutture, che risultano facili da interpretare in un'applicazione C. Queste strutture possono contenere informazioni su molti aspetti diversi di un dispositivo. Le stringhe di comando che recuperano le informazioni vengono eseguite sotto forma di stringhe e possono recuperare una sola stringa alla volta. L'applicazione deve analizzare o testare ogni stringa per interpretarla. È possibile che i messaggi di comando siano più facili da utilizzare rispetto alle stringhe di comando in alcuni casi, ma le stringhe di comando sono facili da ricordare e implementare. Alcune applicazioni MCI usano stringhe di comando quando il valore restituito non verrà usato (ad eccezione di per verificare l'esito positivo) e i messaggi di comando durante il recupero delle informazioni dal dispositivo.

Quando vengono discussi i comandi, in questa panoramica viene usato il formato stringa del comando seguito dal form del messaggio tra parentesi.

 

 