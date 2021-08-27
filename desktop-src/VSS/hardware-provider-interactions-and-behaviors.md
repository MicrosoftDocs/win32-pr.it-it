---
description: Interazioni e comportamenti del provider di hardware
ms.assetid: 059968cf-43e5-4442-b757-80afdd66799f
title: Interazioni e comportamenti del provider di hardware
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7c8029b32ee3387b86519da8630d995820bf3dab5da79769ca26f618ef32660
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118122060"
---
# <a name="hardware-provider-interactions-and-behaviors"></a>Interazioni e comportamenti del provider di hardware

I provider hardware possono supportare copie shadow copy-on-write e/o full copy mirror (copie shadow differenziali e/o plex). L'allocazione delle risorse per le copie shadow deve seguire il contesto specificato dal richiedente in [**IVssBackupComponents::SetContext,**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setcontext)enumerato da [**\_ VSS \_ SNAPSHOT \_ CONTEXT,**](/windows/desktop/api/Vss/ne-vss-vss_snapshot_context)per il set di copie shadow.

-   Se il richiedente specifica un contesto di copia shadow supportato dal provider, il provider deve creare una copia shadow usando tale metodo.
-   Se il richiedente specifica un contesto di copia shadow non supportato dal provider, il provider non deve tentare di creare la copia shadow e restituire **FALSE** tramite il *parametro pbIsSupported* in [**IVssHardwareSnapshotProvider::AreLunsSupported**](/windows/desktop/api/VsProv/nf-vsprov-ivsshardwaresnapshotprovider-arelunssupported).
-   Se il richiedente non specifica in modo esplicito un contesto di copia shadow, il provider deve usare un comportamento predefinito ragionevole per la creazione della copia shadow.

I provider hardware associati ai sottosistemi RAID SAN devono supportare copie shadow trasportabili per consentire lo spostamento tra host in una SAN.

I provider di hardware in esecuzione su più computer in una SAN ma che gestiscono lo stesso sottosistema RAID non devono coordinarsi tra i provider in una SAN. Il coordinatore mantiene qualsiasi stato necessario. Vengono riconosciuti due tipi di stato:

-   Stato necessario per supportare l'accesso ai dati ai volumi contenuti in una copia shadow hardware. Ciò include l'assegnazione di tag a un volume come di sola lettura o nascosta. Questo stato deve essere sul LUN hardware e deve essere in viaggio con il LUN. Questo stato viene mantenuto tra epoche di avvio e/o individuazione dei dispositivi. VSS gestisce questo stato per la durata della copia shadow.
-   Stato necessario per riconoscere un volume specifico come parte di un set di copie shadow. Questo stato viene reso persistente da VSS insieme al richiedente che ha originariamente creato il set di copie shadow.

Per altre informazioni, vedere i seguenti argomenti:

-   [Processo di creazione della copia shadow](the-shadow-copy-creation-process.md)
-   [Comportamenti obbligatori per i provider di copie shadow](required-behaviors-for-shadow-copy-providers.md)
-   [Transizioni di stato nei provider di copie shadow](state-transitions-in-shadow-copy-providers.md)
-   [Gestione degli errori nei provider di copie shadow](error-handling-in-shadow-copy-providers.md)

 

 



