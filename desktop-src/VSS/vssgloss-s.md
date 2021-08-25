---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: c4f826bc-ea80-4fd5-99da-630e7ae56dd7
title: S (Servizio Copia Shadow del volume)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92843e9277709a1138bc51b403089c932387e1b282e349c7907fc4cde88e9de8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124481"
---
# <a name="s-volume-shadow-copy-service"></a>S (Servizio Copia Shadow del volume)

[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [](vssgloss-o.md) [O P](vssgloss-p.md) Q [R](vssgloss-r.md) S T [U](vssgloss-t.md) [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z

<dl> <dt>

<span id="base.vssgloss_selectability_for_backup"></span><span id="BASE.VSSGLOSS_SELECTABILITY_FOR_BACKUP"></span>**selezionabilità per il backup**
</dt> <dd>

Un componente è detto selezionabile per il backup se la relativa inclusione esplicita in un'operazione di backup è facoltativa. La selezionabilità per il backup è abilitata se il valore del membro **bSelectable** della [**struttura \_ COMPONENTINFO di VSS**](/windows/desktop/api/VsBackup/ns-vsbackup-vss_componentinfo) è **true.** Non esiste alcun valore predefinito per la selezionabilità di un componente per il backup. Un writer deve sempre impostare questo valore in modo esplicito.

I writer usano anche la selezionabilità per il ripristino per organizzare la partecipazione del componente alle operazioni di ripristino.

Vedere anche *componente selezionabile,* selezionabilità per il *ripristino,* [*inclusione esplicita del componente,*](vssgloss-e.md)inclusione [*implicita del componente.*](vssgloss-i.md)

</dd> <dt>

<span id="base.vssgloss_selectability_for_restore"></span><span id="BASE.VSSGLOSS_SELECTABILITY_FOR_RESTORE"></span>**selezionabilità per il ripristino**
</dt> <dd>

Un componente è detto selezionabile per il ripristino se può essere sottoposto a backup implicito come parte di un set di componenti e successivamente ripristinato singolarmente senza il resto del set di componenti. La selezionabilità per il ripristino è abilitata se il valore del membro **bSelectableForRestore** della struttura [**\_ COMPONENTINFO di VSS**](/windows/desktop/api/VsBackup/ns-vsbackup-vss_componentinfo) è **true.** Per impostazione predefinita, la selezionabilità di un componente per il ripristino è **false.** La selezionabilità per il ripristino ha significato solo quando un componente non è stato aggiunto al documento di backup.

Vedere anche *componente selezionabile,* *selezionabilità per il backup,* [*inclusione esplicita del componente,*](vssgloss-e.md)inclusione [*implicita del componente.*](vssgloss-i.md)

</dd> <dt>

<span id="base.vssgloss_selectable_component"></span><span id="BASE.VSSGLOSS_SELECTABLE_COMPONENT"></span>**componente selezionabile**
</dt> <dd>

Un componente è detto selezionabile se la relativa inclusione esplicita in un'operazione di backup o ripristino è facoltativa.

La selezionabilità per il backup e la selezionabilità per il ripristino sono indipendenti l'una dall'altra: un componente può essere selezionabile per entrambe le operazioni, per il ripristino e non per il backup o per il backup e non per il ripristino.

Gli autori usano anche la selezionabilità per organizzare i componenti in gruppi:

-   I componenti non selezionabili senza predecessori selezionabili nei percorsi logici devono sempre essere inclusi in modo esplicito se è necessario eseguire il backup o il ripristino di un writer.
-   I componenti non selezionabili con predecessori selezionabili verranno inclusi in un backup o ripristino solo se è incluso almeno un predecessore selezionabile.
-   I componenti selezionabili senza predecessori selezionabili possono essere inclusi solo in un'operazione di backup o ripristino in modo esplicito.
-   I componenti selezionabili con predecessori selezionabili possono essere inclusi in modo esplicito in un'operazione di backup o ripristino oppure possono essere inclusi in modo implicito se è incluso uno dei relativi predecessori selezionabili.

Vedere anche [*componenti,*](vssgloss-c.md) *selezionabilità per il backup,* *selezionabilità per il* ripristino, [*inclusione esplicita dei componenti,*](vssgloss-e.md) [*inclusione implicita dei componenti.*](vssgloss-i.md)

</dd> <dt>

<span id="base.vssgloss_shadow_copy"></span><span id="BASE.VSSGLOSS_SHADOW_COPY"></span>**copia shadow**
</dt> <dd>

Replica tempor virtuale di sola lettura del contenuto di un volume originale. Ogni copia shadow è impostata su una chiave da un GUID permanente. Chiamata anche copia shadow del volume. Vedere anche *set di copie shadow.*

</dd> <dt>

<span id="base.vssgloss_shadow_copies_for_shared_folders"></span><span id="BASE.VSSGLOSS_SHADOW_COPIES_FOR_SHARED_FOLDERS"></span>**copie shadow per cartelle condivise**
</dt> <dd>

Una funzionalità di Windows che consente di creare copie di backup online leggere dei volumi usando il Servizio Copia Shadow del volume. I client possono accedere a questi backup tramite Windows shell per visualizzare le versioni precedenti dei file e annullare gli errori senza richiedere un ripristino completo. Vedere anche [*Copia shadow accessibile dal client.*](vssgloss-c.md)

</dd> <dt>

<span id="base.vssgloss_shadow_copy_set"></span><span id="BASE.VSSGLOSS_SHADOW_COPY_SET"></span>**set di copie shadow**
</dt> <dd>

Raccolta di copie shadow del volume create contemporaneamente e identificate da un valore comune di ID set di copie shadow (GUID persistente). Si tratta del meccanismo usato per consentire la gestione di un'operazione di copia shadow tra volumi. Vedere anche *copia shadow.*

</dd> <dt>

<span id="base.vssgloss_software_based_provider"></span><span id="BASE.VSSGLOSS_SOFTWARE_BASED_PROVIDER"></span>**provider di software**
</dt> <dd>

Provider che intercetta le richieste di I/O a livello di software tra il file system e gestione volumi. Vedere anche [*provider hardware*](vssgloss-h.md), [*provider*](vssgloss-p.md).

</dd> <dt>

<span id="base.vssgloss_subcomponent"></span><span id="BASE.VSSGLOSS_SUBCOMPONENT"></span>**Sottocomponente**
</dt> <dd>

Qualsiasi componente con un percorso logico contenente un componente padre selezionabile (per il backup o il ripristino). I sottocomponenti devono avere un percorso logico nel formato \_ {nome componente} \\ {nome \_ sottocomponente}. Se il predecessore selezionabile (per il backup o il ripristino) di un sottocomponente viene incluso in modo esplicito in un backup o ripristino, il sottocomponente viene incluso in modo implicito nell'operazione. I sottocomponenti inclusi in modo implicito non includono i dati nel documento dei componenti di backup, indipendentemente dal fatto che siano selezionabili (per il ripristino o il backup) o meno. Vedere anche [*il componente*](vssgloss-c.md), il [*percorso logico*](vssgloss-l.md).

</dd> <dt>

<span id="base.vssgloss_surfaced_shadow_copy"></span><span id="BASE.VSSGLOSS_SURFACED_SHADOW_COPY"></span>**copia shadow con superficie**
</dt> <dd>

Un volume shadow copiato visibile allo spazio dei nomi di Gestione montaggio di un sistema, ovvero **FindFirstVolume** e **FindNextVolume,** può trovarlo e vengono generate le notifiche di arrivo e partenza del volume. Tutte le copie shadow esposte vengono inoltre esposte come copie shadow. Tuttavia, una copia shadow esposta non deve essere esposta. Se una copia shadow è trasportabile, non può essere esondata. Vedere anche [*copia shadow esposta,*](vssgloss-e.md) [*copia shadow trasportabile.*](vssgloss-t.md)

</dd> <dt>

<span id="base.vssgloss_system_file_protection"></span><span id="BASE.VSSGLOSS_SYSTEM_FILE_PROTECTION"></span>**Protezione file di sistema**
</dt> <dd>

Vedere [*Windows Protezione file.*](vssgloss-w.md)

</dd> <dt>

<span id="base.vssgloss_system_level_applications"></span><span id="BASE.VSSGLOSS_SYSTEM_LEVEL_APPLICATIONS"></span>**applicazioni a livello di sistema**
</dt> <dd>

Indica il punto in cui VSS notifica un blocco a un writer. I writer inizializzati come applicazioni a livello di sistema vengono informati dopo che i writer sono stati inizializzati come applicazioni di livello front-end o come applicazioni di livello back-end. Vedere anche [*a livello di*](vssgloss-a.md)applicazione , applicazioni di livello [*back-end*](vssgloss-b.md), [*applicazioni di livello front-end*](vssgloss-f.md).

</dd> <dt>

<span id="base.vssgloss_system_provider"></span><span id="BASE.VSSGLOSS_SYSTEM_PROVIDER"></span>**provider di sistema**
</dt> <dd>

Provider preinstallato predefinito fornito come parte di Windows.

</dd> <dt>

<span id="base.vssgloss_system_volume_folder"></span><span id="BASE.VSSGLOSS_SYSTEM_VOLUME_FOLDER"></span>**Cartella del volume di sistema**
</dt> <dd>

Directory condivisa in cui sono archiviate le copie condivise dei file pubblici di un dominio, ovvero i file replicati tra tutti i controller di dominio nel dominio.

</dd> </dl>

 

 



