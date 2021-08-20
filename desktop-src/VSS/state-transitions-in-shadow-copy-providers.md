---
description: Il modello di transizione dello stato in un provider di copie shadow è semplificato dalla serializzazione della creazione della copia shadow dal momento in cui viene chiamato IVssBackupComponents::StartSnapshotSet fino a quando non viene restituita la chiamata a IVssBackupComponents::D oSnapshotSet.
ms.assetid: 5dbf0fb3-53cb-4532-9a8f-bd955afe16c4
title: Transizioni di stato nei provider di copie shadow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad6141b9b8f221a1e67e95fde1e6b33ad819c0cbdead57eeb676164e89acc392
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118121601"
---
# <a name="state-transitions-in-shadow-copy-providers"></a>Transizioni di stato nei provider di copie shadow

Il modello di transizione dello stato in un provider di copie shadow è semplificato dalla serializzazione della creazione della copia shadow dal momento in cui viene chiamato [**IVssBackupComponents::StartSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset) fino a quando non viene restituita la chiamata [**a IVssBackupComponents::D oSnapshotSet.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) Se un altro richiedente tenta di creare una copia shadow durante questo periodo di tempo, la chiamata a **StartSnapshotSet** avrà esito negativo con l'errore **VSS \_ E SNAPSHOT SET \_ IN \_ \_ \_ PROGRESS**, a indicare che il secondo richiedente deve attendere e riprovare.

VSS chiamerà [**IVssProviderCreateSnapshotSet::AbortSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-abortsnapshots) solo dopo che il richiedente ha chiamato [**DoSnapshotSet,**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset)anche se la copia shadow ha esito negativo o viene interrotta prima di questo punto. Ciò significa che un provider non riceverà una chiamata a **AbortSnapshots** fino a quando non è stato chiamato [**IVssProviderCreateSnapshotSet::EndPrepareSnapshots.**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-endpreparesnapshots) Se una copia shadow viene interrotta o ha esito negativo prima di questo punto, al provider non viene data alcuna indicazione fino all'avvio di una nuova copia shadow. Per questo motivo, il provider deve essere preparato per gestire una chiamata out-of-sequence a [**IVssHardwareSnapshotProvider::BeginPrepareSnapshot**](/windows/desktop/api/VsProv/nf-vsprov-ivsshardwaresnapshotprovider-beginpreparesnapshot) in qualsiasi punto. Questa chiamata out-of-sequence rappresenta l'inizio di una nuova sequenza di copia shadow e avrà un nuovo ID set di copie shadow.

 

 



