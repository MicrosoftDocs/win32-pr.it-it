---
description: Il mapping dei file è l'associazione del contenuto di un file a una parte dello spazio degli indirizzi virtuali di un processo.
ms.assetid: 86a8bc81-914d-46a2-99fd-65dfd03bbcdd
title: Mapping dei file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7f49162a4545d0e087e6b291e429d89049dbf57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526370"
---
# <a name="file-mapping"></a>Mapping dei file

Il *mapping dei file* è l'associazione del contenuto di un file a una parte dello spazio degli indirizzi virtuali di un processo. Il sistema crea un *oggetto di mapping dei file* (noto anche come *oggetto sezione*) per mantenere questa associazione. Una *visualizzazione file* è la parte dello spazio degli indirizzi virtuali utilizzata da un processo per accedere al contenuto del file. Il mapping dei file consente al processo di utilizzare l'input e l'output (I/O) casuali e l'I/O sequenziale. Consente inoltre di usare in modo efficiente il processo con un file di dati di grandi dimensioni, ad esempio un database, senza dover eseguire il mapping dell'intero file in memoria. Più processi possono anche usare file mappati alla memoria per condividere i dati.

Elabora le letture e le Scritture nella visualizzazione file usando i puntatori, così come farebbero con la memoria allocata in modo dinamico. L'uso del mapping dei file migliora l'efficienza perché il file risiede sul disco, ma la visualizzazione file risiede in memoria. I processi possono anche modificare la visualizzazione file con la funzione [**VirtualProtect**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotect) .

Nella figura seguente viene illustrata la relazione tra il file su disco, un oggetto mapping di file e una visualizzazione file.

![relazione tra il file su disco, un oggetto mapping di file e una visualizzazione file.](images/fmap.png)

Il file su disco può essere un file di cui si desidera eseguire il mapping in memoria oppure il file di paging di sistema. L'oggetto di mapping dei file può essere costituito solo da parte del file. È supportato dal file su disco. Ciò significa che quando il sistema scambia le pagine dell'oggetto mapping di file, tutte le modifiche apportate all'oggetto mapping dei file vengono scritte nel file. Quando le pagine dell'oggetto mapping dei file vengono nuovamente scambiate, vengono ripristinate dal file.

Una visualizzazione file può essere costituita solo da parte dell'oggetto mapping di file. Un processo modifica il file tramite le visualizzazioni di file. Un processo può creare più visualizzazioni per un oggetto mapping di file. Le visualizzazioni di file create da ogni processo si trovano nello spazio degli indirizzi virtuale del processo. Quando il processo richiede dati da una parte del file diversa da quella presente nella visualizzazione file corrente, può annullare la visualizzazione file corrente, quindi creare una nuova visualizzazione file.

Quando più processi utilizzano lo stesso oggetto mapping di file per creare visualizzazioni per un file locale, i dati sono coerenti. Ovvero le visualizzazioni contengono copie identiche del file su disco. Il file non può risiedere in un computer remoto se si desidera condividere la memoria tra più processi.

Per altre informazioni, vedere i seguenti argomenti:

-   [Creazione di un oggetto di mapping dei file](creating-a-file-mapping-object.md)
-   [Creazione di una visualizzazione file](creating-a-file-view.md)
-   [Condivisione di file e memoria](sharing-files-and-memory.md)
-   [Lettura e scrittura da una visualizzazione file](reading-and-writing-from-a-file-view.md)
-   [Chiusura di un oggetto di mapping dei file](closing-a-file-mapping-object.md)
-   [Diritti di accesso e sicurezza per il mapping dei file](file-mapping-security-and-access-rights.md)
-   [Uso del mapping dei file](using-file-mapping.md)

 

 
