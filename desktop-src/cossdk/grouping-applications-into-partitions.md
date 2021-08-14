---
description: Raggruppamento di applicazioni in partizioni
ms.assetid: bdfe2428-9769-4bcb-b74e-a141ba67a67e
title: Raggruppamento di applicazioni in partizioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40491e95313544a32e23db78d8959736665db8c21782d3f1b30729e6eda6f1db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119991101"
---
# <a name="grouping-applications-into-partitions"></a>Raggruppamento di applicazioni in partizioni

Quando si decide come raggruppare le applicazioni in partizioni, gli amministratori devono essere a conoscenza di determinate regole e restrizioni, tra cui le seguenti:

-   Un'applicazione può essere installata in una o più partizioni.
-   In un'applicazione può esistere una sola istanza di un determinato componente.

## <a name="public-and-private-components"></a>Componenti pubblici e privati

Esistono altre restrizioni quando si decide come raggruppare le applicazioni COM+. Queste restrizioni riguardano i componenti pubblici e privati all'interno di un'applicazione. I componenti dell'applicazione possono in genere essere pubblici o privati. Tuttavia, quando si raggruppano le applicazioni in partizioni, gli amministratori devono essere consapevoli di alcune restrizioni relative ai componenti pubblici e privati. Nella tabella seguente sono elencate queste restrizioni.



| Se un'applicazione è:              | I componenti in una partizione possono quindi essere:                                                                                   |
|------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| Un'applicazione server<br/>    | Pubblico e privato.<br/>                                                                                           |
| Un'applicazione di libreria<br/>   | Solo pubblico. In caso contrario, l'applicazione chiamante potrebbe avere gli stessi componenti, che creerebbe ambiguità.<br/> |
| Nella partizione globale<br/> | Solo pubblico. Ciò garantisce la compatibilità con le versioni precedenti.<br/>                                                             |



 

## <a name="application-ids"></a>ID applicazione

Ogni applicazione COM+ installata in un computer ha un ID applicazione univoco. Tuttavia, i nomi delle applicazioni devono essere univoci solo all'interno di una singola partizione e non nell'intero computer.

La tabella seguente illustra cosa accade all'ID applicazione quando un'applicazione viene importata in una partizione o esportata da una partizione.



| Se un'applicazione è:                                              | Quindi l'ID applicazione:                    |
|--------------------------------------------------------------------|---------------------------------------------|
| Importato nella partizione globale<br/>                        | Rimane invariato<br/>                 |
| Importato in una partizione diversa dalla partizione globale<br/> | È stato modificato<br/>                       |
| Esportato<br/>                                                | È incluso nel file esportato<br/> |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Raccolta delle metriche delle partizioni](collecting-partition-metrics.md)
</dt> <dt>

[Configurazione della cache delle partizioni](configuring-the-partition-cache.md)
</dt> <dt>

[Gestione delle partizioni locali](managing-local-partitions.md)
</dt> <dt>

[Gestione delle partizioni all'interno di Active Directory](managing-partitions-within-active-directory.md)
</dt> <dt>

[Impostazione dei diritti amministrativi per una partizione](setting-administrative-rights-for-a-partition.md)
</dt> </dl>

 

 




