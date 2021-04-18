---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 7eb1d433-21db-45cc-a141-13a89993e30c
title: E (Servizio Copia Shadow del volume)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e97425100d8e2e3d0add6ea0e6fd1de67bc6f4ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307149"
---
# <a name="e-volume-shadow-copy-service"></a>E (Servizio Copia Shadow del volume)

[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [d](vssgloss-d.md) E [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [i](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z

<dl> <dt>

<span id="base.vssgloss_explicit_component_inclusion"></span><span id="BASE.VSSGLOSS_EXPLICIT_COMPONENT_INCLUSION"></span>**inclusione componente esplicito**
</dt> <dd>

Aggiunta delle informazioni di un componente al documento dei componenti di backup di un richiedente quando partecipa a un'operazione di backup o ripristino. I richiedenti usano [**IVssBackupComponents:: AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) per includere in modo esplicito un componente in un'operazione di backup e [**IVssBackupComponents:: SetSelectedForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore) o [**IVssBackupComponents:: AddRestoreSubcomponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addrestoresubcomponent) per includere in modo esplicito un componente in un'operazione di ripristino.

Se viene eseguito il backup o il ripristino di un componente di un writer, tutti i componenti non selezionabili senza alcun predecessore selezionabile devono essere inclusi in modo esplicito in un'operazione di backup o ripristino.

I componenti selezionabili senza predecessori selezionabili scelti da un richiedente per la partecipazione a un backup o un ripristino devono essere inclusi in modo esplicito nell'operazione.

I componenti non selezionabili con un predecessore selezionabile non sono mai inclusi in modo esplicito.

I componenti selezionabili con un predecessore selezionabile possono essere inclusi in modo esplicito oppure possono essere inclusi in modo implicito se il predecessore è incluso in modo esplicito.

</dd> <dt>

<span id="base.vssgloss_exposed_shadow_copy"></span><span id="BASE.VSSGLOSS_EXPOSED_SHADOW_COPY"></span>**copia shadow esposta**
</dt> <dd>

Copia shadow del volume montata in un sistema e disponibile per processi diversi da quello che la gestisce. Un volume di copia Shadow montato sotto una lettera di unità o un percorso di directory viene definito "esposto localmente". Un volume di copia shadow accessibile tramite una condivisione (ad eccezione delle copie shadow accessibili dal client) viene definito "esposto in modalità remota". Tutte le copie shadow esposte sono anche copie shadow di superficie. Vedere anche [*Copia Shadow accessibile dal client*](vssgloss-c.md), [*Copia Shadow*](vssgloss-s.md).

</dd> </dl>

 

 



