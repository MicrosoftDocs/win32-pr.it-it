---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: ebf8d0a7-e465-4f9f-9e3d-b97dbcf321b8
title: I (Servizio Copia Shadow del volume)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b043c340de5d1703587b83f72851db76d367832a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751538"
---
# <a name="i-volume-shadow-copy-service"></a>I (Servizio Copia Shadow del volume)

[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [d](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) i J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z

<dl> <dt>

<span id="base.vssgloss_identify_event"></span><span id="BASE.VSSGLOSS_IDENTIFY_EVENT"></span>**Identifica evento**
</dt> <dd>

Evento VSS che indica che un writer o un richiedente deve eseguire una query sul writer corrente. Viene utilizzato per creare le informazioni sui metadati del writer corrente. Vedere anche [*richiedente*](vssgloss-r.md), [*writer*](vssgloss-w.md).

</dd> <dt>

<span id="base.vssgloss_implicit_component_inclusion"></span><span id="BASE.VSSGLOSS_IMPLICIT_COMPONENT_INCLUSION"></span>**inclusione di componenti impliciti**
</dt> <dd>

Non aggiungere le informazioni di un componente al documento dei componenti di backup di un richiedente quando partecipa a un'operazione di backup o ripristino.

I componenti non selezionabili con un predecessore selezionabile sono inclusi implicitamente solo se il relativo predecessore è incluso.

I componenti selezionabili con un predecessore selezionabile possono essere inclusi implicitamente, se il predecessore è incluso, oppure possono essere inclusi in modo esplicito.

I componenti non selezionabili senza predecessori selezionabili non sono mai inclusi in modo implicito in un'operazione di backup o ripristino. tutti questi componenti devono essere aggiunti in modo esplicito al documento componenti di backup se uno dei componenti del writer partecipa.

I componenti selezionabili senza predecessori selezionabili scelti da un richiedente per la partecipazione a un backup o un ripristino non possono essere inclusi in modo implicito nell'operazione, ma devono essere aggiunti esplicitamente al documento componenti di backup.

</dd> <dt>

<span id="base.vssgloss_incremental_backup_operations"></span><span id="BASE.VSSGLOSS_INCREMENTAL_BACKUP_OPERATIONS"></span>**operazioni di backup incrementali**
</dt> <dd>

Un'operazione di backup o ripristino viene eseguita solo su file creati o modificati dopo il salvataggio dell'ultimo backup completo, incrementale o differenziale. Vedere anche [*operazioni di backup differenziali*](vssgloss-d.md).

</dd> </dl>

 

 



