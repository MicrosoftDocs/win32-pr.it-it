---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: c4f826bc-ea80-4fd5-99da-630e7ae56dd7
title: S (Servizio Copia Shadow del volume)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb5979d30f0b88762a2d022a89063ee44bd91a3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307144"
---
# <a name="s-volume-shadow-copy-service"></a>S (Servizio Copia Shadow del volume)

[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [d](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [i](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) S [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z

<dl> <dt>

<span id="base.vssgloss_selectability_for_backup"></span><span id="BASE.VSSGLOSS_SELECTABILITY_FOR_BACKUP"></span>**selezione per il backup**
</dt> <dd>

Un componente viene definito selezionabile per il backup se l'inclusione esplicita in un'operazione di backup è facoltativa. La selezione per il backup è abilitata se il valore del membro **bSelectable** della [**struttura \_ COMPONENTINFO VSS**](/windows/desktop/api/VsBackup/ns-vsbackup-vss_componentinfo) è **true**. Non esiste alcun valore predefinito per la selezione di un componente per il backup; un writer deve sempre impostare questo valore in modo esplicito.

I writer utilizzano inoltre la selezione per il ripristino per organizzare la partecipazione del componente alle operazioni di ripristino.

Vedere anche *componente selezionabile*, *selezione per ripristino*, [*inclusione componente esplicita*](vssgloss-e.md), [*inclusione componente implicito*](vssgloss-i.md).

</dd> <dt>

<span id="base.vssgloss_selectability_for_restore"></span><span id="BASE.VSSGLOSS_SELECTABILITY_FOR_RESTORE"></span>**selezione per il ripristino**
</dt> <dd>

Un componente viene definito selezionabile per il ripristino se è possibile eseguirne il backup in modo implicito come parte di un set di componenti e successivamente ripristinato singolarmente senza il resto del set di componenti. La selezione per il ripristino è abilitata se il valore del membro **bSelectableForRestore** della [**struttura \_ COMPONENTINFO VSS**](/windows/desktop/api/VsBackup/ns-vsbackup-vss_componentinfo) è **true**. Per impostazione predefinita, la selezione di un componente per il ripristino è **false**. La selezione per il ripristino ha un significato solo quando un componente non è stato aggiunto al documento di backup.

Vedere anche *componente selezionabile*, *selezione per backup*, [*inclusione componente esplicita*](vssgloss-e.md), [*inclusione componente implicito*](vssgloss-i.md).

</dd> <dt>

<span id="base.vssgloss_selectable_component"></span><span id="BASE.VSSGLOSS_SELECTABLE_COMPONENT"></span>**componente selezionabile**
</dt> <dd>

Un componente viene definito selezionabile se la relativa inclusione esplicita in un'operazione di backup o ripristino è facoltativa.

La selezione per il backup e la selezione per il ripristino sono indipendenti tra loro: è possibile selezionare un componente per entrambe le operazioni, per il ripristino e non per il backup o per il backup e non per il ripristino.

I writer utilizzano anche la selezione per organizzare i componenti in gruppi:

-   I componenti non selezionabili senza predecessori selezionabili nei percorsi logici devono essere sempre inclusi in modo esplicito se è necessario eseguire il backup o il ripristino di un writer.
-   I componenti non selezionabili con i predecessori selezionabili verranno inclusi solo in un backup o un ripristino se è incluso almeno un predecessore selezionabile.
-   I componenti selezionabili senza predecessori selezionabili possono essere inclusi solo in un'operazione di backup o ripristino in modo esplicito.
-   I componenti selezionabili con i predecessori selezionabili possono essere inclusi in modo esplicito in un'operazione di backup o ripristino oppure possono essere inclusi implicitamente se uno dei relativi predecessori selezionabili è incluso.

Vedere anche [*componenti*](vssgloss-c.md), *selezione per il backup*, *selezione per il ripristino*, [*inclusione di componenti espliciti*](vssgloss-e.md), [*inclusione di componenti impliciti*](vssgloss-i.md).

</dd> <dt>

<span id="base.vssgloss_shadow_copy"></span><span id="BASE.VSSGLOSS_SHADOW_COPY"></span>**copia shadow**
</dt> <dd>

Replica temporizzata di sola lettura del contenuto di un volume originale. Ogni copia shadow è codificata da un GUID permanente. Detto anche copia shadow del volume. Vedere anche *set di copie shadow*.

</dd> <dt>

<span id="base.vssgloss_shadow_copies_for_shared_folders"></span><span id="BASE.VSSGLOSS_SHADOW_COPIES_FOR_SHARED_FOLDERS"></span>**copie shadow per cartelle condivise**
</dt> <dd>

Funzionalità di Windows che consente di creare copie di backup leggere in linea dei volumi con VSS. I client possono accedere a questi backup tramite la shell di Windows per visualizzare le versioni precedenti dei file e annullare gli errori senza richiedere un ripristino completo. Vedere anche [*Copia Shadow accessibile dal client*](vssgloss-c.md).

</dd> <dt>

<span id="base.vssgloss_shadow_copy_set"></span><span id="BASE.VSSGLOSS_SHADOW_COPY_SET"></span>**set di copie shadow**
</dt> <dd>

Raccolta di copie shadow del volume create contemporaneamente e identificate da un valore di ID del set di copie shadow comune (un GUID permanente). Si tratta del meccanismo utilizzato per consentire la gestione di un'operazione di copia shadow tra i volumi. Vedere anche *Copia Shadow*.

</dd> <dt>

<span id="base.vssgloss_software_based_provider"></span><span id="BASE.VSSGLOSS_SOFTWARE_BASED_PROVIDER"></span>**provider software**
</dt> <dd>

Provider che intercetta le richieste di I/O a livello di software tra il file system e il gestore dei volumi. Vedere anche [*provider hardware*](vssgloss-h.md), [*provider*](vssgloss-p.md).

</dd> <dt>

<span id="base.vssgloss_subcomponent"></span><span id="BASE.VSSGLOSS_SUBCOMPONENT"></span>**sottocomponente**
</dt> <dd>

Qualsiasi componente con un percorso logico contenente un componente padre selezionabile (per il backup o il ripristino). I sottocomponenti devono avere un percorso logico nel formato { \_ nome componente} \\ {nome sottocomponente \_ }. Se il predecessore selezionabile di un sottocomponente (per backup o ripristino) viene incluso in modo esplicito in un backup o un ripristino, il sottocomponente viene incluso in modo implicito nell'operazione. I sottocomponenti inclusi in modo implicito non dispongono di dati inclusi nel documento componenti di backup, indipendentemente dal fatto che siano selezionabili (per il ripristino o il backup). Vedere anche [*componente*](vssgloss-c.md), [*percorso logico*](vssgloss-l.md).

</dd> <dt>

<span id="base.vssgloss_surfaced_shadow_copy"></span><span id="BASE.VSSGLOSS_SURFACED_SHADOW_COPY"></span>**copia shadow di superficie**
</dt> <dd>

Volume replicato nascosto visibile allo spazio dei nomi del gestore di montaggio di un sistema, ovvero **FindFirstVolume** e **FindNextVolume** possono trovarlo e vengono generate le notifiche di arrivo e di partenza del volume. Tutte le copie shadow esposte sono anche copie shadow di superficie. Tuttavia, non è necessario esporre una copia shadow di superficie. Se una copia shadow è trasportabile, non può essere rilevata. Vedere anche [*Copia Shadow esposta*](vssgloss-e.md), [*copia shadow trasportabile*](vssgloss-t.md).

</dd> <dt>

<span id="base.vssgloss_system_file_protection"></span><span id="BASE.VSSGLOSS_SYSTEM_FILE_PROTECTION"></span>**Protezione file di sistema**
</dt> <dd>

Vedere [*protezione file di Windows*](vssgloss-w.md).

</dd> <dt>

<span id="base.vssgloss_system_level_applications"></span><span id="BASE.VSSGLOSS_SYSTEM_LEVEL_APPLICATIONS"></span>**applicazioni a livello di sistema**
</dt> <dd>

Indica il punto in cui VSS invia una notifica al writer di un blocco. I writer inizializzati come applicazioni a livello di sistema ricevono una notifica dopo che i writer sono stati inizializzati come applicazioni di livello front-end o come applicazioni di livello back-end. Vedere anche il [*livello applicazione*](vssgloss-a.md), [*le applicazioni di livello back-end*](vssgloss-b.md), [*le applicazioni di livello front-end*](vssgloss-f.md).

</dd> <dt>

<span id="base.vssgloss_system_provider"></span><span id="BASE.VSSGLOSS_SYSTEM_PROVIDER"></span>**provider di sistema**
</dt> <dd>

Provider preinstallato predefinito fornito come parte di Windows.

</dd> <dt>

<span id="base.vssgloss_system_volume_folder"></span><span id="BASE.VSSGLOSS_SYSTEM_VOLUME_FOLDER"></span>**Cartella volume di sistema**
</dt> <dd>

Una directory condivisa in cui sono archiviate le copie condivise dei file pubblici di un dominio, ovvero i file replicati tra tutti i controller di dominio del dominio.

</dd> </dl>

 

 



