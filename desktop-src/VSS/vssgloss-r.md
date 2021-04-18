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
# <a name="r-volume-shadow-copy-service"></a><span data-ttu-id="d8a67-103">R (Servizio Copia Shadow del volume)</span><span class="sxs-lookup"><span data-stu-id="d8a67-103">R (Volume Shadow Copy Service)</span></span>

<span data-ttu-id="d8a67-104">[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [d](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [i](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q R [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="d8a67-104">[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q R [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="d8a67-105"><span id="base.vssgloss_requester"></span><span id="BASE.VSSGLOSS_REQUESTER"></span>**richiedente**</span><span class="sxs-lookup"><span data-stu-id="d8a67-105"><span id="base.vssgloss_requester"></span><span id="BASE.VSSGLOSS_REQUESTER"></span>**requester**</span></span>
</dt> <dd>

<span data-ttu-id="d8a67-106">Almeno, qualsiasi processo che interagisce con VSS per creare e gestire copie shadow e set di copie shadow di uno o più volumi.</span><span class="sxs-lookup"><span data-stu-id="d8a67-106">Minimally, any process that interacts with VSS to create and manage shadow copies and shadow copy sets of one or more volumes.</span></span>

<span data-ttu-id="d8a67-107">In genere, un richiedente gestisce le copie shadow per supportare altre funzionalità, ad esempio le operazioni di backup e ripristino e il mirroring del disco.</span><span class="sxs-lookup"><span data-stu-id="d8a67-107">Typically, a requester manages shadow copies to support some other functionality, such as backup and restore operations and disk mirroring.</span></span> <span data-ttu-id="d8a67-108">Vedere anche [*Copia Shadow*](vssgloss-s.md), [*set di copie shadow*](vssgloss-s.md).</span><span class="sxs-lookup"><span data-stu-id="d8a67-108">See also [*shadow copy*](vssgloss-s.md), [*shadow copy set*](vssgloss-s.md).</span></span>

</dd> <dt>

<span data-ttu-id="d8a67-109"><span id="base.vssgloss_restore_method"></span><span id="BASE.VSSGLOSS_RESTORE_METHOD"></span>**Metodo Restore**</span><span class="sxs-lookup"><span data-stu-id="d8a67-109"><span id="base.vssgloss_restore_method"></span><span id="BASE.VSSGLOSS_RESTORE_METHOD"></span>**restore method**</span></span>
</dt> <dd>

<span data-ttu-id="d8a67-110">Specifica del metodo del processo di ripristino.</span><span class="sxs-lookup"><span data-stu-id="d8a67-110">A specification of the restore process method.</span></span> <span data-ttu-id="d8a67-111">Consente di controllare problemi quali il fatto che i file vengano sovrascritti durante il ripristino.</span><span class="sxs-lookup"><span data-stu-id="d8a67-111">It controls such issues as whether files are overwritten on restore.</span></span> <span data-ttu-id="d8a67-112">Se un'impostazione del metodo Restore è in conflitto con quelle della destinazione Restore, la destinazione Restore avrà la precedenza.</span><span class="sxs-lookup"><span data-stu-id="d8a67-112">If a restore method setting is in conflict with those of the restore target, then the restore target takes precedence.</span></span> <span data-ttu-id="d8a67-113">Vedere anche *destinazione di ripristino*.</span><span class="sxs-lookup"><span data-stu-id="d8a67-113">See also *restore target*.</span></span>

</dd> <dt>

<span data-ttu-id="d8a67-114"><span id="base.vssgloss_restore_target"></span><span id="BASE.VSSGLOSS_RESTORE_TARGET"></span>**destinazione ripristino**</span><span class="sxs-lookup"><span data-stu-id="d8a67-114"><span id="base.vssgloss_restore_target"></span><span id="BASE.VSSGLOSS_RESTORE_TARGET"></span>**restore target**</span></span>
</dt> <dd>

<span data-ttu-id="d8a67-115">In VSS, una destinazione di ripristino è una specifica del modo in cui un richiedente deve ripristinare un file, ad esempio se deve sovrascrivere i file esistenti.</span><span class="sxs-lookup"><span data-stu-id="d8a67-115">Under VSS, a restore target is a specification of how a requester should restore a file, for example, if it should overwrite existing files.</span></span>

</dd> </dl>

 

 



