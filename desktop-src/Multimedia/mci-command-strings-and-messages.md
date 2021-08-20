---
title: Stringhe di comando e messaggi MCI
description: Stringhe di comando e messaggi MCI
ms.assetid: eb60c96b-e89e-4673-a8e0-98fabe4af7ca
keywords:
- stringhe di comando MCI, informazioni
- messaggi di comando MCI, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b34dc9c152265abb51572131751b5cb370782dba83cc3ed6d09bff11f2ca9290
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117986851"
---
# <a name="mci-command-strings-and-messages"></a>Stringhe di comando e messaggi MCI

MCI supporta le stringhe [di comando e](command-strings.md) i messaggi di [comando](command-messages.md). È possibile usare stringhe o messaggi o entrambi nell'applicazione MCI.

-   *L'interfaccia del messaggio di* comando è costituita da costanti e strutture. Usare la [**funzione mciSendCommand**](/previous-versions//dd757160(v=vs.85)) per inviare messaggi a un dispositivo MCI.
-   *L'interfaccia della stringa di* comando fornisce una versione testuale dei messaggi di comando. Usare la [**funzione mciSendString**](/previous-versions//dd757161(v=vs.85)) per inviare stringhe a un dispositivo MCI. Le stringhe di comando duplicano la funzionalità dei messaggi di comando. Il sistema operativo converte le stringhe di comando in messaggi di comando prima di inviarle al driver MCI per l'elaborazione.

I messaggi di comando che recuperano informazioni sono sotto forma di strutture, facili da interpretare in un'applicazione C. Queste strutture possono contenere informazioni su molti aspetti diversi di un dispositivo. Le stringhe di comando che recuperano informazioni sotto forma di stringhe e possono recuperare solo una stringa alla volta. L'applicazione deve analizzare o testare ogni stringa per interpretarla. È possibile che i messaggi di comando siano più facili da usare rispetto alle stringhe di comando in alcuni casi, ma le stringhe di comando sono facili da ricordare e implementare. Alcune applicazioni MCI usano stringhe di comando quando il valore restituito non verrà usato (a parte per verificare l'esito positivo) e messaggi di comando durante il recupero di informazioni dal dispositivo.

Quando vengono illustrati i comandi, in questa panoramica viene utilizzato il formato stringa del comando seguito dal formato del messaggio tra parentesi.

 

 