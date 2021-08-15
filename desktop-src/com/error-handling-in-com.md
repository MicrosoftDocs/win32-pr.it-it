---
title: Gestione degli errori in COM (COM)
description: Gestione degli errori in COM
ms.assetid: 15f3ae3e-1794-4948-a7aa-6309a703364b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7953a970e470f5ae2c04b6a22c07f1de4fe663b100485732050b13c12a00b559
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119381911"
---
# <a name="error-handling-in-com-com"></a>Gestione degli errori in COM (COM)

Quasi tutte le funzioni COM e i metodi di interfaccia restituiscono un valore di tipo **HRESULT.** **HRESULT** (per *l'handle dei* risultati) è un modo per restituire valori di esito positivo, di avviso ed errore. **HRESULT** non sono in realtà handle a nulla; sono solo valori con diversi campi codificati nel valore. In base alla specifica COM, un risultato pari a zero indica l'esito positivo e un risultato diverso da zero indica un errore.

A livello di codice sorgente, tutti i valori di errore sono costituiti da tre parti, separate da caratteri di sottolineatura. La prima parte è il prefisso che identifica la funzionalità associata all'errore, la seconda parte è E per l'errore e la terza parte è una stringa che descrive la condizione effettiva. Ad esempio, **STG \_ E \_ MEDIUMFULL** viene restituito quando non è disponibile spazio su un disco rigido. Il **prefisso STG** indica la struttura di archiviazione, **E** indica che il codice di stato rappresenta un errore e **MEDIUMFULL** fornisce informazioni specifiche sull'errore. Molti dei valori che è possibile restituire da una funzione o un metodo di interfaccia sono definiti in Winerror.h.

Per altre informazioni sulla gestione degli errori, vedere le sezioni seguenti:

-   [Struttura dei codici di errore COM](structure-of-com-error-codes.md)
-   [Codici in FACILITY \_ ITF](codes-in-facility-itf.md)
-   [Uso di macro per la gestione degli errori](using-macros-for-error-handling.md)
-   [Gestione degli errori COM in Java e Visual Basic](com-error-handling-in-java-and-visual-basic.md)
-   [Strategie di gestione degli errori](error-handling-strategies.md)
-   [Gestione degli errori sconosciuti](handling-unknown-errors.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Codici di errore COM](com-error-codes.md)
</dt> </dl>

 

 




