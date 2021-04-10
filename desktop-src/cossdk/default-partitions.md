---
description: Partizioni predefinite
ms.assetid: ce6ad7c1-d4a1-4573-860e-f7859c588773
title: Partizioni predefinite
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5115b6b2480958c78a53c264804eb1f292808545
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225780"
---
# <a name="default-partitions"></a>Partizioni predefinite

Quando a un utente viene assegnata una partizione predefinita, COM+ tenta innanzitutto di attivare i componenti in tale partizione. Se l'attivazione non riesce, COM+ cerca la partizione globale affinché il componente venga attivato. L'eccezione a questo processo si verifica quando il componente COM+ include un moniker di partizione che specifica in modo esplicito la partizione in cui si trova il componente. In questo caso, il moniker della partizione ha la precedenza su qualsiasi configurazione di partizione predefinita.

Quando si utilizzano partizioni locali, la partizione predefinita viene assegnata agli utenti che utilizzano la cartella **com+ Partition Users** nello strumento di amministrazione Servizi componenti nel server applicazioni. Quando si usano i set di partizioni nella Active Directory, la partizione predefinita dell'utente è determinata dal set di partizioni dell'utente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Partizioni locali](local-partitions.md)
</dt> <dt>

[Proprietà partizione](partition-properties.md)
</dt> <dt>

[Partizioni e Active Directory](partitions-and-active-directory.md)
</dt> <dt>

[Partizione globale](the-global-partition.md)
</dt> </dl>

 

 



