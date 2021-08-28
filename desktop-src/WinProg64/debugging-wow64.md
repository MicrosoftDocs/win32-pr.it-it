---
title: Debug di WOW64
description: È possibile eseguire il debug delle applicazioni in esecuzione in WOW64 con un debugger ospitato da x86 o un debugger nativo.
ms.assetid: e0945bdd-998d-4531-869f-21c505cb2135
keywords:
- WOW64 64-bit Windows programmazione , debug
- debug di WOW64 a 64 bit Windows programmazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fa0f101f382239d146cf668e46efc245753f86ec3c876087f9a4a94bbd356f0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121811"
---
# <a name="debugging-wow64"></a>Debug di WOW64

È possibile eseguire il debug delle applicazioni in esecuzione in WOW64 in due modi:

-   Usare un debugger ospitato da x86, ad esempio NTSD, WinDbg o Visual Studio. NtSD a 32 bit viene installato in %systemroot% \\ syswow64 nelle installazioni retail. Si noti che i debugger x86 possono essere usati per eseguire il debug del codice x86, ma non per disassemblare o impostare punti di interruzione all'interno del livello thunk WOW64 perché si tratta di codice nativo a 64 bit.
-   Usare un debugger nativo, ad esempio CDB, NTSD o WinDbg e l'estensione del debugger WOW64, Wow64exts.dll. Se il debugger nativo si interrompe mentre il processore è in modalità x86, il debugger presenta il processo come processo x86. Se il processore è in modalità nativa, il debugger presenta il processo come nativo.

CDB, NTSD e WinDbg sono inclusi negli strumenti di debug per Windows. Per altre informazioni, vedere la [documentazione relativa agli strumenti Windows](/windows-hardware/drivers/debugger/) debug.

L'estensione del debugger Wow64exts viene installata con WinDbg. Usare il comando !load wow64exts per caricare l'estensione del debugger. Nella tabella seguente sono elencati i comandi dell'estensione del debugger !wow64exts.



| Comando                | Descrizione                                                                                                                              |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| !wow64exts.sw          | Passa dalla modalità x86 alla modalità nativa.                                                                                                    |
| !wow64exts.k *count*   | Esegue il dump di un'analisi combinata dello stack a 32 bit/64 bit. Se *si specifica count,* il comando esegue il dump dei primi *indirizzi di* conteggio in ogni analisi dello stack.  |
| !wow64exts.info        | Esegue il dump delle informazioni di base sul file PEB del processo, sul TEB del thread corrente e sugli slot di archiviazione thread-local (TLS) usati da WOW64. |
| !wow64exts.r *address* | Esegue il dump del contesto per l'indirizzo specificato. Se *address* non viene specificato, il comando esegue il dump del contesto per il processore.                     |



 

 

 