---
title: Pam Version-Independent i nomi e la destinazione di versioni specifiche di Windows
description: In molti casi, l'API Windows Filtering Platform (WFP) fornisce più di una versione di una funzione o di una struttura.
ms.assetid: FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41be83a50b4786aa4b98cd7f8dd7405a33fe94be
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297789"
---
# <a name="wfp-version-independent-names-and-targeting-specific-versions-of-windows"></a>Pam Version-Independent i nomi e la destinazione di versioni specifiche di Windows

In molti casi, l'API Windows Filtering Platform (WFP) fornisce più di una versione di una funzione o di una struttura.

La maggior parte dei nomi di dati e funzioni nell'API PAM termina con un numero di versione, ad esempio "0" o "1", anche se è presente una sola versione.

## <a name="version-mapping-in-fwpvih"></a>Mapping della versione in fwpvi. h

Il file di intestazione fwpvi. h è incluso a partire da Windows 7 SDK e WDK. Questo file di intestazione esegue il mapping del nome API senza versione alla versione appropriata per l'uso con un sistema operativo specifico.

Ecco, ad esempio, un breve estratto dalla versione di fwpvi. h inclusa in Windows 8 SDK.


```C++
#define FwpmNetEventCreateEnumHandle FwpmNetEventCreateEnumHandle0
#if (NTDDI_VERSION >= NTDDI_WIN8)
#define FwpmNetEventEnum FwpmNetEventEnum2
#elif (NTDDI_VERSION >= NTDDI_WIN7)
#define FwpmNetEventEnum FwpmNetEventEnum1
#else
#define FwpmNetEventEnum FwpmNetEventEnum0
#endif
```



Come illustrato in precedenza, esiste una sola versione di **FwpmNetEventCreateEnumHandle** – [**FwpmNetEventCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventcreateenumhandle0) , pertanto qualsiasi chiamata a **FwpmNetEventCreateEnumHandle** chiamerà sempre **FwpmNetEventCreateEnumHandle0**, indipendentemente dal sistema operativo di destinazione.

Tuttavia, sono disponibili tre versioni di **FwpmNetEventEnum**: [**FwpmNetEventEnum0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum0), [**FwpmNetEventEnum1**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum1)e [**FwpmNetEventEnum2**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum2). Il file di intestazione fwpvi. h garantisce che una chiamata a **FwpmNetEventEnum** chiamerà la versione più appropriata per il sistema operativo di destinazione:

-   [**FwpmNetEventEnum2**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum2) per Windows 8 (o versioni successive)
-   [**FwpmNetEventEnum1**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum1) per Windows 7 è destinato
-   [**FwpmNetEventEnum0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum0) per sistemi operativi precedenti, ad esempio Windows Vista o Windows Vista con Service Pack 1 (SP1)

## <a name="calling-version-independent-functions-and-structures"></a>Chiamata di funzioni e strutture Version-Independent

Gli sviluppatori WFP destinati a un particolare sistema operativo o a una versione WDK sono invitati a programmare sempre in base alle macro indipendenti dalla versione. Verrà selezionata automaticamente la versione più recente supportata nel sistema operativo di destinazione. È consigliabile usare i file di intestazione più recenti, anche quando la destinazione è un sistema operativo precedente. In questo modo si garantisce che venga usata la versione supportata più recente e che sia possibile semplificare la manutenzione e l'aggiornamento del codice.

La [documentazione di riferimento dell'API WFP](fwp-reference.md) descrive ogni versione di un'API numerata. Se esiste più di una versione, viene indicato il sistema operativo di destinazione. Tuttavia, gli sviluppatori in genere vogliono chiamare le API indipendenti dalla versione (numerate) e indicare il sistema operativo di destinazione (ad esempio **NTDDI \_ WIN6** per Windows Vista o **NTDDI \_ Win8** per Windows 8).

Per garantire la corretta gestione delle funzioni che accettano parametri diversi in versioni diverse, è possibile includere blocchi condizionali, ad esempio `#if (NTDDI_VERSION >= NTDDI_WIN7)` .

 

 




