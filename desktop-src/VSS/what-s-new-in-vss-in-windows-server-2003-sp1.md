---
description: "Nell'elenco seguente vengono indicate le aggiunte e le modifiche apportate all'interfaccia Servizio Copia Shadow del volume in Windows Server 2003 con Service Pack 1 (SP1):"
ms.assetid: 9e0dba98-5d23-444d-bd2f-cb72de8fb2d2
title: Novità di VSS in Windows Server 2003 SP1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 559b51d5b019d9d57aa154c4728ef5c8f4bb19d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485020"
---
# <a name="whats-new-in-vss-in-windows-server-2003-sp1"></a>Novità di VSS in Windows Server 2003 SP1

Nell'elenco seguente vengono indicate le aggiunte e le modifiche apportate all'interfaccia Servizio Copia Shadow del volume in Windows Server 2003 con Service Pack 1 (SP1):

## <a name="auto-recovery"></a>Ripristino automatico

Il [*Ripristino automatico*](vssgloss-a.md) consente ai writer di aggiornare i componenti in una copia shadow prima che la copia shadow venga modificata in modo permanente in sola lettura. Ad esempio, è possibile che un database debba eseguire il rollback di tutte le transazioni incomplete per tutte le copie shadow. il writer del database potrebbe impostare il flag di **\_ ripristino del \_ backup \_ di VSS CF** per i componenti del database. Il recupero automatico avviato dal richiedente consente il ripristino con granularità fine, ad esempio il ripristino di una tabella in un database o in una cartella in un server di posta, oppure il rollback per supportare data mining per eseguire analisi che potrebbero essere troppo lente per un server di produzione (il richiedente aggiungerà il **rollback di VSS \_ VolSnap \_ attr \_ \_** al contesto della copia shadow). Il ripristino automatico non è compatibile con le copie shadow trasportabili, ma la stessa funzionalità è supportata tramite il [ripristino rapido tramite volumi di copia shadow trasportabili](fast-recovery-using-transportable-shadow-copied-volumes.md).

Gli elementi di programmazione seguenti presentano modifiche per supportare il ripristino automatico:

Metodi della classe

-   [**CVssWriter:: GetSnapshotDeviceName**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-getsnapshotdevicename)
-   [**CVssWriter:: OnPostSnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot)

Enumerazioni

-   [**\_flag componente \_ VSS**](/windows/desktop/api/VsWriter/ne-vswriter-vss_component_flags)
-   [**\_\_ \_ attributi snapshot del volume VSS \_**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes)

Metodi di interfaccia

-   [**IVssProviderCreateSnapshotSet::P reFinalCommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-prefinalcommitsnapshots)
-   [**IVssProviderCreateSnapshotSet::P ostFinalCommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-postfinalcommitsnapshots)

## <a name="full-support-for-transportable-shadow-copies"></a>Supporto completo per le copie shadow trasportabili

Le copie shadow trasportabili sono supportate in tutte le edizioni di Windows Server 2003 con SP1. Per ulteriori informazioni, vedere [importazione di volumi di copie shadow trasportabili](importing-transportable-shadow-copied-volumes.md).

## <a name="fast-recovery-using-transportable-shadow-copied-volumes"></a>Ripristino rapido tramite volumi di copie shadow trasportabili

[Ripristino rapido tramite volumi di copie shadow trasportabili](fast-recovery-using-transportable-shadow-copied-volumes.md)

## <a name="shadow-copy-storage-area-management"></a>Gestione area di archiviazione copia shadow

[**IVssSnapshotMgmt2**](/windows/desktop/api/VsMgmt/nn-vsmgmt-ivsssnapshotmgmt2)

 

 



