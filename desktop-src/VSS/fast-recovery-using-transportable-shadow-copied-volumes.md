---
description: Le copie shadow trasportabili possono essere utilizzate per facilitare un ripristino rapido.
ms.assetid: 2eaffcf7-01b2-44ce-8bc4-fd9fa42c8a8c
title: Ripristino rapido tramite volumi di copie shadow trasportabili
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a588395de36b0e6773eacf7f46a45452a69c13c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318581"
---
# <a name="fast-recovery-using-transportable-shadow-copied-volumes"></a>Ripristino rapido tramite volumi di copie shadow trasportabili

Le [*copie shadow trasportabili*](vssgloss-t.md) possono essere utilizzate per facilitare un *ripristino rapido*.

Il ripristino rapido può essere usato per ripristinare rapidamente una copia shadow precedente. I passaggi necessari sono i seguenti:

1.  Creare la copia shadow trasportabile dei LUN appropriati. La copia shadow può essere [*persistente*](vssgloss-p.md) o non permanente.
2.  Rimuovere i LUN originali
    1.  Se il computer si trova all'interno di un cluster, contrassegnare le risorse disco interessate come offline o abilitare la [modalità di manutenzione](/previous-versions/windows/desktop/mscs/maintaining-physical-disk-resources) per queste risorse disco.
    2.  Mascherare i LUN interessati dal computer (e tutti gli altri nodi se il computer si trova in un cluster).
3.  Importare la copia shadow usando il metodo [**IVssBackupComponents:: ImportSnapshots**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-importsnapshots) .
4.  Suddividere la copia shadow usando il metodo [**IVssBackupComponents:: BreakSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-breaksnapshotset) .
5.  Contrassegnare i nuovi volumi di copia shadow come di lettura/scrittura.
6.  Se il computer si trova in un cluster, esporre i nuovi LUN delle copie shadow come lun originali.
    1.  Annullare il mascheramento dei lun delle copie shadow negli altri nodi del cluster.
    2.  Contrassegnare le risorse contrassegnate in precedenza come offline come online o disabilitare la modalità di manutenzione per tali risorse disco.

> [!Note]  
> Le copie shadow trasportabili in un cluster non sono supportate prima di Windows Server 2003 con Service Pack 1 (SP1). Questa operazione è supportata solo con i LUN conformi, che hanno almeno una pagina di dati del prodotto SCSI Vital (Vital) 0x83 \_ identificatore di archiviazione di tipo 1, 2 o 8 e associazione 0 e i LUN devono mantenere un disco di base con il partizionamento MBR.

 

 

 
