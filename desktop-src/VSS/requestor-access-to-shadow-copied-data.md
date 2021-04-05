---
description: Al termine della copia shadow, il meccanismo più importante per ottenere l'accesso ai dati del file che contiene consiste nell'usare l'oggetto dispositivo della copia shadow.
ms.assetid: 21efdbd6-a487-4e6f-8e3c-b9224bcf92da
title: Accesso del richiedente ai dati copiati in Shadow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6265586f70054277170b44f23efc52d56842e3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131266"
---
# <a name="requester-access-to-shadow-copied-data"></a>Accesso del richiedente ai dati copiati in Shadow

Al termine della copia shadow, il meccanismo più importante per ottenere l'accesso ai dati del file che contiene consiste nell'usare l' [*oggetto dispositivo*](vssgloss-d.md)della copia shadow.

Il **membro \_ pwszSnapshotDeviceObject m** di una [**struttura \_ \_ prop snapshot VSS**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) è una stringa che contiene un oggetto dispositivo del volume copiato dall'ombreggiatura. Un richiedente può ottenere un oggetto **\_ \_ prop dello snapshot VSS** del volume copiato shadow se conosce l' **\_ ID VSS** del volume (GUID di identificazione) e lo passa a [**IVssBackupComponents:: GetSnapshotProperties**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getsnapshotproperties).

Un richiedente può anche ottenere informazioni sulle proprietà della copia shadow usando il membro **obj. snap** della [**struttura \_ \_ prop dell'oggetto VSS**](/windows/desktop/api/Vss/ns-vss-vss_object_prop) (ovvero una struttura di [**\_ \_ prop snapshot VSS**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) ) ottenuta usando [**IVssEnumObject**](/windows/desktop/api/Vss/nn-vss-ivssenumobject) per eseguire l'iterazione dell'elenco di oggetti restituiti da una chiamata a [**IVssBackupComponents:: query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query).

L'oggetto dispositivo deve essere interpretato come la radice di un volume copiato Shadow. Per questo motivo, l'oggetto dispositivo non contiene la barra rovesciata (" \\ ").

I percorsi nel volume copiato shadow vengono ottenuti sostituendo la radice del percorso originale con l'oggetto dispositivo. Se, ad esempio, si specifica un percorso nel volume originale di "C: \\ database \\ \* . mdb" e un'istanza della [**\_ \_ prop snapshot VSS**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) di snapProp, è possibile ottenere il percorso nel volume copiato Shadow concatenando snapPropm \_ pwszShadow copyDeviceObject, " \\ " e " \\ database \\ \* . mdb".

I set di file VSS potrebbero contenere caratteri jolly nei relativi descrittori di file. Pertanto, il recupero di un elenco completo dei file in una copia shadow gestita da un componente potrebbe richiedere l'uso di metodi come **FindFileFirst**, **FindFileFirstEx** e **FindNextFile**.

 

 



