---
description: 'Un richiedente può suddividere un set di copie shadow usando il metodo IVssBackupComponents:: BreakSnapshotSet o IVssBackupComponentsEx2:: BreakSnapshotSetEx.'
ms.assetid: fb796b2f-b6fb-48ee-8d42-36f88cb165aa
title: Suddivisione delle copie shadow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dac84c9f45d16d8a88f9d61ad6e4c277dfad3ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318906"
---
# <a name="breaking-shadow-copies"></a>Suddivisione delle copie shadow

Un richiedente può suddividere un set di copie shadow usando il metodo [**IVssBackupComponents:: BreakSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-breaksnapshotset) o [**IVssBackupComponentsEx2:: BreakSnapshotSetEx**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-breaksnapshotsetex) .

Una copia shadow interruppe è un volume che contiene una copia shadow non più gestita da VSS. La suddivisione di una copia shadow ha un significato solo se il [*provider*](vssgloss-p.md) della copia shadow è un [*provider hardware*](vssgloss-h.md). Questo perché solo i provider hardware possono implementare una copia shadow come volume effettivo con un ciclo di vita indipendente da VSS. Se VSS non gestisce un volume di questo tipo, è ancora disponibile.

I provider di software mantengono le copie shadow solo quando sono incluse nelle operazioni VSS. Per questo motivo, l'infrazione di una copia shadow non ha significato per i provider di software.

Se la copia shadow è stata gestita da un provider hardware, il richiedente deve importare la copia shadow prima di chiamare [**BreakSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-breaksnapshotset) o [**BreakSnapshotSetEx**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-breaksnapshotsetex). Nel caso di copie shadow non trasferibili (create da un provider hardware), le copie vengono importate in modo implicito come parte della chiamata [**IVssBackupComponents::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) .

Dopo che il richiedente ha chiamato [**BreakSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-breaksnapshotset) o [**BreakSnapshotSetEx**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-breaksnapshotsetex), il set di copie shadow è ancora accessibile tramite gli oggetti dispositivo o altri percorsi di accesso, ma non è più un set di copie shadow. Può essere gestita come uno o più lun usando le interfacce COM del servizio dischi virtuali. Utilizzando VDS, un richiedente può convertire i LUN in lettura/scrittura, montarli con lettere di unità oppure mascherarli e annullarne il mascheramento in altri computer. Per ulteriori informazioni, vedere la [documentazione dell'API VDS](../vds/virtual-disk-service-portal.md) .

 

 
