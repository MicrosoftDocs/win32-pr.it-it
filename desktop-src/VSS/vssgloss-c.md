---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: d6528e81-2082-4180-a21e-d12ffe3c9c9c
title: C (Servizio Copia Shadow del volume)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e10734fa1676980473b53cb16f5cf1166d5b2ff2813f9bf59159c37116514c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117751447"
---
# <a name="c-volume-shadow-copy-service"></a>C (Servizio Copia Shadow del volume)

[A](vssgloss-a.md) [B](vssgloss-b.md) C [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) T [U](vssgloss-t.md) [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z

<dl> <dt>

<span id="base.vssgloss_certification_authority"></span><span id="BASE.VSSGLOSS_CERTIFICATION_AUTHORITY"></span>**autorità di certificazione**
</dt> <dd>

Entità affidata all'emissione di certificati che attestano che l'utente, il computer o l'organizzazione destinatario che richiede il certificato soddisfa le condizioni di un criterio stabilito.

</dd> <dt>

<span id="base.vssgloss_client_accessible_shadow_copy"></span><span id="BASE.VSSGLOSS_CLIENT_ACCESSIBLE_SHADOW_COPY"></span>**copia shadow accessibile dal client**
</dt> <dd>

Copia shadow creata dal provider di sistema per supportare copie shadow per cartelle condivise e altri meccanismi di rollback, che consentono ai client di visualizzare le versioni precedenti dei file e annullare gli errori senza richiedere un ripristino completo. Una copia shadow accessibile dal client viene creata usando il valore ACCESSIBLE di **VSS \_ CTX \_ CLIENT \_** dell'enumerazione [**\_ VSS \_ SNAPSHOT \_ CONTEXT.**](/windows/desktop/api/Vss/ne-vss-vss_snapshot_context) Inoltre, il valore \_ VSS VOLSNAP ATTR CLIENT ACCESSIBLE dell'enumerazione \_ \_ \_ [**\_ VSS \_ VOLUME SNAPSHOT \_ \_ ATTRIBUTES**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes) viene impostato automaticamente per le copie shadow accessibili dal client. Vedere anche [*copie shadow per cartelle condivise*](vssgloss-s.md).

</dd> <dt>

<span id="base.vssgloss_component"></span><span id="BASE.VSSGLOSS_COMPONENT"></span>**Componente**
</dt> <dd>

Gruppo di file, definito da un writer, che deve essere gestito come unità durante le operazioni di backup e ripristino. Vedere anche [*componente di database*](vssgloss-d.md), componente file [*group.*](vssgloss-f.md)

</dd> <dt>

<span id="base.vssgloss_component_dependency"></span><span id="BASE.VSSGLOSS_COMPONENT_DEPENDENCY"></span>**dipendenza del componente**
</dt> <dd>

Una situazione in cui un componente (e il set di componenti definito) gestito da un writer non può essere sottoposto a backup o ripristino indipendentemente dai componenti gestiti da altri writer. Una dipendenza non indica un ordine di preferenza tra il componente con le dipendenze documentate e i componenti da cui dipende: una dipendenza indica semplicemente che il componente e i componenti da cui dipende devono sempre essere sottoposti a backup o ripristinati insieme.

</dd> <dt>

<span id="base.vssgloss_component_mode"></span><span id="BASE.VSSGLOSS_COMPONENT_MODE"></span>**modalità componente**
</dt> <dd>

Modalità in cui un'operazione di backup o ripristino utilizza le informazioni sui componenti di un writer. Vedere anche [*componente selezionabile.*](vssgloss-s.md)

</dd> <dt>

<span id="base.vssgloss_component_set"></span><span id="BASE.VSSGLOSS_COMPONENT_SET"></span>**set di componenti**
</dt> <dd>

Gruppo di componenti con almeno un componente selezionabile (per il backup o il ripristino) e un numero di componenti non selezionabili organizzati in una gerarchia in base ai relativi percorsi logici. La partecipazione implicita a un'operazione di backup o ripristino dipende dall'inclusione esplicita del componente selezionabile di primo livello. Nel documento Backup Components (Componenti di backup) sono incluse solo le informazioni sui componenti di questo componente selezionabile. Un set di componenti può includere sottocomponenti selezionabili e non selezionabili. Vedere anche [*percorso logico*](vssgloss-l.md), [*componente selezionabile.*](vssgloss-s.md)

</dd> <dt>

<span id="base.vssgloss_copy_on_write_shadow_copy"></span><span id="BASE.VSSGLOSS_COPY_ON_WRITE_SHADOW_COPY"></span>**copia shadow su scrittura**
</dt> <dd>

Copia shadow creata salvando solo le differenze rispetto al volume originale.

</dd> <dt>

<span id="base.vssgloss_crash_consistent_state"></span><span id="BASE.VSSGLOSS_CRASH_CONSISTENT_STATE"></span>**stato coerente con l'arresto anomalo del sistema**
</dt> <dd>

Lo stato dei dischi equivale a quello che verrebbe rilevato in seguito a un errore irreversibile che arresta improvvisamente il sistema. Un ripristino da un set di copie shadow di questo tipo equivale a un riavvio dopo un arresto improvviso. Si tratta dello stato predefinito dei dati di cui è stata creata una copia shadow senza il supporto dei writer.

</dd> </dl>

 

 



