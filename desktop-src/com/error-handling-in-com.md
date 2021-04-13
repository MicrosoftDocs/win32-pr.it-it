---
title: Gestione degli errori in COM (COM)
description: Gestione degli errori in COM
ms.assetid: 15f3ae3e-1794-4948-a7aa-6309a703364b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19af496eabf50833c99d462ff074254bc39bb7a0
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104475010"
---
# <a name="error-handling-in-com-com"></a>Gestione degli errori in COM (COM)

Quasi tutte le funzioni COM e i metodi di interfaccia restituiscono un valore di tipo **HRESULT**. **HRESULT** (per *handle di risultato*) è un modo per restituire i valori di esito positivo, avviso ed errore. Gli oggetti **HRESULT** s non sono effettivamente handle sono solo valori con diversi campi codificati nel valore. In base alla specifica COM, un risultato pari a zero indica un esito positivo e un risultato diverso da zero indica un errore.

A livello di codice sorgente tutti i valori di errore sono costituiti da tre parti, separate da caratteri di sottolineatura. La prima parte è il prefisso che identifica la struttura associata all'errore, la seconda parte è E per errore e la terza parte è una stringa che descrive la condizione effettiva. Ad esempio, **STG \_ E \_ MEDIUMFULL** vengono restituiti quando non è disponibile spazio su disco rigido. Il prefisso **STG** indica la funzionalità di archiviazione, **e** indica che il codice di stato rappresenta un errore e **MEDIUMFULL** fornisce informazioni specifiche sull'errore. Molti dei valori che possono essere restituiti da una funzione o un metodo di interfaccia sono definiti in Winerror. h.

Per ulteriori informazioni sulla gestione degli errori, vedere le sezioni seguenti:

-   [Struttura dei codici di errore COM](structure-of-com-error-codes.md)
-   [Codici in funzionalità \_ ITF](codes-in-facility-itf.md)
-   [Uso delle macro per la gestione degli errori](using-macros-for-error-handling.md)
-   [Gestione degli errori COM in Java e Visual Basic](com-error-handling-in-java-and-visual-basic.md)
-   [Strategie di gestione degli errori](error-handling-strategies.md)
-   [Gestione degli errori sconosciuti](handling-unknown-errors.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Codici di errore COM](com-error-codes.md)
</dt> </dl>

 

 




