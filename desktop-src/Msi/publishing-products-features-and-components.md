---
description: Per pubblicare un prodotto, un componente o una funzionalità, utilizzare una delle azioni di pubblicazione.
ms.assetid: 2c395d81-4f46-444e-a275-7a5d806e473c
title: Pubblicazione di prodotti, funzionalità e componenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cdd8c8445491646399c7d118a69ae497d27faff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227399"
---
# <a name="publishing-products-features-and-components"></a><span data-ttu-id="c2393-103">Pubblicazione di prodotti, funzionalità e componenti</span><span class="sxs-lookup"><span data-stu-id="c2393-103">Publishing Products, Features, and Components</span></span>

<span data-ttu-id="c2393-104">Per [pubblicare](components-and-features.md) un prodotto, un componente o una funzionalità, utilizzare una delle azioni di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="c2393-104">To [publish](components-and-features.md) a product, component, or feature, use one of the publishing actions.</span></span> <span data-ttu-id="c2393-105">L' [azione PublishProduct](publishproduct-action.md) registra le informazioni sul prodotto con il sistema.</span><span class="sxs-lookup"><span data-stu-id="c2393-105">The [PublishProduct action](publishproduct-action.md) registers the product information with the system.</span></span> <span data-ttu-id="c2393-106">Dopo aver eseguito l'azione PublishProduct, pubblicare i componenti con l' [azione PublishComponents](publishcomponents-action.md), che a sua volta usa la [tabella PublishComponent](publishcomponent-table.md) per determinare i componenti impostati come annunciati.</span><span class="sxs-lookup"><span data-stu-id="c2393-106">After executing the PublishProduct action, publish the components with the [PublishComponents action](publishcomponents-action.md), which in turn uses the [PublishComponent table](publishcomponent-table.md) to determine the components that are set as advertised.</span></span> <span data-ttu-id="c2393-107">Per eseguire la pubblicazione in base alle singole funzionalità, richiamare l' [azione PublishFeatures](publishfeatures-action.md).</span><span class="sxs-lookup"><span data-stu-id="c2393-107">To publish on a per-feature basis, invoke the [PublishFeatures action](publishfeatures-action.md).</span></span> <span data-ttu-id="c2393-108">Questa azione usa la [tabella FeatureComponents](featurecomponents-table.md) come dati per risolvere le funzionalità annunciate.</span><span class="sxs-lookup"><span data-stu-id="c2393-108">This action uses the [FeatureComponents table](featurecomponents-table.md) as data to resolve which features are advertised.</span></span>

<span data-ttu-id="c2393-109">Sono inoltre disponibili due azioni corrispondenti che annulla la pubblicazione di una funzionalità o di un componente, ovvero l' [azione UnpublishComponents](unpublishcomponents-action.md) e l' [azione UnpublishFeatures](unpublishfeatures-action.md).</span><span class="sxs-lookup"><span data-stu-id="c2393-109">There are also two corresponding actions that unpublish a feature or a component: the [UnpublishComponents action](unpublishcomponents-action.md) and the [UnpublishFeatures action](unpublishfeatures-action.md).</span></span>

 

 



