---
description: In alternativa alla gestione delle partizioni di Active Directory tramite lo strumento amministrativo Utenti e computer di Active Directory, è possibile gestire le partizioni COM+ a livello di codice tramite l'uso di un set di oggetti COM+ all'interno di Active Directory System Interface (ADSI).
ms.assetid: 915b4643-cbda-433a-a383-65a6b0fd0874
title: Gestione delle partizioni all'interno di Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a87c0aebc9ca52dee005a0343e504756e3e117c3e012098e529fb6d52033428f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070581"
---
# <a name="managing-partitions-within-active-directory"></a>Gestione delle partizioni all'interno di Active Directory

In alternativa alla gestione delle partizioni di Active Directory tramite lo strumento amministrativo Utenti e computer di Active Directory, è possibile gestire le partizioni COM+ a livello di codice tramite l'uso di un set di oggetti COM+ all'interno di Active Directory System Interface (ADSI).

Indipendentemente dalla tecnica amministrativa scelta per la gestione delle partizioni COM+, gli amministratori devono seguire una sequenza generale di passaggi:

1.  Creare le nuove partizioni COM+ all'interno di Active Directory per il dominio.
2.  Creare set di partizioni COM+ all'interno di Active Directory ed eseguire il mapping alle partizioni COM+ appena create.
3.  Configurare le partizioni di Active Directory nel computer locale usando l'oggetto COM+ appropriato. Quando si configura una partizione di Active Directory in un computer locale, viene creata automaticamente una **cartella Applicazioni COM+** in tale cartella di partizione.
4.  Installare le applicazioni COM+ nelle partizioni COM+ appropriate.

È possibile eseguire tutti i passaggi precedenti a livello di codice, usando un set di interfacce di Active Directory denominato ADSI. Gli oggetti disponibili per la gestione delle partizioni disponibili in ADSI sono i seguenti:

-   DS \_ USERPARTITIONSETLINK \_ NAME
-   DS \_ PARTITIONLINK \_ NAME
-   DS \_ OBJECTID \_ NAME
-   DS \_ DEFAULTPARTITIONLINK \_ NAME
-   DS \_ USERLINK \_ NAME
-   NOME \_ SET DI PARTIZIONI DS \_
-   NOME \_ PARTIZIONE DS \_

Per informazioni sulla creazione e sulla gestione delle partizioni COM+ tramite l'uso degli strumenti di amministrazione Utenti e computer di Active Directory e Servizi componenti, vedere la Guida online disponibile all'interno di ogni strumento.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Raccolta delle metriche delle partizioni](collecting-partition-metrics.md)
</dt> <dt>

[Configurazione della cache delle partizioni](configuring-the-partition-cache.md)
</dt> <dt>

[Raggruppamento di applicazioni in partizioni](grouping-applications-into-partitions.md)
</dt> <dt>

[Gestione delle partizioni locali](managing-local-partitions.md)
</dt> <dt>

[Impostazione dei diritti amministrativi per una partizione](setting-administrative-rights-for-a-partition.md)
</dt> </dl>

 

 



