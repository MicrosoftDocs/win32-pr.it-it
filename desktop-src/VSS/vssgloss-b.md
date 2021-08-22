---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: d7d9c8bf-993f-469c-aea1-5d86ca856690
title: B (Servizio Copia Shadow del volume)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f20bbe9f858066d7fca09a3f263aa618c79c4174664b9a4e0994c900fb81c75
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998051"
---
# <a name="b-volume-shadow-copy-service"></a>B (Servizio Copia Shadow del volume)

[A](vssgloss-a.md) B [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T U](vssgloss-t.md) [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z

<dl> <dt>

<span id="base.vssgloss_back_end_level_applications"></span><span id="BASE.VSSGLOSS_BACK_END_LEVEL_APPLICATIONS"></span>**applicazioni di livello back-end**
</dt> <dd>

Indica il punto in cui un writer viene informato di un blocco da parte di VSS. I writer inizializzati come applicazioni di livello back-end vengono informati dopo che i writer sono stati inizializzati come applicazioni di livello front-end e prima di quelli inizializzati come applicazioni a livello di sistema. Vedere anche applicazioni a [*livello di*](vssgloss-a.md) [*applicazione, applicazioni front-end,*](vssgloss-f.md) [*applicazioni a livello di sistema,*](vssgloss-s.md) [*writer.*](vssgloss-w.md)

</dd> <dt>

<span id="base.vssgloss_backupcomplete_event"></span><span id="BASE.VSSGLOSS_BACKUPCOMPLETE_EVENT"></span>**Evento BackupComplete**
</dt> <dd>

Evento VSS che indica che un backup vss è stato completato. Questo evento deve essere seguito da un evento BackupShutdown in condizioni normali. Vedere anche *l'evento BackupShutdown*.

</dd> <dt>

<span id="base.vssgloss_backup_components_document"></span><span id="BASE.VSSGLOSS_BACKUP_COMPONENTS_DOCUMENT"></span>**Documento componenti di backup**
</dt> <dd>

Documento XML creato da un richiedente (usando **l'interfaccia IVssBackupComponents)** durante la configurazione di un'operazione di ripristino o backup. Il documento dei componenti di backup contiene un elenco dei componenti inclusi in modo esplicito, da uno o più writer, che partecipano a un'operazione di backup o di ripristino. Non contiene informazioni sui componenti inclusi in modo implicito. Al contrario, un documento di metadati del writer contiene solo i componenti del writer che possono partecipare a un backup.

Un documento dei componenti di backup può essere salvato su disco. Vedere anche [*inclusione esplicita del componente*](vssgloss-e.md), inclusione [*implicita di componenti*](vssgloss-i.md).

</dd> <dt>

<span id="base.vssgloss_backup_set"></span><span id="BASE.VSSGLOSS_BACKUP_SET"></span>**set di backup**
</dt> <dd>

File di cui eseguire il backup. Include i file selezionati in base all'inclusione in un componente, quelli indicati dalle istruzioni include a livello di writer, meno i file che sono stati inclusi in modo esplicito.

</dd> <dt>

<span id="base.vssgloss_backupshutdown_event"></span><span id="BASE.VSSGLOSS_BACKUPSHUTDOWN_EVENT"></span>**Evento BackupShutdown**
</dt> <dd>

Evento VSS che indica che un'applicazione di backup conforme è stata arrestata. In genere, questa operazione è preceduta da un evento BackupComplete. Tuttavia, se un backup viene terminato in modo imprevisto, questo evento può essere generato senza un evento BackupComplete precedente. Vedere anche *Evento BackupComplete*.

</dd> <dt>

<span id="base.vssgloss_backup_stamp"></span><span id="BASE.VSSGLOSS_BACKUP_STAMP"></span>**stamp di backup**
</dt> <dd>

Stringa contenente informazioni su quando è stato eseguito un backup. VSS non pone alcuna restrizione sul formato di questa stringa, ad eccezione del fatto che è intelligibile per tutte le istanze del writer di una determinata classe. Può contenere informazioni su data e ora, numeri di sequenza logici o qualsiasi altra informazione che consenta a un writer della stessa classe di determinare quando è stato eseguito l'ultimo backup.

</dd> </dl>

 

 



