---
title: Attributi del puntatore applicati al parametro
description: Ogni attributo del puntatore (\ Ref \, \ Unique \ e \ PTR \) presenta caratteristiche che influiscono sull'allocazione della memoria. Nella tabella seguente sono riepilogate queste caratteristiche.
ms.assetid: 25a609cd-efe7-4cbb-b80e-b6a3ad8cda38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c7710fb3c39702b2b2fdb789ed1218dc88d44ea
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047191"
---
# <a name="pointer-attributes-applied-to-the-parameter"></a><span data-ttu-id="23a9a-104">Attributi del puntatore applicati al parametro</span><span class="sxs-lookup"><span data-stu-id="23a9a-104">Pointer Attributes Applied to the Parameter</span></span>

<span data-ttu-id="23a9a-105">Ogni attributo del puntatore ( \[ [ref](/windows/desktop/Midl/ref) \] , \[ [Unique](/windows/desktop/Midl/unique) \] e \[ [ptr](/windows/desktop/Midl/ptr) \] ) presenta caratteristiche che influiscono sull'allocazione di memoria.</span><span class="sxs-lookup"><span data-stu-id="23a9a-105">Each pointer attribute (\[ [ref](/windows/desktop/Midl/ref)\], \[ [unique](/windows/desktop/Midl/unique)\], and \[ [ptr](/windows/desktop/Midl/ptr)\]) has characteristics that affect memory allocation.</span></span> <span data-ttu-id="23a9a-106">Nella tabella seguente sono riepilogate queste caratteristiche.</span><span class="sxs-lookup"><span data-stu-id="23a9a-106">The following table summarizes these characteristics.</span></span>



| <span data-ttu-id="23a9a-107">Puntatore (attributo)</span><span class="sxs-lookup"><span data-stu-id="23a9a-107">Pointer attribute</span></span>       | <span data-ttu-id="23a9a-108">Client</span><span class="sxs-lookup"><span data-stu-id="23a9a-108">Client</span></span>                                                                                                                                                                                                            | <span data-ttu-id="23a9a-109">Server</span><span class="sxs-lookup"><span data-stu-id="23a9a-109">Server</span></span>                                                              |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="23a9a-110">Riferimento ( \[ **ref** \] )</span><span class="sxs-lookup"><span data-stu-id="23a9a-110">Reference (\[**ref**\])</span></span> | <span data-ttu-id="23a9a-111">L'applicazione client deve allocare.</span><span class="sxs-lookup"><span data-stu-id="23a9a-111">Client application must allocate.</span></span>                                                                                                                                                                                 | <span data-ttu-id="23a9a-112">Gestione speciale necessaria per i puntatori a **\[ \] livello di nontop**.</span><span class="sxs-lookup"><span data-stu-id="23a9a-112">Special handling needed for **\[out\]**-only nontop-level pointers.</span></span> |
| <span data-ttu-id="23a9a-113">Univoco ( \[ **univoco** \] )</span><span class="sxs-lookup"><span data-stu-id="23a9a-113">Unique (\[**unique**\])</span></span> | <span data-ttu-id="23a9a-114">Se un parametro, l'applicazione client deve allocare; Se incorporato, può essere null.</span><span class="sxs-lookup"><span data-stu-id="23a9a-114">If a parameter, the client application must allocate; if embedded, can be null.</span></span> <span data-ttu-id="23a9a-115">Se si modifica da null a non null, lo stub client viene allocato; la modifica da un valore diverso da null a null può causare l'isolamento.</span><span class="sxs-lookup"><span data-stu-id="23a9a-115">Changing from null to non-null causes the client stub to allocate; changing from non-null to null can cause orphaning.</span></span><br/> |                                                                     |
| <span data-ttu-id="23a9a-116">Completo ( \[ **ptr** \] )</span><span class="sxs-lookup"><span data-stu-id="23a9a-116">Full (\[**ptr**\])</span></span>      | <span data-ttu-id="23a9a-117">Se un parametro, l'applicazione client deve allocare; Se incorporato, può essere null.</span><span class="sxs-lookup"><span data-stu-id="23a9a-117">If a parameter, the client application must allocate; if embedded, can be null.</span></span> <span data-ttu-id="23a9a-118">Se si modifica da null a non null, lo stub client viene allocato; la modifica da un valore diverso da null a null può causare l'isolamento.</span><span class="sxs-lookup"><span data-stu-id="23a9a-118">Changing from null to non-null causes the client stub to allocate; changing from non-null to null can cause orphaning.</span></span><br/> |                                                                     |



 

<span data-ttu-id="23a9a-119">L'attributo **\[ ref \]** indica che il puntatore punta alla memoria valida.</span><span class="sxs-lookup"><span data-stu-id="23a9a-119">The **\[ref\]** attribute indicates that the pointer points to valid memory.</span></span> <span data-ttu-id="23a9a-120">Per definizione, l'applicazione client deve allocare tutta la memoria necessaria per i puntatori di riferimento.</span><span class="sxs-lookup"><span data-stu-id="23a9a-120">By definition, the client application must allocate all the memory that the reference pointers require.</span></span>

<span data-ttu-id="23a9a-121">Il puntatore univoco può variare da null a non null.</span><span class="sxs-lookup"><span data-stu-id="23a9a-121">The unique pointer can change from null to non-null.</span></span> <span data-ttu-id="23a9a-122">Se il puntatore univoco passa da null a non null, viene allocata una nuova memoria nel client.</span><span class="sxs-lookup"><span data-stu-id="23a9a-122">If the unique pointer changes from null to non-null, new memory is allocated on the client.</span></span> <span data-ttu-id="23a9a-123">Se il puntatore univoco passa da un valore diverso da null a un valore null, è possibile che venga generato un orfano.</span><span class="sxs-lookup"><span data-stu-id="23a9a-123">If the unique pointer changes from non-null to null, orphaning can result.</span></span> <span data-ttu-id="23a9a-124">Per ulteriori informazioni, vedere [orfano di memoria](memory-orphaning.md).</span><span class="sxs-lookup"><span data-stu-id="23a9a-124">For more information, see [Memory Orphaning](memory-orphaning.md).</span></span>

 

