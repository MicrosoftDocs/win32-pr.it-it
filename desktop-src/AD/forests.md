---
title: Foreste
description: Una foresta è un set di uno o più alberi di dominio che non formano uno spazio dei nomi contiguo.
ms.assetid: b7beb305-0022-477a-85bf-779821202b26
ms.tgt_platform: multiple
keywords:
- foreste Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc84fca35ce90b20582bd62a675e6cf8d0285f7e
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "103956326"
---
# <a name="forests"></a><span data-ttu-id="38b49-104">Foreste</span><span class="sxs-lookup"><span data-stu-id="38b49-104">Forests</span></span>

<span data-ttu-id="38b49-105">Una [*foresta*](/previous-versions/windows/desktop/legacy/ms681904(v=vs.85)) è un set di uno o più alberi di dominio che non formano uno spazio dei nomi contiguo.</span><span class="sxs-lookup"><span data-stu-id="38b49-105">A [*forest*](/previous-versions/windows/desktop/legacy/ms681904(v=vs.85)) is a set of one or more domain trees that do not form a contiguous namespace.</span></span> <span data-ttu-id="38b49-106">Tutti gli alberi di una foresta condividono uno schema comune, una configurazione e un catalogo globale.</span><span class="sxs-lookup"><span data-stu-id="38b49-106">All trees in a forest share a common schema, configuration, and global catalog.</span></span> <span data-ttu-id="38b49-107">Tutti gli alberi in una determinata foresta si considerano attendibili in base alle relazioni di trust Kerberos gerarchiche.</span><span class="sxs-lookup"><span data-stu-id="38b49-107">All trees in a given forest exchange trust according to transitive hierarchical Kerberos trust relationships.</span></span> <span data-ttu-id="38b49-108">A differenza degli alberi, una foresta non richiede un nome distinto.</span><span class="sxs-lookup"><span data-stu-id="38b49-108">Unlike trees, a forest does not require a distinct name.</span></span> <span data-ttu-id="38b49-109">Una foresta esiste come un set di oggetti di riferimento incrociato e relazioni di trust Kerberos riconosciute dagli alberi dei membri.</span><span class="sxs-lookup"><span data-stu-id="38b49-109">A forest exists as a set of cross-reference objects and Kerberos trust relationships recognized by the member trees.</span></span> <span data-ttu-id="38b49-110">Gli alberi di una foresta formano una gerarchia ai fini del trust Kerberos. il nome dell'albero alla radice dell'albero di trust fa riferimento a una foresta specificata.</span><span class="sxs-lookup"><span data-stu-id="38b49-110">Trees in a forest form a hierarchy for the purposes of Kerberos trust; the tree name at the root of the trust tree refers to a given forest.</span></span>

<span data-ttu-id="38b49-111">Nella figura seguente è illustrata una foresta di spazi dei nomi non contigui.</span><span class="sxs-lookup"><span data-stu-id="38b49-111">The following figure shows a forest of noncontiguous namespaces.</span></span>

![foresta di spazi dei nomi non contigui](images/forests.png)

 

 