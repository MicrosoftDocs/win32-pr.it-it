---
description: Per sincronizzare l'accesso a una risorsa, usare uno degli oggetti di sincronizzazione in una delle funzioni di attesa.
ms.assetid: 0930bf12-6d5f-4f2c-914d-53e6e862d3bd
title: Informazioni sulla sincronizzazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb8bca156eec523b30d8f28df8b18a24d9691a33598f5dfe985e4b6b9756ffe3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118886405"
---
# <a name="about-synchronization"></a>Informazioni sulla sincronizzazione

Per sincronizzare l'accesso a una risorsa, usare uno degli oggetti [di sincronizzazione](synchronization-objects.md) in una delle funzioni [di attesa](wait-functions.md). Lo stato di un oggetto di sincronizzazione è *segnalato* o *non segnalato.* Le funzioni di attesa consentono a un thread di bloccare la propria esecuzione fino a quando un oggetto non segnalato specificato non viene impostato sullo stato segnalato. Per altre informazioni, vedere [Sincronizzazione interprocesso.](interprocess-synchronization.md)

Di seguito sono riportati altri meccanismi di sincronizzazione:

-   [input e output sovrapposti](synchronization-and-overlapped-input-and-output.md)
-   [chiamate di procedura asincrone](asynchronous-procedure-calls.md)
-   [oggetti sezione critica](critical-section-objects.md)
-   [variabili di condizione](condition-variables.md)
-   [Blocchi di lettura/scrittura sottili](slim-reader-writer--srw--locks.md)
-   [inizializzazione una sola volta](one-time-initialization.md)
-   [accesso a variabili interlock](interlocked-variable-access.md)
-   [elenchi collegati in modo singly interlocked](interlocked-singly-linked-lists.md)
-   [code timer](timer-queues.md)
-   macro [**MemoryBarrier**](/windows/win32/api/winnt/nf-winnt-memorybarrier)

Per altre informazioni sulla sincronizzazione, vedere [Problemi di sincronizzazione e multiprocessore](synchronization-and-multiprocessor-issues.md).

 

 
