---
description: La funzione CreateThread crea un nuovo thread per un processo.
ms.assetid: df59eedd-45ec-4564-96a5-8cecb345cfcc
title: Funzioni thread per il debug
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb5ab0865d5585656a5c22c24e2604032de8b888
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523673"
---
# <a name="thread-functions-for-debugging"></a>Funzioni thread per il debug

La funzione [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) crea un nuovo thread per un processo. Per i debugger è in genere necessario esaminare o modificare il contenuto dei registri di un thread. A tale scopo, è necessario che un debugger ottenga un handle per il thread utilizzando la funzione [**DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) e specificando l'accesso appropriato al thread (contesto Get del thread, \_ contesto del set di \_ thread \_ \_ o entrambi). La funzione [**OpenThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthread) consente a un debugger di ottenere l'identificatore di un thread esistente.

Un processo con accesso appropriato a un thread può esaminare i registri del thread utilizzando la funzione [**GetThreadContext**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadcontext) e impostare il contenuto dei registri del thread utilizzando la funzione [**SetThreadContext**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadcontext) .

Un processo può inoltre ottenere \_ \_ l'accesso a un thread per sospendere la sospensione del thread. Questo tipo di accesso consente a un debugger di controllare l'esecuzione di un thread con le funzioni [**SuspendThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-suspendthread) e [**ResumeThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-resumethread) . Per ulteriori informazioni sui thread, vedere [processi e thread](../procthread/processes-and-threads.md).

 

 
