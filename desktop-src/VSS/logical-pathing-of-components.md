---
description: Il percorso logico viene usato per organizzare i componenti gestiti da un writer in gruppi ben definiti.
ms.assetid: 663c8ca9-8f5b-48bd-af2d-b2d90de9e492
title: Percorso logico dei componenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2ce4feeeb2147a7be736547eb69cbbb1a254c5940b18e904bc3be3290a2c79b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119767751"
---
# <a name="logical-pathing-of-components"></a>Percorso logico dei componenti

[*Il percorso logico*](vssgloss-l.md) viene usato per organizzare i componenti gestiti da un writer in gruppi ben definiti.

Il percorso logico è analogo nella struttura al percorso di file tradizionale, usando la barra rovesciata " " per \\ separare gli elementi nel percorso. A differenza dei percorsi di file, la radice di un percorso logico è **NULL** anziché " \\ ".

Il percorso logico viene espresso come **stringa con** terminazione NULL e non esistono altre restrizioni sui caratteri che il percorso può contenere.

L'uso più importante del percorso logico è la definizione di set di componenti [*,*](vssgloss-c.md)in cui l'inclusione esplicita del componente [*in*](vssgloss-e.md) un'operazione di backup o ripristino di un componente selezionabile richiede l'inclusione di un numero di altri componenti ([*sottocomponente*](vssgloss-s.md)). Il percorso logico del componente di definizione di un set di componenti è un elemento padre dei percorsi logici dei relativi sottocomponenti e:

-   I sottocomponenti devono condividere come percorso radice il percorso logico del componente selezionabile che definisce il set di componenti.
-   Un percorso radice **null** è valido.
-   Il nome del componente selezionabile di definizione deve essere il primo elemento di percorso logico dopo il percorso radice per ogni sottocomponente non selezionabile del set di componenti.
-   I set di componenti possono essere annidati.
-   La combinazione di percorso logico e nome del componente deve essere univoca in tutte le istanze di una classe [*writer.*](vssgloss-w.md)

L'ipotetico esempio di un writer *MyWriter* con una struttura di percorso logico definita di seguito illustra il percorso logico.



| Nome componente | Percorso logico            | Selezionabile per il backup |
|----------------|-------------------------|-----------------------|
| "Eseguibili"  | ""                      | N                     |
| "ConfigFiles"  | "Eseguibili"           | N                     |
| "LicenseInfo"  | ""                      | S                     |
| "Security"     | ""                      | S                     |
| "UserInfo"     | "Security"              | N                     |
| "Certificati" | "Security"              | N                     |
| "writerData"   | ""                      | S                     |
| "Set1"         | "writerData"            | N                     |
| "Jan"          | "writerData \\ Set1"      | N                     |
| "Dec"          | "writerData \\ Set1"      | N                     |
| "Set2"         | "writerData"            | N                     |
| "Jan"          | "writerData \\ Set2"      | N                     |
| "Dec"          | "writerData \\ Set2"      | N                     |
| "Query"        | "writerData \\ QueryLogs" | N                     |
| "Utilizzo"        | "writerData"            | S                     |
| "Jan"          | "writerData \\ Usage"     | N                     |
| "Dec"          | "writerData \\ Usage"     | N                     |



 

Si noti che i componenti "Eseguibili" e "ConfigFile" hanno una relazione padre-figlio, ma entrambi non sono selezionabili. Pertanto, non formano un set di componenti. Ogni volta che viene *eseguito* il backup o il ripristino del writer, questi due componenti devono essere inclusi in [*modo esplicito*](vssgloss-e.md) nell'operazione.

Il componente "LicenseInfo" è selezionabile senza predecessori né discendenti. Può essere incluso in modo esplicito o meno in un'operazione di backup o ripristino a discrezione del richiedente.

Il componente "Security" definisce un semplice set di componenti, che non contiene set di componenti sottostanti.

Il componente "writerData" definisce un set di componenti, che contiene una raccolta complessa di componenti con diverse gerarchie di percorsi logici ben definite al suo interno.

Un sottocomponente, "Usage", è selezionabile e definisce un set di componenti.

Diversi componenti hanno lo stesso nome e si distinguono per i relativi percorsi logici. Le istanze dei componenti non selezionabili "Dec" e "Jan" sono presenti nei componenti non selezionabili "Set1" e "Set2" e nel sottocomponente selezionabile "Usage".

Se il componente "writerData" è incluso in modo esplicito in un backup o un ripristino, tutti i relativi sottocomponenti, anche quelli nel set di componenti annidato definito da "Usage", verranno inclusi [*implicitamente*](vssgloss-e.md)[](vssgloss-i.md) nell'operazione.

Se il set di componenti definito da "writerData" non è incluso in modo esplicito in un backup o ripristino, i componenti "Set1", "Set2" e "QueryLogs" (e le relative istanze dei sottocomponenti "Dec" e "Jan") non verranno inclusi in modo implicito nell'operazione di backup o ripristino.

Tuttavia, anche se "writerData" non è incluso nell'operazione, il componente "Usage" è ancora selezionabile e può comunque essere incluso in modo esplicito in un'operazione di backup o ripristino. In caso contrario, i relativi sottocomponenti "Jan" e "Dec" verranno inclusi in modo implicito.

Altri punti degni di nota:

-   I componenti selezionabili "LicenseInfo" e "writerData" e il componente non selezionabile "Executables" sono tutti allo stesso livello nella gerarchia dei percorsi logici di *MyWriter:* tutti hanno lo stesso percorso logico **NULL** o "", il percorso logico radice.
-   Il componente selezionabile "Usage" non deve mai essere incluso in modo esplicito in un backup, se il relativo elemento padre selezionabile ("writerData") è incluso in modo esplicito in un'operazione di backup o ripristino.
-   I componenti che definiscono i set di componenti possono esistere solo per motivi organizzativi. Ad esempio, il componente "writerData" o "Usage" o entrambi potrebbero essere vuoti. in altri termini, non sono stati aggiunti set di [*file*](vssgloss-f.md) usando il metodo [**IVssCreateWriterMetadata::AddFilesToFileGroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup), [**IVssCreateWriterMetadata::AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles) o [**IVssCreateWriterMetadata::AddDatabaseLogFiles.**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles) I componenti definiscono comunque un set di componenti.

 

 



