---
description: Raccolta delle metriche delle partizioni
ms.assetid: 2dc35011-24fa-49df-9cf8-96db2de39efa
title: Raccolta delle metriche delle partizioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8168972a0bac0b4eb79c5adde3530d1a0673469adff6b66b4c1b31cc6446bca2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047688"
---
# <a name="collecting-partition-metrics"></a>Raccolta delle metriche delle partizioni

In alcuni casi, un'organizzazione potrebbe voler raccogliere informazioni sull'uso delle applicazioni COM+ ai fini del monitoraggio, della pianificazione della capacità e della contabilità delle risorse.

Ad esempio, un provider di servizi applicazioni (ASP) potrebbe voler addebitare a un cliente l'utilizzo delle risorse. A tale scopo, COM+ consente di raccogliere informazioni su eventi e metriche in base alla partizione.

Il modo per raccogliere queste informazioni per una partizione specifica è specificando, per ogni interfaccia di strumentazione COM+, il membro ID di partizione all'interno della struttura di eventi standard. La struttura di eventi è il primo valore di un'interfaccia di strumentazione COM+. Per altre informazioni, vedere [Interfacce di strumentazione COM+.](com--instrumentation-interfaces.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Configurazione della cache delle partizioni](configuring-the-partition-cache.md)
</dt> <dt>

[Raggruppamento di applicazioni in partizioni](grouping-applications-into-partitions.md)
</dt> <dt>

[Gestione delle partizioni locali](managing-local-partitions.md)
</dt> <dt>

[Gestione delle partizioni all'interno di Active Directory](managing-partitions-within-active-directory.md)
</dt> <dt>

[Impostazione dei diritti amministrativi per una partizione](setting-administrative-rights-for-a-partition.md)
</dt> </dl>

 

 



