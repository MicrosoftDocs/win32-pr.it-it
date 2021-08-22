---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: ebf8d0a7-e465-4f9f-9e3d-b97dbcf321b8
title: I (Servizio Copia Shadow del volume)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a672a8cd25792dedb6e32e0916e85ddf50634824b00491733e19bab2c30ece4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056174"
---
# <a name="i-volume-shadow-copy-service"></a>I (Servizio Copia Shadow del volume)

[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) I J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T U](vssgloss-t.md) [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z

<dl> <dt>

<span id="base.vssgloss_identify_event"></span><span id="BASE.VSSGLOSS_IDENTIFY_EVENT"></span>**Identificare l'evento**
</dt> <dd>

Evento VSS che indica che un writer o un richiedente deve eseguire query sul writer corrente. Viene usato per costruire le informazioni sui metadati del writer corrente. Vedere anche [*richiedente*](vssgloss-r.md), [*writer*](vssgloss-w.md).

</dd> <dt>

<span id="base.vssgloss_implicit_component_inclusion"></span><span id="BASE.VSSGLOSS_IMPLICIT_COMPONENT_INCLUSION"></span>**inclusione implicita di componenti**
</dt> <dd>

Non aggiungendo le informazioni di un componente al documento dei componenti di backup del richiedente quando partecipa a un'operazione di backup o ripristino.

I componenti non selezionabili con un predecessore selezionabile vengono inclusi in modo implicito solo se il predecessore è incluso.

I componenti selezionabili con un predecessore selezionabile possono essere inclusi in modo implicito, se il predecessore è incluso o possono essere inclusi in modo esplicito.

I componenti non selezionabili senza predecessori selezionabili non vengono mai inclusi in modo implicito in un'operazione di backup o ripristino. Tutti questi componenti devono essere aggiunti in modo esplicito al documento Componenti di backup se fanno parte di uno dei componenti del writer.

I componenti selezionabili senza predecessori selezionabili scelti da un richiedente per la partecipazione a un backup o un ripristino non possono essere inclusi in modo implicito nell'operazione, ma devono essere aggiunti in modo esplicito al documento Componenti di backup.

</dd> <dt>

<span id="base.vssgloss_incremental_backup_operations"></span><span id="BASE.VSSGLOSS_INCREMENTAL_BACKUP_OPERATIONS"></span>**operazioni di backup incrementale**
</dt> <dd>

Un'operazione di backup o ripristino viene eseguita solo sui file creati o modificati dopo il salvataggio dell'ultimo backup completo, incrementale o differenziale. Vedere anche [*operazioni di backup differenziali.*](vssgloss-d.md)

</dd> </dl>

 

 



