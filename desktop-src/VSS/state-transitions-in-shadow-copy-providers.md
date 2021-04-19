---
description: 'Il modello di transizione dello stato in un provider di copie shadow è semplificato dalla serializzazione della creazione della copia shadow dal momento in cui viene chiamato IVssBackupComponents:: StartSnapshotSet finché la chiamata a IVssBackupComponents::D oSnapshotSet restituisce.'
ms.assetid: 5dbf0fb3-53cb-4532-9a8f-bd955afe16c4
title: Transizioni di stato nei provider di copie shadow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d628d11419158f947225b2e4cabd7f93975f421
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311844"
---
# <a name="state-transitions-in-shadow-copy-providers"></a>Transizioni di stato nei provider di copie shadow

Il modello di transizione dello stato in un provider di copie shadow è semplificato dalla serializzazione della creazione della copia shadow dal momento in cui viene chiamato [**IVssBackupComponents:: StartSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset) finché la chiamata a [**IVssBackupComponents::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) restituisce. Se un altro richiedente tenta di creare una copia shadow durante questo periodo di tempo, la chiamata a **StartSnapshotSet** avrà esito negativo con errore **VSS \_ e \_ \_ set \_ di snapshot in \_ corso, a** indicare che il secondo richiedente deve attendere e riprovare.

VSS chiamerà solo [**IVssProviderCreateSnapshotSet:: AbortSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-abortsnapshots) dopo che il richiedente ha chiamato [**DoSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset), anche se la copia shadow ha esito negativo o viene interrotta prima di questo punto. Questo significa che un provider non riceverà una chiamata a **AbortSnapshots** fino a quando non viene chiamato [**IVssProviderCreateSnapshotSet:: EndPrepareSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-endpreparesnapshots) . Se una copia shadow viene interrotta o ha esito negativo prima di questo punto, al provider non viene fornita alcuna indicazione fino a quando non viene avviata una nuova copia shadow. Per questo motivo, il provider deve essere preparato a gestire una chiamata out-of-Sequence a [**IVssHardwareSnapshotProvider:: BeginPrepareSnapshot**](/windows/desktop/api/VsProv/nf-vsprov-ivsshardwaresnapshotprovider-beginpreparesnapshot) in qualsiasi momento. Questa chiamata fuori sequenza rappresenta l'inizio di una nuova sequenza di copia shadow e avrà un nuovo ID del set di copie shadow.

 

 



