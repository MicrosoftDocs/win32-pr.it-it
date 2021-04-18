---
description: Sebbene i provider siano invitati a usare nomi di istanza univoci, non tutti i provider lo eseguono.
ms.assetid: 3c8fcb8d-2ea4-4b24-b649-7bd375c1133d
title: Gestione dei nomi di istanza duplicati
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: 220e5d7d0181a79c1d1415486cc946d484e11952
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312164"
---
# <a name="handling-duplicate-instance-names"></a>Gestione dei nomi di istanza duplicati

Sebbene i provider siano fortemente invitati a usare nomi di istanza univoci, non tutti i provider lo eseguono. La convenzione per la visualizzazione di nomi di istanza duplicati consiste nell'accodare un `#` carattere e un numero di serie al nome dell'istanza, ad eccezione della prima occorrenza del nome. Se, ad esempio, sono presenti tre istanze di `svchost` in un campione, i tre nomi vengono visualizzati come `svchost` , `svchost#1` e `svchost#2` .

Sfortunatamente, questa convenzione non risolve completamente il problema. I numeri di serie vengono assegnati in base all'ordine in cui un determinato nome di istanza viene visualizzato in un campione e questo ordine potrebbe non essere coerente da esempio a campione. Ad esempio, l'esempio A può vedere `svchost` (pid 100), `svchost#1` (PID 200) e `svchost#2` (PID 300). Se quindi il svchost con PID 100 si arresta, l'esempio seguente visualizzerà `svchost` (pid 200) e `svchost#1` (PID 300). La logica di corrispondenza di base tenterà di trovare una corrispondenza tra le statistiche di esempio `svchost#1` (da pid 200) e le statistiche di esempio b `svchost#1` (dal PID 300), ottenendo risultati non validi per l'esempio B. gli errori si verificano quando una nuova istanza non univoca viene visualizzata in un campione o quando un'istanza non univoca smette di essere visualizzata in un campione (a meno che l'istanza aggiunta

## <a name="process-counterset"></a>Contatore processi

Questo problema è particolarmente problematico per il `Process` contatore perché usa solo il nome dell'exe del processo come nome dell'istanza anche se il nome dell'exe non è univoco. `Process`Non è possibile modificare il comportamento predefinito del contatore in Windows a causa di problemi di compatibilità.

È possibile modificare il comportamento di `Process` e `Thread` CounterSet in modo da utilizzare nomi di istanza univoci impostando i valori del registro di sistema `ProcessNameFormat` o `ThreadNameFormat` nella chiave del registro di `HKLM\System\CurrentControlSet\Services\Perfproc\Performance` sistema.

> [!CAUTION]
> L'abilitazione di nomi di istanza univoci per il `Process` contatore può causare un comportamento non corretto di alcuni programmi, poiché molti programmi prevedono il modello di denominazione non univoco. Ad esempio, un programma che cerca un'istanza con un nome di EXE noto specifico non sarà più in grado di trovare tale istanza dopo aver abilitato i nomi di istanza univoci.

Il tipo di registro per questi valori è `REG_DWORD` . Impostando il valore su `2` , l'identificatore di processo (PID) viene aggiunto al nome dell'istanza del processo e all'identificatore del thread (TID) al nome dell'istanza del thread. Per disabilitare questa funzionalità, impostare il valore su 1 o eliminare il valore.
