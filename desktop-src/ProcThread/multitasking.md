---
description: Un sistema operativo multitasking divide il tempo di elaborazione disponibile tra i processi o i thread che lo richiedono.
ms.assetid: ac45bef6-f078-40ac-95f4-06bd61ff46c4
title: Multitasking
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d06c1d8d44f397f06923c793971bcb20f35b2b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345466"
---
# <a name="multitasking"></a>Multitasking

Un sistema operativo multitasking divide il tempo di elaborazione disponibile tra i processi o i thread che lo richiedono. Il sistema è progettato per il multitasking preemptive. alloca un *intervallo di tempo* del processore a ogni thread che esegue. Il thread attualmente in esecuzione viene sospeso al termine del periodo di tempo specificato, consentendo l'esecuzione di un altro thread. Quando il sistema passa da un thread a un altro, Salva il contesto del thread con precedenza e ripristina il contesto salvato del thread successivo nella coda.

L'entità della porzione di tempo dipende dal sistema operativo e dal processore. Poiché ogni intervallo di tempo è ridotto (circa 20 millisecondi), più thread sembrano essere in esecuzione nello stesso momento. Questa situazione si verifica essenzialmente nei sistemi a più processori, in cui i thread eseguibili vengono distribuiti tra i vari processori disponibili. Tuttavia, è necessario prestare attenzione quando si usano più thread in un'applicazione, perché le prestazioni del sistema possono diminuire se sono presenti troppi thread.

Per altre informazioni, vedere i seguenti argomenti:

-   [Vantaggi del multitasking](advantages-of-multitasking.md)
-   [Quando usare il multitasking](when-to-use-multitasking.md)
-   [Considerazioni sul multitasking](multitasking-considerations.md)

 

 



