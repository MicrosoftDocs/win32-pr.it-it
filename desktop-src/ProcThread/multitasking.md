---
description: Un sistema operativo multitasking divide il tempo del processore disponibile tra i processi o i thread che ne hanno bisogno.
ms.assetid: ac45bef6-f078-40ac-95f4-06bd61ff46c4
title: Multitasking
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee7826ca79d6095715c722b4b5c3da479e276444825343ac096cd9822d9e365a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032181"
---
# <a name="multitasking"></a>Multitasking

Un sistema operativo multitasking divide il tempo del processore disponibile tra i processi o i thread che ne hanno bisogno. Il sistema è progettato per il multitasking preemptive; alloca un intervallo di *tempo del* processore a ogni thread eseguito. Il thread attualmente in esecuzione viene sospeso al termine dell'intervallo di tempo, consentendo l'esecuzione di un altro thread. Quando il sistema passa da un thread a un altro, salva il contesto del thread preempted e ripristina il contesto salvato del thread successivo nella coda.

L'entità della porzione di tempo dipende dal sistema operativo e dal processore. Poiché ogni intervallo di tempo è piccolo (circa 20 millisecondi), più thread sembrano essere in esecuzione contemporaneamente. Questa situazione si verifica essenzialmente nei sistemi a più processori, in cui i thread eseguibili vengono distribuiti tra i vari processori disponibili. Tuttavia, è necessario prestare attenzione quando si usano più thread in un'applicazione, perché le prestazioni del sistema possono diminuire se sono presenti troppi thread.

Per altre informazioni, vedere i seguenti argomenti:

-   [Vantaggi del multitasking](advantages-of-multitasking.md)
-   [Quando usare il multitasking](when-to-use-multitasking.md)
-   [Considerazioni sul multitasking](multitasking-considerations.md)

 

 



