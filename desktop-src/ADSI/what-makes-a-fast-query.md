---
title: Che cosa esegue una query veloce
description: Questo argomento elenca i metodi di programmazione preferiti da usare durante l'esecuzione di query su una directory.
ms.assetid: d96f330f-3c57-4edc-9fd2-970f908b54c2
ms.tgt_platform: multiple
keywords:
- Che cosa fa una query ADSI rapida
- query ADSI, che cosa esegue una query veloce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 883db1e9de7b7b7a1179c814d6f66f774685083e
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103872958"
---
# <a name="what-makes-a-fast-query"></a>Che cosa esegue una query veloce?

Quando si esegue una query, tenere presenti i seguenti concetti di miglioramento delle prestazioni:

-   Se possibile, filtrare solo sugli attributi indicizzati. Usare gli attributi di indice che si prevede genereranno il minor numero di riscontri. Per ulteriori informazioni e per un elenco completo degli attributi indicizzati per Windows, vedere [Active Directory schema](/windows/desktop/ADSchema/active-directory-schema).
-   Eseguire la ricerca in **objectCategory** anziché in **objectClass** perché **objectClass** non è una proprietà indicizzata.
-   Tenere presente i riferimenti. Se gli attributi sono elencati come GC replicati, provare a eseguire ricerche nel catalogo globale.
-   Evitare la ricerca di testo al centro e alla fine di una stringa. Ad esempio, "CN = \* Hille \* " o "CN = \* Larouse".
-   Si supponga che una ricerca del sottoalbero restituisca un set di risultati di grandi dimensioni. Usare il paging quando si eseguono ricerche di sottoalbero. Il server sarà quindi in grado di trasmettere un set di risultati di grandi dimensioni in blocchi riducendo le risorse di memoria sul lato server. Questo semplifica l'utilizzo della rete e riduce la necessità di inviare blocchi di dati molto grandi sulla rete.
-   Definire correttamente l'ambito delle ricerche in modo da non recuperare più di quanto necessario.
-   Eseguire una ricerca complessa su più attributi, perché si tratta di una riduzione delle prestazioni più elevata rispetto all'esecuzione di più ricerche. Una ricerca di un oggetto che legge due attributi è più efficiente di due ricerche per lo stesso oggetto, ognuno dei quali restituisce un attributo.
-   Per leggere l'attributo con un numero elevato di valori, usare i limiti di intervallo per ridurre al minimo le dimensioni di ricerca in modo da poter leggere alcune migliaia di membri alla volta. Per ulteriori informazioni su come specificare i limiti dell'intervallo di attributi, vedere [recupero di intervalli di attributi](attribute-range-retrieval.md).
-   Eseguire l'associazione a un oggetto per il resto della sessione. Non associare e annullare il binding per ogni chiamata. Se si utilizza ADO o OLE DB, non creare molti oggetti connessione.
-   Leggere il rootDSE una volta e ricordarne il contenuto per il resto della sessione.

 

 