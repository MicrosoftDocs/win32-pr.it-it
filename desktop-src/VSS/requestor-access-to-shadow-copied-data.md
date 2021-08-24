---
description: Al termine della copia shadow, il meccanismo più importante per ottenere l'accesso ai dati del file in essa contenuti è l'uso dell'oggetto dispositivo della copia shadow.
ms.assetid: 21efdbd6-a487-4e6f-8e3c-b9224bcf92da
title: Accesso del richiedente ai dati copiati shadow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 779e3947adff28c8f3190026921c398677afc7efaa484903bf165250f41bc191
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119767701"
---
# <a name="requester-access-to-shadow-copied-data"></a>Accesso del richiedente ai dati copiati shadow

Al termine della copia shadow, il meccanismo più importante per ottenere l'accesso ai dati del file in essa contenuti è l'uso dell'oggetto dispositivo [*della copia shadow.*](vssgloss-d.md)

Il **membro m \_ pwszSnapshotDeviceObject** di una struttura [**VSS SNAPSHOT \_ \_ PROP**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) è una stringa contenente l'oggetto dispositivo di un volume copiato in modo shadow. Un richiedente può ottenere l'oggetto **VSS \_ SNAPSHOT \_ PROP** di un volume copiato tramite shadow se conosce l'ID **VSS \_** del volume (GUID di identificazione) e lo passa a [**IVssBackupComponents::GetSnapshotProperties**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getsnapshotproperties).

Un richiedente può anche ottenere informazioni sulla proprietà della copia shadow usando il membro **Obj.Snap** della struttura VSS OBJECT PROP (ovvero una struttura [**VSS \_ SNAPSHOT \_**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) [**\_ \_ PROP)**](/windows/desktop/api/Vss/ns-vss-vss_object_prop) ottenuta usando [**IVssEnumObject**](/windows/desktop/api/Vss/nn-vss-ivssenumobject) per scorrere l'elenco di oggetti restituiti da una chiamata a [**IVssBackupComponents::Query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query).

L'oggetto dispositivo deve essere interpretato come la radice di un volume copiato shadow. Per questo motivo, l'oggetto dispositivo non contiene barre rovesciate (" \\ ").

I percorsi nel volume copiato shadow vengono ottenuti sostituendo la radice del percorso originale con l'oggetto dispositivo. Ad esempio, dato un percorso nel volume originale di "C: DATABASE .mdb" e un'istanza VSS SNAPSHOT PROP di snapProp, è possibile ottenere il percorso sul \\ \\ \* volume copiato shadow concatenando snapPropm [**\_ \_**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) \_ pwszShadow copyDeviceObject, " \\ " e " DATABASE \\ \\ \* .mdb".

I set di file VSS potrebbero contenere caratteri jolly nei relativi descrittori di file, pertanto per ottenere un elenco completo dei file in una copia shadow gestita da un componente potrebbe essere necessario usare metodi come **FindFileFirst,** **FindFileFirstEx** e **FindNextFile**.

 

 



