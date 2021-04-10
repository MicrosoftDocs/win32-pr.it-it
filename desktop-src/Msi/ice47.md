---
description: ICE47 controlla la funzionalità e le tabelle FeatureComponents per le funzionalità con 1600 o più componenti.
ms.assetid: e3101569-4d0b-48c9-8ba2-6f0de0c39e74
title: ICE47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: baa04c2df52571f56612242d2dc7da8b5a91647c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227406"
---
# <a name="ice47"></a><span data-ttu-id="e2d51-103">ICE47</span><span class="sxs-lookup"><span data-stu-id="e2d51-103">ICE47</span></span>

<span data-ttu-id="e2d51-104">ICE47 controlla la [funzionalità](feature-table.md) e le tabelle [FeatureComponents](featurecomponents-table.md) per le funzionalità con 1600 o più componenti.</span><span class="sxs-lookup"><span data-stu-id="e2d51-104">ICE47 checks the [Feature](feature-table.md) and [FeatureComponents](featurecomponents-table.md) tables for features with 1600 or more components.</span></span>

## <a name="result"></a><span data-ttu-id="e2d51-105">Risultato</span><span class="sxs-lookup"><span data-stu-id="e2d51-105">Result</span></span>

<span data-ttu-id="e2d51-106">ICE47 Invia un messaggio di errore se una funzionalità supera il limite massimo di 1600 componenti per funzionalità.</span><span class="sxs-lookup"><span data-stu-id="e2d51-106">ICE47 posts an error message if a feature exceeds the maximum limit of 1600 components per feature.</span></span>

## <a name="example"></a><span data-ttu-id="e2d51-107">Esempio</span><span class="sxs-lookup"><span data-stu-id="e2d51-107">Example</span></span>

<span data-ttu-id="e2d51-108">ICE47 segnala l'avviso seguente:</span><span class="sxs-lookup"><span data-stu-id="e2d51-108">ICE47 would report the following warning:</span></span>

``` syntax
Feature 'Feature1' has 1600 components. This could cause 
    problems on Win9X systems. You should try to have less 
    than 800 components per feature."
```

<span data-ttu-id="e2d51-109">[Tabella delle funzionalità](feature-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="e2d51-109">[Feature Table](feature-table.md) (partial)</span></span>



| <span data-ttu-id="e2d51-110">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="e2d51-110">Feature</span></span>  |
|----------|
| <span data-ttu-id="e2d51-111">Feature1</span><span class="sxs-lookup"><span data-stu-id="e2d51-111">Feature1</span></span> |



 

<span data-ttu-id="e2d51-112">[Tabella FeatureComponents](featurecomponents-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="e2d51-112">[FeatureComponents Table](featurecomponents-table.md) (partial)</span></span>



| <span data-ttu-id="e2d51-113">Azione</span><span class="sxs-lookup"><span data-stu-id="e2d51-113">Action</span></span>   | <span data-ttu-id="e2d51-114">Condizione</span><span class="sxs-lookup"><span data-stu-id="e2d51-114">Condition</span></span>     |
|----------|---------------|
| <span data-ttu-id="e2d51-115">Feature1</span><span class="sxs-lookup"><span data-stu-id="e2d51-115">Feature1</span></span> | <span data-ttu-id="e2d51-116">Component1</span><span class="sxs-lookup"><span data-stu-id="e2d51-116">Component1</span></span>    |
| <span data-ttu-id="e2d51-117">Feature1</span><span class="sxs-lookup"><span data-stu-id="e2d51-117">Feature1</span></span> | <span data-ttu-id="e2d51-118">Component1600</span><span class="sxs-lookup"><span data-stu-id="e2d51-118">Component1600</span></span> |



 

<span data-ttu-id="e2d51-119">Per correggere il problema, provare a suddividere la funzionalità in diverse funzionalità</span><span class="sxs-lookup"><span data-stu-id="e2d51-119">To fix this warning, try splitting the feature into several features</span></span>

## <a name="related-topics"></a><span data-ttu-id="e2d51-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e2d51-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e2d51-121">Riferimento ghiaccio</span><span class="sxs-lookup"><span data-stu-id="e2d51-121">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



