---
description: Raggruppamento di applicazioni in partizioni
ms.assetid: bdfe2428-9769-4bcb-b74e-a141ba67a67e
title: Raggruppamento di applicazioni in partizioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28b35c726662d7dbe2cf039678ba5cdb4f94eeea
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305323"
---
# <a name="grouping-applications-into-partitions"></a>Raggruppamento di applicazioni in partizioni

Quando si decide come raggruppare le applicazioni in partizioni, è necessario che gli amministratori siano consapevoli di alcune regole e restrizioni, incluse le seguenti:

-   Un'applicazione può essere installata in una o più partizioni.
-   In un'applicazione può esistere una sola istanza di un determinato componente.

## <a name="public-and-private-components"></a>Componenti pubblici e privati

Quando si decide come raggruppare le applicazioni COM+, esistono altre restrizioni. Queste restrizioni riguardano i componenti pubblici e privati all'interno di un'applicazione. I componenti dell'applicazione possono in genere essere pubblici o privati. Tuttavia, quando si raggruppano le applicazioni in partizioni, gli amministratori devono tenere presente alcune restrizioni relative ai componenti pubblici e privati. Nella tabella seguente sono elencate queste restrizioni.



| Se un'applicazione è:              | I componenti di una partizione possono essere:                                                                                   |
|------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| Un'applicazione server<br/>    | Public e private.<br/>                                                                                           |
| Un'applicazione di libreria<br/>   | Solo pubblico. In caso contrario, l'applicazione chiamanti potrebbe avere gli stessi componenti, che creerebbe ambiguità.<br/> |
| Nella partizione globale<br/> | Solo pubblico. Ciò garantisce la compatibilità con le versioni precedenti.<br/>                                                             |



 

## <a name="application-ids"></a>ID applicazione

Ogni applicazione COM+ installata in un computer dispone di un ID applicazione univoco. Tuttavia, i nomi delle applicazioni devono essere univoci solo all'interno di una singola partizione e non sull'intero computer.

La tabella seguente mostra cosa accade all'ID applicazione quando un'applicazione viene importata in una partizione o esportata da una partizione.



| Se un'applicazione è:                                              | Quindi l'ID applicazione:                    |
|--------------------------------------------------------------------|---------------------------------------------|
| Importazione nella partizione globale<br/>                        | Rimane invariato<br/>                 |
| Importazione in una partizione diversa dalla partizione globale<br/> | Modificato<br/>                       |
| Esportato<br/>                                                | È incluso nel file esportato<br/> |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Raccolta delle metriche della partizione](collecting-partition-metrics.md)
</dt> <dt>

[Configurazione della cache della partizione](configuring-the-partition-cache.md)
</dt> <dt>

[Gestione delle partizioni locali](managing-local-partitions.md)
</dt> <dt>

[Gestione di partizioni all'interno Active Directory](managing-partitions-within-active-directory.md)
</dt> <dt>

[Impostazione dei diritti amministrativi per una partizione](setting-administrative-rights-for-a-partition.md)
</dt> </dl>

 

 




