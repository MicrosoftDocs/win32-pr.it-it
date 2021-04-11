---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 3e8b9c48-9d2d-4055-b78d-c4a22d780764
title: L (Servizio Copia Shadow del volume)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a568ed662019cbc0f3c0a242faf884df72acb015
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226112"
---
# <a name="l-volume-shadow-copy-service"></a><span data-ttu-id="3fc71-103">L (Servizio Copia Shadow del volume)</span><span class="sxs-lookup"><span data-stu-id="3fc71-103">L (Volume Shadow Copy Service)</span></span>

<span data-ttu-id="3fc71-104">[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [d](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [i](vssgloss-i.md) J K L M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="3fc71-104">[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K L M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="3fc71-105"><span id="base.vssgloss_logical_path"></span><span id="BASE.VSSGLOSS_LOGICAL_PATH"></span>**percorso logico**</span><span class="sxs-lookup"><span data-stu-id="3fc71-105"><span id="base.vssgloss_logical_path"></span><span id="BASE.VSSGLOSS_LOGICAL_PATH"></span>**logical path**</span></span>
</dt> <dd>

<span data-ttu-id="3fc71-106">Meccanismo per la descrizione dei componenti di un writer.</span><span class="sxs-lookup"><span data-stu-id="3fc71-106">A mechanism for describing a writer's components.</span></span> <span data-ttu-id="3fc71-107">Viene usato per esprimere le relazioni tra i componenti, in particolare la gerarchia.</span><span class="sxs-lookup"><span data-stu-id="3fc71-107">It is used to express relationships between components, in particularly their hierarchy.</span></span> <span data-ttu-id="3fc71-108">Ad esempio, se un writer gestisce diversi libri elettronici, potrebbe assegnare i percorsi logici di " \\ eBook \\ Book1" e " \\ eBook \\ book2" ai componenti del gruppo di file che contengono ogni libro.</span><span class="sxs-lookup"><span data-stu-id="3fc71-108">For instance, if a writer managed several electronic books, it might assign logical paths of "\\ebook\\book1" and "\\ebook\\book2" to file group components containing each book.</span></span> <span data-ttu-id="3fc71-109">Quando si specificano sottocomponenti, sono necessari percorsi logici.</span><span class="sxs-lookup"><span data-stu-id="3fc71-109">Logical paths are required when specifying subcomponents.</span></span>

<span data-ttu-id="3fc71-110">Per convenzione, la barra rovesciata " \\ " viene utilizzata per separare gli elementi di un percorso logico.</span><span class="sxs-lookup"><span data-stu-id="3fc71-110">By convention the backslash "\\" is used to separate elements of a logical path.</span></span> <span data-ttu-id="3fc71-111">Oltre a questo, non esistono restrizioni sui caratteri che possono essere visualizzati in un percorso logico non **null** .</span><span class="sxs-lookup"><span data-stu-id="3fc71-111">Beyond that, there are no restrictions on the characters that can appear in a non-**NULL** logical path.</span></span>

<span data-ttu-id="3fc71-112">Un percorso logico può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="3fc71-112">A logical path can be **NULL**.</span></span> <span data-ttu-id="3fc71-113">Per convenzione, i componenti con percorsi logici **null** sono detti al livello superiore della gerarchia di percorsi logici di un writer.</span><span class="sxs-lookup"><span data-stu-id="3fc71-113">By convention, components with **NULL** logical paths are said to be at the top level of a writer's logical path hierarchy.</span></span>

<span data-ttu-id="3fc71-114">Vedere anche [*componente*](vssgloss-c.md), [*sottocomponente*](vssgloss-s.md).</span><span class="sxs-lookup"><span data-stu-id="3fc71-114">See also [*component*](vssgloss-c.md), [*subcomponent*](vssgloss-s.md).</span></span>

</dd> </dl>

 

 



