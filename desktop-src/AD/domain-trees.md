---
title: Alberi di dominio
description: Un albero di dominio è costituito da diversi domini che condividono uno schema e una configurazione comuni, costituendo uno spazio dei nomi contiguo.
ms.assetid: 3deb4053-3124-4180-8ab0-35fff689a37e
ms.tgt_platform: multiple
keywords:
- Active Directory albero di dominio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a21d2b36968615fd4e92912fdd94246ef8dda0c1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104220949"
---
# <a name="domain-trees"></a><span data-ttu-id="3a181-104">Alberi di dominio</span><span class="sxs-lookup"><span data-stu-id="3a181-104">Domain Trees</span></span>

<span data-ttu-id="3a181-105">Un *albero di dominio* è costituito da diversi domini che condividono uno schema e una configurazione comuni, costituendo uno spazio dei nomi contiguo.</span><span class="sxs-lookup"><span data-stu-id="3a181-105">A *domain tree* is made up of several domains that share a common schema and configuration, forming a contiguous namespace.</span></span> <span data-ttu-id="3a181-106">I domini in un albero sono collegati anche da relazioni di trust.</span><span class="sxs-lookup"><span data-stu-id="3a181-106">Domains in a tree are also linked together by trust relationships.</span></span> <span data-ttu-id="3a181-107">Active Directory è un set di uno o più alberi.</span><span class="sxs-lookup"><span data-stu-id="3a181-107">Active Directory is a set of one or more trees.</span></span>

<span data-ttu-id="3a181-108">Gli alberi possono essere visualizzati in due modi.</span><span class="sxs-lookup"><span data-stu-id="3a181-108">Trees can be viewed two ways.</span></span> <span data-ttu-id="3a181-109">Una vista rappresenta le relazioni di trust tra i domini.</span><span class="sxs-lookup"><span data-stu-id="3a181-109">One view is the trust relationships between domains.</span></span> <span data-ttu-id="3a181-110">L'altra visualizzazione è lo spazio dei nomi dell'albero del dominio.</span><span class="sxs-lookup"><span data-stu-id="3a181-110">The other view is the namespace of the domain tree.</span></span>

## <a name="viewing-trust-relationships"></a><span data-ttu-id="3a181-111">Visualizzazione di relazioni di trust</span><span class="sxs-lookup"><span data-stu-id="3a181-111">Viewing Trust Relationships</span></span>

<span data-ttu-id="3a181-112">È possibile creare un diagramma di un albero di dominio in base ai singoli domini e alla relazione di trust esistente.</span><span class="sxs-lookup"><span data-stu-id="3a181-112">You can draw a diagram of a domain tree based on the individual domains and the existing trust relationship.</span></span>

<span data-ttu-id="3a181-113">Windows 2000 stabilisce relazioni di trust tra domini basati sul protocollo di sicurezza Kerberos.</span><span class="sxs-lookup"><span data-stu-id="3a181-113">Windows 2000 establishes trust relationships between domains based on the Kerberos security protocol.</span></span> <span data-ttu-id="3a181-114">Il trust Kerberos è transitivo e gerarchico: se il dominio A considera attendibile il dominio B e il dominio B considera attendibile il dominio C, il dominio A considera attendibili il dominio C.</span><span class="sxs-lookup"><span data-stu-id="3a181-114">Kerberos trust is transitive and hierarchical—if domain A trusts domain B, and domain B trusts domain C, then domain A trusts domain C.</span></span>

![relazione di trust albero di dominio](images/domain-trust.png)

## <a name="viewing-the-namespace"></a><span data-ttu-id="3a181-116">Visualizzazione dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="3a181-116">Viewing the Namespace</span></span>

<span data-ttu-id="3a181-117">È anche possibile creare un diagramma di un albero di dominio basato sullo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="3a181-117">You can also draw a diagram of a domain tree based on the namespace.</span></span> <span data-ttu-id="3a181-118">È possibile determinare il nome distinto di un oggetto seguendo il percorso verso l'alto nella gerarchia dello spazio dei nomi dell'albero di dominio.</span><span class="sxs-lookup"><span data-stu-id="3a181-118">You can determine an object's distinguished name by following the path up the hierarchy of the domain tree namespace.</span></span> <span data-ttu-id="3a181-119">Questa vista è utile per raggruppare gli oggetti in una gerarchia logica.</span><span class="sxs-lookup"><span data-stu-id="3a181-119">This view is useful for grouping objects into a logical hierarchy.</span></span> <span data-ttu-id="3a181-120">Il vantaggio principale di uno spazio dei nomi contiguo è che una ricerca completa dalla radice dello spazio dei nomi Cerca nell'intera gerarchia.</span><span class="sxs-lookup"><span data-stu-id="3a181-120">The chief advantage of a contiguous namespace is that a deep search from the root of the namespace searches the entire hierarchy.</span></span>

![albero del dominio dello spazio dei nomi](images/namespace.png)

 

 




