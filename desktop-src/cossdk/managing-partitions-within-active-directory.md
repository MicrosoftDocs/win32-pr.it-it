---
description: In alternativa alla gestione delle partizioni Active Directory tramite lo strumento di amministrazione Active Directory utenti e computer, è possibile gestire le partizioni COM+ a livello di codice tramite l'utilizzo di un set di oggetti COM+ all'interno di Active Directory System Interface (ADSI).
ms.assetid: 915b4643-cbda-433a-a383-65a6b0fd0874
title: Gestione di partizioni all'interno Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6635e49b7d2833a1e6e177c25f9f2fb05ff0dff4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524177"
---
# <a name="managing-partitions-within-active-directory"></a>Gestione di partizioni all'interno Active Directory

In alternativa alla gestione delle partizioni Active Directory tramite lo strumento di amministrazione Active Directory utenti e computer, è possibile gestire le partizioni COM+ a livello di codice tramite l'utilizzo di un set di oggetti COM+ all'interno di Active Directory System Interface (ADSI).

Indipendentemente dalla tecnica amministrativa scelta per la gestione delle partizioni COM+, esiste una sequenza generale di passaggi che gli amministratori devono seguire:

1.  Creare le nuove partizioni COM+ all'interno Active Directory per il dominio.
2.  Creare set di partizioni COM+ all'interno Active Directory ed eseguirne il mapping alle partizioni COM+ appena create.
3.  Configurare le partizioni Active Directory nel computer locale utilizzando l'oggetto COM+ appropriato. Quando si configura una partizione Active Directory in un computer locale, nella cartella della partizione viene creata automaticamente una cartella **applicazioni com+** .
4.  Installare le applicazioni COM+ nelle partizioni COM+ appropriate.

Tutti i passaggi precedenti possono essere eseguiti a livello di codice, usando un set di interfacce di Active Directory denominato ADSI. Gli oggetti disponibili per la gestione delle partizioni disponibili all'interno di ADSI sono i seguenti:

-   \_nome USERPARTITIONSETLINK \_ DS
-   \_nome PARTITIONLINK \_ DS
-   \_nome objectId \_ DS
-   \_nome DEFAULTPARTITIONLINK \_ DS
-   \_nome USERLINK \_ DS
-   \_nome partizioni DS \_
-   \_nome partizione \_ DS

Per informazioni sulla creazione e la gestione di partizioni COM+ tramite l'utilizzo degli strumenti di amministrazione Active Directory utenti e computer e Servizi componenti, vedere la guida online disponibile all'interno di ogni strumento.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Raccolta delle metriche della partizione](collecting-partition-metrics.md)
</dt> <dt>

[Configurazione della cache della partizione](configuring-the-partition-cache.md)
</dt> <dt>

[Raggruppamento di applicazioni in partizioni](grouping-applications-into-partitions.md)
</dt> <dt>

[Gestione delle partizioni locali](managing-local-partitions.md)
</dt> <dt>

[Impostazione dei diritti amministrativi per una partizione](setting-administrative-rights-for-a-partition.md)
</dt> </dl>

 

 



