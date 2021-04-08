---
title: Funzioni della guida dello strumento
description: Elenca le funzioni della libreria della guida dello strumento.
ms.assetid: 83732bd6-f4cf-409d-ad17-86503d408dc3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54f9d95598f9b48343ea9731e1a826fb147a73a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045219"
---
# <a name="tool-help-functions"></a>Funzioni della guida dello strumento

Le funzioni seguenti fanno parte della libreria della Guida di strumenti.



| Funzione                                                           | Descrizione                                                                                                      |
|--------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [**CreateToolhelp32Snapshot**](/windows/desktop/api/TlHelp32/nf-tlhelp32-createtoolhelp32snapshot)       | Esegue uno snapshot dei processi specificati, nonché gli heap, i moduli e i thread utilizzati da questi processi. |
| [**Heap32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32first)                                 | Recupera le informazioni sul primo blocco di un heap allocato da un processo.                      |
| [**Heap32ListFirst**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listfirst)                         | Recupera le informazioni sul primo heap allocato da un processo specificato.                       |
| [**Heap32ListNext**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listnext)                           | Recupera le informazioni sull'heap successivo allocato da un processo.                                  |
| [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next)                                   | Recupera informazioni sul blocco successivo di un heap allocato da un processo.                       |
| [**Module32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32first)                             | Recupera le informazioni sul primo modulo associato a un processo.                                          |
| [**Module32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32next)                               | Recupera le informazioni sul modulo successivo associato a un processo o a un thread.                                 |
| [**Process32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32first)                           | Recupera le informazioni sul primo processo rilevato in uno snapshot del sistema.                                  |
| [**Process32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32next)                             | Recupera le informazioni sul processo successivo registrato in uno snapshot del sistema.                                      |
| [**Thread32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32first)                             | Recupera le informazioni sul primo thread di qualsiasi processo rilevato in uno snapshot del sistema.                    |
| [**Thread32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32next)                               | Recupera le informazioni sul thread successivo di qualsiasi processo rilevato nello snapshot della memoria di sistema.            |
| [**Toolhelp32ReadProcessMemory**](/windows/desktop/api/TlHelp32/nf-tlhelp32-toolhelp32readprocessmemory) | Copia la memoria allocata a un altro processo in un buffer fornito dall'applicazione.                                  |



 

 

 




