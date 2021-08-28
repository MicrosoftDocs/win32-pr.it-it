---
description: Le copie shadow trasportabili possono essere usate per facilitare un ripristino rapido.
ms.assetid: 2eaffcf7-01b2-44ce-8bc4-fd9fa42c8a8c
title: Ripristino rapido tramite volumi copiati shadow trasportabili
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fb5ddd7604b1463def4ceaa6cd474487255682cf4489b13c5da520128c06811
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120006401"
---
# <a name="fast-recovery-using-transportable-shadow-copied-volumes"></a>Ripristino rapido tramite volumi copiati shadow trasportabili

[*Le copie shadow trasportabili possono*](vssgloss-t.md) essere usate per facilitare un *ripristino rapido.*

Il ripristino rapido può essere usato per ripristinare rapidamente una copia shadow precedente. I passaggi necessari sono i seguenti:

1.  Creare la copia shadow trasportabile dei LUN appropriati. La copia shadow può essere [*persistente*](vssgloss-p.md) o non persistente.
2.  Rimuovere i LUN originali
    1.  Se il computer si trova all'interno di un cluster, contrassegnare le risorse disco interessate come offline oppure abilitare la [modalità di](/previous-versions/windows/desktop/mscs/maintaining-physical-disk-resources) manutenzione per queste risorse disco.
    2.  Mascherare i LUN interessati da questo computer (e tutti gli altri nodi se il computer si trova in un cluster).
3.  Importare la copia shadow [**usando il metodo IVssBackupComponents::ImportSnapshots.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-importsnapshots)
4.  Interrompere la copia shadow usando il [**metodo IVssBackupComponents::BreakSnapshotSet.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-breaksnapshotset)
5.  Contrassegnare i nuovi volumi di copia shadow come di lettura/scrittura.
6.  Se il computer si trova in un cluster, esporre i nuovi LUN della copia shadow come LUN originali.
    1.  Annullare il mascheramento dei LUN della copia shadow negli altri nodi del cluster.
    2.  Contrassegnare le risorse precedentemente contrassegnate come offline come online oppure disabilitare la modalità di manutenzione per tali risorse disco.

> [!Note]  
> Le copie shadow trasportabili in un cluster non sono supportate prima di Windows Server 2003 con Service Pack 1 (SP1). Questa opzione è supportata solo con LUN conformi, che hanno almeno una pagina SCSI Vital Product Data (VPD) 0x83 STORAGE IDENTIFIER di tipo 1,2 o 8 e associazione 0 e i LUN devono mantenere un disco di base con \_ partizionamento MBR.

 

 

 
