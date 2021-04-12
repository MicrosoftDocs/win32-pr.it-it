---
title: Procedura dettagliata
description: Uno snapshot che include l'elenco dei processi contiene informazioni su ogni processo attualmente in esecuzione.
ms.assetid: 4fb55763-2206-48ad-8b1f-ed2c33b6f56b
keywords:
- enumerazione
- Enumerazione, processi
- processi
- processi, enumerazione dei processi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbc95f0de4021ce3c355286376decbdecef2c883
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473550"
---
# <a name="process-walking"></a>Procedura dettagliata

Uno snapshot che include l'elenco dei processi contiene informazioni su ogni processo attualmente in esecuzione. È possibile recuperare le informazioni per il primo processo nell'elenco usando la funzione [**Process32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32first) . Dopo aver recuperato il primo processo nell'elenco, è possibile attraversare l'elenco dei processi per le voci successive utilizzando la funzione [**Process32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32next) . **Process32First** e **Process32Next** riempiono una struttura [**PROCESSENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-processentry32) con informazioni su un processo nello snapshot. Per un esempio, vedere [acquisizione di uno snapshot e visualizzazione dei processi](taking-a-snapshot-and-viewing-processes.md).

È possibile recuperare un codice di stato di errore esteso per [**Process32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32first) e [**Process32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32next) utilizzando la funzione [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) .

È possibile leggere la memoria in un processo specifico in un buffer usando la funzione [**Toolhelp32ReadProcessMemory**](/windows/desktop/api/TlHelp32/nf-tlhelp32-toolhelp32readprocessmemory) (o la funzione [**VirtualQueryEx**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualqueryex) ).

> [!Note]  
> Il contenuto dei membri **th32ProcessID** e **th32ParentProcessID** di [**PROCESSENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-processentry32) è costituito da identificatori di processo e può essere usato da qualsiasi funzione che richiede un identificatore di processo.

 

 

 