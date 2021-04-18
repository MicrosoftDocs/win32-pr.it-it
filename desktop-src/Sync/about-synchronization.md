---
description: Per sincronizzare l'accesso a una risorsa, usare uno degli oggetti di sincronizzazione in una delle funzioni di attesa.
ms.assetid: 0930bf12-6d5f-4f2c-914d-53e6e862d3bd
title: Informazioni sulla sincronizzazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ad53dc8c309d8ec55f37cef5f78839348071477
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315315"
---
# <a name="about-synchronization"></a>Informazioni sulla sincronizzazione

Per sincronizzare l'accesso a una risorsa, usare uno degli [oggetti di sincronizzazione](synchronization-objects.md) in una delle [funzioni di attesa](wait-functions.md). Lo stato di un oggetto di sincronizzazione è *segnalato* o non *segnalato*. Le funzioni Wait consentono a un thread di bloccare la propria esecuzione fino a quando un oggetto non segnalato specificato non è impostato sullo stato segnalato. Per ulteriori informazioni, vedere [sincronizzazione interprocesso](interprocess-synchronization.md).

Di seguito sono riportati altri meccanismi di sincronizzazione:

-   [input e output sovrapposti](synchronization-and-overlapped-input-and-output.md)
-   [chiamate di procedure asincrone](asynchronous-procedure-calls.md)
-   [oggetti sezione critica](critical-section-objects.md)
-   [variabili di condizione](condition-variables.md)
-   [blocchi in lettura/scrittura Slim](slim-reader-writer--srw--locks.md)
-   [inizializzazione unica](one-time-initialization.md)
-   [accesso a variabili Interlocked](interlocked-variable-access.md)
-   [elenchi collegati singolarmente con Interlocking](interlocked-singly-linked-lists.md)
-   [Code timer](timer-queues.md)
-   macro [**MemoryBarrier**](/windows/win32/api/winnt/nf-winnt-memorybarrier)

Per ulteriori informazioni sulla sincronizzazione, vedere la pagina relativa ai [problemi di sincronizzazione e multiprocessore](synchronization-and-multiprocessor-issues.md).

 

 
