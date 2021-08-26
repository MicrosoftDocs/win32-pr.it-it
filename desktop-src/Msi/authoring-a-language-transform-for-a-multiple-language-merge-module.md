---
description: Quando un modulo viene unito in un database con una lingua predefinita diversa, potrebbe essere necessario applicare una trasformazione del linguaggio al modulo per fornire il linguaggio finale. Per altre informazioni, vedere Multiple Language Merge Modules.
ms.assetid: 51e8774e-f358-423f-a283-ad7beeabbbdb
title: Creazione di una trasformazione del linguaggio per un modulo unione in più lingue
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cf9a9c2294d310959bcd82f13010c88eb513e40ad4536c4dbca61e50d260873
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078061"
---
# <a name="authoring-a-language-transform-for-a-multiple-language-merge-module"></a>Creazione di una trasformazione del linguaggio per un modulo unione in più lingue

Quando un modulo viene unito in un database con una lingua predefinita diversa, potrebbe essere necessario applicare una trasformazione del linguaggio al modulo per fornire il linguaggio finale. Per altre informazioni, vedere [Multiple Language Merge Modules](multiple-language-merge-modules.md).

Le trasformazioni del linguaggio vengono archiviate nel file con estensione msm del modulo e devono avere il nome e il formato: MergeModule.Lang \# \# \# \# . rappresenta \# \# \# \# l'LANGID fino a [quattro](localizing-the-error-and-actiontext-tables.md) cifre della lingua finale. Ad esempio, MergeModule.Lang1033, MergeModule.Lang9 e MergeModule.Lang0 per le trasformazioni in inglese stati Uniti, inglese mondiale e lingua neutra. Sono uguali alle trasformazioni [incorporate ed](embedded-transforms.md) è possibile aggiungerle alle risorse di archiviazione secondarie nel file con estensione msm.

La trasformazione del linguaggio deve eseguire le operazioni seguenti:

-   Modificare la lingua predefinita nella colonna Lingua della [tabella ModuleSignature](modulesignature-table.md) con la nuova lingua del modulo.
-   Modificare la lingua predefinita nella colonna Lingua della [tabella ModuleComponents](modulecomponents-table.md) nel nuovo linguaggio del modulo. La trasformazione può aggiungere o rimuovere righe da questa tabella.
-   Se necessario, modificare la lingua nella colonna RequiredLanguage oppure aggiungere o eliminare righe nella [tabella ModuleDependency](moduledependency-table.md).
-   Se necessario, modificare la lingua nella colonna ExcludedLanguage oppure aggiungere o eliminare righe nella [tabella ModuleExclusion](moduleexclusion-table.md).
-   La trasformazione può eseguire qualsiasi operazione di trasformazione valida nel modulo, inclusa l'aggiunta o la rimozione di componenti, file, voci del Registro di sistema o azioni.

Si noti che l'applicazione di una trasformazione del linguaggio all'apertura del modulo non modifica la lingua predefinita o le lingue supportate dal modulo, ma solo la lingua richiesta. Di [**conseguenza, la**](template-summary.md) proprietà Riepilogo modelli non cambia, ma dovrebbe già elencare tutte le lingue supportate dal modulo con la lingua predefinita elencata per prima.

Tutti i file necessari per tutte le possibili trasformazioni del linguaggio vengono comunemente archiviati in un singolo file CAB incluso nel modulo. Poiché non è pratico fare in modo che la trasformazione del linguaggio modififi questo file CAB, è meglio usare una sequenza di file globale nel file CAB, nella tabella [File](file-table.md)e nella trasformazione del linguaggio. Per informazioni dettagliate, [vedere Ordinamento della sequenza di file nel file CAB di un modulo unione in più lingue](ordering-the-file-sequence-in-the-cab-of-a-multiple-language-merge-module.md)

 

 



