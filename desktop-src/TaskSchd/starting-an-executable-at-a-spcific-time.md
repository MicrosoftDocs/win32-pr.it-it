---
title: Avvio di un eseguibile a un'ora specifica
description: La scrittura di un'attività che avvia un eseguibile in un momento specifico viene eseguita definendo un trigger di ora e un'azione eseguibile.
ms.assetid: a45a403d-5a54-4648-b517-41e01a0745c9
keywords:
- Utilità di pianificazione esempi Utilità di pianificazione , trigger temporale
- Utilità di pianificazione esempi Utilità di pianificazione , avvio di un eseguibile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62276568f7c626935d8c5c518d51f58ad0a58b5c313e780ec5651067af625068
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119059959"
---
# <a name="starting-an-executable-at-a-specific-time"></a>Avvio di un eseguibile a un'ora specifica

La scrittura di un'attività che avvia un eseguibile in un momento specifico viene eseguita definendo un trigger di ora e un'azione eseguibile.

## <a name="start-boundary"></a>Limite iniziale

È importante notare che un trigger temporale è diverso da altri trigger basati sul tempo in quanto viene attivato quando il trigger viene attivato dal limite iniziale. Altri trigger basati sull'ora vengono attivati dal limite di inizio, ma non iniziano a eseguire le azioni (in questo caso l'avvio di un eseguibile) fino a quando non viene raggiunta una data pianificata.

## <a name="time-trigger-examples"></a>Esempi di trigger di tempo

Gli esempi seguenti iniziano Blocco note 30 secondi dopo l'attivazione dell'attività:

-   [Esempio di trigger temporale (C++)](time-trigger-example--c---.md)
-   [Esempio di trigger temporale (scripting)](time-trigger-example--scripting-.md)
-   [Esempio di trigger temporale (XML)](time-trigger-example--xml-.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso del Utilità di pianificazione](using-the-task-scheduler.md)
</dt> </dl>

 

 




