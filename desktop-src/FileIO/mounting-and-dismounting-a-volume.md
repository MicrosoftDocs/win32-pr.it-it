---
description: La creazione di una cartella montata è un processo in due passaggi.
ms.assetid: 02ecdf93-1133-48af-a6c9-52142256673f
title: Creazione di cartelle montate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d3067af38a893085adcc407263711c80a64c3eea1e535f6814db2cd2742f899
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119650231"
---
# <a name="creating-mounted-folders"></a>Creazione di cartelle montate

La creazione di una cartella montata è un processo in due passaggi. Chiamare innanzitutto [**GetVolumeNameForVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumenameforvolumemountpointw) con il punto di montaggio (lettera di unità, percorso GUID del volume o cartella montata) del volume da assegnare alla cartella montata. Usare quindi la [**funzione SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) per associare il percorso GUID del volume restituito alla directory desiderata in un altro volume. Per codice di esempio, vedere [Creazione di una cartella montata](mounting-a-volume-at-a-mount-point.md).

L'applicazione può designare qualsiasi directory vuota in un volume diverso dalla radice come cartella montata. Quando si chiama la [**funzione SetVolumeMountPoint,**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) tale directory diventa la cartella montata. È possibile assegnare lo stesso volume a più cartelle montate.

Dopo che la cartella montata è stata stabilita, viene mantenuta tramite il riavvio automatico del computer.

Se un volume ha esito negativo, tutti i volumi assegnati alle cartelle montate in tale volume non sono più accessibili tramite tali cartelle montate. Si supponga, ad esempio, di avere due volumi, C: e D:, e che D: sia associato alla cartella montata C: \\ MountD \\ . Se il volume C: ha esito negativo, il volume D: non è più accessibile tramite il percorso C: \\ MountD \\ .

Solo i volumi file system NTFS possono avere cartelle montate, ma i volumi di destinazione per le cartelle montate possono essere volumi non NTFS.

Le cartelle montate vengono implementate usando reparse point e sono soggette alle relative restrizioni. Per altre informazioni, vedere [Reparse Points](reparse-points.md). Non è necessario modificare i reparse point per usare le cartelle montate. Le funzioni come [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) gestiscono automaticamente tutti i dettagli del reparse point.

Poiché le cartelle montate sono directory, è possibile rinominarle, rimuoverle, spostarle e modificarle in altro modo, come si farebbe con altre directory.

Nota: la documentazione di TechNet usa il termine *unità montate* per fare riferimento *alle cartelle montate.*

 

 



