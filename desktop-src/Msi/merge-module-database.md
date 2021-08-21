---
description: Il database di un modulo unione contiene tutte le proprietà di installazione e la logica di installazione per il modulo.
ms.assetid: 72e42392-54e6-4be8-9a43-04158552be3d
title: Merge Module Database
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fb75614218e7464879f62ea1527245e36d65d1dc14f19a9b82a13a893997f1c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117804603"
---
# <a name="merge-module-database"></a>Merge Module Database

Il database di un modulo unione contiene tutte le proprietà di installazione e la logica di installazione per il modulo. Si tratta essenzialmente di un database del [programma di installazione semplificato](installer-database.md) o .msi file. I file di database del modulo unione standard sono indicati da un'estensione msm. Per un elenco di tutte le tabelle di database che possono esistere nei moduli unione, vedere [Merge Module Database Tables](merge-module-database-tables.md). Nel database di ogni file con estensione msm sono necessarie le tabelle seguenti:

[Componente](component-table.md)

[Directory](directory-table.md)

[FeatureComponents](featurecomponents-table.md)

[File](file-table.md)

[ModuleSignature](modulesignature-table.md)

[ModuleComponents](modulecomponents-table.md)

Si noti che le tabelle Component, Directory, FeatureComponents e File sono presenti anche in tutti .msi file. Un database del modulo unione non contiene una [tabella di funzionalità](feature-table.md) e pertanto il file con estensione msm non può essere installato da solo. Per installare un modulo unione, è necessario innanzitutto eseguire il merge di un modulo in un file .msi merge.

La [tabella ModuleSignature](modulesignature-table.md) è presente solo in .msi file uniti con almeno un file con estensione msm. Se questa tabella è presente in un file .msi, contiene un record per ogni modulo di merge unito in precedenza al database di installazione.

I moduli unione possono contenere tabelle di sequenza MergeModule facoltative. Queste tabelle si verificano solo nei file con estensione msm. Quando i file con estensione msm vengono uniti in un file [](s-gly.md) .msi, queste tabelle modificano le tabelle della sequenza di azioni del file .msi.

I moduli unione possono contenere tabelle personalizzate. Queste tabelle vengono usate [dalle azioni personalizzate](custom-actions.md) definite nel modulo merge.

I moduli unione richiedono raramente tabelle dell'interfaccia utente. Queste tabelle devono essere presenti solo nei rari casi in cui il modulo merge richiede l'input dell'utente durante l'installazione. Per altre informazioni, vedere [Creazione di interfacce utente nei moduli unione.](authoring-user-interfaces-in-merge-modules.md)

 

 



