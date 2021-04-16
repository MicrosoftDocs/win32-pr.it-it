---
description: Per lo sviluppo di un'applicazione COM+ corretta è necessario progettare l'architettura dell'applicazione di primo piano.
ms.assetid: 6a7cc610-e09a-4097-bc31-4e53db0ee152
title: Progettazione dell'applicazione COM+ tramite UML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48526623df5bc929daa4d8ce9cbe4d7592d6b30c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401423"
---
# <a name="designing-the-com-application-using-uml"></a>Progettazione dell'applicazione COM+ tramite UML

Per lo sviluppo di un'applicazione COM+ corretta è necessario progettare l'architettura dell'applicazione di primo piano. Il Unified Modeling Language (UML) è fondamentale per questo sviluppo di progettazione. UML è una notazione di modellazione per i dati e i processi delle applicazioni che combina le procedure consigliate del settore software. Poiché UML suddivide l'applicazione in tre visualizzazioni che riflettono l'applicazione, nonché la creazione di pacchetti e l'implementazione, la notazione di modellazione si estende per supportare la modellazione aziendale.

UML indirizza tre visualizzazioni dell'applicazione, come indicato di seguito:

-   Visualizzazione statica, modellata da informazioni ricavate da scenari utente e diagrammi classi.
-   Visualizzazione dinamica, modellata usando diagrammi di sequenza, collaborazione e transizione di stato.
-   Visualizzazione funzionale, ovvero la descrizione descrittiva più tradizionale con pseudocodice e specifiche.

Le informazioni per queste visualizzazioni possono essere raccolte seguendo tre passaggi di progettazione che funzionano bene con UML. Prima di scrivere una singola riga di codice, è necessario creare i modelli seguenti:

<dl> <dt>

<span id="Conceptual_model"></span><span id="conceptual_model"></span><span id="CONCEPTUAL_MODEL"></span>Modello concettuale
</dt> <dd>

Decidere quali componenti e servizi sono obbligatori.

</dd> <dt>

<span id="Logical_model"></span><span id="logical_model"></span><span id="LOGICAL_MODEL"></span>Modello logico
</dt> <dd>

Determinare il livello di progettazione logico a cui appartengono.

</dd> <dt>

<span id="Physical_model"></span><span id="physical_model"></span><span id="PHYSICAL_MODEL"></span>Modello fisico
</dt> <dd>

Determinare dove risiedono fisicamente i componenti e il modo in cui devono essere codificati.

</dd> </dl>

Questi modelli possono essere quindi usati con gli strumenti per i casi basati su UML. Per ulteriori informazioni su questi tre modelli di progettazione, vedere gli argomenti seguenti in questa sezione:

-   [Modello concettuale: requisiti delle applicazioni](the-conceptual-model--application-requirements.md)
-   [Modello logico: definizione dell'applicazione e pianificazione](the-logical-model--application-definition-and-planning.md)
-   [Modello fisico: architettura dell'applicazione](the-physical-model--application-architecture.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Presupposti e principi di progettazione COM+](com--design-assumptions-and-principles.md)
</dt> <dt>

[Suggerimenti di progettazione generali per l'utilizzo di COM+](general-design-tips-for-using-com-.md)
</dt> <dt>

[Ottimizzazione delle interazioni con il livello di logica di business COM+](optimizing-interactions-with-the-com--business-logic-tier.md)
</dt> <dt>

[Altri strumenti Microsoft per la creazione di applicazioni distribuite](other-microsoft-tools-for-building-distributed-applications.md)
</dt> </dl>

 

 



