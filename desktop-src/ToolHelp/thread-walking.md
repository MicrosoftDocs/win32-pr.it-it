---
title: Thread Walking
description: Uno snapshot che include l'elenco di thread contiene informazioni su ogni thread di ogni processo attualmente in esecuzione.
ms.assetid: 2440b781-652d-4d73-b173-87504e7b49b5
keywords:
- enumerazione
- enumerazione, thread
- thread
- thread, enumerazione di thread
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec4f75f4690be05a7703dab80965fb41035da03cb21f244a4b5a9039a4a61ef0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119513851"
---
# <a name="thread-walking"></a>Thread Walking

Uno snapshot che include l'elenco di thread contiene informazioni su ogni thread di ogni processo attualmente in esecuzione. È possibile recuperare informazioni per il primo thread nell'elenco usando la [**funzione Thread32First.**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32first) Dopo aver recuperato il primo thread nell'elenco, è possibile recuperare informazioni per i thread successivi usando la [**funzione Thread32Next.**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32next) **Thread32First** e **Thread32Next** compilano una [**struttura THREADENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-threadentry32) con informazioni sui singoli thread nello snapshot.

È possibile enumerare i thread di un processo specifico, creare uno snapshot che include i thread e quindi attraversare l'elenco di thread, mantenendo le informazioni sui thread che hanno lo stesso identificatore di processo del processo specificato.

È possibile recuperare un codice di stato di errore esteso per [**Thread32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32first) e [**Thread32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32next) usando la [**funzione GetLastError.**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)

> [!Note]  
> Il contenuto del membro **th32ThreadID** di [**THREADENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-threadentry32) è un identificatore di thread e può essere usato da qualsiasi funzione che richiede un identificatore di thread.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Attraversamento dell'elenco di thread](traversing-the-thread-list.md)
</dt> </dl>

 

 