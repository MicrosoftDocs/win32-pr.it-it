---
description: Anche se i provider sono invitati a usare nomi di istanza univoci, non tutti i provider lo fanno.
ms.assetid: 3c8fcb8d-2ea4-4b24-b649-7bd375c1133d
title: Gestione dei nomi di istanza duplicati
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: f58f6ed11951c7b66951f5154009127c5029de3760a9419a7c9716781be8234f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144004"
---
# <a name="handling-duplicate-instance-names"></a>Gestione dei nomi di istanza duplicati

Anche se i provider sono fortemente invitati a usare nomi di istanza univoci, non tutti i provider lo fanno. La convenzione per la visualizzazione di nomi di istanza duplicati è l'aggiunta di un carattere e di un numero di serie al nome dell'istanza, ad eccezione della prima `#` occorrenza del nome. Ad esempio, se in un esempio sono presenti tre istanze di , i tre nomi vengono `svchost` visualizzati come , e `svchost` `svchost#1` `svchost#2` .

Sfortunatamente, questa convenzione non risolve completamente il problema. I numeri di serie vengono assegnati in base all'ordine in cui un determinato nome di istanza viene visualizzato in un campione e questo ordine può essere incoerente da un campione all'altro. Ad esempio, l'esempio A potrebbe visualizzare `svchost` (PID 100), `svchost#1` (PID 200) e `svchost#2` (PID 300). Quindi, se svchost con PID 100 si arresta, l'esempio successivo visualizza `svchost` (PID 200) e `svchost#1` (PID 300). La logica di corrispondenza di base tenterebbe di trovare una corrispondenza tra le statistiche del campione A (dal PID 200) e le statistiche del campione `svchost#1` B `svchost#1` (dal PID 300), causando risultati non validi per il campione B. Gli errori si verificano quando viene visualizzata una nuova istanza non univoca in un campione o quando un'istanza non univoca smette di essere visualizzata in un esempio (a meno che l'istanza aggiunta/rimossa non sia l'ultima).

## <a name="process-counterset"></a>Counterset del processo

Questo problema è particolarmente problematico per l'insieme di contatori perché usa solo il nome EXE del processo come nome dell'istanza anche se il nome `Process` EXE non è univoco. Il comportamento predefinito del contatore `Process` in Windows non può essere modificato a causa di problemi di compatibilità.

È possibile modificare il comportamento dei contatori e in modo da usare nomi di istanza univoci impostando i valori del Registro di sistema o `Process` nella chiave del Registro di sistema `Thread` `ProcessNameFormat` `ThreadNameFormat` `HKLM\System\CurrentControlSet\Services\Perfproc\Performance` .

> [!CAUTION]
> L'abilitazione di nomi di istanza univoci per il contatore può causare un comportamento non corretto di alcuni programmi, poiché molti programmi prevedono il modello di denominazione `Process` non univoco. Ad esempio, un programma che cerca un'istanza con un nome EXE noto specifico non sarà più in grado di trovare tale istanza dopo l'abilitazione di nomi di istanza univoci.

Il tipo di Registro di sistema per questi valori è `REG_DWORD` . Se si imposta il valore su , l'identificatore del processo (PID) viene aggiunto al nome dell'istanza del processo e l'identificatore di `2` thread (TID) al nome dell'istanza del thread. Per disabilitare questa funzionalità, impostare il valore su 1 o eliminare il valore.
