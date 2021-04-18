---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 26e7eaae-f540-47d1-99ec-6af0fd223039
title: D (Servizio Copia Shadow del volume)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b25af02bd43c5130fa7ce60ed08ec4ab822ff1de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307151"
---
# <a name="d-volume-shadow-copy-service"></a>D (Servizio Copia Shadow del volume)

[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) d [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [i](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z

<dl> <dt>

<span id="base.vssgloss_database_component"></span><span id="BASE.VSSGLOSS_DATABASE_COMPONENT"></span>**componente di database**
</dt> <dd>

Gruppo di file utilizzato da un database e definito da un writer che deve essere gestito come un'unità durante le operazioni di backup e ripristino. Vedere anche [*componente*](vssgloss-c.md), [*componente del gruppo di file*](vssgloss-f.md).

</dd> <dt>

<span id="base.vssgloss_default_provider"></span><span id="BASE.VSSGLOSS_DEFAULT_PROVIDER"></span>**provider predefinito**
</dt> <dd>

Vedere [*provider di sistema*](vssgloss-s.md).

</dd> <dt>

<span id="base.vssgloss_deleted_shadow_copy"></span><span id="BASE.VSSGLOSS_DELETED_SHADOW_COPY"></span>**copia shadow eliminata**
</dt> <dd>

Le copie shadow eliminate non sono accessibili e non devono essere rese accessibili in qualsiasi momento in futuro.

</dd> <dt>

<span id="base.vssgloss_dependency"></span><span id="BASE.VSSGLOSS_DEPENDENCY"></span>**dipendenza**
</dt> <dd>

Vedere [*dipendenza Component*](vssgloss-c.md).

</dd> <dt>

<span id="base.vssgloss_device_object"></span><span id="BASE.VSSGLOSS_DEVICE_OBJECT"></span>**oggetto dispositivo**
</dt> <dd>

Stringa che indica la "radice" di un volume copiato da un'ombreggiatura. È possibile fare riferimento ai file e alle directory in un volume copiato da un'ombreggiatura anteponendo la stringa dell'oggetto dispositivo a un percorso corrispondente nel volume originale. Come ottenuto come membro **\_ pwszSnapshotDeviceObject** della struttura di [**\_ \_ prop snapshot VSS**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) , l'oggetto dispositivo non dispone di una barra rovesciata (" \\ ").

</dd> <dt>

<span id="base.vssgloss_diff_area"></span><span id="BASE.VSSGLOSS_DIFF_AREA"></span>**area diff**
</dt> <dd>

Posizione del volume in cui sono archiviati i *dati differenziali* . Questa operazione è nota anche come spazio di archiviazione della copia shadow.

</dd> <dt>

<span id="base.vssgloss_differenced_files"></span><span id="BASE.VSSGLOSS_DIFFERENCED_FILES"></span>**file differenziati**
</dt> <dd>

File interessati da un'operazione di backup incrementale o differenziale implementata aggiornando interi file, anziché modificare le sezioni di tali file mediante il supporto di file parziali. Ad esempio, se per implementare un backup differenziale un intero file, anziché solo la sezione modificata, viene copiato in un supporto di backup, tale file è un file differenziato. Vedere anche [*operazioni di backup incrementali*](vssgloss-i.md), *operazioni di backup differenziali*, [*supporto file parziale*](vssgloss-p.md).

</dd> <dt>

<span id="base.vssgloss_differential_backup_operations"></span><span id="BASE.VSSGLOSS_DIFFERENTIAL_BACKUP_OPERATIONS"></span>**operazioni di backup differenziale**
</dt> <dd>

Un'operazione di backup o ripristino è stata eseguita solo su file creati o modificati dopo il salvataggio dell'ultimo backup completo. Vedere anche [*operazioni di backup incrementali*](vssgloss-i.md), [*supporto di file parziali*](vssgloss-p.md), *file differenziati*.

</dd> <dt>

<span id="base.vssgloss_differential_data"></span><span id="BASE.VSSGLOSS_DIFFERENTIAL_DATA"></span>**dati differenziali**
</dt> <dd>

Dati che possono essere applicati a un volume originale per generare un volume di copia shadow. Questa operazione è nota anche come dati Copy-on-Write, ma in questa documentazione viene usato il termine dati differenziali.

</dd> <dt>

<span id="base.vssgloss_directed_targeting"></span><span id="BASE.VSSGLOSS_DIRECTED_TARGETING"></span>**destinazione diretta**
</dt> <dd>

Modalità di ripristino in base alla quale un writer indica che quando un file deve essere ripristinato, è necessario rimappare il file di origine. Il file può essere ripristinato in un nuovo percorso di ripristino e/o intervalli di dati ripristinati con un offset diverso con il percorso di ripristino.

</dd> </dl>

 

 



