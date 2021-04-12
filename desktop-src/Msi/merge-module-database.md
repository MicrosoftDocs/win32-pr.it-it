---
description: Il database di un modulo merge contiene tutte le proprietà di installazione e la logica di installazione per il modulo.
ms.assetid: 72e42392-54e6-4be8-9a43-04158552be3d
title: Database del modulo merge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74158e38d10b302c28520f6c1736e9cc6d823641
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347156"
---
# <a name="merge-module-database"></a>Database del modulo merge

Il database di un modulo merge contiene tutte le proprietà di installazione e la logica di installazione per il modulo. Si tratta essenzialmente di un [database di installazione](installer-database.md) semplificato o di un file con estensione msi. I file di database del modulo merge standard sono indicati da un'estensione MSM. Per un elenco di tutte le tabelle di database che possono esistere nei moduli merge, vedere [Merge Module Database Tables](merge-module-database-tables.md). Nel database di ogni file con estensione MSM sono necessarie le tabelle seguenti:

[Componente](component-table.md)

[Directory](directory-table.md)

[FeatureComponents](featurecomponents-table.md)

[File](file-table.md)

[ModuleSignature](modulesignature-table.md)

[ModuleComponents](modulecomponents-table.md)

Si noti che le tabelle Component, directory, FeatureComponents e file sono presenti anche in tutti i file con estensione msi. Un database del modulo merge non contiene una [tabella delle funzionalità](feature-table.md) e pertanto non è possibile installare il file con estensione MSM da solo. Per installare un modulo merge, è necessario innanzitutto eseguirne il merge utilizzando uno strumento di merge in un file con estensione msi.

La [tabella ModuleSignature](modulesignature-table.md) è presente solo nei file con estensione msi di cui è stato eseguito il merge con almeno un file. msm. Se questa tabella è presente in un file con estensione msi, contiene un record per ogni modulo merge precedentemente Unito al database di installazione.

I moduli merge possono contenere tabelle di sequenza MergeModule facoltative. Queste tabelle si verificano solo nei file con estensione MSM. Quando i file con estensione MSM vengono uniti in un file con estensione msi, queste tabelle modificano le [*tabelle di sequenza*](s-gly.md) delle azioni del file con estensione msi.

I moduli merge possono contenere tabelle personalizzate. Queste tabelle vengono utilizzate da [azioni personalizzate](custom-actions.md) definite nel modulo unione.

I moduli merge richiedono raramente tabelle dell'interfaccia utente. Queste tabelle devono essere presenti solo in rari casi in cui il modulo merge richiede l'input dell'utente durante l'installazione. Per ulteriori informazioni, vedere [creazione di interfacce utente nei moduli unione](authoring-user-interfaces-in-merge-modules.md).

 

 



