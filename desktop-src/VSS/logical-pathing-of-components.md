---
description: Il percorso logico viene usato per organizzare i componenti gestiti da un writer in gruppi ben definiti.
ms.assetid: 663c8ca9-8f5b-48bd-af2d-b2d90de9e492
title: Percorso logico dei componenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a591f3eec0e00257740dbbd24ab7c609c53c27a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310696"
---
# <a name="logical-pathing-of-components"></a>Percorso logico dei componenti

Il [*percorso logico*](vssgloss-l.md) viene usato per organizzare i componenti gestiti da un writer in gruppi ben definiti.

Il percorso logico è analogo nella struttura al percorso tradizionale dei file, usando la barra rovesciata " \\ " per separare gli elementi del percorso. A differenza dei percorsi di file, la radice di un percorso logico è **null**, anziché " \\ ".

Il percorso logico è espresso come stringa con terminazione **null** e non esistono altre restrizioni sui caratteri che il percorso può contenere.

L'utilizzo più importante dei percorsi logici è la definizione dei [*set di componenti*](vssgloss-c.md), in cui l' [*inclusione esplicita del componente*](vssgloss-e.md) in un'operazione di backup o ripristino di un componente selezionabile richiede l'inclusione di un numero di altri componenti ([*sottocomponente*](vssgloss-s.md)). Il percorso logico del componente di definizione di un set di componenti è un elemento padre per i percorsi logici dei relativi sottocomponenti e:

-   I sottocomponenti devono condividere come percorso radice il percorso logico del componente selezionabile che definisce il set di componenti.
-   Un percorso radice **null** è valido.
-   Il nome del componente selezionabile che definisce deve essere il primo elemento del percorso logico dopo il percorso radice per ogni sottocomponente non selezionabile del set di componenti.
-   I set di componenti possono essere annidati.
-   La combinazione di percorso logico e nome del componente deve essere univoca in tutte le istanze di una [*classe Writer*](vssgloss-w.md).

L'esempio ipotetico di un writer di *scrittura* con una struttura di percorso logica definita di seguito illustra il percorso logico.



| Nome componente | Percorso logico            | Selezionabile per il backup |
|----------------|-------------------------|-----------------------|
| Eseguibili  | ""                      | N                     |
| "ConfigFiles"  | Eseguibili           | N                     |
| LicenseInfo  | ""                      | S                     |
| "Security"     | ""                      | S                     |
| UserInfo     | "Security"              | N                     |
| Certificati | "Security"              | N                     |
| "writerData"   | ""                      | S                     |
| Set1         | "writerData"            | N                     |
| Jan          | "writerData \\ set1"      | N                     |
| Dec          | "writerData \\ set1"      | N                     |
| Set2         | "writerData"            | N                     |
| Jan          | "writerData \\ set2"      | N                     |
| Dec          | "writerData \\ set2"      | N                     |
| Query        | "writerData \\ QueryLogs" | N                     |
| Utilizzo        | "writerData"            | S                     |
| Jan          | " \\ utilizzo writerData"     | N                     |
| Dec          | " \\ utilizzo writerData"     | N                     |



 

Si noti che i componenti "Executables" e "ConfigFile" hanno una relazione padre-figlio, ma entrambi non sono selezionabili. Pertanto, non formano un set di componenti. Ogni volta che viene eseguito il backup o il ripristino del *writeback* del writer, questi due componenti dovranno essere [*inclusi in modo esplicito*](vssgloss-e.md) nell'operazione.

Il componente "LicenseInfo" può essere selezionato senza predecessore né discendente. Può essere incluso o meno in modo esplicito in un'operazione di backup o ripristino a discrezione del richiedente.

Il componente "sicurezza" definisce un set di componenti semplice, che non contiene alcun set di componenti al di sotto di esso.

Il componente "writerData" definisce un set di componenti che contiene una raccolta complessa di componenti con diverse gerarchie di percorsi logici ben definite al di sotto di esso.

Un sottocomponente, "Usage", è selezionabile e definisce un set di componenti.

Molti componenti hanno lo stesso nome e sono distinti in base ai relativi percorsi logici. Le istanze dei componenti non selezionabili "Dec" e "Jan" sono disponibili nei componenti non selezionabili "set1" e "set2" e nel sottocomponente selezionabile "Usage".

Se il componente "writerData" è incluso in modo esplicito in un backup o un ripristino, tutti i relativi sottocomponenti, anche quelli nel set di componenti annidato definito da "Usage", [*verranno inclusi in*](vssgloss-e.md)[*modo implicito nell'operazione*](vssgloss-i.md) .

Se il set di componenti definito da "writerData" non è incluso in modo esplicito in un backup o un ripristino, i componenti "set1", "set2" e "QueryLogs" (e le relative istanze dei sottocomponenti "Dec" e "Jan") non verranno inclusi in modo implicito nell'operazione di backup o ripristino.

Tuttavia, anche se "writerData" non è incluso nell'operazione, il componente "Usage" è ancora selezionabile e può comunque essere incluso in modo esplicito in un'operazione di backup o ripristino. In caso contrario, i relativi sottocomponenti "Jan" e "Dec" verranno inclusi in modo implicito.

Altri punti degni di Nota:

-   I componenti selezionabili "LicenseInfo" e "writerData" e i "eseguibili" del componente non selezionabile sono tutti allo stesso livello nella gerarchia dei percorsi logici di *writer*, ovvero tutti hanno lo stesso percorso logico **null** o "", il percorso logico radice.
-   Il componente selezionabile "Usage" non deve mai essere incluso in modo esplicito in un backup, se il padre selezionabile ("writerData") è incluso in modo esplicito in un'operazione di backup o ripristino.
-   I componenti che definiscono i set di componenti possono esistere semplicemente per motivi organizzativi. Ad esempio, il componente "writerData" o "Usage", o entrambi, potrebbe essere vuoto. ovvero, non è stato aggiunto alcun [*set di file*](vssgloss-f.md) usando il metodo [**IVssCreateWriterMetadata:: AddFilesToFileGroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup), [**IVssCreateWriterMetadata:: AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles) o [**IVssCreateWriterMetadata:: AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles) . I componenti definiscono ancora un set di componenti.

 

 



