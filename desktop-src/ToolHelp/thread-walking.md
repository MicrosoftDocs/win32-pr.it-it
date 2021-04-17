---
title: Thread a piedi
description: Uno snapshot che include l'elenco di thread contiene informazioni su ogni thread di ogni processo attualmente in esecuzione.
ms.assetid: 2440b781-652d-4d73-b173-87504e7b49b5
keywords:
- enumerazione
- Enumerazione, thread
- thread
- thread, enumerazione dei thread
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32eff584aedaa3f6124cc358a4ee9d2a94962843
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300101"
---
# <a name="thread-walking"></a>Thread a piedi

Uno snapshot che include l'elenco di thread contiene informazioni su ogni thread di ogni processo attualmente in esecuzione. È possibile recuperare le informazioni per il primo thread nell'elenco usando la funzione [**Thread32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32first) . Dopo aver recuperato il primo thread nell'elenco, è possibile recuperare le informazioni per i thread successivi usando la funzione [**Thread32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32next) . **Thread32First** e **Thread32Next** riempiono una struttura [**THREADENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-threadentry32) con informazioni sui singoli thread dello snapshot.

È possibile enumerare i thread di un processo specifico eseguendo uno snapshot che include i thread e quindi attraversando l'elenco dei thread, mantenendo le informazioni sui thread con lo stesso identificatore di processo del processo specificato.

È possibile recuperare un codice di stato di errore esteso per [**Thread32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32first) e [**Thread32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32next) utilizzando la funzione [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) .

> [!Note]  
> Il contenuto del membro **th32ThreadID** di [**THREADENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-threadentry32) è un identificatore del thread e può essere usato da qualsiasi funzione che richiede un identificatore di thread.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Attraversamento dell'elenco dei thread](traversing-the-thread-list.md)
</dt> </dl>

 

 