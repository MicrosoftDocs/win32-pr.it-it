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
# <a name="publishing-products-features-and-components"></a>Pubblicazione di prodotti, funzionalità e componenti

Per [pubblicare](components-and-features.md) un prodotto, un componente o una funzionalità, utilizzare una delle azioni di pubblicazione. L' [azione PublishProduct](publishproduct-action.md) registra le informazioni sul prodotto con il sistema. Dopo aver eseguito l'azione PublishProduct, pubblicare i componenti con l' [azione PublishComponents](publishcomponents-action.md), che a sua volta usa la [tabella PublishComponent](publishcomponent-table.md) per determinare i componenti impostati come annunciati. Per eseguire la pubblicazione in base alle singole funzionalità, richiamare l' [azione PublishFeatures](publishfeatures-action.md). Questa azione usa la [tabella FeatureComponents](featurecomponents-table.md) come dati per risolvere le funzionalità annunciate.

Sono inoltre disponibili due azioni corrispondenti che annulla la pubblicazione di una funzionalità o di un componente, ovvero l' [azione UnpublishComponents](unpublishcomponents-action.md) e l' [azione UnpublishFeatures](unpublishfeatures-action.md).

 

 



