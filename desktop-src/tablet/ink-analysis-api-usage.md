---
description: 'Sono disponibili quattro livelli per la libreria di analisi input penna: Windows, WPF, COM e il livello di base. Questa sezione descrive quando usare ogni livello.'
ms.assetid: bd190606-5bd8-4280-ba2b-267588904ed3
title: Utilizzo dell'API Analisi input penna
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdfada58868c7fe959f832e0c1243bc91a373fb0186d8deee2f9481d78a95714
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032349"
---
# <a name="ink-analysis-api-usage"></a>Utilizzo dell'API Analisi input penna

Sono disponibili quattro livelli per la libreria di analisi input penna: Windows, WPF, COM e il livello di base. Questa sezione descrive quando usare ogni livello.

## <a name="ink-analysis-api-overview"></a>Panoramica dell'API Analisi input penna

Le librerie di analisi input penna sono progettate per essere usate in un'ampia gamma di ambienti di programmazione supportati. Esistono quattro livelli di base tramite i quali l'applicazione può usare l'analisi input penna. Questi livelli sono:

-   Livello Windows Forms
-   Livello WPF
-   Livello COM
-   Livello di base

### <a name="windows-forms-applications"></a>Applicazioni Windows Forms

È possibile usare l'API Analisi input penna nel progetto gestito aggiungendo un riferimento alle librerie seguenti:

-   Microsoft.Ink.Analysis (Microsoft.Ink.Analysis.dll)
-   Ink Document Analysis Library (IACore.dll)

Nelle Windows Forms, è molto probabile che si usino le librerie insieme agli oggetti della piattaforma Tablet PC standard disponibili nell'assembly dell'API Microsoft Tablet PC v1.7. Assicurarsi di avere anche un riferimento a:

-   API Microsoft Tablet PC v1.7.2600.2180 (Microsoft.Ink.dll)

### <a name="windows-presentation-framework-applications"></a>Windows Applicazioni Presentation Framework

È possibile usare l'API Analisi input penna nel progetto WPF aggiungendo un riferimento ai membri di Analisi input penna definiti nel sistema. Windows. Spazio dei nomi Ink nell'assembly IAWinFX.dll input penna. Questo assembly viene installato dall'SDK.

### <a name="com-applications"></a>Applicazioni COM

Le applicazioni COM non di automazione devono usare il livello COM delle API Di analisi input penna.

Gli oggetti [ContextNode specifici](/previous-versions/ms551996(v=vs.100)) del tipo, ad esempio [ParagraphNode,](/previous-versions/ms580136(v=vs.100)) [InkWordNode](/previous-versions/ms580133(v=vs.100))e altri, non vengono usati nel livello COM. È invece consigliabile usare [**IContextNode::AddPropertyData**](icontextnode-addpropertydata.md) [**nell'interfaccia IContextNode**](icontextnode.md) standard.

È necessario \# includere "IACom.h". Molto probabilmente si useranno le librerie insieme all'oggetto Ink della piattaforma Tablet PC, quindi è necessario includere \# anche "msinkaut.h".

### <a name="rts-and-other-applications"></a>RTS e altre applicazioni

Il livello di base Analisi input penna funziona in modo diverso rispetto agli altri in quanto accetta dati punto per l'analisi anziché [oggetti Stroke.](/previous-versions/ms552692(v=vs.100)) Esempi di utilizzo diretto del livello base invece di usare i moduli Windows o i livelli COM includono applicazioni che non usano oggetti Input penna della piattaforma Tablet PC di prima [](/previous-versions/ms583670(v=vs.100)) generazione o applicazioni che usano le API [**RealTimeStylus**](realtimestylus-class.md) per gestire l'input dello stilo anziché usare gli oggetti Input penna della piattaforma Tablet PC.

## <a name="32-bit-support-only"></a>Solo supporto a 32 bit

Si noti che le librerie di analisi input penna sono supportate solo nei processi a 32 bit.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Panoramica dell'analisi input penna](ink-analysis-overview.md)
</dt> <dt>

[Informazioni di riferimento per l'analisi input penna](ink-analysis-reference.md)
</dt> </dl>

 

 
