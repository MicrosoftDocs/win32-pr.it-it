---
description: Lo sviluppo di un'applicazione COM+ efficace richiede una progettazione dell'architettura dell'applicazione in anticipo.
ms.assetid: 6a7cc610-e09a-4097-bc31-4e53db0ee152
title: Progettazione dell'applicazione COM+ tramite UML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50b5ab7cc96d753e023f8b89825ce7540c5abc6d79b7b78f231eea8cce4e2730
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117916735"
---
# <a name="designing-the-com-application-using-uml"></a>Progettazione dell'applicazione COM+ tramite UML

Lo sviluppo di un'applicazione COM+ efficace richiede una progettazione dell'architettura dell'applicazione in anticipo. Il Unified Modeling Language (UML) è fondamentale per questo sviluppo di progettazione. UML è una notazione di modellazione per i dati e i processi delle applicazioni che combina le procedure consigliate del settore software. Poiché l'UML suddivide l'applicazione in tre visualizzazioni che riflettono l'applicazione, nonché la creazione di pacchetti e l'implementazione, la notazione di modellazione si estende bene per supportare la modellazione aziendale.

Il modello UML è in base a tre visualizzazioni dell'applicazione, come indicato di seguito:

-   Visualizzazione statica, modellata in base alle informazioni derivate da scenari utente e diagrammi classi.
-   Visualizzazione dinamica, modellata usando diagrammi di sequenza, collaborazione e transizione di stato.
-   La visualizzazione funzionale, che è la narrazione descrittiva più tradizionale che usa pseudocodice e specifiche.

Le informazioni per queste viste possono essere raccolte seguendo tre passaggi di progettazione che funzionano bene con UML. Prima di scrivere una singola riga di codice, è necessario creare i modelli seguenti:

<dl> <dt>

<span id="Conceptual_model"></span><span id="conceptual_model"></span><span id="CONCEPTUAL_MODEL"></span>Modello concettuale
</dt> <dd>

Decidere quali componenti e servizi sono necessari.

</dd> <dt>

<span id="Logical_model"></span><span id="logical_model"></span><span id="LOGICAL_MODEL"></span>Modello logico
</dt> <dd>

Determinare a quale livello di progettazione logica appartengono.

</dd> <dt>

<span id="Physical_model"></span><span id="physical_model"></span><span id="PHYSICAL_MODEL"></span>Modello fisico
</dt> <dd>

Determinare dove si trovano fisicamente i componenti e come devono essere codificati.

</dd> </dl>

Questi modelli possono quindi essere usati con gli strumenti CASE basati su UML. Per altre informazioni su questi tre modelli di progettazione, vedere gli argomenti seguenti in questa sezione:

-   [Modello concettuale: requisiti dell'applicazione](the-conceptual-model--application-requirements.md)
-   [Modello logico: definizione e pianificazione dell'applicazione](the-logical-model--application-definition-and-planning.md)
-   [Modello fisico: Architettura dell'applicazione](the-physical-model--application-architecture.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Presupposti e principi della progettazione COM+](com--design-assumptions-and-principles.md)
</dt> <dt>

[Progettazione generale Suggerimenti'uso di COM+](general-design-tips-for-using-com-.md)
</dt> <dt>

[Ottimizzazione delle interazioni con il livello di logica di business COM+](optimizing-interactions-with-the-com--business-logic-tier.md)
</dt> <dt>

[Altri strumenti Microsoft per la creazione di applicazioni distribuite](other-microsoft-tools-for-building-distributed-applications.md)
</dt> </dl>

 

 



