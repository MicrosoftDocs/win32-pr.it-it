---
description: ICE21 verifica che ogni componente della tabella dei componenti appartenga a una funzionalità. Usa la tabella FeatureComponents per verificare il mapping.
ms.assetid: 68983d6a-b807-4730-a645-378001e558ec
title: ICE21
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c457d026b3dc57a718eabea704254a3448a3de26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314230"
---
# <a name="ice21"></a><span data-ttu-id="ec971-104">ICE21</span><span class="sxs-lookup"><span data-stu-id="ec971-104">ICE21</span></span>

<span data-ttu-id="ec971-105">ICE21 verifica che ogni componente della tabella dei [componenti](component-table.md) appartenga a una funzionalità.</span><span class="sxs-lookup"><span data-stu-id="ec971-105">ICE21 validates that every component in the [Component table](component-table.md) belongs to a feature.</span></span> <span data-ttu-id="ec971-106">Usa la [tabella FeatureComponents](featurecomponents-table.md) per verificare il mapping.</span><span class="sxs-lookup"><span data-stu-id="ec971-106">It uses the [FeatureComponents table](featurecomponents-table.md) to check for this mapping.</span></span>

## <a name="result"></a><span data-ttu-id="ec971-107">Risultato</span><span class="sxs-lookup"><span data-stu-id="ec971-107">Result</span></span>

<span data-ttu-id="ec971-108">ICE21 Invia un messaggio di errore se il pacchetto di installazione contiene un componente che non appartiene a una funzionalità.</span><span class="sxs-lookup"><span data-stu-id="ec971-108">ICE21 posts an error message if the installation package contains a component that does not belong to a feature.</span></span>

## <a name="example"></a><span data-ttu-id="ec971-109">Esempio</span><span class="sxs-lookup"><span data-stu-id="ec971-109">Example</span></span>

<span data-ttu-id="ec971-110">Per l'esempio seguente, ICE21 Invia un messaggio di errore che informa che il componente comp1 non è mappato ad alcuna funzionalità.</span><span class="sxs-lookup"><span data-stu-id="ec971-110">For the following example, ICE21 posts an error message stating that the component Comp1 does not map to any feature.</span></span>

<span data-ttu-id="ec971-111">[Tabella componenti](component-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="ec971-111">[Component Table](component-table.md) (partial)</span></span>



| <span data-ttu-id="ec971-112">Componente</span><span class="sxs-lookup"><span data-stu-id="ec971-112">Component</span></span> |
|-----------|
| <span data-ttu-id="ec971-113">Comp1</span><span class="sxs-lookup"><span data-stu-id="ec971-113">Comp1</span></span>     |
| <span data-ttu-id="ec971-114">Comp2</span><span class="sxs-lookup"><span data-stu-id="ec971-114">Comp2</span></span>     |



 

<span data-ttu-id="ec971-115">[Tabella FeatureComponents](featurecomponents-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="ec971-115">[FeatureComponents Table](featurecomponents-table.md) (partial)</span></span>



| <span data-ttu-id="ec971-116">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="ec971-116">Feature</span></span>  | <span data-ttu-id="ec971-117">Componente</span><span class="sxs-lookup"><span data-stu-id="ec971-117">Component</span></span> |
|----------|-----------|
| <span data-ttu-id="ec971-118">Feature1</span><span class="sxs-lookup"><span data-stu-id="ec971-118">Feature1</span></span> | <span data-ttu-id="ec971-119">Comp2</span><span class="sxs-lookup"><span data-stu-id="ec971-119">Comp2</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="ec971-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ec971-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ec971-121">Riferimento ghiaccio</span><span class="sxs-lookup"><span data-stu-id="ec971-121">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



