---
description: Le versioni dei qualificatori forniscono ulteriori informazioni su un qualificatore, ad esempio se una classe o un'istanza derivata può eseguire l'override del valore originale del qualificatore.
ms.assetid: 6a0769ac-e16c-45e1-92b6-26e4969bf23d
ms.tgt_platform: multiple
title: Versioni qualificatore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec8ddf6c2daea59931e533174c532e3d07b147a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318547"
---
# <a name="qualifier-flavors"></a><span data-ttu-id="985bf-103">Versioni qualificatore</span><span class="sxs-lookup"><span data-stu-id="985bf-103">Qualifier Flavors</span></span>

<span data-ttu-id="985bf-104">Le versioni dei qualificatori forniscono ulteriori informazioni su un qualificatore, ad esempio se una classe o un'istanza derivata può eseguire l'override del valore originale del qualificatore.</span><span class="sxs-lookup"><span data-stu-id="985bf-104">Qualifier flavors provide more information about a qualifier, such as whether a derived class or instance can override the qualifier's original value.</span></span>

<span data-ttu-id="985bf-105">Le versioni dei qualificatori possono essere aggiunte all'inizio del file MOF, usando la sintassi seguente, in modo che vengano applicate in tutta la definizione.</span><span class="sxs-lookup"><span data-stu-id="985bf-105">Qualifier flavors may be added to the top of the MOF file, using the following syntax, causing them to be applied throughout the definition.</span></span> <span data-ttu-id="985bf-106">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="985bf-106">For example:</span></span>

``` syntax
Qualifier Description : ToSubClass Amended;
```

<span data-ttu-id="985bf-107">Le versioni **ToClass** e **emendate** si applicano a tutti i qualificatori della **Descrizione** nel file MOF.</span><span class="sxs-lookup"><span data-stu-id="985bf-107">The **ToSubClass** and **Amended** flavors applies to all the **Description** qualifiers in the MOF.</span></span>

<span data-ttu-id="985bf-108">Nella tabella seguente sono elencate le versioni del qualificatore.</span><span class="sxs-lookup"><span data-stu-id="985bf-108">The following table lists the qualifier flavors.</span></span>



| <span data-ttu-id="985bf-109">Versione qualificatore</span><span class="sxs-lookup"><span data-stu-id="985bf-109">Qualifier Flavor</span></span>    | <span data-ttu-id="985bf-110">Significato</span><span class="sxs-lookup"><span data-stu-id="985bf-110">Meaning</span></span>                                                                                                                                                                                                                                         |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="985bf-111">**Corretto**</span><span class="sxs-lookup"><span data-stu-id="985bf-111">**Amended**</span></span>         | <span data-ttu-id="985bf-112">Il qualificatore non è necessario nella definizione della classe di base e può essere spostato nella modifica da localizzare.</span><span class="sxs-lookup"><span data-stu-id="985bf-112">The qualifier is not required in the basic class definition and can be moved to the amendment to be localized.</span></span>                                                                                                                                  |
| <span data-ttu-id="985bf-113">**DisableOverride**</span><span class="sxs-lookup"><span data-stu-id="985bf-113">**DisableOverride**</span></span> | <span data-ttu-id="985bf-114">Il qualificatore non può essere sottoposto a override in una classe o in un'istanza derivata.</span><span class="sxs-lookup"><span data-stu-id="985bf-114">The qualifier cannot be overridden in a derived class or instance.</span></span> <span data-ttu-id="985bf-115">Si noti che la possibilità di eseguire l'override di un qualificatore propagato è il valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="985bf-115">Note that being able to override a propagated qualifier is the default.</span></span>                                                                                                      |
| <span data-ttu-id="985bf-116">**EnableOverride**</span><span class="sxs-lookup"><span data-stu-id="985bf-116">**EnableOverride**</span></span>  | <span data-ttu-id="985bf-117">Quando viene propagata a una classe o a un'istanza derivata, il valore del qualificatore può essere sottoposto a override.</span><span class="sxs-lookup"><span data-stu-id="985bf-117">When propagated to a derived class or instance, the value of the qualifier can be overridden.</span></span> <span data-ttu-id="985bf-118">L'impostazione di **EnableOverride** è facoltativa perché la possibilità di eseguire l'override del valore del qualificatore è la funzionalità predefinita per i qualificatori propagati.</span><span class="sxs-lookup"><span data-stu-id="985bf-118">Setting **EnableOverride** is optional because being able to override the qualifier value is the default functionality for propagated qualifiers.</span></span> |
| <span data-ttu-id="985bf-119">**NotToInstance**</span><span class="sxs-lookup"><span data-stu-id="985bf-119">**NotToInstance**</span></span>   | <span data-ttu-id="985bf-120">Il qualificatore non viene propagato alle istanze della classe.</span><span class="sxs-lookup"><span data-stu-id="985bf-120">The qualifier is not propagated to class instances.</span></span>                                                                                                                                                                                             |
| <span data-ttu-id="985bf-121">**NotToSubClass**</span><span class="sxs-lookup"><span data-stu-id="985bf-121">**NotToSubClass**</span></span>   | <span data-ttu-id="985bf-122">Il qualificatore non viene propagato alle classi derivate.</span><span class="sxs-lookup"><span data-stu-id="985bf-122">The qualifier is not propagated to derived classes.</span></span>                                                                                                                                                                                             |
| <span data-ttu-id="985bf-123">**Con restrizioni**</span><span class="sxs-lookup"><span data-stu-id="985bf-123">**Restricted**</span></span>      | <span data-ttu-id="985bf-124">Il qualificatore non viene propagato a istanze o classi derivate.</span><span class="sxs-lookup"><span data-stu-id="985bf-124">The qualifier is not propagated to instances or derived classes.</span></span>                                                                                                                                                                                |
| <span data-ttu-id="985bf-125">**Istanza di**</span><span class="sxs-lookup"><span data-stu-id="985bf-125">**ToInstance**</span></span>      | <span data-ttu-id="985bf-126">Il qualificatore viene propagato alle istanze.</span><span class="sxs-lookup"><span data-stu-id="985bf-126">The qualifier is propagated to instances.</span></span>                                                                                                                                                                                                       |
| <span data-ttu-id="985bf-127">**ToClass**</span><span class="sxs-lookup"><span data-stu-id="985bf-127">**ToSubClass**</span></span>      | <span data-ttu-id="985bf-128">Il qualificatore viene propagato alle classi derivate.</span><span class="sxs-lookup"><span data-stu-id="985bf-128">The qualifier is propagated to derived classes.</span></span> <span data-ttu-id="985bf-129">Questa caratteristica è appropriata solo per i qualificatori definiti per una classe e non può essere associata a un qualificatore che descrive un'istanza di classe.</span><span class="sxs-lookup"><span data-stu-id="985bf-129">This flavor is only appropriate for qualifiers defined for a class and cannot be attached to a qualifier describing a class instance.</span></span>                                                           |



 

 

 



