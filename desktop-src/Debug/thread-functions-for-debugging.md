---
description: Informazioni su come usare la funzione CreateThread per creare un nuovo thread per un processo. I debugger in genere devono esaminare o modificare il contenuto dei registri di un thread.
ms.assetid: df59eedd-45ec-4564-96a5-8cecb345cfcc
title: Funzioni di thread per il debug
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d46e9c94ef776cd14bc76afb2c824f2150a1e7c0eb8c94176b237e1c6d54430f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119655221"
---
# <a name="thread-functions-for-debugging"></a>Funzioni di thread per il debug

La [**funzione CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) crea un nuovo thread per un processo. I debugger in genere devono esaminare o modificare il contenuto dei registri di un thread. A tale scopo, un debugger deve ottenere un handle per il thread usando la funzione [**DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) e specificando l'accesso appropriato al thread (THREAD \_ GET \_ CONTEXT, THREAD \_ SET CONTEXT \_ o entrambi). La [**funzione OpenThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthread) consente a un debugger di ottenere l'identificatore di un thread esistente.

Un processo con accesso appropriato a un thread può esaminare i registri del thread usando la [**funzione GetThreadContext**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadcontext) e impostare il contenuto dei registri del thread usando la [**funzione SetThreadContext.**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadcontext)

Un processo può anche ottenere l'accesso THREAD \_ SUSPEND RESUME a un \_ thread. Questo tipo di accesso consente a un debugger di controllare l'esecuzione di un thread con le [**funzioni SuspendThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-suspendthread) [**e ResumeThread.**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-resumethread) Per altre informazioni sui thread, vedere [Processi e thread](../procthread/processes-and-threads.md).

 

 
