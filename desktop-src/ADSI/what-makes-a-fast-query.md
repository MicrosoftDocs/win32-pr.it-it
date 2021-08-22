---
title: Elementi che rendono una query veloce
description: Questo argomento elenca i metodi di programmazione preferiti da usare durante l'esecuzione di query su una directory.
ms.assetid: d96f330f-3c57-4edc-9fd2-970f908b54c2
ms.tgt_platform: multiple
keywords:
- Elementi che rendono ad ADSI una query veloce
- query ADSI , che cosa rende una query veloce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 134d391c728d543c407ee770081e2ced96afbba86d205462e814d89f74e82a57
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119589841"
---
# <a name="what-makes-a-fast-query"></a>Che cosa rende una query veloce?

Quando si esegue una query, considerare i concetti seguenti relativi al miglioramento delle prestazioni:

-   Se possibile, filtrare solo in base agli attributi indicizzati. Usare gli attributi dell'indice previsti genereranno il numero più limitato di riscontri. Per altre informazioni e un elenco completo degli attributi indicizzati per Windows, vedere [Schema di Active Directory](/windows/desktop/ADSchema/active-directory-schema).
-   Cercare **objectCategory anziché** **objectClass** perché **objectClass** non è una proprietà indicizzata.
-   Tenere presenti le segnalazioni. Provare a cercare nel catalogo globale se gli attributi sono elencati come replicati gc.
-   Evitare di cercare testo al centro e alla fine di una stringa. Ad esempio, "cn= \* collere \* " o "cn= \* larouse".
-   Si supponga che una ricerca nel sottoalbero restituirà un set di risultati di grandi dimensioni. Usare il paging quando si eseguono ricerche nel sottoalbero. Il server sarà quindi in grado di trasmettere un set di risultati di grandi dimensioni in blocchi riducendo le risorse di memoria sul lato server. In questo modo si riduce in modo efficace l'utilizzo della rete e si riduce la necessità di inviare blocchi di dati estremamente grandi in rete.
-   Impostare correttamente l'ambito delle ricerche in modo da non recuperare più del necessario.
-   Eseguire una ricerca complessa su più attributi, poiché le prestazioni sono inferiori rispetto all'esecuzione di più ricerche. Una ricerca di un oggetto che legge due attributi è più efficiente di due ricerche dello stesso oggetto, ognuna delle quali restituisce un attributo.
-   Per la lettura dell'attributo con un numero elevato di valori, usare i limiti di intervallo per ridurre al minimo le dimensioni della ricerca in modo da poter leggere alcune migliaia di membri alla volta. Per altre informazioni sulla specifica dei limiti dell'intervallo di attributi, vedere [Recupero di intervalli di attributi](attribute-range-retrieval.md).
-   L'associazione a un oggetto contiene l'handle di associazione per il resto della sessione. Non associare e annullare l'associazione per ogni chiamata. Se si usa ADO o OLE DB, non creare molti oggetti connessione.
-   Leggere una sola volta rootDSE e ricordarne il contenuto per il resto della sessione.

 

 