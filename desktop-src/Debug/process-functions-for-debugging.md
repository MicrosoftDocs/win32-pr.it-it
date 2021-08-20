---
description: La funzione CreateProcess consente a un debugger di avviare un processo ed eseguirne il debug.
ms.assetid: 7056e181-9bc5-4530-a7b8-d5ff1e345eef
title: Funzioni di elaborazione per il debug
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6dec70de05e9b77cd3ff0b2ee8cd01c90ded2987f7ba1cacc3530f040344915
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118162632"
---
# <a name="process-functions-for-debugging"></a>Funzioni di elaborazione per il debug

La [**funzione CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) consente a un debugger di avviare un processo ed eseguirne il debug. Il *parametro fdwCreate* di **CreateProcess** viene usato per specificare il tipo di operazione di debug. Se per il parametro viene specificato il flag DEBUG PROCESS, un debugger esegue il debug del nuovo processo e di tutti i discendenti del processo, a condizione che i discendenti siano creati senza il \_ flag DEBUG \_ PROCESS.

Se i flag DEBUG PROCESS e DEBUG ONLY THIS PROCESS sono specificati per \_ \_ \_ \_ *fdwCreate,* un debugger esegue il debug del nuovo processo ma nessuno dei relativi discendenti.

Un debugger può eseguire il debug di un altro creando un processo con il flag DEBUG \_ PROCESS. Il nuovo processo (il debugger in fase di debug) deve quindi creare un processo con il flag DEBUG \_ PROCESS.

La [**funzione OpenProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocess) consente a un debugger di ottenere l'identificatore di un processo esistente. La [**funzione DebugActiveProcess**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocess) usa questo identificatore per collegare il debugger al processo. In genere, i debugger aprono un processo con i flag PROCESS \_ VM READ ed PROCESS VM \_ \_ \_ WRITE. L'uso di questi flag consente al debugger di leggere e scrivere nella memoria virtuale del processo usando le funzioni [**ReadProcessMemory**](/windows/win32/api/memoryapi/nf-memoryapi-readprocessmemory) [**e WriteProcessMemory.**](/windows/win32/api/memoryapi/nf-memoryapi-writeprocessmemory) Per altre informazioni, vedere [**Processi e thread.**](../procthread/processes-and-threads.md)

 

 
