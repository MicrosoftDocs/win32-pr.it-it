---
description: Quando viene installato in un server applicazioni, COM+ crea automaticamente una partizione, nota come partizione globale.
ms.assetid: fbe894ae-5356-4522-884a-dc579a3a8dd3
title: Implementazione della partizione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0130b1d2daeddee28b01271aa6b767ebc5a7eac5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305135"
---
# <a name="partition-implementation"></a>Implementazione della partizione

Quando viene installato in un server applicazioni, COM+ crea automaticamente una partizione, nota come *partizione globale*. La partizione globale include un set standard di applicazioni COM+. Le applicazioni COM+ installate nella partizione globale sono automaticamente disponibili per tutti gli utenti del server. Se si dispone di altre applicazioni COM+ che si desidera rendere disponibili a tutti gli utenti del server, è possibile aggiungerle alla partizione globale.

Oltre alla partizione globale, è possibile creare altre partizioni solo per gli utenti del server o per gli utenti di tutto il dominio. La creazione di partizioni aggiuntive e l'installazione di più configurazioni di un'applicazione COM+ consentono agli utenti di eseguire contemporaneamente tali configurazioni di applicazioni nello stesso computer. Inoltre, l'installazione di applicazioni COM+ in una partizione diversa dalla partizione globale consente di controllare l'accesso degli utenti a tali applicazioni.

**Windows XP:** La possibilità di creare, configurare o delegare partizioni COM+ non è disponibile. La partizione globale è l'unica partizione COM+ disponibile.

Per ulteriori informazioni sulle partizioni e le partizioni locali definite in Active Directory, vedere gli argomenti seguenti:

-   [Partizioni locali](local-partitions.md)
-   [Partizioni e Active Directory](partitions-and-active-directory.md)
-   [Partizioni predefinite](default-partitions.md)
-   [Partizione globale](the-global-partition.md)
-   [Proprietà partizione](partition-properties.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Limitazioni relative alla progettazione di applicazioni](application-design-restrictions.md)
</dt> <dt>

[Componenti e partizioni in coda COM+](com--queued-components-and-partitions.md)
</dt> <dt>

[Registrazione e attivazione di componenti nelle partizioni](registering-and-activating-components-in-partitions.md)
</dt> <dt>

[Che cosa sono le partizioni COM+?](what-are-com--partitions-.md)
</dt> </dl>

 

 



