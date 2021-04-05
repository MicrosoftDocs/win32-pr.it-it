---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: d6528e81-2082-4180-a21e-d12ffe3c9c9c
title: C (Servizio Copia Shadow del volume)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f4f66a29a64e85418767fe561d0068cdcce381a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751554"
---
# <a name="c-volume-shadow-copy-service"></a>C (Servizio Copia Shadow del volume)

[A](vssgloss-a.md) [B](vssgloss-b.md) C [d](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [i](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z

<dl> <dt>

<span id="base.vssgloss_certification_authority"></span><span id="BASE.VSSGLOSS_CERTIFICATION_AUTHORITY"></span>**autorità di certificazione**
</dt> <dd>

Entità considerata attendibile per emettere certificati che dichiara che il destinatario, il computer o l'organizzazione che richiede il certificato soddisfa le condizioni di un criterio stabilito.

</dd> <dt>

<span id="base.vssgloss_client_accessible_shadow_copy"></span><span id="BASE.VSSGLOSS_CLIENT_ACCESSIBLE_SHADOW_COPY"></span>**copia shadow accessibile dal client**
</dt> <dd>

Copia shadow creata dal provider di sistema per supportare copie shadow per cartelle condivise e altri meccanismi di rollback, che consentono ai client di visualizzare le versioni precedenti dei file e di annullare gli errori senza richiedere un ripristino completo. Viene creata una copia shadow accessibile dal client usando il **valore \_ \_ \_ accessibile del client VSS CTX** dell'enumerazione del [**\_ \_ \_ contesto dello snapshot VSS**](/windows/desktop/api/Vss/ne-vss-vss_snapshot_context) . Inoltre, il \_ \_ valore accessibile del client VSS VolSnap attr \_ \_ dell'enumerazione degli [**\_ \_ attributi degli \_ snapshot \_ del volume VSS**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes) viene impostato automaticamente per le copie shadow accessibili dal client. Vedere anche [*copie shadow per cartelle condivise*](vssgloss-s.md).

</dd> <dt>

<span id="base.vssgloss_component"></span><span id="BASE.VSSGLOSS_COMPONENT"></span>**componente**
</dt> <dd>

Gruppo di file, definito da un writer, che deve essere gestito come un'unità durante le operazioni di backup e ripristino. Vedere anche componente del [*database*](vssgloss-d.md), [*componente del gruppo di file*](vssgloss-f.md).

</dd> <dt>

<span id="base.vssgloss_component_dependency"></span><span id="BASE.VSSGLOSS_COMPONENT_DEPENDENCY"></span>**dipendenza componente**
</dt> <dd>

Una situazione in cui un componente (e il set di componenti che definisce) gestito da un writer non può essere eseguito il backup o il ripristino indipendentemente dai componenti gestiti da altri writer. Una dipendenza non indica un ordine di preferenza tra il componente con le dipendenze documentate e i componenti da cui dipende: una dipendenza indica semplicemente che il componente e i componenti da cui dipende devono essere sempre sottoposti a backup o ripristino contemporaneamente.

</dd> <dt>

<span id="base.vssgloss_component_mode"></span><span id="BASE.VSSGLOSS_COMPONENT_MODE"></span>**modalità componente**
</dt> <dd>

Modalità in cui un'operazione di backup o ripristino usa le informazioni sul componente di un writer. Vedere anche [*componente selezionabile*](vssgloss-s.md).

</dd> <dt>

<span id="base.vssgloss_component_set"></span><span id="BASE.VSSGLOSS_COMPONENT_SET"></span>**set di componenti**
</dt> <dd>

Gruppo di componenti con almeno un componente selezionabile (per il backup o il ripristino) e un numero di componenti non selezionabili organizzati in una gerarchia in base ai relativi percorsi logici. La partecipazione implicita a un'operazione di backup o ripristino dipende dall'inclusione esplicita del componente selezionabile di primo livello. Solo le informazioni sul componente di questo componente selezionabile sono incluse nel documento componenti di backup. Un set di componenti può includere sottocomponenti selezionabili e non selezionabili. Vedere anche [*percorso logico*](vssgloss-l.md), [*componente selezionabile*](vssgloss-s.md).

</dd> <dt>

<span id="base.vssgloss_copy_on_write_shadow_copy"></span><span id="BASE.VSSGLOSS_COPY_ON_WRITE_SHADOW_COPY"></span>**copia shadow copia su scrittura**
</dt> <dd>

Copia shadow creata salvando solo le differenze rispetto al volume originale.

</dd> <dt>

<span id="base.vssgloss_crash_consistent_state"></span><span id="BASE.VSSGLOSS_CRASH_CONSISTENT_STATE"></span>**stato di arresto anomalo del sistema**
</dt> <dd>

Stato dei dischi equivalente a quello che verrebbe rilevato in seguito a un errore irreversibile che arresta improvvisamente il sistema. Un ripristino da un set di copie shadow di questo tipo sarebbe equivalente a un riavvio dopo un arresto improvviso. Si tratta dello stato predefinito dei dati che sono stati replicati senza il supporto dei writer.

</dd> </dl>

 

 



