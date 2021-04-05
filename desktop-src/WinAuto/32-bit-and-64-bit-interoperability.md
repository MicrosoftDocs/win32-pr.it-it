---
title: interoperabilità a 32 bit e a 64 bit
description: Per ottenere informazioni sull'interfaccia utente dai server Microsoft Active Accessibility e dai provider di automazione interfaccia utente Microsoft, le applicazioni per l'accessibilità devono comunicare attraverso i limiti dei processi.
ms.assetid: 8b46daed-4fd9-430c-bb4d-24be9c8015b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6897082db00e27d77d90e5fc72d5f229834ce760
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728439"
---
# <a name="32-bit-and-64-bit-interoperability"></a>interoperabilità a 32 bit e a 64 bit

Per ottenere informazioni sull'interfaccia utente dai server Microsoft Active Accessibility e dai provider di automazione interfaccia utente Microsoft, le applicazioni per l'accessibilità devono comunicare attraverso i limiti dei processi. In questo argomento vengono descritti i principali problemi di comunicazione tra processi che è necessario tenere presenti quando si sviluppano applicazioni di accessibilità di Windows.

Quando le applicazioni usano l'API di automazione di Windows, i componenti della fase di esecuzione di Microsoft Active Accessibility e di automazione interfaccia utente gestiscono automaticamente tutti i problemi e le complessità che interessano l'esecuzione delle comunicazioni interprocesso, inclusi i problemi di interoperabilità che si verificano quando un processo è 32 bit e l'altro è 64 bit. Microsoft riconosce che in alcuni casi è possibile che un'applicazione di Assistive Technology debba utilizzare una sorta di IPC anziché l'API di automazione di Windows per comunicare con un server Microsoft Active Accessibility o un provider di automazione interfaccia utente. In questi casi, Microsoft consiglia di usare messaggi DCOM o Windows (quelli con valori inferiori a quelli dell' **\_ utente WM**) per comunicare con altri processi. Analogamente all'API di automazione di Windows, i messaggi DCOM e Windows gestiscono automaticamente tutti i problemi IPC, inclusa l'interoperabilità da 32 bit a 64 bit.

Quando l'API di automazione di Windows, DCOM e i messaggi di Windows non sono un'opzione, tenere presenti i seguenti problemi quando si implementa il metodo IPC scelto:

-   Memoria condivisa: quando si usa la memoria condivisa, tenere presente che una struttura in un processo a 32 bit può avere dimensioni e layout differenti rispetto alla stessa struttura in un processo a 64 bit. Questa operazione è particolarmente valida per le strutture che contengono puntatori o handle.
-   Troncamento del puntatore: anche se un'applicazione a 32 bit può usare il tipo di dati **LONGLONG** per archiviare un valore a 64 bit, esistono istanze in cui non esiste alcun elemento API Windows che consenta all'applicazione a 32 bit di ricevere un valore a 64 bit da un processo a 64 bit o di inviare un valore a 64 bit a un processo a 64 bit. Le funzioni [**GetWindowLongPtr**](/windows/desktop/api/winuser/nf-winuser-getwindowlongptra) e [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) , ad esempio, troncano tutti i valori del puntatore, lasciando l'applicazione a 32 bit con un valore inutile.
-   Handle: poiché gli handle Kernel32 e User32 sono significativi solo a 32 bit nei processi a 32 bit e 64 bit, possono essere trasferiti tra processi senza problemi. Tuttavia, alcuni elementi definiti da Windows come handle sono solo puntatori di wrapper, ad esempio **HTREEITEM**. Questi "handle" verranno troncati se vengono passati da un processo a 64 bit a un processo a 32 bit.
-   [WinEvent](winevents-infrastructure.md) Funzioni hook: per registrare una funzione hook nel contesto con un processo server a 32 bit, la funzione hook deve risiedere in una DLL a 32 bit. Analogamente, per registrare una funzione hook nel contesto con un processo server a 64 bit, la funzione hook deve risiedere in una DLL a 64 bit. Se un'applicazione Assistive Technology tenta di registrare una funzione hook nel contesto con un server con una profondità di bit diversa, gli eventi verranno comunque recapitati alla funzione hook, ma verranno recapitati fuori contesto. Per altre informazioni, vedere WinEvents e [funzioni hook in-context e out-of-Context](in-context-and-out-of-context-hook-functions.md).

Per ulteriori informazioni sull'interoperabilità a 32 bit e a 64 bit, vedere [interoperabilità dei processi](/windows/desktop/WinProg64/process-interoperability).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Panoramica dell'API di automazione di Windows](windows-automation-api-overview.md)
</dt> </dl>

 

 