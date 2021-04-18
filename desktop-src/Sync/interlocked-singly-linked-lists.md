---
description: Un elenco collegato singolarmente (SList) Interlocked semplifica l'attività di inserimento ed eliminazione da un elenco collegato.
ms.assetid: 35463ace-33ab-4eb9-9901-2504a92456e2
title: Elenchi collegati singolarmente con Interlocking
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9af39847fa2fd1b1873c661d6ec904783e0139b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315305"
---
# <a name="interlocked-singly-linked-lists"></a>Elenchi collegati singolarmente con Interlocking

Un *elenco collegato singolarmente (slist) Interlocked* semplifica l'attività di inserimento ed eliminazione da un elenco collegato. SLists vengono implementati usando un algoritmo di non blocco per fornire la sincronizzazione atomica, migliorare le prestazioni del sistema ed evitare problemi, ad esempio l'inversione di priorità e i convogli di blocco.

SLists sono semplici da implementare e usare nel codice a 32 bit. Tuttavia, è difficile implementarli nel codice a 64 bit perché la quantità di dati scambiati dalle primitive di scambio native Interlocked non è il doppio delle dimensioni dell'indirizzo, come avviene nel codice a 32 bit. Pertanto, SLists consente il porting di algoritmi scalabili di fascia alta a Windows.

**Windows 8:** A partire da Windows 8 sono disponibili le primitive di scambio native Interlocked appropriate per il codice a 64 bit, ad esempio [**InterlockedCompare64Exchange128**](/previous-versions/windows/desktop/legacy/ms683553(v=vs.85)).

Le applicazioni possono usare SLists chiamando la funzione [**InitializeSListHead**](/windows/win32/api/interlockedapi/nf-interlockedapi-initializeslisthead) per inizializzare l'intestazione dell'elenco. Per inserire elementi nell'elenco, usare la funzione [**InterlockedPushEntrySList**](/windows/win32/api/interlockedapi/nf-interlockedapi-interlockedpushentryslist) . Per eliminare elementi dall'elenco, usare la funzione [**InterlockedPopEntrySList**](/windows/win32/api/interlockedapi/nf-interlockedapi-interlockedpopentryslist) .

Tutti gli elementi dell'elenco devono essere allineati in un limite di **\_ \_ allineamento dell'allocazione di memoria** . Gli elementi non allineati possono provocare risultati imprevedibili. Vedere **\_ \_ malloc allineato**.

Per un esempio, vedere [uso di elenchi collegati singolarmente](using-singly-linked-lists.md).

Nella tabella seguente sono elencate le funzioni di SList.



| Funzione                                                         | Descrizione                                                                                                                                               |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**InitializeSListHead**](/windows/win32/api/interlockedapi/nf-interlockedapi-initializeslisthead)               | Inizializza l'intestazione di un elenco collegato singolarmente.                                                                                                             |
| [**InterlockedFlushSList**](/windows/win32/api/interlockedapi/nf-interlockedapi-interlockedflushslist)           | Scarica l'intero elenco di elementi in un elenco collegato singolarmente.                                                                                                 |
| [**InterlockedPopEntrySList**](/windows/win32/api/interlockedapi/nf-interlockedapi-interlockedpopentryslist)     | Rimuove un elemento dall'inizio di un elenco collegato singolarmente.                                                                                                   |
| [**InterlockedPushEntrySList**](/windows/win32/api/interlockedapi/nf-interlockedapi-interlockedpushentryslist)   | Inserisce un elemento all'inizio di un elenco collegato singolarmente.                                                                                                     |
| [**InterlockedPushListSList**](/previous-versions/windows/desktop/legacy/hh448545(v=vs.85))     | Inserisce un elenco collegato singolarmente davanti a un altro elenco collegato singolarmente.                                                                                  |
| [**InterlockedPushListSListEx**](/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedpushlistslistex) | Inserisce un elenco collegato singolarmente davanti a un altro elenco collegato singolarmente. Questa versione del metodo non usa la convenzione di chiamata **\_ \_ fastcall** . |
| [**RtlFirstEntrySList**](/windows/desktop/api/WinNT/nf-winnt-rtlfirstentryslist)                 | Recupera la prima voce in un elenco collegato singolarmente.                                                                                                        |
| [**QueryDepthSList**](/windows/win32/api/interlockedapi/nf-interlockedapi-querydepthslist)                       | Recupera il numero di voci nell'elenco collegato singolarmente specificato.                                                                                      |



 

 

 
