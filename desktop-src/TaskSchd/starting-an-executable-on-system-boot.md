---
title: Avvio di un eseguibile all'avvio del sistema
description: La scrittura di un'attività che avvia un eseguibile quando un sistema viene avviato viene eseguita definendo un trigger di avvio e un'azione eseguibile.
ms.assetid: 9e2359df-a223-4a0c-9051-01b73a83c1f7
keywords:
- Esempi di Utilità di pianificazione Utilità di pianificazione, trigger di avvio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7d41c39e9c80d3fc8f14c0bc9b9d9305de38e16
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103712577"
---
# <a name="starting-an-executable-on-system-boot"></a>Avvio di un eseguibile all'avvio del sistema

La scrittura di un'attività che avvia un eseguibile quando un sistema viene avviato viene eseguita definendo un trigger di avvio e un'azione eseguibile.

## <a name="boot-trigger"></a>Trigger di avvio

I trigger di avvio vengono attivati dal limite iniziale, ma non avviano l'eseguibile fino a quando il sistema non viene avviato. È anche possibile specificare un tempo di ritardo nel trigger di avvio che specifica la quantità di tempo tra il momento in cui il sistema viene avviato e l'avvio dell'attività. Questa impostazione è definita dalla proprietà [**delay**](/windows/desktop/api/taskschd/nf-taskschd-iboottrigger-get_delay) nell'interfaccia [**IBootTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iboottrigger) (oggetto [**BootTrigger**](boottrigger.md) per lo scripting).

## <a name="boot-trigger-examples"></a>Esempi di trigger di avvio

Gli esempi seguenti avviano il blocco note dopo l'avvio del sistema:

-   [Esempio di trigger di avvio (scripting)](boot-trigger-example--scripting-.md)
-   [Esempio di trigger di avvio (C++)](boot-trigger-example--c---.md)
-   [Esempio di trigger di avvio (XML)](boot-trigger-example--xml-.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso della Utilità di pianificazione](using-the-task-scheduler.md)
</dt> </dl>

 

 




