---
description: La creazione di una cartella montata è un processo in due passaggi.
ms.assetid: 02ecdf93-1133-48af-a6c9-52142256673f
title: Creazione di cartelle montate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5d64630716be6e85ac323c80e89dda0500ba6c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319066"
---
# <a name="creating-mounted-folders"></a>Creazione di cartelle montate

La creazione di una cartella montata è un processo in due passaggi. In primo luogo, chiamare [**GetVolumeNameForVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumenameforvolumemountpointw) con il punto di montaggio (lettera di unità, percorso GUID volume o cartella montata) del volume da assegnare alla cartella montata. Usare quindi la funzione [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) per associare il percorso GUID del volume restituito alla directory desiderata in un altro volume. Per un esempio di codice, vedere [creazione di una cartella montata](mounting-a-volume-at-a-mount-point.md).

L'applicazione può designare qualsiasi directory vuota in un volume diverso dalla radice come cartella montata. Quando si chiama la funzione [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) , tale directory diventa la cartella montata. È possibile assegnare lo stesso volume a più cartelle montate.

Una volta stabilita, la cartella montata viene gestita automaticamente tramite il riavvio del computer.

Se si verifica un errore in un volume, non sarà più possibile accedere ai volumi assegnati alle cartelle montate in tale volume tramite le cartelle montate. Si supponga, ad esempio, di avere due volumi, C: e D: e che D: sia associato alla cartella montata C: \\ mountd \\ . Se il volume C: ha esito negativo, non è più possibile accedere al volume D: tramite il percorso C: \\ mountd \\ .

Solo i volumi di file system NTFS possono avere cartelle montate, ma i volumi di destinazione per le cartelle montate possono essere volumi non NTFS.

Le cartelle montate vengono implementate usando i reparse point e sono soggette alle restrizioni. Per ulteriori informazioni, vedere [reparse point](reparse-points.md). Non è necessario modificare i reparse point per usare le cartelle montate; funzioni come [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) gestiscono tutti i dettagli dei reparse point.

Poiché le cartelle montate sono directory, è possibile rinominarle, rimuoverle, spostarle e modificarle in altro modo, come per le altre directory.

Nota: la documentazione di TechNet usa il termine *unità montate* per fare riferimento alle *cartelle montate*.

 

 



