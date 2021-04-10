---
description: Quando un modulo viene unito a un database con una lingua predefinita diversa, potrebbe essere necessario che lo strumento di merge applichi una trasformazione del linguaggio al modulo per fornire la lingua finale. Per ulteriori informazioni, vedere la pagina relativa ai moduli merge con più lingue.
ms.assetid: 51e8774e-f358-423f-a283-ad7beeabbbdb
title: Creazione di una trasformazione lingua per un modulo merge a più lingue
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 970c8908ddbf89e31f0fc7a415358bb887f0838e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227207"
---
# <a name="authoring-a-language-transform-for-a-multiple-language-merge-module"></a>Creazione di una trasformazione lingua per un modulo merge a più lingue

Quando un modulo viene unito a un database con una lingua predefinita diversa, potrebbe essere necessario che lo strumento di merge applichi una trasformazione del linguaggio al modulo per fornire la lingua finale. Per ulteriori informazioni, vedere la pagina relativa ai [moduli merge con più lingue](multiple-language-merge-modules.md).

Le trasformazioni del linguaggio vengono archiviate nel file con estensione MSM del modulo e devono avere il nome e il formato: MergeModule. lang \# \# \# \# . L'oggetto \# \# \# \# rappresenta l' [LangID](localizing-the-error-and-actiontext-tables.md) a quattro cifre della lingua finale. Ad esempio, MergeModule. Lang1033, MergeModule. Lang9 e MergeModule. Lang0 per le trasformazioni in inglese (Stati Uniti), inglese mondiale e lingua indipendente dalla lingua. Queste sono le stesse [trasformazioni incorporate](embedded-transforms.md) ed è possibile aggiungerle alle sottoarchiviazioni nel file. msm.

La trasformazione lingua deve eseguire le operazioni seguenti:

-   Modificare la lingua predefinita nella colonna lingua della [tabella ModuleSignature](modulesignature-table.md) nella nuova lingua del modulo.
-   Modificare la lingua predefinita nella colonna lingua della [tabella ModuleComponents](modulecomponents-table.md) nella nuova lingua del modulo. La trasformazione può aggiungere o rimuovere righe dalla tabella.
-   Se necessario, modificare la lingua nella colonna RequiredLanguage o aggiungere o eliminare righe nella [tabella ModuleDependency](moduledependency-table.md).
-   Se necessario, modificare la lingua nella colonna ExcludedLanguage o aggiungere o eliminare righe nella [tabella ModuleExclusion](moduleexclusion-table.md).
-   La trasformazione può eseguire qualsiasi operazione di trasformazione valida sul modulo, inclusa l'aggiunta o la rimozione di componenti, file, voci del registro di sistema o azioni.

Si noti che l'applicazione di una trasformazione lingua quando si apre il modulo non modifica la lingua predefinita o le lingue supportate dal modulo, ma solo modifica la lingua richiesta. Quindi, la proprietà di [**Riepilogo del modello**](template-summary.md) non cambia, dovrebbe già elencare tutte le lingue supportate dal modulo con la lingua predefinita elencata per prima.

Tutti i file necessari per tutte le trasformazioni di linguaggio possibili vengono in genere archiviati in un unico file cab incluso con il modulo. Poiché non è pratico che la trasformazione del linguaggio modifichi questo file CAB, è preferibile usare una sequenza di file globale nel file CAB, nella [tabella dei file](file-table.md)e nella trasformazione della lingua. Per informazioni dettagliate, vedere [ordinamento della sequenza di file nel file CAB di un modulo di merge a più lingue](ordering-the-file-sequence-in-the-cab-of-a-multiple-language-merge-module.md)

 

 



