---
description: Nella procedura riportata di seguito vengono descritti i passaggi generali per la creazione di moduli unione.
ms.assetid: 4b3871c0-f452-4935-9ee3-78b0ac847e67
title: Creazione di moduli unione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ece67151872a8d065d321c6adaae660be643ad8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227205"
---
# <a name="authoring-merge-modules"></a>Creazione di moduli unione

Nella procedura riportata di seguito vengono descritti i passaggi generali per la creazione di moduli unione.

**Per creare un nuovo modulo merge**

1.  Ottenere uno strumento software che è possibile utilizzare per modificare il database del modulo merge.
2.  Ottenere un database del modulo merge vuoto.
3.  Generare un [GUID](guid.md) per il modulo unione. È necessario utilizzare questo GUID quando si creano le chiavi primarie delle tabelle di database nel modulo merge.
4.  Aggiungere un record alla [tabella dei componenti](component-table.md) per ogni componente recapitato dall'Unione. In ogni modulo merge è necessaria una tabella di componenti. Si noti che i moduli merge operano con i componenti e non con le funzionalità di. In alcuni casi, tuttavia, potrebbe essere necessario che una voce della tabella di database faccia riferimento a una funzionalità. Per informazioni dettagliate, vedere [riferimento alle funzionalità nei moduli unione](referencing-features-in-merge-modules.md).
5.  Aggiungere una [tabella di directory](directory-table.md) al modulo merge che specifica il layout delle directory che il modulo merge aggiunge al database di destinazione. In ogni modulo merge è necessaria una tabella di directory.
6.  Importare una [tabella FeatureComponents](featurecomponents-table.md) vuota nel database del modulo merge. Questa tabella vuota fornisce linee guida per lo strumento di merge nei casi in cui il file con estensione msi non contiene la propria tabella FeatureComponents.
7.  Raccogliere tutti i file recapitati da questo modulo merge e creare il file CAB [MergeModule.CABinet](mergemodule-cabinet.md) . Aggiungere il file CAB al modulo merge come flusso all'interno del file. msm.
8.  Aggiungere un record alla tabella file per ogni file archiviato in MergeModule.CABinet.
9.  Aggiungere le informazioni necessarie per identificare il modulo merge nella [tabella ModuleSignature](modulesignature-table.md). Ogni modulo merge richiede una tabella ModuleSignature.
10. Elenca i componenti del modulo merge nella [tabella ModuleComponents](modulecomponents-table.md). Ogni modulo merge richiede una tabella ModuleComponents.
11. Aggiungere le tabelle di sequenza dei moduli merge al file MSM solo se il modulo merge deve modificare le [*tabelle di sequenza*](s-gly.md) del database di installazione di destinazione.
12. Aggiungere una \_ tabella di convalida al modulo merge. Un modulo merge richiede una \_ tabella di convalida per il superamento della convalida.
13. I moduli merge richiedono un'interfaccia utente solo in rari casi. Non è consigliabile includere un'interfaccia utente con un modulo merge. Nei casi in cui è necessaria un'interfaccia utente, le tabelle dell'interfaccia utente possono essere unite nel file con estensione msi come le altre tabelle.
14. Aggiungere le informazioni del registro di sistema alle tabelle del registro di sistema appropriate nel database del modulo merge. Aggiungere le informazioni del registro di sistema per le librerie dei tipi, le classi, le estensioni e i verbi nelle tabelle [typelib](typelib-table.md), [Class](class-table.md), [AppID](appid-table.md), [ProgID](progid-table.md), [Extension](extension-table.md), [Verb](verb-table.md)o [MIME](mime-table.md) . Tutte le altre informazioni del registro di sistema possono essere inserite nella [tabella del registro di sistema](registry-table.md). Non è consigliabile usare la tabella SelfReg.
15. Aggiungere le informazioni di riepilogo al [flusso di informazioni di riepilogo del modulo unione](merge-module-summary-information-stream-reference.md).
16. Prima di tentare l'installazione, eseguire la convalida su tutti i moduli unione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Recupero di database del modulo merge vuoti](obtaining-blank-merge-module-databases.md)
</dt> <dt>

[Recupero di strumenti di creazione di moduli merge](obtaining-merge-module-authoring-tools.md)
</dt> <dt>

[Denominazione di chiavi primarie nei database del modulo merge](naming-primary-keys-in-merge-module-databases.md)
</dt> <dt>

[Creazione di tabelle di componenti del modulo merge](authoring-merge-module-component-tables.md)
</dt> <dt>

[Creazione di tabelle di directory del modulo merge](authoring-merge-module-directory-tables.md)
</dt> <dt>

[Creazione di tabelle FeatureComponents del modulo merge](authoring-merge-module-featurecomponents-tables.md)
</dt> <dt>

[Generazione di MergeModule.CABfile CAB inet](generating-mergemodule-cabinet-cabinet-files.md)
</dt> <dt>

[Creazione di tabelle di file del modulo merge](authoring-merge-module-file-tables.md)
</dt> <dt>

[Creazione di tabelle ModuleSignature](authoring-modulesignature-tables.md)
</dt> <dt>

[Creazione di tabelle ModuleComponents](authoring-modulecomponents-tables.md)
</dt> <dt>

[Creazione di tabelle di sequenza del modulo merge](authoring-merge-module-sequence-tables.md)
</dt> <dt>

[Convalida di moduli merge](validating-merge-modules.md)
</dt> <dt>

[Creazione di interfacce utente nei moduli merge](authoring-user-interfaces-in-merge-modules.md)
</dt> <dt>

[Creazione di tabelle del registro di sistema del modulo merge](authoring-merge-module-registry-tables.md)
</dt> <dt>

[Creazione di flussi di informazioni di riepilogo del modulo merge](authoring-merge-module-summary-information-streams.md)
</dt> <dt>

[Riferimento al flusso di informazioni di riepilogo del modulo merge](merge-module-summary-information-stream-reference.md)
</dt> <dt>

Convalida di moduli merge
</dt> <dt>

[Uso di moduli unione a 64 bit](using-64-bit-merge-modules.md)
</dt> </dl>

 

 



