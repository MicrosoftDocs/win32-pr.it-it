---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: cbaa7eff-a88b-4b0e-b7b5-5c0d99397942
title: V (Servizio Copia Shadow del volume)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6da999c820e7a18ce27fc6fac144f88d1d1dafee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526269"
---
# <a name="v-volume-shadow-copy-service"></a><span data-ttu-id="09e19-103">V (Servizio Copia Shadow del volume)</span><span class="sxs-lookup"><span data-stu-id="09e19-103">V (Volume Shadow Copy Service)</span></span>

<span data-ttu-id="09e19-104">[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [d](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [i](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U V [W](vssgloss-w.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="09e19-104">[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U V [W](vssgloss-w.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="09e19-105"><span id="base.vssgloss_volume"></span><span id="BASE.VSSGLOSS_VOLUME"></span>**volume**</span><span class="sxs-lookup"><span data-stu-id="09e19-105"><span id="base.vssgloss_volume"></span><span id="BASE.VSSGLOSS_VOLUME"></span>**volume**</span></span>
</dt> <dd>

<span data-ttu-id="09e19-106">Unità di archiviazione logica.</span><span class="sxs-lookup"><span data-stu-id="09e19-106">A logical storage unit.</span></span> <span data-ttu-id="09e19-107">Un volume è la destinazione delle operazioni di creazione di copie shadow.</span><span class="sxs-lookup"><span data-stu-id="09e19-107">A volume is the target of shadow copy creation operations.</span></span>

</dd> <dt>

<span data-ttu-id="09e19-108"><span id="base.vssgloss_volume_name"></span><span id="BASE.VSSGLOSS_VOLUME_NAME"></span>**nome GUID volume**</span><span class="sxs-lookup"><span data-stu-id="09e19-108"><span id="base.vssgloss_volume_name"></span><span id="BASE.VSSGLOSS_VOLUME_NAME"></span>**volume GUID name**</span></span>
</dt> <dd>

<span data-ttu-id="09e19-109">Nome univoco per un volume.</span><span class="sxs-lookup"><span data-stu-id="09e19-109">A unique name for a volume.</span></span> <span data-ttu-id="09e19-110">Il nome di un GUID del volume è una stringa nel formato seguente:</span><span class="sxs-lookup"><span data-stu-id="09e19-110">A volume GUID name is a string of the following form:</span></span>

<span data-ttu-id="09e19-111">\\\\?\\ Volume {GUID}</span><span class="sxs-lookup"><span data-stu-id="09e19-111">\\\\?\\Volume{GUID}</span></span>\\

<span data-ttu-id="09e19-112">(si noti il carattere " \\ "), dove GUID è un identificatore univoco globale per il volume.</span><span class="sxs-lookup"><span data-stu-id="09e19-112">(note the trailing "\\") where GUID is a globally unique identifier for the volume.</span></span> <span data-ttu-id="09e19-113">Il sistema operativo assegna un nome di volume quando viene rilevato per la prima volta un volume, ad esempio, durante la formattazione o l'installazione.</span><span class="sxs-lookup"><span data-stu-id="09e19-113">The operating system assigns a volume name when it first encounters a volume, for example, during formatting or installation.</span></span>

<span data-ttu-id="09e19-114">Si noti che un volume può avere più di un nome GUID del volume.</span><span class="sxs-lookup"><span data-stu-id="09e19-114">Note that a volume can have more than one volume GUID name.</span></span>

</dd> </dl>

 

 



