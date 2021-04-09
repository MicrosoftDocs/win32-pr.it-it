---
description: "Sono disponibili quattro livelli per la libreria di analisi dell'input penna: Windows Form, WPF, COM e il livello di base. In questa sezione viene descritto quando utilizzare ogni livello."
ms.assetid: bd190606-5bd8-4280-ba2b-267588904ed3
title: Utilizzo API analisi input penna
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24e291066d6cfd6ecdec319728b7394d730ba311
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966515"
---
# <a name="ink-analysis-api-usage"></a>Utilizzo API analisi input penna

Sono disponibili quattro livelli per la libreria di analisi dell'input penna: Windows Form, WPF, COM e il livello di base. In questa sezione viene descritto quando utilizzare ogni livello.

## <a name="ink-analysis-api-overview"></a>Panoramica dell'API di analisi dell'input penna

Le librerie di analisi dell'input penna sono progettate per essere usate in un'ampia gamma di ambienti di programmazione supportati. Sono disponibili quattro livelli di base tramite i quali l'applicazione può usare l'analisi dell'input penna. Questi livelli sono:

-   Livello Windows Form
-   Livello WPF
-   Livello COM
-   Livello di base

### <a name="windows-forms-applications"></a>Applicazioni Windows Forms

È possibile usare l'API di analisi dell'input penna nel progetto gestito aggiungendo un riferimento alle librerie seguenti:

-   Microsoft. Ink. Analysis (Microsoft.Ink.Analysis.dll)
-   Libreria di analisi documenti input penna (IACore.dll)

Nelle applicazioni Windows Form è probabile che le librerie vengano utilizzate insieme agli oggetti della piattaforma Tablet PC standard disponibili nell'assembly Microsoft Tablet PC API v 1.7. Assicurarsi che sia presente anche un riferimento a:

-   Microsoft Tablet PC API v 1.7.2600.2180 (Microsoft.Ink.dll)

### <a name="windows-presentation-framework-applications"></a>Applicazioni Windows Presentation Framework

È possibile usare l'API di analisi dell'input penna nel progetto WPF aggiungendo un riferimento ai membri dell'analisi dell'input penna definiti nello spazio dei nomi System. Windows. Ink nell'assembly IAWinFX.dll. Questo assembly viene installato dall'SDK.

### <a name="com-applications"></a>Applicazioni COM

Le applicazioni COM non di automazione devono usare il livello COM delle API di analisi dell'input penna.

Tipi di oggetti [ContextNode](/previous-versions/ms551996(v=vs.100)) specifici, ad esempio [ParagraphNode](/previous-versions/ms580136(v=vs.100)), [InkWordNode](/previous-versions/ms580133(v=vs.100))e altri, non vengono utilizzati nel livello com. È invece consigliabile usare [**IContextNode:: AddPropertyData**](icontextnode-addpropertydata.md) sull'interfaccia [**IContextNode**](icontextnode.md) standard.

È necessario \# includere "IACom. h". È probabile che le librerie vengano utilizzate insieme all'oggetto input penna della piattaforma Tablet PC, pertanto è necessario \# includere anche "msinkaut. h".

### <a name="rts-and-other-applications"></a>RTS e altre applicazioni

Il livello di base dell'analisi dell'input penna funziona in modo diverso rispetto agli altri in quanto accetta dati punto per l'analisi anziché oggetti [Stroke](/previous-versions/ms552692(v=vs.100)) . Esempi di come usare direttamente il livello di base anziché i livelli di Windows Form o COM includono applicazioni che non usano oggetti input penna della piattaforma Tablet PC di prima generazione o applicazioni che usano le API [**RealTimeStylus**](realtimestylus-class.md) per gestire l'input dello stilo anziché usare gli oggetti [input penna](/previous-versions/ms583670(v=vs.100)) della piattaforma Tablet PC.

## <a name="32-bit-support-only"></a>Solo supporto a 32 bit

Si noti che le librerie di analisi dell'input penna sono supportate solo nei processi a 32 bit.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Panoramica dell'analisi dell'input penna](ink-analysis-overview.md)
</dt> <dt>

[Riferimento all'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

 
