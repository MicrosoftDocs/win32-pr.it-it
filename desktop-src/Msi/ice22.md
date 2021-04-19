---
description: ICE22 utilizza la tabella FeatureComponents per convalidare il mapping delle funzionalità e dei componenti a cui viene fatto riferimento nella tabella PublishComponent.
ms.assetid: 1aa3e2e6-3f05-411e-829f-aeddbb53445d
title: ICE22
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26574b11f9d908026d901a74632766998246d31a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314229"
---
# <a name="ice22"></a><span data-ttu-id="795c7-103">ICE22</span><span class="sxs-lookup"><span data-stu-id="795c7-103">ICE22</span></span>

<span data-ttu-id="795c7-104">ICE22 utilizza la [tabella FeatureComponents](featurecomponents-table.md) per convalidare il mapping delle funzionalità e dei componenti a cui viene fatto riferimento nella [tabella PublishComponent](publishcomponent-table.md).</span><span class="sxs-lookup"><span data-stu-id="795c7-104">ICE22 uses the [FeatureComponents table](featurecomponents-table.md) to validate the mapping of features and components referenced in the [PublishComponent table](publishcomponent-table.md).</span></span>

## <a name="result"></a><span data-ttu-id="795c7-105">Risultato</span><span class="sxs-lookup"><span data-stu-id="795c7-105">Result</span></span>

<span data-ttu-id="795c7-106">ICE22 Invia un messaggio di errore se le funzionalità e i componenti non sono mappati correttamente nella [tabella PublishComponent](publishcomponent-table.md).</span><span class="sxs-lookup"><span data-stu-id="795c7-106">ICE22 posts an error message if the features and components are mapped incorrectly in the [PublishComponent table](publishcomponent-table.md).</span></span>

## <a name="example"></a><span data-ttu-id="795c7-107">Esempio</span><span class="sxs-lookup"><span data-stu-id="795c7-107">Example</span></span>

<span data-ttu-id="795c7-108">Per l'esempio seguente ICE22 Invia un errore che non {00000003-0004-0000-0000-624474732465} dispone del mapping corretto per le colonne feature \_ e Component \_ .</span><span class="sxs-lookup"><span data-stu-id="795c7-108">For the following example ICE22 posts an error that {00000003-0004-0000-0000-624474732465} does not have the correct mapping for the Feature\_ and Component\_ columns.</span></span>

<span data-ttu-id="795c7-109">[Tabella PublishComponent](publishcomponent-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="795c7-109">[PublishComponent Table](publishcomponent-table.md) (partial)</span></span>



| <span data-ttu-id="795c7-110">ComponentId</span><span class="sxs-lookup"><span data-stu-id="795c7-110">ComponentId</span></span>                            | <span data-ttu-id="795c7-111">Funzionalità\_</span><span class="sxs-lookup"><span data-stu-id="795c7-111">Feature\_</span></span> | <span data-ttu-id="795c7-112">Componente\_</span><span class="sxs-lookup"><span data-stu-id="795c7-112">Component\_</span></span> |
|----------------------------------------|-----------|-------------|
| {00000002-0003-0000-0000-624474736554} | <span data-ttu-id="795c7-113">Feat1</span><span class="sxs-lookup"><span data-stu-id="795c7-113">Feat1</span></span>     | <span data-ttu-id="795c7-114">Comp1</span><span class="sxs-lookup"><span data-stu-id="795c7-114">Comp1</span></span>       |
| {00000003-0004-0000-0000-624474732465} | <span data-ttu-id="795c7-115">Feat1</span><span class="sxs-lookup"><span data-stu-id="795c7-115">Feat1</span></span>     | <span data-ttu-id="795c7-116">Comp2</span><span class="sxs-lookup"><span data-stu-id="795c7-116">Comp2</span></span>       |



 

<span data-ttu-id="795c7-117">[Tabella FeatureComponents](featurecomponents-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="795c7-117">[FeatureComponents Table](featurecomponents-table.md) (partial)</span></span>



| <span data-ttu-id="795c7-118">Funzionalità\_</span><span class="sxs-lookup"><span data-stu-id="795c7-118">Feature\_</span></span> | <span data-ttu-id="795c7-119">Componente\_</span><span class="sxs-lookup"><span data-stu-id="795c7-119">Component\_</span></span> |
|-----------|-------------|
| <span data-ttu-id="795c7-120">Feat1</span><span class="sxs-lookup"><span data-stu-id="795c7-120">Feat1</span></span>     | <span data-ttu-id="795c7-121">Comp1</span><span class="sxs-lookup"><span data-stu-id="795c7-121">Comp1</span></span>       |



 

## <a name="related-topics"></a><span data-ttu-id="795c7-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="795c7-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="795c7-123">Riferimento ghiaccio</span><span class="sxs-lookup"><span data-stu-id="795c7-123">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



