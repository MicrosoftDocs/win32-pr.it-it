---
description: Il mapping dei file è l'associazione del contenuto di un file a una parte dello spazio degli indirizzi virtuali di un processo.
ms.assetid: 86a8bc81-914d-46a2-99fd-65dfd03bbcdd
title: File Mapping
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8efa02b7de4565adc6ec9cc4c252a7b3114169f1897a2950340a492035409008
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067856"
---
# <a name="file-mapping"></a>File Mapping

*Il mapping* dei file è l'associazione del contenuto di un file a una parte dello spazio degli indirizzi virtuali di un processo. Il sistema crea un *oggetto di mapping dei file* (noto anche come oggetto *sezione*) per mantenere questa associazione. Una *visualizzazione file* è la parte dello spazio di indirizzi virtuali utilizzata da un processo per accedere al contenuto del file. Il mapping dei file consente al processo di usare sia input e output casuali (I/O) che operazioni di I/O sequenziali. Consente inoltre al processo di funzionare in modo efficiente con un file di dati di grandi dimensioni, ad esempio un database, senza dover eseguire il mapping dell'intero file in memoria. Più processi possono anche usare file mappati alla memoria per condividere i dati.

I processi leggono e scrivono nella visualizzazione file usando puntatori, proprio come farebbe con la memoria allocata dinamicamente. L'uso del mapping dei file migliora l'efficienza perché il file si trova su disco, ma la visualizzazione file risiede in memoria. I processi possono anche modificare la visualizzazione file con la [**funzione VirtualProtect.**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotect)

Nella figura seguente viene illustrata la relazione tra il file su disco, un oggetto di mapping dei file e una visualizzazione file.

![relazione tra il file su disco, un oggetto di mapping dei file e una visualizzazione file.](images/fmap.png)

Il file su disco può essere qualsiasi file di cui si vuole eseguire il mapping in memoria oppure può essere il file di pagina di sistema. L'oggetto mapping di file può essere costituito da una parte o da una parte del file. È supportato dal file su disco. Ciò significa che quando il sistema scambia le pagine dell'oggetto mapping file, tutte le modifiche apportate all'oggetto mapping file vengono scritte nel file. Quando le pagine dell'oggetto mapping file vengono scambiate nuovamente, vengono ripristinate dal file.

Una visualizzazione file può essere costituita da tutta o solo una parte dell'oggetto mapping file. Un processo modifica il file tramite le visualizzazioni file. Un processo può creare più visualizzazioni per un oggetto di mapping file. Le viste file create da ogni processo si trovano nello spazio degli indirizzi virtuali di tale processo. Quando il processo richiede dati da una parte del file diversa da quella presente nella visualizzazione file corrente, può annullare il mapping della visualizzazione file corrente e quindi creare una nuova visualizzazione file.

Quando più processi usano lo stesso oggetto di mapping dei file per creare viste per un file locale, i dati sono coerenti. In altre informazioni, le viste contengono copie identiche del file su disco. Il file non può risiedere in un computer remoto se si vuole condividere la memoria tra più processi.

Per altre informazioni, vedere i seguenti argomenti:

-   [Creazione di un oggetto mapping file](creating-a-file-mapping-object.md)
-   [Creazione di una visualizzazione file](creating-a-file-view.md)
-   [Condivisione di file e memoria](sharing-files-and-memory.md)
-   [Lettura e scrittura da una visualizzazione file](reading-and-writing-from-a-file-view.md)
-   [Chiusura di un oggetto mapping file](closing-a-file-mapping-object.md)
-   [Sicurezza e diritti di accesso per il mapping dei file](file-mapping-security-and-access-rights.md)
-   [Uso del mapping dei file](using-file-mapping.md)

 

 
