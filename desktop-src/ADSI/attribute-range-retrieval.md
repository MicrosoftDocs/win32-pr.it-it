---
title: Recupero dell'intervallo di attributi
description: Un attributo multivalore può avere quasi qualsiasi numero di valori. In molti casi, può essere vantaggioso, o addirittura necessario, limitare l'intervallo di valori recuperati da una query.
ms.assetid: 3a0eb764-fca9-4ca6-9991-b85f293961af
ms.tgt_platform: multiple
keywords:
- Recupero di intervalli di attributi ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 994b1c4535ebce264386b088a53b730e679147f07b4bef9fe99d3a45a63461fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117840578"
---
# <a name="attribute-range-retrieval"></a>Recupero dell'intervallo di attributi

Un attributo multivalore può avere quasi qualsiasi numero di valori. In molti casi, può essere vantaggioso, o addirittura necessario, limitare l'intervallo di valori recuperati da una query.

Il recupero di intervalli comporta la richiesta di un numero limitato di valori di attributo in una singola query. Il numero di valori richiesti deve essere minore o uguale al numero massimo di valori supportati dal server. Per ridurre il numero di volte in cui la query deve contattare il server, il numero di valori richiesti deve essere il più vicino possibile a questo valore massimo. Per consentire a un'applicazione di funzionare correttamente con Windows server, è necessario usare un numero massimo di 1000.

Gli identificatori di intervallo per una query di proprietà richiedono il formato seguente:


```C++
range=<low range>-<high range>
```



dove " low range " è l'indice in base zero del primo valore della proprietà da recuperare e " high range " è l'indice in base zero dell'ultimo valore &lt; &gt; della proprietà da &lt; &gt; recuperare. Zero viene usato per " &lt; low range " per specificare la prima &gt; voce. Il carattere jolly ( \* ) può essere usato per " intervallo elevato " per specificare tutte le voci &lt; &gt; rimanenti.

Nella tabella seguente sono elencati esempi di identificatori di intervallo.



| Esempio      | Descrizione                                                                                   |
|--------------|-----------------------------------------------------------------------------------------------|
| range=0-\*   | Recuperare tutti i valori delle proprietà. Questo è soggetto ai limiti imposti dal server.                |
| range=0-500  | Recuperare dal primo al 501° valore in modo inclusivo.                                                |
| range=2-3    | Recuperare il terzo e il 4° valore.                                                                  |
| range=501-\* | Recuperare il 502° e tutti i valori rimanenti. Questo è soggetto ai limiti imposti dal server. |



 

Esistono diversi modi per recuperare un intervallo di valori di proprietà. Il [**metodo IADs.GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) può essere usato in un linguaggio di automazione o in C++. Il **metodo IADs.GetInfoEx** è il metodo preferito per eseguire il recupero dell'intervallo. Per altre informazioni **sull'uso di IADs.GetInfoEx** per il recupero di intervalli, vedere [Using IADs::GetInfoEx for Range Retrieval](using-iads--getinfoex-for-range-retrieval.md).

Se si usa un linguaggio di automazione, ActiveX Directory Objects (ADO) può essere usato per recuperare un intervallo di valori di proprietà. Per altre informazioni sull'uso di ADO per il recupero di intervalli, vedere [Uso di ADO per il recupero di intervalli](using-ado-for-range-retrieval.md).

Se si usa C++, è possibile usare le [**interfacce IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) e [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) per recuperare un intervallo di valori di proprietà. Per altre informazioni sull'uso **di IDirectorySearch** e **IDirectoryObject** per il recupero di intervalli, vedere [Uso di IDirectorySearch e IDirectoryObject per il recupero di intervalli.](using-idirectorysearch-and-idirectoryobject-for-range-retrieval.md)

 

 




