---
title: Debug di WOW64
description: È possibile eseguire il debug di applicazioni in esecuzione in WOW64 con un debugger ospitato da x86 o un debugger nativo.
ms.assetid: e0945bdd-998d-4531-869f-21c505cb2135
keywords:
- Programmazione Windows WOW64 a 64 bit, debug
- debug della programmazione Windows WOW64 a 64 bit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcc7590b0b4f44f9e1a48a204723fb0652b9c2e4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399585"
---
# <a name="debugging-wow64"></a>Debug di WOW64

È possibile eseguire il debug di applicazioni in esecuzione in WOW64 in due modi:

-   Usare un debugger ospitato da x86, ad esempio NTSD, WinDbg o Visual Studio. Il NTSD a 32 bit è installato in% SystemRoot% \\ SysWow64 nelle installazioni al dettaglio. Si noti che i debugger x86 possono essere usati per eseguire il debug del codice x86, ma non possono essere usati per disassemblare o impostare punti di interruzione all'interno del livello di thunk WOW64 perché si tratta di codice nativo a 64 bit.
-   Usare un debugger nativo, ad esempio CDB, NTSD o WinDbg e l'estensione del debugger WOW64, Wow64exts.dll. Se il debugger nativo si interrompe mentre il processore è in modalità x86, il processo viene presentato come processo x86. Se il processore è in modalità nativa, il debugger Visualizza il processo come nativo.

CDB, NTSD e WinDbg sono inclusi negli strumenti di debug per Windows. Per ulteriori informazioni, vedere la documentazione relativa agli [strumenti di debug per Windows](/windows-hardware/drivers/debugger/) .

L'estensione del debugger Wow64exts viene installata con WinDbg. Usare il comando! Load wow64exts per caricare l'estensione del debugger. La tabella seguente elenca i comandi dell'estensione del debugger wow64exts.



| Comando                | Descrizione                                                                                                                              |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| ! wow64exts. SW          | Passa dalla modalità x86 alla modalità nativa.                                                                                                    |
| ! wow64exts. k *conteggio*   | Dump di un'analisi dello stack a 32 bit/64 bit combinata. Se *count* viene specificato, il comando eseguirà il dump dei primi indirizzi di *conteggio* in ogni traccia dello stack.  |
| ! wow64exts.info        | Effettua il dump delle informazioni di base sul PEB del processo, sulla TEB del thread corrente e sugli slot di archiviazione locale di thread (TLS) usati da WOW64. |
| ! wow64exts. r *Indirizzo* | Dump del contesto per l'indirizzo specificato. Se *Address* non è specificato, il comando dump il contesto per il processore.                     |



 

 

 