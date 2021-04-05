---
title: Recupero intervallo attributi
description: Un attributo multivalore può contenere quasi un numero qualsiasi di valori. In molti casi può essere vantaggioso, o addirittura necessario, limitare l'intervallo di valori recuperati da una query.
ms.assetid: 3a0eb764-fca9-4ca6-9991-b85f293961af
ms.tgt_platform: multiple
keywords:
- ADSI recupero intervallo attributi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47f8787eb0b2aba30d1926b4d9cbb7e566e0f59c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955113"
---
# <a name="attribute-range-retrieval"></a>Recupero intervallo attributi

Un attributo multivalore può contenere quasi un numero qualsiasi di valori. In molti casi può essere vantaggioso, o addirittura necessario, limitare l'intervallo di valori recuperati da una query.

Il recupero di intervalli implica la richiesta di un numero limitato di valori di attributo in una singola query. Il numero di valori richiesti deve essere minore o uguale al numero massimo di valori supportati dal server. Per ridurre il numero di volte in cui la query deve contattare il server, il numero di valori richiesti dovrebbe essere il più vicino possibile al massimo possibile. Per consentire a un'applicazione di funzionare correttamente con tutti i server Windows, è necessario usare un numero massimo di 1000.

Gli identificatori di intervallo per una query di proprietà richiedono il formato seguente:


```C++
range=<low range>-<high range>
```



dove " &lt; intervallo minimo &gt; " è l'indice in base zero del primo valore della proprietà da recuperare e " &lt; intervallo elevato &gt; " è l'indice in base zero dell'ultimo valore della proprietà da recuperare. Per &lt; &gt; specificare la prima voce, viene utilizzato zero per "intervallo minimo". Il carattere jolly ( \* ) può essere usato per " &lt; intervallo elevato &gt; " per specificare tutte le voci rimanenti.

Nella tabella seguente sono elencati esempi di identificatori di intervallo.



| Esempio      | Descrizione                                                                                   |
|--------------|-----------------------------------------------------------------------------------------------|
| intervallo = 0-\*   | Recuperare tutti i valori delle proprietà. Questa operazione è soggetta ai limiti imposti dal server.                |
| intervallo = 0-500  | Recuperare da 1 a 501st valori inclusivi.                                                |
| intervallo = 2-3    | Recuperare i valori 3 e 4.                                                                  |
| intervallo = 501-\* | Recuperare 502nd e tutti i valori rimanenti. Questa operazione è soggetta ai limiti imposti dal server. |



 

Esistono diversi modi per recuperare un intervallo di valori di proprietà. Il metodo [**IADs. GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) può essere usato in un linguaggio di automazione o in C++. Il metodo **IADs. GetInfoEx** è il metodo preferito per eseguire il recupero di intervalli. Per ulteriori informazioni sull'utilizzo di **IADs. GetInfoEx** per il recupero di intervalli, vedere [utilizzo di IADs:: GetInfoEx per il recupero di intervalli](using-iads--getinfoex-for-range-retrieval.md).

Se viene utilizzato un linguaggio di automazione, è possibile utilizzare ADO (ActiveX Directory Objects) per recuperare un intervallo di valori di proprietà. Per ulteriori informazioni sull'utilizzo di ADO per il recupero di intervalli, vedere [utilizzo di ADO per il recupero di intervalli](using-ado-for-range-retrieval.md).

Se si usa C++, le interfacce [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) e [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) possono essere usate per recuperare un intervallo di valori di proprietà. Per altre informazioni sull'uso di **IDirectorySearch** e **IDirectoryObject** per il recupero di intervalli, vedere [uso di IDirectorySearch e IDirectoryObject per il recupero di intervalli](using-idirectorysearch-and-idirectoryobject-for-range-retrieval.md).

 

 




