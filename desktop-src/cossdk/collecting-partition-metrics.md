---
description: Raccolta delle metriche della partizione
ms.assetid: 2dc35011-24fa-49df-9cf8-96db2de39efa
title: Raccolta delle metriche della partizione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6467dfb9c891e7ae57505c8ec3815bfa99e49d8a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126363"
---
# <a name="collecting-partition-metrics"></a>Raccolta delle metriche della partizione

In alcuni casi, un'organizzazione potrebbe voler raccogliere informazioni sull'uso dell'applicazione COM+ ai fini del monitoraggio, della pianificazione della capacità e dell'account delle risorse.

Ad esempio, un provider di servizi dell'applicazione (ASP) potrebbe voler addebitare un cliente per l'utilizzo delle risorse. A tale scopo, COM+ consente di raccogliere informazioni relative a eventi e metriche in base a ogni partizione.

Per raccogliere queste informazioni per una partizione specifica, è necessario specificare, per ogni interfaccia di strumentazione COM+, il membro dell'ID di partizione all'interno della struttura di eventi standard. La struttura dell'evento è il primo valore di un'interfaccia di strumentazione COM+. Per ulteriori informazioni, vedere [interfacce di strumentazione com+](com--instrumentation-interfaces.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Configurazione della cache della partizione](configuring-the-partition-cache.md)
</dt> <dt>

[Raggruppamento di applicazioni in partizioni](grouping-applications-into-partitions.md)
</dt> <dt>

[Gestione delle partizioni locali](managing-local-partitions.md)
</dt> <dt>

[Gestione di partizioni all'interno Active Directory](managing-partitions-within-active-directory.md)
</dt> <dt>

[Impostazione dei diritti amministrativi per una partizione](setting-administrative-rights-for-a-partition.md)
</dt> </dl>

 

 



