---
title: Interoperabilità a 32 bit e a 64 bit
description: Le applicazioni assistive technology devono comunicare attraverso i limiti del processo per ottenere informazioni sull'interfaccia utente dai server Microsoft Active Accessibility e dai provider di Automazione interfaccia utente Microsoft.
ms.assetid: 8b46daed-4fd9-430c-bb4d-24be9c8015b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1c056c9fe2792734e9369fa311e69528ce226f7edf15b82440b63c12c52de66
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118327990"
---
# <a name="32-bit-and-64-bit-interoperability"></a>Interoperabilità a 32 bit e a 64 bit

Le applicazioni assistive technology devono comunicare attraverso i limiti del processo per ottenere informazioni sull'interfaccia utente dai server Microsoft Active Accessibility e dai provider di Automazione interfaccia utente Microsoft. Questo argomento descrive i principali problemi di comunicazione interprocesso che è necessario tenere presenti quando si sviluppano Windows di accessibilità.

Quando le applicazioni usano l'API di automazione di Windows, i componenti di run-time Microsoft Active Accessibility e Automazione interfaccia utente gestiscono automaticamente tutti i problemi e le complessità dell'esecuzione delle comunicazioni interprocesso (IPC), inclusi i problemi di interoperabilità relativi a un processo a 32 bit e l'altro a 64 bit. Microsoft riconosce che in alcuni casi un'applicazione assistive technology potrebbe dover usare una forma di IPC anziché l'API di automazione di Windows per comunicare con un server Microsoft Active Accessibility o un provider Automazione interfaccia utente. In questi casi, Microsoft consiglia di usare I messaggi DCOM o Windows (quelli con valori inferiori a quelli di **WM \_ USER)** per comunicare con altri processi. Analogamente all'API di automazione di Windows, i messaggi DCOM e Windows gestiscono automaticamente tutti i problemi IPC, inclusa l'interoperabilità da 32 bit a 64 bit.

Quando i Windows dell'API di automazione, DCOM e Windows non sono un'opzione, tenere presenti i problemi seguenti quando si implementa il metodo IPC scelto:

-   Memoria condivisa: quando si usa la memoria condivisa, tenere presente che una struttura in un processo a 32 bit può avere dimensioni e layout diversi rispetto alla stessa struttura in un processo a 64 bit. Ciò vale soprattutto per le strutture che contengono puntatori o handle.
-   Troncamento del puntatore: anche se un'applicazione a 32 bit può usare il tipo di dati **LONGLONG** per archiviare un valore a 64 bit, esistono istanze in cui non esiste alcun elemento API Windows che consentirebbe all'applicazione a 32 bit di ricevere un valore a 64 bit da un processo a 64 bit o di inviare un valore a 64 bit a un processo a 64 bit. Ad esempio, le [**funzioni GetWindowLongPtr**](/windows/desktop/api/winuser/nf-winuser-getwindowlongptra) e [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) troncano tutti i valori del puntatore, lasciando all'applicazione a 32 bit un valore inutile.
-   Handle: poiché gli handle kernel32 e user32 sono significativi solo a 32 bit nei processi a 32 e a 64 bit, possono essere trasferiti tra processi senza problemi. Tuttavia, alcuni elementi che Windows come handle sono in realtà solo puntatori di cui è stato eseguito il wrapping (ad esempio, **HTREEITEM**). Questi "handle" verranno troncati se vengono passati da un processo a 64 bit a un processo a 32 bit.
-   [WinEvent](winevents-infrastructure.md) Funzioni hook: per registrare una funzione hook nel contesto con un processo server a 32 bit, la funzione hook deve risiedere in una DLL a 32 bit. Analogamente, per registrare una funzione hook nel contesto con un processo server a 64 bit, la funzione hook deve risiedere in una DLL a 64 bit. Se un'applicazione assistive technology tenta di registrare una funzione hook nel contesto con un server con una profondità di bit diversa, gli eventi verranno comunque recapitati alla funzione hook, ma verranno recapitati fuori contesto. Per altre informazioni, vedere WinEvents e Funzioni hook in contesto e [Out-of-Context](in-context-and-out-of-context-hook-functions.md).

Per altre informazioni sull'interoperabilità a 32 bit e a 64 bit, vedere [Interoperabilità dei processi](/windows/desktop/WinProg64/process-interoperability).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Windows Panoramica dell'API di automazione](windows-automation-api-overview.md)
</dt> </dl>

 

 