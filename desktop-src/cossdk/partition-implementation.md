---
description: Se installato in un server applicazioni, COM+ crea automaticamente una partizione, nota come partizione globale.
ms.assetid: fbe894ae-5356-4522-884a-dc579a3a8dd3
title: Implementazione della partizione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3014aac80e853ca387538faf034eeadae91dd70cf36931de34638cbcbec7b02f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047349"
---
# <a name="partition-implementation"></a>Implementazione della partizione

Se installato in un server applicazioni, COM+ crea automaticamente una partizione, nota come *partizione globale*. La partizione globale include un set standard di applicazioni COM+. Le applicazioni COM+ installate nella partizione globale sono automaticamente disponibili per tutti gli utenti nel server. Se si hanno altre applicazioni COM+ che si desidera rendere disponibili a tutti gli utenti nel server, è possibile aggiungerle alla partizione globale.

Oltre alla partizione globale, è possibile creare altre partizioni per gli utenti solo in tale server o per gli utenti in tutto il dominio. La creazione di partizioni aggiuntive e l'installazione di più configurazioni di un'applicazione COM+ in esse consente agli utenti di eseguire contemporaneamente tali configurazioni di applicazione nello stesso computer. Inoltre, installando applicazioni COM+ in una partizione diversa dalla partizione globale, è possibile controllare l'accesso utente a tali applicazioni.

**Windows XP:** La possibilità di creare, configurare o delegare partizioni COM+ non è disponibile. La partizione globale è l'unica partizione COM+ disponibile.

Per altre informazioni sulle partizioni locali e sulle partizioni definite all'interno di Active Directory, vedere gli argomenti seguenti:

-   [Partizioni locali](local-partitions.md)
-   [Partizioni e Active Directory](partitions-and-active-directory.md)
-   [Partizioni predefinite](default-partitions.md)
-   [Partizione globale](the-global-partition.md)
-   [Proprietà partizione](partition-properties.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Restrizioni di progettazione delle applicazioni](application-design-restrictions.md)
</dt> <dt>

[Componenti e partizioni in coda COM+](com--queued-components-and-partitions.md)
</dt> <dt>

[Registrazione e attivazione di componenti nelle partizioni](registering-and-activating-components-in-partitions.md)
</dt> <dt>

[Che cosa sono le partizioni COM+?](what-are-com--partitions-.md)
</dt> </dl>

 

 



