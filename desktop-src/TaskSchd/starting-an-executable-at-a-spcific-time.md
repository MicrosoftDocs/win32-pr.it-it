---
title: Avvio di un eseguibile in un momento specifico
description: La scrittura di un'attività che avvia un eseguibile in un momento specifico viene eseguita definendo un trigger di ora e un'azione eseguibile.
ms.assetid: a45a403d-5a54-4648-b517-41e01a0745c9
keywords:
- Esempi di Utilità di pianificazione Utilità di pianificazione, Trigger Time
- Esempi di Utilità di pianificazione Utilità di pianificazione, avvio di un eseguibile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c0ce5a1be1586e12399f1dd5d6969170bffa92f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856501"
---
# <a name="starting-an-executable-at-a-specific-time"></a>Avvio di un eseguibile in un momento specifico

La scrittura di un'attività che avvia un eseguibile in un momento specifico viene eseguita definendo un trigger di ora e un'azione eseguibile.

## <a name="start-boundary"></a>Limite iniziale

È importante notare che un trigger di ora è diverso dagli altri trigger basati sul tempo in quanto viene generato quando il trigger viene attivato dal limite iniziale. Altri trigger basati sul tempo vengono attivati dal limite iniziale, ma non iniziano a eseguire le azioni, in questo caso avviando un eseguibile, fino a quando non viene raggiunta una data pianificata.

## <a name="time-trigger-examples"></a>Esempi di trigger di ora

Gli esempi seguenti avviano il blocco note 30 secondi dopo l'attivazione dell'attività:

-   [Esempio di trigger time (C++)](time-trigger-example--c---.md)
-   [Esempio di trigger di ora (scripting)](time-trigger-example--scripting-.md)
-   [Esempio di trigger time (XML)](time-trigger-example--xml-.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso della Utilità di pianificazione](using-the-task-scheduler.md)
</dt> </dl>

 

 




