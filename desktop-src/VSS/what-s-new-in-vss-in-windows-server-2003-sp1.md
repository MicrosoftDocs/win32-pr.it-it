---
description: "L'elenco seguente indica aggiunte e modifiche all'interfaccia Servizio Copia Shadow del volume in Windows Server 2003 con Service Pack 1 (SP1):"
ms.assetid: 9e0dba98-5d23-444d-bd2f-cb72de8fb2d2
title: Novità di VSS in Windows Server 2003 SP1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: baed6cde05eb1aabe1bc43f48aa035146e020f23d215e7902d3544414619b4e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118344197"
---
# <a name="whats-new-in-vss-in-windows-server-2003-sp1"></a>Novità di VSS in Windows Server 2003 SP1

L'elenco seguente indica aggiunte e modifiche all'interfaccia Servizio Copia Shadow del volume in Windows Server 2003 con Service Pack 1 (SP1):

## <a name="auto-recovery"></a>Ripristino automatico

[*Il ripristino automatico consente*](vssgloss-a.md) ai writer di aggiornare i componenti in una copia shadow prima che la copia shadow venga modificata in modo permanente in sola lettura. Ad esempio, un database potrebbe dover eseguire il rollback di qualsiasi transazione incompleta per tutte le copie shadow (il writer del database imposta il flag **BACKUP \_ \_ \_ RECOVERY** di VSS CF per i componenti di database). Il ripristino automatico avviato dal richiedente consente sia il ripristino con granularità fine (ad esempio il ripristino di una tabella in un database o di una cartella in un server di posta) sia il rollback per supportare data mining per eseguire un'analisi che sarebbe troppo lenta per un server di produzione (il richiedente aggiungerebbe **VSS \_ VOLS VOLSNAP \_ ATTR \_ ROLLBACK \_ RECOVERY** al contesto di copia shadow). Il ripristino automatico non è compatibile con le copie shadow trasportabili, ma la stessa funzionalità è supportata tramite il ripristino rapido tramite [volumi copiati shadow trasportabili.](fast-recovery-using-transportable-shadow-copied-volumes.md)

Gli elementi di programmazione seguenti hanno modifiche per supportare il ripristino automatico:

Metodi della classe

-   [**CVssWriter::GetSnapshotDeviceName**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-getsnapshotdevicename)
-   [**CVssWriter::OnPostSnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot)

Enumerazioni

-   [**FLAG DEL COMPONENTE \_ VSS \_**](/windows/desktop/api/VsWriter/ne-vswriter-vss_component_flags)
-   [**\_ATTRIBUTI DELLO \_ SNAPSHOT DEL VOLUME VSS \_ \_**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes)

Metodi di interfaccia

-   [**IVssProviderCreateSnapshotSet::P reFinalCommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-prefinalcommitsnapshots)
-   [**IVssProviderCreateSnapshotSet::P ostFinalCommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-postfinalcommitsnapshots)

## <a name="full-support-for-transportable-shadow-copies"></a>Supporto completo per copie shadow trasportabili

Le copie shadow trasportabili sono supportate in tutte le edizioni di Windows Server 2003 con SP1. Per altre informazioni, vedere [Importazione di volumi copiati shadow trasportabili](importing-transportable-shadow-copied-volumes.md).

## <a name="fast-recovery-using-transportable-shadow-copied-volumes"></a>Ripristino rapido tramite volumi copiati shadow trasportabili

[Ripristino rapido tramite volumi copiati shadow trasportabili](fast-recovery-using-transportable-shadow-copied-volumes.md)

## <a name="shadow-copy-storage-area-management"></a>Gestione dell'area di archiviazione delle copie shadow

[**IVssSnapshotMgmt2**](/windows/desktop/api/VsMgmt/nn-vsmgmt-ivsssnapshotmgmt2)

 

 



