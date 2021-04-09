---
description: La funzione CreateProcess consente a un debugger di avviare un processo ed eseguirne il debug.
ms.assetid: 7056e181-9bc5-4530-a7b8-d5ff1e345eef
title: Funzioni di elaborazione per il debug
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d31378a4115acfdd5a4a1836199b7387adeb6e3f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966052"
---
# <a name="process-functions-for-debugging"></a>Funzioni di elaborazione per il debug

La funzione [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) consente a un debugger di avviare un processo ed eseguirne il debug. Il parametro *fdwCreate* di **CreateProcess** viene usato per specificare il tipo di operazione di debug. Se \_ viene specificato il flag del processo di debug per il parametro, un debugger esegue il debug del nuovo processo e di tutti i discendenti del processo, purché i discendenti vengano creati senza il flag del processo di debug \_ .

Se il processo di DEBUG \_ e il debug \_ solo \_ \_ di questi flag di processo sono specificati per *fdwCreate*, un debugger esegue il debug del nuovo processo, ma nessuno dei relativi discendenti.

Un debugger può eseguire il debug di un altro creando un processo con il flag del processo di DEBUG \_ . Il nuovo processo (il debugger sottoposto a debug) deve quindi creare un processo con il flag del processo di DEBUG \_ .

La funzione [**OpenProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocess) consente a un debugger di ottenere l'identificatore di un processo esistente. La funzione [**DebugActiveProcess**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocess) utilizza questo identificatore per alleghi il debugger al processo. In genere, i debugger aprono un processo con i flag di scrittura della macchina virtuale di processo \_ \_ lettura ed elaborazione VM \_ \_ . L'uso di questi flag consente al debugger di leggere e scrivere nella memoria virtuale del processo usando le funzioni [**ReadProcessMemory**](/windows/win32/api/memoryapi/nf-memoryapi-readprocessmemory) e [**WriteProcessMemory**](/windows/win32/api/memoryapi/nf-memoryapi-writeprocessmemory) . Per ulteriori informazioni, vedere [**processi e thread**](../procthread/processes-and-threads.md).

 

 
