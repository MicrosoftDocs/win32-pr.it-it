---
description: Un richiedente può interrompere un set di copie shadow usando il metodo IVssBackupComponents::BreakSnapshotSet o IVssBackupComponentsEx2::BreakSnapshotSetEx.
ms.assetid: fb796b2f-b6fb-48ee-8d42-36f88cb165aa
title: Copie shadow di rilievo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fee7a17a77bb806bc6e3713c00c9a01b9bc583f56822b9940b0fe2afebb4e7f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032901"
---
# <a name="breaking-shadow-copies"></a>Copie shadow di rilievo

Un richiedente può interrompere un set di copie shadow usando il metodo [**IVssBackupComponents::BreakSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-breaksnapshotset) o [**IVssBackupComponentsEx2::BreakSnapshotSetEx.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-breaksnapshotsetex)

Una copia shadow interrotta è un volume che contiene una copia shadow che non è più gestita da VSS. L'interruzione di una copia shadow ha significato solo se il [*provider*](vssgloss-p.md) della copia shadow è un [*provider hardware*](vssgloss-h.md). Ciò è dovuto al fatto che solo i provider di hardware possono implementare una copia shadow come volume effettivo con un ciclo di vita indipendente da VSS. Se VSS non gestisce un volume di questo tipo, è ancora disponibile.

I provider di software mantengono le copie shadow solo durante le operazioni del Servizio Copia Shadow del volume. Per questo motivo, l'interruzione di una copia shadow non ha alcun significato per i provider di software.

Se la copia shadow è stata gestita da un provider hardware, il richiedente deve importare la copia shadow prima di chiamare [**BreakSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-breaksnapshotset) [**o BreakSnapshotSetEx**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-breaksnapshotsetex). Nel caso di copie shadow non trasportabili (create da un provider hardware), vengono importate in modo implicito come parte della chiamata [**IVssBackupComponents::D oSnapshotSet.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset)

Dopo che il richiedente ha chiamato [**BreakSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-breaksnapshotset) o [**BreakSnapshotSetEx,**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-breaksnapshotsetex)il set di copie shadow è ancora accessibile tramite i relativi oggetti dispositivo o altri percorsi di accesso, ma non è più un set di copie shadow. Può essere gestito come uno o più LUN usando le interfacce COM del servizio dischi virtuali (VDS). Usando VDS, un richiedente può convertire i LUN in lettura/scrittura, montarli con lettere di unità o mascherarli/annullarne il mascheramento in altri computer. Per altre informazioni, vedere la [documentazione dell'API VDS.](../vds/virtual-disk-service-portal.md)

 

 
