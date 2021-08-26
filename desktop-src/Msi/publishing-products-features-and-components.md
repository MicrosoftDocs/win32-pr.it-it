---
description: Per pubblicare un prodotto, un componente o una funzionalità, usare una delle azioni di pubblicazione.
ms.assetid: 2c395d81-4f46-444e-a275-7a5d806e473c
title: Pubblicazione di prodotti, funzionalità e componenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74dd62e080cf58188405e20d1fd69507f849dd37ceddd01eaf1f4bbe7c59ea76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120041991"
---
# <a name="publishing-products-features-and-components"></a>Pubblicazione di prodotti, funzionalità e componenti

Per [pubblicare](components-and-features.md) un prodotto, un componente o una funzionalità, usare una delle azioni di pubblicazione. [L'azione PublishProduct](publishproduct-action.md) registra le informazioni sul prodotto con il sistema. Dopo aver eseguito l'azione PublishProduct, pubblicare i componenti con l'azione [PublishComponents](publishcomponents-action.md), che a sua volta usa la tabella [PublishComponent](publishcomponent-table.md) per determinare i componenti impostati come annunciati. Per pubblicare in base alle funzionalità, richiamare [l'azione PublishFeatures](publishfeatures-action.md). Questa azione usa la [tabella FeatureComponents](featurecomponents-table.md) come dati per risolvere le funzionalità annunciate.

Esistono anche due azioni corrispondenti che annullano la pubblicazione di una funzionalità o di un componente: l'azione [UnpublishComponents](unpublishcomponents-action.md) e [l'azione UnpublishFeatures](unpublishfeatures-action.md).

 

 



