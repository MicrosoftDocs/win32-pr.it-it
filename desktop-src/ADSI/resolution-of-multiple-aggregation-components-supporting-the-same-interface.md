---
title: Risoluzione di più componenti di aggregazione che supportano la stessa interfaccia
description: Non è raro che due estensioni espongano la stessa interfaccia a ADSI.
ms.assetid: 87cb1a17-04f7-4ad0-989a-a9506dfdca05
ms.tgt_platform: multiple
keywords:
- Risoluzione di più componenti di aggregazione che supportano la stessa interfaccia ADSI
- risoluzione di più componenti di aggregazione che supportano la stessa interfaccia ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f58b7b606a05543444a172e2f76b436f6048431
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297659"
---
# <a name="resolution-of-multiple-aggregation-components-supporting-the-same-interface"></a><span data-ttu-id="fa902-105">Risoluzione di più componenti di aggregazione che supportano la stessa interfaccia</span><span class="sxs-lookup"><span data-stu-id="fa902-105">Resolution of Multiple Aggregation Components Supporting the Same Interface</span></span>

<span data-ttu-id="fa902-106">Non è raro che due estensioni espongano la stessa interfaccia a ADSI.</span><span class="sxs-lookup"><span data-stu-id="fa902-106">It is uncommon that two extensions expose the same interface to ADSI.</span></span> <span data-ttu-id="fa902-107">In tal caso, si applicano le regole seguenti:</span><span class="sxs-lookup"><span data-stu-id="fa902-107">If this happens, the following rules apply:</span></span>

-   <span data-ttu-id="fa902-108">Se un'interfaccia, ad esempio **IMyInterface**, è supportata da entrambi gli oggetti Aggregator (ADSI) ed any Extension, **QueryInterface** restituisce sempre il **IMyInterface** per ADSI.</span><span class="sxs-lookup"><span data-stu-id="fa902-108">If an interface, such as **IMyInterface**, is supported by both the aggregator (ADSI) and any extension objects, **QueryInterface** always returns the **IMyInterface** for ADSI.</span></span>
-   <span data-ttu-id="fa902-109">Se un'interfaccia, ad esempio **IMyInterface**, non è supportata da Aggregator (ADSI), ma è supportata da più di un oggetto di estensione, **QueryInterface** restituisce il **IMyInterface** del primo oggetto di estensione elencato nel registro di sistema che supporta l'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="fa902-109">If an interface, such as **IMyInterface**, is not supported by the aggregator (ADSI), but is supported by more than one extension object, **QueryInterface** returns the **IMyInterface** of the first extension object listed in the registry that supports the interface.</span></span>

<span data-ttu-id="fa902-110">Tenere presente che l'ordine dei componenti nel registro di sistema influiscono anche sulla risoluzione dei conflitti di nome in automazione.</span><span class="sxs-lookup"><span data-stu-id="fa902-110">Be aware that the order of components in the registry also affects the resolution of name conflicts in Automation.</span></span> <span data-ttu-id="fa902-111">Per altre informazioni, vedere [risoluzione dei conflitti di nome di funzione/proprietà in automazione nelle estensioni](resolution-of-functionproperty-name-conflicts-in-automation-in-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="fa902-111">For more information, see [Resolution of Function/Property Name Conflicts in Automation in Extensions](resolution-of-functionproperty-name-conflicts-in-automation-in-extensions.md).</span></span>

 

 




