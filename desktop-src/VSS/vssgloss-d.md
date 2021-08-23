---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 26e7eaae-f540-47d1-99ec-6af0fd223039
title: D (Servizio Copia Shadow del volume)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3910a2fb09688e26b33b586f4558c05cb804688645486dfec751c9839fcff278
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998031"
---
# <a name="d-volume-shadow-copy-service"></a>D (Servizio Copia Shadow del volume)

[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) D [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P Q](vssgloss-p.md) R [S](vssgloss-r.md) [](vssgloss-s.md) [T U](vssgloss-t.md) [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z

<dl> <dt>

<span id="base.vssgloss_database_component"></span><span id="BASE.VSSGLOSS_DATABASE_COMPONENT"></span>**componente di database**
</dt> <dd>

Gruppo di file usati da un database e definiti da un writer che devono essere gestiti come unità durante le operazioni di backup e ripristino. Vedere anche [*componente*](vssgloss-c.md), [*componente del file group*](vssgloss-f.md).

</dd> <dt>

<span id="base.vssgloss_default_provider"></span><span id="BASE.VSSGLOSS_DEFAULT_PROVIDER"></span>**provider predefinito**
</dt> <dd>

Vedere [*provider di sistema*](vssgloss-s.md).

</dd> <dt>

<span id="base.vssgloss_deleted_shadow_copy"></span><span id="BASE.VSSGLOSS_DELETED_SHADOW_COPY"></span>**copia shadow eliminata**
</dt> <dd>

Le copie shadow eliminate non sono affatto accessibili e non devono essere rese accessibili in futuro.

</dd> <dt>

<span id="base.vssgloss_dependency"></span><span id="BASE.VSSGLOSS_DEPENDENCY"></span>**Dipendenza**
</dt> <dd>

Vedere [*Dipendenza del componente*](vssgloss-c.md).

</dd> <dt>

<span id="base.vssgloss_device_object"></span><span id="BASE.VSSGLOSS_DEVICE_OBJECT"></span>**oggetto dispositivo**
</dt> <dd>

Stringa che indica la "radice" di un volume copiato shadow. È possibile fare riferimento a file e directory in un volume shadow copiato anteponendo la stringa dell'oggetto dispositivo a un percorso corrispondente nel volume originale. Come ottenuto come membro **m \_ pwszSnapshotDeviceObject** della struttura [**VSS \_ SNAPSHOT \_ PROP,**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) l'oggetto dispositivo non ha barra rovesciata (" \\ ").

</dd> <dt>

<span id="base.vssgloss_diff_area"></span><span id="BASE.VSSGLOSS_DIFF_AREA"></span>**Area diff**
</dt> <dd>

Posizione nel volume in cui sono *archiviati i dati* differenziali. Questa operazione è nota anche come spazio di archiviazione delle copie shadow.

</dd> <dt>

<span id="base.vssgloss_differenced_files"></span><span id="BASE.VSSGLOSS_DIFFERENCED_FILES"></span>**file con differenze**
</dt> <dd>

File coinvolti in un'operazione di backup incrementale o differenziale implementata aggiornando interi file (anziché modificare sezioni di tali file usando il supporto di file parziali). Ad esempio, se per implementare un backup differenziale un intero file (anziché solo la sezione modificata) viene copiato in un supporto di backup, tale file è un file con differenze. Vedere anche [*operazioni di backup incrementale,*](vssgloss-i.md) *operazioni di backup differenziali,* [*supporto di file parziali.*](vssgloss-p.md)

</dd> <dt>

<span id="base.vssgloss_differential_backup_operations"></span><span id="BASE.VSSGLOSS_DIFFERENTIAL_BACKUP_OPERATIONS"></span>**operazioni di backup differenziali**
</dt> <dd>

Un'operazione di backup o ripristino eseguita solo sui file creati o modificati dopo il salvataggio dell'ultimo backup completo. Vedere anche [*operazioni di backup incrementali,*](vssgloss-i.md) [*supporto parziale dei file,*](vssgloss-p.md) *file con differenze.*

</dd> <dt>

<span id="base.vssgloss_differential_data"></span><span id="BASE.VSSGLOSS_DIFFERENTIAL_DATA"></span>**dati differenziali**
</dt> <dd>

Dati che possono essere applicati a un volume originale per generare un volume di copia shadow. Questi dati sono noti anche come dati di copia in scrittura, ma questa documentazione usa il termine dati differenziali.

</dd> <dt>

<span id="base.vssgloss_directed_targeting"></span><span id="BASE.VSSGLOSS_DIRECTED_TARGETING"></span>**targeting diretto**
</dt> <dd>

Modalità di ripristino in base alla quale un writer indica che, quando un file deve essere ripristinato, deve essere mappato nuovamente (il file di origine). Il file può essere ripristinato in un nuovo percorso di ripristino e/o in intervalli dei dati ripristinati in un offset diverso con il percorso di ripristino.

</dd> </dl>

 

 



