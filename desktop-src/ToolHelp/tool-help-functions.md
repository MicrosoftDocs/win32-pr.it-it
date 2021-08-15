---
title: Funzioni della Guida degli strumenti
description: Elenca le funzioni della libreria della Guida dello strumento.
ms.assetid: 83732bd6-f4cf-409d-ad17-86503d408dc3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d73cc425f415c9cea8af9290743fb1afbb51182f8c03e7ec087ca95948fd2ebc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119058219"
---
# <a name="tool-help-functions"></a>Funzioni della Guida degli strumenti

Le funzioni seguenti fanno parte della libreria della Guida dello strumento.



| Funzione                                                           | Descrizione                                                                                                      |
|--------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [**CreateToolhelp32Snapshot**](/windows/desktop/api/TlHelp32/nf-tlhelp32-createtoolhelp32snapshot)       | Consente di creare uno snapshot dei processi specificati, nonché degli heap, dei moduli e dei thread usati da questi processi. |
| [**Heap32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32first)                                 | Recupera informazioni sul primo blocco di un heap allocato da un processo.                      |
| [**Heap32ListFirst**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listfirst)                         | Recupera informazioni sul primo heap allocato da un processo specificato.                       |
| [**Heap32ListNext**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listnext)                           | Recupera informazioni sull'heap successivo allocato da un processo.                                  |
| [**Heap32Avanti**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next)                                   | Recupera informazioni sul blocco successivo di un heap allocato da un processo.                       |
| [**Module32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32first)                             | Recupera informazioni sul primo modulo associato a un processo.                                          |
| [**Module32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32next)                               | Recupera informazioni sul modulo successivo associato a un processo o a un thread.                                 |
| [**Process32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32first)                           | Recupera informazioni sul primo processo rilevato in uno snapshot di sistema.                                  |
| [**Processo32Avanti**](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32next)                             | Recupera informazioni sul processo successivo registrato in uno snapshot di sistema.                                      |
| [**Thread32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32first)                             | Recupera informazioni sul primo thread di qualsiasi processo rilevato in uno snapshot di sistema.                    |
| [**Thread32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32next)                               | Recupera informazioni sul thread successivo di qualsiasi processo rilevato nello snapshot della memoria di sistema.            |
| [**Toolhelp32ReadProcessMemory**](/windows/desktop/api/TlHelp32/nf-tlhelp32-toolhelp32readprocessmemory) | Copia la memoria allocata a un altro processo in un buffer fornito dall'applicazione.                                  |



 

 

 




