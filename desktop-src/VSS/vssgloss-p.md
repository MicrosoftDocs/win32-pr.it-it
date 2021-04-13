---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 44279c0e-17f4-4109-bc12-af9064cd321e
title: P (Servizio Copia Shadow del volume)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f018a19c1d00ff3c6530e7c45fbca2350df8fec6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526280"
---
# <a name="p-volume-shadow-copy-service"></a>P (Servizio Copia Shadow del volume)

[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [d](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [i](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) P Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z

<dl> <dt>

<span id="base.vssgloss_partial_file_support"></span><span id="BASE.VSSGLOSS_PARTIAL_FILE_SUPPORT"></span>**supporto file parziale**
</dt> <dd>

Capacità di implementare le operazioni di backup modificando le sottosezioni dei file interessati, anziché usare l'intero file. Vedere anche [*targeting diretto*](vssgloss-d.md).

</dd> <dt>

<span id="base.vssgloss_persistent_shadow_copy"></span><span id="BASE.VSSGLOSS_PERSISTENT_SHADOW_COPY"></span>**copia shadow persistente**
</dt> <dd>

Copia shadow che non viene eliminata automaticamente quando il richiedente rilascia un oggetto [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) o quando il computer viene riavviato. Vedere anche [*copia shadow di rilascio automatico*](vssgloss-a.md), [*Copia Shadow*](vssgloss-s.md).

</dd> <dt>

<span id="base.vssgloss_plex"></span><span id="BASE.VSSGLOSS_PLEX"></span>**Plessi**
</dt> <dd>

Un tipo speciale di volume di copia shadow che rappresenta completamente e completamente un volume di copia shadow senza la necessità di un volume originale. Questo è anche noto come mirroring diviso, ma in questa documentazione viene usato il termine Plex.

</dd> <dt>

<span id="base.vssgloss_postrestore_event"></span><span id="BASE.VSSGLOSS_POSTRESTORE_EVENT"></span>**Evento PostRestore**
</dt> <dd>

Evento VSS che indica il completamento di un ripristino VSS.

</dd> <dt>

<span id="base.vssgloss_postsnapshot_event"></span><span id="BASE.VSSGLOSS_POSTSNAPSHOT_EVENT"></span>**Evento PostSnapshot**
</dt> <dd>

Evento VSS che indica che è stata completata una copia shadow. Vedere anche [*Copia Shadow*](vssgloss-s.md).

</dd> <dt>

<span id="base.vssgloss_preparebackup_event"></span><span id="BASE.VSSGLOSS_PREPAREBACKUP_EVENT"></span>**Evento PrepareForBackup**
</dt> <dd>

Evento VSS che indica che sta per essere eseguita un'operazione di backup.

</dd> <dt>

<span id="base.vssgloss_preparesnapshot_event"></span><span id="BASE.VSSGLOSS_PREPARESNAPSHOT_EVENT"></span>**Evento PrepareForSnapshot**
</dt> <dd>

Evento VSS che indica che i writer devono eseguire i passaggi necessari per preparare un'operazione di copia shadow imminente. Vedere anche [*Copia Shadow*](vssgloss-s.md).

</dd> <dt>

<span id="base.vssgloss_prerestore_event"></span><span id="BASE.VSSGLOSS_PRERESTORE_EVENT"></span>**Evento di preripristino**
</dt> <dd>

Evento VSS che indica che sta per essere eseguita un'operazione di ripristino.

</dd> <dt>

<span id="base.vssgloss_provider"></span><span id="BASE.VSSGLOSS_PROVIDER"></span>**provider**
</dt> <dd>

Oggetto sistema operativo che intercetta e gestisce le richieste di I/O per creare e rappresentare copie shadow del volume nel file system. Vedere anche [*provider hardware*](vssgloss-h.md), [*provider di software*](vssgloss-s.md).

</dd> </dl>

 

 



