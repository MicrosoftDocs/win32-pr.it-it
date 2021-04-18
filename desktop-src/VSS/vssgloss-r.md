---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 2442a788-2e70-44c1-9c38-901c1c18a742
title: R (Servizio Copia Shadow del volume)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5846454ef5d58acf8f1c546b5e1bbce379d0b103
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307145"
---
# <a name="r-volume-shadow-copy-service"></a>R (Servizio Copia Shadow del volume)

[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [d](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [i](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q R [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z

<dl> <dt>

<span id="base.vssgloss_requester"></span><span id="BASE.VSSGLOSS_REQUESTER"></span>**richiedente**
</dt> <dd>

Almeno, qualsiasi processo che interagisce con VSS per creare e gestire copie shadow e set di copie shadow di uno o più volumi.

In genere, un richiedente gestisce le copie shadow per supportare altre funzionalità, ad esempio le operazioni di backup e ripristino e il mirroring del disco. Vedere anche [*Copia Shadow*](vssgloss-s.md), [*set di copie shadow*](vssgloss-s.md).

</dd> <dt>

<span id="base.vssgloss_restore_method"></span><span id="BASE.VSSGLOSS_RESTORE_METHOD"></span>**Metodo Restore**
</dt> <dd>

Specifica del metodo del processo di ripristino. Consente di controllare problemi quali il fatto che i file vengano sovrascritti durante il ripristino. Se un'impostazione del metodo Restore è in conflitto con quelle della destinazione Restore, la destinazione Restore avrà la precedenza. Vedere anche *destinazione di ripristino*.

</dd> <dt>

<span id="base.vssgloss_restore_target"></span><span id="BASE.VSSGLOSS_RESTORE_TARGET"></span>**destinazione ripristino**
</dt> <dd>

In VSS, una destinazione di ripristino è una specifica del modo in cui un richiedente deve ripristinare un file, ad esempio se deve sovrascrivere i file esistenti.

</dd> </dl>

 

 



