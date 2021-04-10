---
description: Interazioni e comportamenti del provider hardware
ms.assetid: 059968cf-43e5-4442-b757-80afdd66799f
title: Interazioni e comportamenti del provider hardware
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5aa30add6b34a7f3a0c45c88346c32c43e99398e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227041"
---
# <a name="hardware-provider-interactions-and-behaviors"></a>Interazioni e comportamenti del provider hardware

I provider hardware possono supportare le copie shadow del mirroring copy-on-Write e/o di copia completa (differenziale e/o Plex). L'allocazione delle risorse per le copie shadow deve seguire il contesto specificato dal richiedente in [**IVssBackupComponents:: secontext**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setcontext), enumerato dal [**\_ \_ \_ contesto dello snapshot VSS**](/windows/desktop/api/Vss/ne-vss-vss_snapshot_context), per il set di copie shadow.

-   Se il richiedente specifica un contesto di copia shadow supportato dal provider, il provider deve creare una copia shadow usando tale metodo.
-   Se il richiedente specifica un contesto di copia shadow non supportato dal provider, il provider non deve tentare di creare la copia shadow e restituire **false** tramite il parametro *pbIsSupported* in [**IVssHardwareSnapshotProvider:: AreLunsSupported**](/windows/desktop/api/VsProv/nf-vsprov-ivsshardwaresnapshotprovider-arelunssupported).
-   Se il richiedente non specifica in modo esplicito un contesto di copia shadow, il provider deve usare un comportamento predefinito ragionevole per la creazione di copie shadow.

I provider di hardware associati ai sottosistemi RAID SAN devono supportare copie shadow trasportabili per consentire lo spostamento tra gli host in una rete SAN.

I provider hardware in esecuzione su più computer in una rete SAN che gestiscono lo stesso sottosistema RAID non devono coordinarsi tra i provider di una rete SAN. Il coordinatore mantiene lo stato necessario. Sono stati riconosciuti due tipi di stato:

-   Stato necessario per supportare l'accesso ai dati nei volumi contenuti in una copia shadow dell'hardware. Sono inclusi i tag di un volume come di sola lettura o nascosti. Questo stato deve essere sul LUN hardware e viaggiare con il LUN. Questo stato viene mantenuto tra le Epoch di avvio e/o l'individuazione del dispositivo. VSS gestisce questo stato per la durata della copia shadow.
-   Stato necessario per riconoscere un volume specifico come parte di un set di copie shadow. Questo stato viene reso permanente da VSS insieme al richiedente che ha creato originariamente il set di copie shadow.

Per altre informazioni, vedere i seguenti argomenti:

-   [Processo di creazione della copia shadow](the-shadow-copy-creation-process.md)
-   [Comportamenti necessari per i provider di copie shadow](required-behaviors-for-shadow-copy-providers.md)
-   [Transizioni di stato nei provider di copie shadow](state-transitions-in-shadow-copy-providers.md)
-   [Gestione degli errori nei provider di copie shadow](error-handling-in-shadow-copy-providers.md)

 

 



