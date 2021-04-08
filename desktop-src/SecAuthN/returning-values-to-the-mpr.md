---
description: Le funzioni di rete di Windows restituiscono l' \_ esito positivo in caso di esito positivo oppure restituiscono un valore diverso da zero se la funzione rileva un errore. Inoltre, restituiscono informazioni estese sugli errori utilizzando WNetSetLastError e SetLastError.
ms.assetid: cb9d29a1-b3a5-4440-a069-3cd1565b1699
title: Restituzione di valori a MPR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c96a5636f57d5c926af4e43e676f0b6db75d164
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967391"
---
# <a name="returning-values-to-the-mpr"></a>Restituzione di valori a MPR

Le funzioni di rete di Windows restituiscono l' \_ esito positivo in caso di esito positivo oppure restituiscono un valore diverso da zero se la funzione rileva un errore. Inoltre, restituiscono informazioni estese sugli errori utilizzando [**WNetSetLastError**](/windows/desktop/api/Npapi/nf-npapi-wnetsetlasterrora) e [**SetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-setlasterror).

Per supportare il comportamento precedente, le funzioni del provider di rete non devono chiamare [**SetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-setlasterror) prima di restituire. Questo è dovuto al fatto che MPR chiama **SetLastError** per le funzioni nell'API del provider di rete dopo la restituzione. Se i provider di rete chiamano direttamente **SetLastError** , verranno effettuate chiamate di funzione ridondanti. Le funzioni del provider di rete devono semplicemente restituire un codice di errore. I codici di errore vengono specificati nella descrizione della funzione o nei [valori restituiti](network-security-return-values.md). Inoltre, le funzioni del provider di rete possono restituire eventuali [codici di errore di sistema](../debug/system-error-codes.md), ad esempio memoria insufficiente. L'unica eccezione è [**NPGetCaps**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps), che deve restituire una maschera che indica le funzioni supportate dal provider di rete.

Se una funzione del provider di rete deve restituire informazioni estese sugli errori, deve chiamare [**WNetSetLastError**](/windows/desktop/api/Npapi/nf-npapi-wnetsetlasterrora). Questa funzione viene fornita dal sistema operativo Windows per l'uso da parte dei provider di rete. Quando il provider chiama **WNetSetLastError**, può impostare una stringa contenente informazioni aggiuntive sull'errore. Queste informazioni vengono archiviate in base ai singoli thread. Questo è analogo a [**SetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-setlasterror) per le applicazioni Windows. Il sistema operativo Windows chiama **WNetSetLastError** per verificare la presenza di una stringa archiviata con **WNetSetLastError** e, se presente, restituisce le informazioni estese sull'errore all'applicazione chiamante che ha avviato la richiesta di rete.

> [!Note]  
> Il prefisso WNet di [**WNetSetLastError**](/windows/desktop/api/Npapi/nf-npapi-wnetsetlasterrora) è fuorviante perché questa API, a differenza di **WNetSetLastError**, non fa parte del set di API di rete di Windows. **WNetSetLastError** deve essere utilizzato solo dai provider di rete. Il nome **WNetSetLastError** viene mantenuto per la compatibilità con i provider esistenti.

 

 

 
